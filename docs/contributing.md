# Contributing {: .doctitle}
Tips for contributing to BracketHighlighter.

---

# Overview
BracketHighligher welcomes contribution from the community and is encouraged.  Contribution can be done in a variety of ways:

- Bug reports.
- Reviewing code.
- Code patches via pull requests.
- Documentation improvements via pull requests.

!!! warning "Bracket Rules are Supported by the Community"
    The most common requested enhancement for BH is for new rules to add support for \{insert your favorite language here}.  I, like you, am proficient in very specific languages.  I probably don't use your favorite language or there would already be a support for it.  I don't have time to learn the nuances of your language.  For these reasons, support for new language brackets **requires** pull requests from the community.

    Though I will not personally implement rules for your favorite language, I am more than willing to offer suggestions and guidance to help those who may struggle to create rules for their specific language of interest.

# Bug Reports

1. Please **read the documentation** and **search the issue tracker** to try to find the answer to your question **before** posting an issue.

2. When creating an issue on the BH repository, please provide as much info as possible:

    - Sublime Text build.
    - Operating system.
    - Errors in console.
    - Detailed description of the problem.
    - Examples for reproducing the error.  You can post pictures, but if specific text or code is required to reproduce the issue, please provide the text in a plain text format for easy copy/paste.

    The more info provided the greater the chance someone will take the time to answer, implement, or fix the issue.

3. Be prepared to answer questions and provide additional information if required.  Issues in which the creator refuses to respond to follow up questions will be marked as stale and closed.

# Reviewing Code
Take part in reviewing pull requests and/or reviewing direct commits.  Make suggestions to improve the code and discuss solutions to overcome weakness in the algorithm.

# Pull Requests
BH will gladly accept pull requests.  If you plan on contributing directly to the code, there are a couple of things to be mindful of.

BH runs continuous integration tests on pull requests and commits via Travis CI.  When making a pull request, the tests will automatically be run, and the request must pass to be accepted.  You can (and should) run these tests before pull requesting.  If it is not possible to run these tests locally, they will be run when the pull request is made, but it is strongly suggested that requesters make an effort to verify before requesting to allow for a quick, smooth merge.

## Running Validation Tests
There are a couple of dependencies that must present before running the tests.

1. As ST3 is the only current actively supported version, Python 3.3 must be used to validate the tests.

2. Unit tests are run with `nose`.  You can install nose via:

    ```
    pip install nose
    ```

    The tests should be run from the root folder of BH by using the following command:

    ```
    nosetests .
    ```

3. Linting is performed on the entire project with `flake8` and `flake8_docstrings`.  These can be installed via:

    ```
    pip install flake8
    pip install flake8_docstrings
    ```

    Linting is performed with the following command:

    ```
    flake8 --ignore=D202 --max-line-length=120 .
    ```

# Documentation Improvements
Help with documentation is always appreciated and can be done via pull requests.  There shouldn't be any need to run validation tests if only updating documentation.

*[BH]: BracketHighlighter
*[ST2]: Sublime Text 2
*[ST3]: Sublime Text 3