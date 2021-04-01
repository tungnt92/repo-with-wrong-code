MACOS, LINUX
## Install
```
npm install -g @commitlint/cli @commitlint/config-conventional
```
## Configure
```
touch commitlint.config.js

echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
```
## Test
```
# Lint from stdin
echo 'foo: bar' | commitlint

⧗   input: foo: bar
✖   type must be one of [build, chore, ci, docs, feat, fix, perf, refactor, revert, style, test] [type-enum]

✖   found 1 problems, 0 warnings
ⓘ   Get help: https://github.com/conventional-changelog/commitlint/#what-is-commitlint
```
```
# Lint last commit from history
commitlint --from=HEAD~1
```
