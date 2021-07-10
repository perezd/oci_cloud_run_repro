load("@io_bazel_rules_docker//container:push.bzl", "container_push")
load("@io_bazel_rules_docker//java:image.bzl", "java_image")

java_image(
    name = "main",
    srcs = ["Main.java"],
    main_class = "repro.Main",
)

container_push(
    name = "main.push",
    format = "OCI",
    image = ":main",
    registry = "gcr.io",
    repository = "<GCR REPO HERE>",
    tag = "{BUILD_TIMESTAMP}",
)
