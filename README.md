README

Author: Sam Malik

Here is a list of all the included scripts, and a brief description of what they do.



Usage:

./<scriptname> <assignmentname> [options]

Run with no arguments to see script specific usage instructions



complexitystats - calculates desired complexity stats of your code, also saves output of complexity tool to a file

inst - attempts to find and run the instructor executable for the specified assignment-prompts if multiple executables are found (supports command line args)

newtest - creates and runs a new test case (Note: it prompts for command line args to pass to your codde)
PATHS - specifies path to your 357 directory - CHANGE THIS

requirements - creates folder and copies Makefile if absent, and prints requirements, core tests, and feature tests to stdout
run - recompiles and runs your code (supports command line args)

submit - recompiles, stylechecks, runs complexity, zips, and hands in your code

test - runs all test cases at once

vd - checks all output files from tests and opens all pairs with diffs using vimdiff, each pair in its own tab (can take an optional extra parameter - test case number. if specified, vd will only open that test case's output and error file pairs in vimdiff mode)



TEST CASES

In order to work with this testing system, test cases MUST have any command line args on the first line of the test case file (usually in#, with # being a number). This is the format that ./newtest creates them in, and the format that ./test expects.



KNOWN ISSUES:

~~./submit does not handin for Project1 due to a difference in Mammen's naming convention; if this persists I'll write a fix~~ FIXED
   


INSTALLATION:

mkdir -p INSTALL_DIR && git clone http://github.com/smalik0/CPE-357-Scripts INSTALL_DIR && chmod +x INSTALL_DIR/* && chmod -x INSTALL_DIR/PATHS && chmod -x INSTALL_DIR/README.md

Then look at PATHS and point all the variables to the appropriate paths on your filesystem!!

Notes:

Put the scripts on the CSL Servers!!

Even if you want to work from your local environment, there must be an IDENTICAL copy of these scripts on the CSL servers in the path specified by $REMOTEDIR

For local editing, you will need the scripts BOTH on your machine and on the servers (the local scripts copy your files to the servers then do all the work on the servers before returning the output to your local machine)

ssh keys is extremely helpful for the local environment, as each script connects to the server several times (see Piazza for ssh key setup instructions)
