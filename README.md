# gitlab-runner-local
A git runner to run on developers local machines, to prevent tedious "live" debugging on gitlab.

# Dev script
    $ npm run build
    $ node -r source-map-support/register dist/index.js --cwd D:/Workspace/puzzle-parade

# Build binaries
    $ npm run build-linux
    $ npm run build-win
    $ npm run build-macos

### Missing local overrides
- before_script

### Unsupported tags
- include
- after_script
- allow_failure
- rules
- cache
- artifacts/dependencies
- when:on_failure,always,delayed
- start_in (Used only with when:delayed)
- needs
- coverage
- retry
- timeout
- parallel
- trigger
- resource_group
- extends
- pages
- environment

### Docker specfic tags.
- services
- image

### Gitlab only sematics, will not be stripped nor used by gitlab-runner-local
- interruptible
- when:manual
- only
- except