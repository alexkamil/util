scala_library(
    name = "testutil",
    sources = [
        "!*Test.scala",
        "*.java",
        "*.scala",
    ],
    dependencies = [
        "3rdparty/jvm/org/slf4j:slf4j-api",
        "util/util-core/src/main/scala/com/twitter/io",
        "util/util-slf4j-api/src/main/scala/com/twitter/util/logging",
        "util/util-slf4j-api/src/test/resources",
    ],
    exports = [
        "3rdparty/jvm/org/slf4j:slf4j-api",
        "util/util-core/src/main/scala/com/twitter/io",
        "util/util-slf4j-api/src/main/scala/com/twitter/util/logging",
        "util/util-slf4j-api/src/test/resources",
    ],
)

junit_tests(
    compiler_option_sets = ["fatal_warnings"],
    tags = ["non-exclusive"],
    dependencies = [
        ":testutil",
        "3rdparty/jvm/org/mockito:mockito-scala",
        "3rdparty/jvm/org/scalatest",
        "3rdparty/jvm/org/scalatestplus:junit",
        scoped(
            "3rdparty/jvm/org/slf4j:slf4j-simple",
            scope = "runtime",
        ),
        "util/util-mock/src/main/scala/com/twitter/util/mock",
    ],
)
