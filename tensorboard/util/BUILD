package(default_visibility = ["//tensorboard:internal"])

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])  # Needed for internal repo.

py_library(
    name = "encoder",
    srcs = ["encoder.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":op_evaluator",
        "//tensorboard:expect_numpy_installed",
        "//tensorboard:expect_tensorflow_installed",
        "//tensorboard:tf_contrib_ffmpeg",
    ],
)

py_test(
    name = "encoder_test",
    size = "small",
    srcs = ["encoder_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":encoder",
        "//tensorboard:expect_numpy_installed",
        "//tensorboard:expect_tensorflow_installed",
        "@org_pythonhosted_six",
    ],
)

py_library(
    name = "op_evaluator",
    srcs = ["op_evaluator.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorboard:expect_tensorflow_installed",
    ],
)

py_test(
    name = "op_evaluator_test",
    size = "small",
    srcs = ["op_evaluator_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":op_evaluator",
        "//tensorboard:expect_tensorflow_installed",
    ],
)

py_library(
    name = "util",
    srcs = ["util.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorboard:tf_contrib_ffmpeg",
        "//tensorboard/compat:tensorflow",
        "@org_pythonhosted_six",
    ],
)

py_test(
    name = "util_test",
    size = "small",
    srcs = ["util_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":test_util",
        ":util",
        "//tensorboard:expect_tensorflow_installed",
        "@org_pythonhosted_six",
    ],
)


py_library(
    name = "test_util",
    testonly = 1,
    srcs = ["test_util.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":util",
        "//tensorboard:db",
        "//tensorboard:expect_sqlite3_installed",
        "//tensorboard:expect_tensorflow_installed",
    ],
)
