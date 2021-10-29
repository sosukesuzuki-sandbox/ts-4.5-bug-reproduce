# ts-4.5-bug-reproduce

Both `./4.4` and `./4.5` are same structure. The only difference point is TypeScript compiler version.

## Overview

`typescript@4.5.0-dev.20211029` does not throw error

```
TS5056: Cannot write file '/Users/user/ts-4.5-bug-reproduce/4.4/files/file.js' because it would be overwritten by multiple input files.
```

### Results of `4.4.4` (Expected)

https://github.com/sosukesuzuki-sandbox/ts-4.5-bug-reproduce/runs/4047598037?check_suite_focus=true#step:4:1

```
> 4.4@1.0.0 tsc /home/runner/work/ts-4.5-bug-reproduce/ts-4.5-bug-reproduce/4.4
> tsc

error TS5056: Cannot write file '/home/runner/work/ts-4.5-bug-reproduce/ts-4.5-bug-reproduce/4.4/files/file.js' because it would be overwritten by multiple input files.
npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! 4.4@1.0.0 tsc: `tsc`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the 4.4@1.0.0 tsc script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     /home/runner/.npm/_logs/2021-10-29T14_15_56_174Z-debug.log
Error: Process completed with exit code 1.
```

### Results of `typescript@4.5.0-dev.20211029` (Unexpected, should thorw error)

https://github.com/sosukesuzuki-sandbox/ts-4.5-bug-reproduce/runs/4047598031?check_suite_focus=true#step:4:1

```
added 1 packages in 1.161s

> 4.5@1.0.0 tsc /home/runner/work/ts-4.5-bug-reproduce/ts-4.5-bug-reproduce/4.5
> tsc
```
