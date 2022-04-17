<div align="center">

# cliff-jumper

**A small CLI tool to create a semantic release and [git-cliff] powered
Changelog**

[![GitHub](https://img.shields.io/github/license/favware/cliff-jumper)](https://github.com/favware/cliff-jumper/blob/main/LICENSE)
[![npm](https://img.shields.io/npm/v/@favware/cliff-jumper?color=crimson&logo=npm)](https://www.npmjs.com/package/@favware/cliff-jumper)

[![Support Server](https://discord.com/api/guilds/512303595966824458/embed.png?style=banner2)](https://join.favware.tech)

</div>

## Description

When managing a collection of projects you often want to follow a standard
CHANGELOG template for all of them, but you also do not want to have to setup
the release flow for every package. This is where [cliff-jumper] comes in.

### How this works

[cliff-jumper] uses a combination of [conventional-recommended-bump] and
[git-cliff] to bump your package using semantic versioning (following the
[Angular preset][angular-preset]). It will:

1. Perform preflight checks to verify that the tool can run
1. Resolve which bump strategy should be used by using
   [conventional-recommended-bump]
   - If the CLI tool is ran inside a mono repo then only commits that affect the
     nested package will be considered!
1. Bump the version in your `package.json` using `npm version` with the resolved
   strategy
1. Validate that `-t`, `--skip-tag` (CLI flags) weren't provided or `skipTag`
   wasn't set to `true` in the config file
1. Update the `CHANGELOG.md` file using [git-cliff]
1. Stage the `package.json` and `CHANGELOG.md` files
1. Commit the release
1. Tag the release

## Installation

You can use the following command to install this package, or replace
`npm install -D` with your package manager of choice.

```sh
npm install -D @favware/cliff-jumper
```

Or install it globally:

```sh
npm install -g @favware/cliff-jumper
```

Then call the script with `cliff-jumper` or `cj`:

```sh
cliff-jumper --name "my-package" --package-path "." --bump # Add any other flags or use --help
cj --name "my-package" --package-path "." --bump # Add any other flags or use --help
```

Alternatively you can call the CLI directly with `npx`:

```sh
npx @favware/cliff-jumper --name "my-package" --package-path "." --bump # Add any other flags or use --help
```

## Usage

You can provide all options through CLI flags:

```sh
Usage: cliff-jumper [options]

Options:
  -V, --version                output the version number
  -n, --name <string>          The package name to release
  -p, --package-path <string>  The path to the current package. For non-monorepos this is just "."
  -b, --bump [boolean]         Whether the package should be bumped or not (default: false)
  --first-release [boolean]    Whether this is the first release (skips bumping the version) (default: false)
  -o, --org <string>           The NPM org scope that should be used WITHOUT "@" sign or trailing "/" (default: "")
  --preid [string]             The "prerelease identifier" to use as a prefix for the "prerelease" part of a semver (default: "")
  -t, --skip-tag [boolean]     Whether to skip creating a git tag (default `true` when CI=true, `false` otherwise) (default: false)
  -v, --verbose                Whether to print verbose information (default: false)
  -h, --help                   display help for command
```

Or, you can set most of these options through a configuration file. This file
should be located at your current working directory (where you're calling this
package). It should be named `.cliff-jumperrc`, optionally suffixed with
`.json`, `.yaml`, or `.yml`.

### Config file fields

- `--name` maps to `name`
- `--package-path` maps to `packagePath`
- `--bump` maps to `bump`
- `--first-release` maps to `firstRelease`
- `--org` maps to `org`
- `--preid` maps to `preid`
- `--skip-tag` maps to `skipTag`
- `--verbose` maps to `verbose`

When using `.cliff-jumperrc` or `.cliff-jumperrc.json` as your config file you
can also use the JSON schema to get schema validation. To do so, add the
following to your config file:

```json
{
  "$schema": "https://raw.githubusercontent.com/favware/cliff-jumper/main/assets/cliff-jumper.schema.json"
}
```

**Example JSON file**:

```json
{
  "$schema": "https://raw.githubusercontent.com/favware/cliff-jumper/main/assets/cliff-jumper.schema.json",
  "name": "my-package",
  "packagePath": ".",
  "bump": true,
  "verbose": true
}
```

**Example YAML file**:

```yaml
name: my-package
packagePath: .
bump: true
verbose: true
```

### Default values

This library has opinionated defaults for its options. These are as follows:

- `--bump` will default to `false`.
- `--first-release` will default to `false`.
- `--org` will default to `''`.
- `--preid` will default to `''`.
- `--skip-tag` will default to `false` (`true` when `CI` environment variable is
  `'true'`).
- `--verbose` will default to `false`.

### Merging of config file, defaults and CLI provided flags

When you have a config file the options in the file are merged with the default
options and with any other provided CLI flags. Which source takes highest
priority depends on the type of the option.

For `boolean` options (`bump`, `skipTag`, `firstRelease`, and `verbose`) the
priority is as follows (lower means it gets lower priority):

1. Config file
2. CLI flags
3. Default value

For `string` options (`name`, `org`, `packagePath`, and `preid`) the priority is
as follows (lower means it gets lower priority):

1. CLI flags
2. Default value
3. Config file

## Buy us some doughnuts

Favware projects are and always will be open source, even if we don't get
donations. That being said, we know there are amazing people who may still want
to donate just to show their appreciation. Thank you very much in advance!

We accept donations through Ko-fi, Paypal, Patreon, GitHub Sponsorships, and
various cryptocurrencies. You can use the buttons below to donate through your
method of choice.

|   Donate With   |                      Address                      |
| :-------------: | :-----------------------------------------------: |
|      Ko-fi      |  [Click Here](https://donate.favware.tech/kofi)   |
|     Patreon     | [Click Here](https://donate.favware.tech/patreon) |
|     PayPal      | [Click Here](https://donate.favware.tech/paypal)  |
| GitHub Sponsors |  [Click Here](https://github.com/sponsors/Favna)  |
|     Bitcoin     |       `1E643TNif2MTh75rugepmXuq35Tck4TnE5`        |
|    Ethereum     |   `0xF653F666903cd8739030D2721bF01095896F5D6E`    |
|    LiteCoin     |       `LZHvBkaJqKJRa8N7Dyu41Jd1PDBAofCik6`        |

## Contributors ✨

Thanks goes to these wonderful people
([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://favware.tech/"><img src="https://avatars3.githubusercontent.com/u/4019718?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Jeroen Claassens</b></sub></a><br /><a href="https://github.com/favware/cliff-jumper/commits?author=favna" title="Code">💻</a> <a href="#design-favna" title="Design">🎨</a> <a href="#ideas-favna" title="Ideas, Planning, & Feedback">🤔</a> <a href="#infra-favna" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a> <a href="#maintenance-favna" title="Maintenance">🚧</a> <a href="#platform-favna" title="Packaging/porting to new platform">📦</a> <a href="#projectManagement-favna" title="Project Management">📆</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the
[all-contributors](https://github.com/all-contributors/all-contributors)
specification. Contributions of any kind welcome!

[git-cliff]: https://github.com/orhun/git-cliff
[cliff-jumper]: https://github.com/favware/cliff-jumper
[angular-preset]:
  https://github.com/angular/angular/blob/master/CONTRIBUTING.md#type
[conventional-recommended-bump]:
  https://github.com/conventional-changelog/conventional-changelog/tree/master/packages/conventional-recommended-bump
