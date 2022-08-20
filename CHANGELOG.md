# Changelog

All notable changes to this project will be documented in this file.

# [@favware/cliff-jumper@1.8.7](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.8.6...@favware/cliff-jumper@1.8.7) - (2022-08-20)

## 🐛 Bug Fixes

- Bump dependencies ([5b2e69a](https://github.com/favware/cliff-jumper/commit/5b2e69aab48860d4c6492635cfb179ad45bc2cd9))
- **deps:** Update sapphire dependencies ([431ed48](https://github.com/favware/cliff-jumper/commit/431ed4890fec20c6b8687ce48ff89c8d09b5bdb5))

# [@favware/cliff-jumper@1.8.6](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.8.5...@favware/cliff-jumper@1.8.6) - (2022-07-30)

## 🐛 Bug Fixes

- Update dependecies ([93eab72](https://github.com/favware/cliff-jumper/commit/93eab72d1b986511e5808c1f5a36c61f7cd9f72e))
- **deps:** Update dependency @sapphire/result to ^2.0.1 ([cc26aa0](https://github.com/favware/cliff-jumper/commit/cc26aa0209d924542bdc1f6333289e36051be10e))
- **deps:** Update dependency @sapphire/utilities to ^3.7.0 ([e9bfa0a](https://github.com/favware/cliff-jumper/commit/e9bfa0ac1aa13ba8999b6e3e65d3d7c8cdf08969))

# [@favware/cliff-jumper@1.8.5](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.8.4...@favware/cliff-jumper@1.8.5) - (2022-06-29)

## 🐛 Bug Fixes

- Use resolved new version if available ([eacdb59](https://github.com/favware/cliff-jumper/commit/eacdb59b6694b063423ab4c19379b4ed1fb76cb1))

# [@favware/cliff-jumper@1.8.4](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.8.3...@favware/cliff-jumper@1.8.4) - (2022-06-26)

## 🏠 Refactor

- Update to sapphire result v2 ([eaeb14a](https://github.com/favware/cliff-jumper/commit/eaeb14a00baa53881c55c8c0410bf86b4ecfd16a))

# [@favware/cliff-jumper@1.8.3](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.8.2...@favware/cliff-jumper@1.8.3) - (2022-06-06)

## 🏠 Refactor

- Change dry run method for comitting ([40190cd](https://github.com/favware/cliff-jumper/commit/40190cd22a010f4822569122fd8804824b156623))
- Deduplicate tag template resolver ([ad95276](https://github.com/favware/cliff-jumper/commit/ad95276226da43454351f84f3dad34c15f64ef9b))

## 🐛 Bug Fixes

- Ensure `--dry-run` goes through the whole process while not writing anything ([1dc7709](https://github.com/favware/cliff-jumper/commit/1dc77099966b10eb71c3f3585277042a184cdddf))
- Use tagTemplate for git cliff ([5a59274](https://github.com/favware/cliff-jumper/commit/5a592745023d194af0797cbbfa5a140aabe71daf))
- **deps:** Update all non-major dependencies ([9f55cb5](https://github.com/favware/cliff-jumper/commit/9f55cb5e293be2aaa1de60479b91c997fbd46bb6))

# [@favware/cliff-jumper@1.8.2](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.8.0...@favware/cliff-jumper@1.8.2) - (2022-06-03)

## 🏠 Refactor

- Stop using npm to read new version and instead read and parse JSON ([7207e45](https://github.com/favware/cliff-jumper/commit/7207e4503350c7469648292e418948847e72b7be))

## 🐛 Bug Fixes

- Properly resolve pre-releases ([cc760af](https://github.com/favware/cliff-jumper/commit/cc760af56ee5f1dfc00264334d42ec95b3520d69))
- Stop using `npm version` to bump package and instead use `semver` directly ([662b90e](https://github.com/favware/cliff-jumper/commit/662b90e9b8acb2f6419a599cbac569f33ccb45a2))

## 📝 Documentation

- Add @renovate[bot] as a contributor ([75da1b1](https://github.com/favware/cliff-jumper/commit/75da1b1f9dcccc53071c77189fe9f3245fd5a3a5))
- Add @renovate-bot as a contributor ([a3558eb](https://github.com/favware/cliff-jumper/commit/a3558eb64ded8671567e4e79c4a1e40f025af014))
- Fix JSON schema ([df316de](https://github.com/favware/cliff-jumper/commit/df316deeb67f9c64fd38fc8138f73dd9a28e55c7))

# [@favware/cliff-jumper@1.8.0](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.7.0...@favware/cliff-jumper@1.8.0) - (2022-05-13)

## 🚀 Features

- Allow forcing `skipChangelog` and `skipTag` to `false` with `--no-*` flags ([99ffe13](https://github.com/favware/cliff-jumper/commit/99ffe132c154bea0d4c6fd9aafac95576977498f))

# [@favware/cliff-jumper@1.7.0](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.6.0...@favware/cliff-jumper@1.7.0) - (2022-05-07)

## 🐛 Bug Fixes

- Log the package and version and bumping the version ([c50a27e](https://github.com/favware/cliff-jumper/commit/c50a27ec0f0ed0ba7f609b9fd6784e0a26012788))

## 🚀 Features

- Revert b4bc73d99482416e73a69320ad09f2b853a26509 (do not auto disable changelog generation in CI) ([41fb85a](https://github.com/favware/cliff-jumper/commit/41fb85acca94fc46fc3a86ed1d35f1060c526388))

# [@favware/cliff-jumper@1.6.0](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.5.1...@favware/cliff-jumper@1.6.0) - (2022-05-07)

## 🐛 Bug Fixes

- Do not auto disable changelog generation in CI ([b4bc73d](https://github.com/favware/cliff-jumper/commit/b4bc73d99482416e73a69320ad09f2b853a26509))

## 🚀 Features

- Log the package and version after generating the changelog ([71ab681](https://github.com/favware/cliff-jumper/commit/71ab681081b237beb9adfff716094820cca5eb5a))

## 🪞 Styling

- Change emoji from 📦 to 📝 ([6304346](https://github.com/favware/cliff-jumper/commit/630434640e07a34da181906c60387ca92a1baef7))

# [@favware/cliff-jumper@1.5.1](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.5.0...@favware/cliff-jumper@1.5.1) - (2022-05-07)

## 🐛 Bug Fixes

- List tag template in verbose options log ([87393a2](https://github.com/favware/cliff-jumper/commit/87393a2d823dabaaeddd2a305ea9e620f09fa363))
- Only require `options.monoRepo` to use mono repo detection for conventional recommended bump ([f1548f3](https://github.com/favware/cliff-jumper/commit/f1548f37533e3d96b3add115376203294b2da600))

# [@favware/cliff-jumper@1.5.0](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.4.0...@favware/cliff-jumper@1.5.0) - (2022-05-07)

## 🚀 Features

- Add tag template option ([1e047b6](https://github.com/favware/cliff-jumper/commit/1e047b660303495812fcdecaeb26ec205856323b))

# [@favware/cliff-jumper@1.4.0](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.3.1...@favware/cliff-jumper@1.4.0) - (2022-04-28)

## Features

- Log `yarn npm publish` when the package is using Yarn v3 ([983b191](https://github.com/favware/cliff-jumper/commit/983b19154e930177ac344a726c746fc87076b0ae))
- Introduce new flag `--skip-changelog` and separate `skip-tag` from it. Follows same behaviour to ensure non-breaking ([b21b772](https://github.com/favware/cliff-jumper/commit/b21b772dd2196689c934b7a0f3af18a60d89af5b))

# [@favware/cliff-jumper@1.3.1](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.3.0...@favware/cliff-jumper@1.3.1) - (2022-04-26)

## Bug Fixes

- **tag:** Only tag with package name in mono repos ([bb73dc3](https://github.com/favware/cliff-jumper/commit/bb73dc3b65a536a021f251116e7caa27dcdf25a6))

# [@favware/cliff-jumper@1.3.0](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.2.0...@favware/cliff-jumper@1.3.0) - (2022-04-26)

## Features

- Add `--mono-repo` and `--no-mono-repo` flags ([6d86477](https://github.com/favware/cliff-jumper/commit/6d86477335a39a13c7f074b7502b05067ebd47fc))

# [@favware/cliff-jumper@1.2.0](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.1.3...@favware/cliff-jumper@1.2.0) - (2022-04-21)

## Features

- Add `commitMessageTemplate` ([933a6e5](https://github.com/favware/cliff-jumper/commit/933a6e5c4ec88e48e9de88aa995ea1a2d94c3d20))

# [@favware/cliff-jumper@1.1.3](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.1.2...@favware/cliff-jumper@1.1.3) - (2022-04-18)

## Bug Fixes

- Fixed commit message being invalid after execa->execSync change ([37ed667](https://github.com/favware/cliff-jumper/commit/37ed667493470d8d912312377b81a5994e36301a))
- Switch from `execa` to `execSync` ([4f26562](https://github.com/favware/cliff-jumper/commit/4f265626317e831c7ceb8567853e6a598f8c5120))

# [@favware/cliff-jumper@1.1.2](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.1.1...@favware/cliff-jumper@1.1.2) - (2022-04-18)

## Bug Fixes

- Properly check if git cliff exists or not ([5ab2727](https://github.com/favware/cliff-jumper/commit/5ab2727f0a6909c53173db0303b32a6a3c9c56fa))

# [@favware/cliff-jumper@1.1.1](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.1.0...@favware/cliff-jumper@1.1.1) - (2022-04-18)

## Bug Fixes

- Only check for changelog and git-cliff when `skip-tag` is `false` ([7d3a2c8](https://github.com/favware/cliff-jumper/commit/7d3a2c87a48fa72cc94a3c121eed50093d78237a))
- Fixed bundle published to npm ([c1d996d](https://github.com/favware/cliff-jumper/commit/c1d996d2a89cd65d08ad784dc3ab5b8306ab3156))

# [@favware/cliff-jumper@1.1.0](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.0.2...@favware/cliff-jumper@1.1.0) - (2022-04-18)

## Features

- Add notice once done about pushing and publishing ([a9a54a5](https://github.com/favware/cliff-jumper/commit/a9a54a5dd81b97690e1ecb8b33c0526419f1dbbf))

## Refactor

- Improve checking for `git cliff` ([82c9500](https://github.com/favware/cliff-jumper/commit/82c9500f13267d759f63257e6bdbcd30554afde1))

# [@favware/cliff-jumper@1.0.2](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.0.1...@favware/cliff-jumper@1.0.2) - (2022-04-18)

## Bug Fixes

- Add missing `conventional-changelog-angular` dependency ([f3efcc8](https://github.com/favware/cliff-jumper/commit/f3efcc811f5d9b980db735f6e64239302c0d2261))

# [@favware/cliff-jumper@1.0.1](https://github.com/favware/cliff-jumper/compare/@favware/cliff-jumper@1.0.0...@favware/cliff-jumper@1.0.1) - (2022-04-18)

## Bug Fixes

- **github-release:** Use yarn publish ([8453aa4](https://github.com/favware/cliff-jumper/commit/8453aa45da4bf6c007b9dcb845e454cb52792329))

# [@favware/cliff-jumper@1.0.0]
(https://github.com/favware/cliff-jumper/tree/@favware/cliff-jumper@1.0.0) - (2022-04-17)

## Bug Fixes

- **commit:** Remove wrapping quotes from commit ([9891524](https://github.com/favware/cliff-jumper/commit/98915241438c4a420d3377b668cf72356985265f))
- Fixed tag in changelog ([14ac52f](https://github.com/favware/cliff-jumper/commit/14ac52f71711ec4c5d10894fbfcdf11f4ce0225b))
- Fixed resolving git-cliff options ([ae7eb84](https://github.com/favware/cliff-jumper/commit/ae7eb84a9fe7e1e235449e24d74906f1e02ba01e))
- Fixed resolving repository root ([7fb9f72](https://github.com/favware/cliff-jumper/commit/7fb9f72f3cef01afa0724cdeb922acb44880dced))
- Better fix for parsing options ([867abe1](https://github.com/favware/cliff-jumper/commit/867abe14ab5f3afa68f2fbdd88d3b9fd24e108a3))
- Resolved issue with merging of options ([b1abe16](https://github.com/favware/cliff-jumper/commit/b1abe16c0eb49b14c00c3e15ae46d4804d5b2903))
- Fixed boolean options ([4bf2b0b](https://github.com/favware/cliff-jumper/commit/4bf2b0b23b05dd8832140f4df41ed3ad9537bdc0))
- Ensure git-cliff can properly be detected ([bea671a](https://github.com/favware/cliff-jumper/commit/bea671ab5a687a94bbfbefa14940c7b03eb1e27e))
- Manually check required options ([8d54298](https://github.com/favware/cliff-jumper/commit/8d54298fb4a9b5e3a81f5bc9f526fc75216aa002))

## Features

- Hello github 🎉 ([765fe15](https://github.com/favware/cliff-jumper/commit/765fe15f005d36e674b08dd0dd82b2fe74546c98))

## Refactor

- Rename bump to dry-run ([87b3ba0](https://github.com/favware/cliff-jumper/commit/87b3ba02550aaa7181b974b14e70ebf6bc09031f))

