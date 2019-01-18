<!---

PROFESSOR TASK LIST:

  * Use cp -r to copy all of the files and directories in this repository
    to the starter repository for this assignment
  * Change into the directory for the starter repository
  * Update the header (e.g., #) to only give the name of the assignment
  * Update the first paragraph to include the commented-out content
  * Change the link in the # Problems section to point to this lab's starter
  * Create the assignment in the GitHub Classroom, noting the URL
  * Test the assignment by accepting it with your own GitHub account
  * Check to ensure that your GitHub repository is created correctly
  * Share the assignment link with all of the students using email or Slack

PROFESSOR PROBLEMS?

  * Contact Gregory M. Kapfhammer by email or Slack
  * Raise an issue in the GitHub repository for this assignment starter

-->

# cs203-S2019-practical1-starter

Designed for use with [GitHub Classroom](https://classroom.github.com/), this
repository contains the starter for Practical 1 in Computer Science 203.

<!--

Since the Travis builds for this repository will initially fail (as evidenced
by a red &#x2717; appearing in the commit logs instead of a green &#x2714;),
the programmer is responsible for completing all of the steps needed to satisfy
the requirements for the assignment, thus causing a &#x2714; to instead appear
in the commit logs.

-->

## Introduction

This assignment requires a programmer to implement, document, and automatically
test a Python program called `src/termfrequency/compute_tf_monolith.py`. Please
refer to the Preface and Chapters 1 through 3 in "Exercises in Programming
Style" to learn more about this program's input, output, and behavior. You can
also review Chapters 1 through 2 in "Think Python" to learn more about how to
program in Python and run Python scripts. In addition to fixing the bugs in this
program and fully documenting it, you must describe and put into practice an
automated testing strategy.

When you use the `git commit` command to transfer your source code to your
GitHub repository, [Travis CI](https://travis-ci.com/) will initialize a build
of your assignment, checking to see if it meets all of the requirements. If both
your source code and writing meet all of the established requirements, then you
will see a green &#x2714; in the listing of commits in GitHub. If your
submission does not meet the requirements, a red &#x2717; will appear instead.
The instructor will reduce a programmer's grade for this assignment if the red
&#x2717; appears on the last commit in GitHub immediately before the
assignment's due date.

## Learning

If you have not done so already, please read all of the relevant [GitHub
Guides](https://guides.github.com/) that explain how to use many of the features
that GitHub provides. In particular, please make sure that you have read the
following GitHub guides: [Mastering
Markdown](https://guides.github.com/features/mastering-markdown/), [Hello
World](https://guides.github.com/activities/hello-world/), and [Documenting Your
Projects on GitHub](https://guides.github.com/features/wikis/). Each of these
guides will help you to understand how to use both [GitHub](http://github.com) and
[GitHub Classroom](https://classroom.github.com/).

To do well on this assignment, you should also read Chapters 1 and 2 in "Think
Python", paying particularly close attention to the content about variables,
expressions, and statements. You should also read the Preface and Chapters 1
through 3 in the "Exercises in Programming Style" book. Please see the course
instructor or one of the teaching assistants or tutors if you have questions
about any of these reading assignments.

## Commands

To get started in using the GatorGrader tool, you can change into the directory
for this assignment and type the command `gradle grade` in your terminal.
Running this command will produce a lot of output that you should carefully
inspect. If the output indicates that GatorGrader judges that there are no
mistakes in the assignment, then this means that your source code and writing
are passing all of the automated baseline checks. However, if the output
indicates that there are mistakes, then you will need to understand what they
are and then try to fix them.

This practical assignment also requires students to use
[Pipenv](https://github.com/pypa/pipenv) to create a virtual environment,
install and manage development packages, and to run Python commands. Here is a
sample of the Pipenv commands that you will need to run during this assignment.

- Install and upgrade the `pipenv` command: `pip install pipenv -U --user`
- Reformat the program with `black`: `pipenv run black src/termfrequency/compute_tf_monolith.py`
- Check the program with `pylint`: `pipenv run pylint src/termfrequency`
- Check the program with `flake8`: `pipenv run flake8 src/termfrequency`
- Run the program with `pipenv` and `python3` and a small input: `pipenv run python3 src/termfrequency/compute_tf_monolith.py inputs/input.txt`
- Run the program with `pipenv` and `python3` and a realistic input: `pipenv run python3 src/termfrequency/compute_tf_monolith.py inputs/pride-and-prejudice.txt`

To run one of these commands, you must be in the main directory for this
assignment where the configuration files are located. Then, you can type these
commands in the terminal and study the output.

## Output

Running the program with the small input should produce the following output:

```
live  -  2
mostly  -  2
white  -  1
tigers  -  1
india  -  1
wild  -  1
lions  -  1
africa  -  1
```

Running the program with the realistic input should produce the following output:

```
mr  -  786
elizabeth  -  635
very  -  488
darcy  -  418
such  -  395
mrs  -  343
much  -  329
more  -  327
bennet  -  323
bingley  -  306
jane  -  295
miss  -  283
one  -  275
know  -  239
before  -  229
herself  -  227
though  -  226
well  -  224
never  -  220
sister  -  218
soon  -  216
think  -  211
now  -  209
time  -  203
good  -  201
```

## Checks

- src/termfrequency/compute_tf_monolith.py:
  - Features at least twelve single-line Python comments
  - Contains exactly one use of a `for tf in words_freq` statement
  - Contains exactly eleven uses of a `words_freq` statement
  - Runs correctly through `pipenv` without crashing or producing an error
  - Produces exactly eight lines of output in the terminal when run with `inputs/input.txt`

- writing/reflection.md:
  - Passes the checks performed by the Markdown linting tool
  - Passes the checks performed by the proselint linting tool
  - Contains exactly four contiguous paragraph of formatted text
  - Each contiguous paragraph contains at least 100 words

- GitHub repository:
  - Contains five commits beyond the repository's starting number of commits

## Updates

If the course instructor updates the provided material for this assignment and
you would like to receive these updates, then you can type this command in the
main directory for this assignment:

```
git remote add download git@github.com:Allegheny-Computer-Science-203-S2019/cs203-S2019-practical1-starter.git
```

You should only need to type this command once; typing the command additional
times may yield an error message but will not negatively influence the state of
your repository. Now, you are ready to download the updates provided by the
course instructor by typing:

```
git pull download master
```

This second command can be run whenever the course instructor needs to provide
you with new source code for this assignment. However, please note that, if you
have edited the files that the course instructor updated, running the previous
command may lead to Git merge conflicts. If this happens, you may need to
manually resolve them with the help of the instructor or a teaching assistant.

## Travis

This assignment uses [Travis CI](https://travis-ci.com/) to automatically run
the checking programs every time you commit to your GitHub repository. The
checking will start as soon as you have accepted the assignment, thus creating
your own private repository, and the course instructor enables Travis for it. If
you are using Travis for the first time, you will need to authorize Travis CI to
access the private repositories that you created on GitHub.

## Requirements

The GatorGrader software that supports the checking of this assignment was
developed for the following software and versions:

- Gradle 4.6
- Java 1.8.0
- MDL 0.4.0
- Proselint 0.8.0
- Python 3.6

## Problems

If you have found a problem with this assignment's provided source code, then
you can go to the [Computer Science 203 Practical 1
Starter](https://github.com/Allegheny-Computer-Science-203-S2019/cs203-S2019-practical1-starter)
repository and create an issue by clicking the "Issues" tab and then clicking
the green "New Issue" button. If you have found a problem with the [GatorGrader
tool](https://github.com/GatorEducator/gatorgrader) and the way that it checks
you assignment, then you can follow the aforementioned steps to create an issue
in its repository. To ensure that your issue is properly resolved, please
provide as many details as is possible about the problem that you experienced.
If you discover a problem with the laboratory assignment sheet, then please
raise an issue in the
[cs203-S2019-sheets](https://github.com/Allegheny-Computer-Science-203-S2019/cs203-S2019-sheets)
repository and mention this assignment.

Students who find &mdash; and use the appropriate GitHub issue tracker to
correctly document &mdash; a mistake in any aspect of this laboratory assignment
will receive free GitHub stickers and extra credit towards their grade for it.

## Assistance

If you are having trouble completing any part of this project, then please talk
with either the course instructor or a teaching assistant during the laboratory
session. Alternatively, you may ask questions in the Slack workspace for this
course. Finally, you can schedule a meeting during the course instructor's
office hours.
