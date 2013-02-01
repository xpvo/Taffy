# Guidelines for Contributing to Taffy

Contributions of all shapes and sizes are welcome, encouraged, and greatly appreciated!

For all contributions, you'll need a [free GitHub account](https://github.com/signup/free).

## Bug Reports / Feature Requests

Please include all of the following information in your ticket:

* CFML Platform and version (e.g. Adobe ColdFusion 9.0.2, Railo 4.0.2)
* Java version (look it up in CF Administrator, or do `java -version` at the command line)
* Taffy version (for bugs)

## Documentation

Please see [how you can contribute to the wiki via pull requests](http://fusiongrokker.com/post/how-you-can-contribute-to-taffy-documentation).

There's no such thing as perfect documentation. It can never be thorough enough, never perfectly organized. If you find something confusing or outdated, please at least be so kind as to file a bug report for it, if you can't or won't fix it.

## Code

Starting with the development of Taffy 1.4, all new development will be done against the **master** branch. When you want to make a change and submit it for the Bleeding Edge Release (BER), do the following:

1. [Fork the project](https://github.com/atuttle/Taffy/fork_select)
1. Clone to your local machine: `git clone https://github.com/YOUR-GITHUB-USERNAME/Taffy.git`
1. Create a topic branch for your changes: `git checkout -b BRANCH_NAME`
1. Make your changes and commit them.
1. Push your changes back to your fork. `git push -u origin BRANCH_NAME`
1. Send a pull request ([help with pull requests](https://help.github.com/articles/using-pull-requests))
  a. please make sure you select **master** as the destination branch

### Tests

If at all possible, please include test cases for anything you add or change. Taffy uses [MXUnit](http://www.mxunit.org) (not included) for testing.

You can run the test suite from the command line with Apache Ant. It's the default target, so just type `ant` from the root of the project directory and it should run them for you.

You can also run the tests in your browser. Install MXunit to `/mxunit` and Taffy to `/taffy`, and then point your browser to: `http://localhost/taffy/tests` (this will initialize the test api), and then to `http://localhost/taffy/tests/tests/`, which will run the test suite.

Taffy uses Jenkins for continuous integration, and you can see [build status/history here](http://fusiongrokker.com:8080/job/Taffy/).