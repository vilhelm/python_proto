workspace(name = "python_proto")

http_archive(
    name = "org_pubref_rules_protobuf",
    strip_prefix = "rules_protobuf-master",
    urls = ["https://github.com/pubref/rules_protobuf/archive/master.zip"],
)

load("@org_pubref_rules_protobuf//python:rules.bzl", "py_proto_repositories")

py_proto_repositories()

# Recursive workspace declarations required until design is implemented.
# https://bazel.build/designs/2016/09/19/recursive-ws-parsing.html
new_http_archive(
    name = "six_archive",
    build_file_content = """
py_library(
    name = "six",
    srcs = ["six.py"],
    srcs_version = "PY2AND3",
    visibility = ["//visibility:public"],
)""",
    strip_prefix = "six-1.11.0",
    urls = ["https://github.com/benjaminp/six/archive/1.11.0.zip"],
)

bind(
    name = "six",
    actual = "@six_archive//:six",
)
