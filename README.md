# Bazel rules-js vite

This repo contains a minimal example of attempting to use Vite with Bazel
rules_js.

To run:

```bash
bazelisk run //:vite -- --help
```

```
$BAZEL_OUT/darwin_arm64-fastbuild/bin/vite_/vite.runfiles/_main/node_modules/.aspect_rules_js/rollup@4.24.3/node_modules/rollup/dist/native.js:63
                throw new Error(
                      ^

Error: Cannot find module @rollup/rollup-darwin-arm64. npm has a bug related to optional dependencies (https://github.com/npm/cli/issues/4828). Please try `npm i` again after removing both package-lock.json and node_modules directory.
    at requireWithFriendlyError ($BAZEL_OUT/darwin_arm64-fastbuild/bin/vite_/vite.runfiles/_main/node_modules/.aspect_rules_js/rollup@4.24.3/node_modules/rollup/dist/native.js:63:9)
    at Object.<anonymous> ($BAZEL_OUT/darwin_arm64-fastbuild/bin/vite_/vite.runfiles/_main/node_modules/.aspect_rules_js/rollup@4.24.3/node_modules/rollup/dist/native.js:72:76)
    ... 3 lines matching cause stack trace ...
    at Module._load (node:internal/modules/cjs/loader:1104:12)
    at cjsLoader (node:internal/modules/esm/translators:346:17)
    at ModuleWrap.<anonymous> (node:internal/modules/esm/translators:286:7)
    at ModuleJob.run (node:internal/modules/esm/module_job:234:25)
    at async ModuleLoader.import (node:internal/modules/esm/loader:473:24) {
  [cause]: Error: Cannot find module '@rollup/rollup-darwin-arm64'
```
