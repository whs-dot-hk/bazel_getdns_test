load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_foreign_cc",
    strip_prefix = "rules_foreign_cc-master",
    url = "https://github.com/bazelbuild/rules_foreign_cc/archive/master.zip",
)

load("@rules_foreign_cc//:workspace_definitions.bzl", "rules_foreign_cc_dependencies")

rules_foreign_cc_dependencies()

http_archive(
    name = "openssl",
    build_file = "@//:BUILD.openssl",
    strip_prefix = "openssl-1.1.1h",
    urls = ["https://www.openssl.org/source/openssl-1.1.1h.tar.gz"],
)

http_archive(
    name = "expat",
    build_file = "@//:BUILD.expat",
    strip_prefix = "expat-2.2.9",
    urls = ["https://github.com/libexpat/libexpat/releases/download/R_2_2_9/expat-2.2.9.tar.gz"],
)

http_archive(
    name = "unbound",
    build_file = "@//:BUILD.unbound",
    strip_prefix = "unbound-1.11.0",
    urls = ["https://www.nlnetlabs.nl/downloads/unbound/unbound-1.11.0.tar.gz"],
)

http_archive(
    name = "check",
    build_file = "@//:BUILD.check",
    strip_prefix = "check-0.15.2",
    urls = ["https://github.com/libcheck/check/releases/download/0.15.2/check-0.15.2.tar.gz"],
)

http_archive(
    name = "yaml",
    build_file = "@//:BUILD.libyaml",
    strip_prefix = "yaml-0.2.5",
    urls = ["https://github.com/yaml/libyaml/releases/download/0.2.5/yaml-0.2.5.tar.gz"],
)

load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")

new_git_repository(
    name = "getdns",
    build_file = "@//:BUILD.getdns",
    init_submodules = True,
    remote = "https://github.com/getdnsapi/getdns.git",
    tag = "v1.6.0",
)
