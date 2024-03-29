# ven Orb

[![CircleCI Build Status](https://circleci.com/gh/vendrive/ven-orb.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/vendrive/ven-orb) [![CircleCI Orb Version](https://img.shields.io/badge/endpoint.svg?url=https://badges.circleci.io/orb/vendrive/ven)](https://circleci.com/orbs/registry/orb/vendrive/ven) [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/vendrive/ven-orb/master/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)

## Resources

[CircleCI Orb Registry Page](https://circleci.com/orbs/registry/orb/vendrive/ven) - The official registry page of this orb for all versions, executors, commands, and jobs described.

[CircleCI Orb Docs](https://circleci.com/docs/2.0/orb-intro/#section=configuration) - Docs for using and creating CircleCI Orbs.

## Usage
* Create and push a branch with your new features.
* When ready to publish a new production version, create a Pull Request from _feature branch_ to `master`.
* The title of the pull request must contain a special semver tag: `[semver:<segement>]` where `<segment>` is replaced by one of the following values.

| Increment | Description|
| ----------| -----------|
| major     | Issue a 1.0.0 incremented release|
| minor     | Issue a x.1.0 incremented release|
| patch     | Issue a x.x.1 incremented release|
| skip      | Do not issue a release|

Example commit message:

```
[semver:patch] Tiny fix
```

### Test Locally

```
circleci orb pack src
```

### Known Issues

If you see the following error:

```
The dev version of vendrive/ven@dev:alpha has expired. Dev versions of orbs are only valid for 90 days after publishing.
```

Do the following:

```
circleci orb pack src | circleci orb validate -
circleci orb pack src | circleci orb publish - vendrive/ven@dev:alpha
```

And push again.