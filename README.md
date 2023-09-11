### Project Summary
This project aims to implement a daemon that serves as a build system manager for modules, providing support for explicitly built modules irrespective of the build system. By simply incorporating a single command line flag, each Clang invocation registers its translation unit with the daemon, which then scans the unit's dependencies. As translation units are registered and analyzed, the daemon constructs a dependency graph for the entire project. Concurrently, it utilizes the emerging graph to schedule and build each module's AST. This approach allows for a single, comprehensive entity to effectively coordinate and manage the build of modules throughout the entire build process.

### RFC
https://discourse.llvm.org/t/rfc-modules-build-daemon-build-system-agnostic-support-for-explicitly-built-modules/71524

### Commits
**[clang][deps] add support for dependency scanning with cc1 command line** \
https://github.com/llvm/llvm-project/commit/6b4de7b1c71b6b701e130c2a533d285dc93b8370

**[clang][deps] module build daemon infrastructure**
https://github.com/cpsughrue/llvm-project/commit/125185543b37fd312ba8df06ce19f15e94237b9a

**[clang][deps] add build functionality to module build daemon**
https://github.com/cpsughrue/llvm-project/commit/7efa8724bbbef47148e6b33842f1b5e8d9f77236
