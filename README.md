The purpose of this code is to demonstrate a seeming bug in the hedronvision
bazel-compile-commands-extractor project.

Steps to reproduce the issue:
1. `sudo apt-get update && apt-get install -y --no-install-recommends libpng-dev`
1. `bazel run @hedron_compile_commands//:refresh_all`
1. Open the file `test.cc`--you should see an error on the first 'include' that says:

    "In included file: 'stdlib.h' file not foundclang(pp_file_not_found)"