# Intro

The goal of this homework is to become familiar with the JUnit 5 Jupiter API. JUnit is the backbone for this course for writing tests and automating tests. As with the prior homework, some steps require research to complete. This lack of specificity is intentional, and students are encouraged to use the Internet to fill in the missing gaps. 

For help see: Part I & II of the [JUnit 5 Jupiter API Tutorial](https://developer.ibm.com/tutorials/j-introducing-junit5-part1-jupiter-api/).
The [HelloJUnit5](https://github.com/makotogo/HelloJUnit5) repository for the solution does include the solution file for reference.   

The [HelloJUnit5](https://github.com/makotogo/HelloJUnit5) project includes the needed support to run tests via `mvn` in the CLI. Look to that `pom.xml` for an example to how to add in support for running tests. That support is provided by the [Maven Surefire Plugin](https://maven.apache.org/surefire/maven-surefire-plugin/examples/junit-platform.html).

Some students have reported that the `pom.xml` file in the tutorial includes dependencies that muddle the reporting in `mvn test`. It is suggested that the following be removed from the `pom.xml`: `junit-platform-runner`, `junit-standalone-console-reporter`, and vintage engine dependencies.

After completing the homework, a student should be able to:

  * Add the JUnit 5 dependency to a Maven project
  * Write standard JUnit 5 tests `@Test`
  * Document tests with `@Tag` and `@DisplayName`
  * Organize tests with `@Nested`
  * Write parameterized JUnit 5 tests
  * Run JUnit 5 tests from the command line via `mvn test` and the [Surefire Plugin](https://maven.apache.org/surefire/maven-surefire-plugin/) for reporting.
  * Create patches with `git` and the `format-patch` command.

# Part I Maven Support of JUnit (20 points)

Complete this part of the homework by copying into this repository the code used to complete the previous **HW0 Tooling** homework with its `pom.xml` file, adding to that file anything needed for the [Maven Surefire Plugin](https://maven.apache.org/surefire/maven-surefire-plugin/examples/junit-platform.html) to build and run JUnit tests, and then adding in a single test to verify `mvn` finds, builds, runs, and reports the test. As a reminder, the code should be a few hundred lines with a fully documented class from the previous homework. 

# Part II  JUnit Tests (80 points)

Complete this part by writing tests for the code added in the previous part. The tests should be useful and related to the JavaDoc specification.

Students are expected to use descriptive naming conventions for test methods. There are a few key elements to [unit test names](https://qualitycoding.org/unit-test-names/). Pick a [convention](https://dzone.com/articles/7-popular-unit-test-naming) that works for you and stick with it.

Students are also expected to use `@Tag` to help filter tests and `@DisplayName` for more readable output in IDEs and reports. These annotations with grouping tests with nesting constitute acceptable documentation for tests.

Create test methods using each of the following annotations:
  * @Test	
  * @BeforeAll	
  * @BeforeEach	
  * @AfterEach	
  * @AfterAll	
  * @Disabled	
  * @ParameterizedTest
  * @Nested

Use each of the following assertions/assumptions somewhere in the created methods:
  * assertEquals(expected, actual)	The assertion fails if expected does not equal actual.
  * assertFalse(booleanExpression)	The assertion fails if booleanExpression is not false.
  * assertNull(actual)	The assertion fails if actual is not null.
  * assertNotNull(actual)	The assertion fails if actual is null.
  * assertTrue(booleanExpression)	The assertion fails if booleanExpression is not true.
  * assertAll(
      "Assert All of these",
      () ‑> assert<...>(...),
      () ‑> assert<...>(...));
  * assertThrows(NullPointerException.class, () ‑> ...do something...);
  * assumeTrue(booleanExpression);
      
# Grading Rubric

See canvas for details



