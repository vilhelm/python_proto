# Any proto
```
bazel build :person_py_pb2

ERROR: [redacted]/python_proto/BUILD:3:1: in deps attribute of py_library rule //:person_py_pb2: '@com_google_protobuf//:any_proto' does not have mandatory providers: 'py'. Since this rule was created by the macro 'py_proto_library', the error might have been caused by the macro implementation in [redacted]/external/org_pubref_rules_protobuf/python/rules.bzl:72:12
ERROR: Analysis of target '//:person_py_pb2' failed; build aborted: Analysis of target '//:person_py_pb2' failed; build aborted
INFO: Elapsed time: 7.250s
FAILED: Build did NOT complete successfully (17 packages loaded)
```
