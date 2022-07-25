load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")
http_archive(
    name = "hedron_compile_commands",
    sha256 = "bfa65c8cf82fa9c9b748bbd33d63d016426bdef6e8c961e8f763dfce9444fa1b",
    strip_prefix = "bazel-compile-commands-extractor-ac78f5f1e2679b9f5b62eeae33055ede355672e6",
    url = "https://github.com/hedronvision/bazel-compile-commands-extractor/archive/ac78f5f1e2679b9f5b62eeae33055ede355672e6.tar.gz",
)

load("@hedron_compile_commands//:workspace_setup.bzl", "hedron_compile_commands_setup")

hedron_compile_commands_setup()

new_local_repository(
    name = "org_libpng_libpng",
    build_file = "//:libpng.BUILD",
    path = "/usr",
)
