# @pnpm/store.cafs

## 2.0.0

### Major Changes

- 083bbf590: Breaking changes to the API.

### Patch Changes

- 0fd9e6a6c: Don't prematurely bail out of adding source files if ENOENT is thrown [#6932](https://github.com/pnpm/pnpm/pull/6932).
- Updated dependencies [494f87544]
- Updated dependencies [70b2830ac]
- Updated dependencies [083bbf590]
- Updated dependencies [083bbf590]
  - @pnpm/store-controller-types@16.0.0
  - @pnpm/fetcher-base@15.0.0
  - @pnpm/graceful-fs@3.1.0

## 1.0.2

### Patch Changes

- 73f2b6826: When several containers use the same store simultaneously, there's a chance that multiple containers may create a temporary file at the same time. In such scenarios, pnpm could fail to rename the temporary file in one of the containers. This issue has been addressed: pnpm will no longer fail if the temporary file is absent but the destination file exists.

## 1.0.1

### Patch Changes

- fe1c5f48d: The length of the temporary file names in the content-addressable store reduced in order to prevent `ENAMETOOLONG` errors from happening [#6842](https://github.com/pnpm/pnpm/issues/6842).

## 1.0.0

### Major Changes

- 4bbf482d1: The package is renamed from `@pnpm/cafs` to `@pnpm/store.cafs`.

  The content-addressable store locker should be only created once per process. This fixes an issue that started happening after merging [#6817](https://github.com/pnpm/pnpm/pull/6817)
