Observe venv crashes below.

```
> bazel run //:conflict
INFO: Analyzed target //:conflict (0 packages loaded, 0 targets configured).
INFO: Found 1 target...
Target //:conflict up-to-date:
  bazel-bin/conflict
  bazel-bin/conflict.venv.pth
INFO: Elapsed time: 0.125s, Critical Path: 0.00s
INFO: 1 process: 1 internal.
INFO: Build completed successfully, 1 total action
INFO: Running command line: bazel-bin/conflict
thread 'main' panicked at py/tools/py/src/pth.rs:150:14:
called `Option::unwrap()` on a `None` value
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
```

