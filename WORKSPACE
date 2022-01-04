load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
http_archive(
    name = "build_bazel_rules_nodejs",
    sha256 = "f0f76a06fd6c10e8fb9a6cb9389fa7d5816dbecd9b1685063f89fb20dc6822f3",
    urls = ["https://github.com/bazelbuild/rules_nodejs/releases/download/4.5.1/rules_nodejs-4.5.1.tar.gz"],
)
load("@build_bazel_rules_nodejs//:index.bzl", "node_repositories", "yarn_install")
node_repositories(
    node_version = "16.13.0",
    yarn_version = "1.22.15",
)
yarn_install(
    name = "npm_a",
    package_json = "//subdir/a:package.json",
    package_path = "subdir/a",
    symlink_node_modules = False,
    yarn_lock = "//subdir/a:yarn.lock",
)
