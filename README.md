# Python project for the monitoring of general log activity.
# Classification (U)

# Description:
  The check_log program checks log files or "standard in" for new data since the last run as determined by the contents of the marker file.  This program is used to monitor ASCII text logs or standard in for any new activity.  The program can also setup filtering options to either ignore specific messages and/or allow specific formatted messages through.  It also has the capability for keyword searching based on an 'and|or' search logic.

###  This README file is broken down into the following sections:
  * Features
  * Prerequisites
  * Installation
  * Program Help Function
  * Testing
    - Unit
    - Integration
    - Blackbox


# Features:
  * Monitor ASCII type logs for changes.
  * Monitor standard in for new entries.
  * Use a marker log file to maintain location within a log file.
  * Filter out specific entries.
  * Regular expression capability for message searching.
  * Keyword searching of files using 'and|or' search logic.
  * Can search gzipped files.


# Prerequisites:

  * List of Linux packages that need to be installed on the server.
    - git
    - python-pip

  * Local class/library dependencies within the program structure.
    - python-lib


# Installation:

Install the project using git.
  * From here on out, any reference to **{Python_Project}** or **PYTHON_PROJECT** replace with the baseline path of the python program.

```
umask 022
cd {Python_Project}
git clone git@github.com:deepcoder42/check-log.git
```

Install/upgrade system modules.

```
cd check-log
sudo bash
umask 022
pip install -r requirements.txt --upgrade --system
exit
```

Install supporting classes and libraries.

```
pip install -r requirements-python-lib.txt --target lib --system
```


# Program Help Function:

  All of the programs, except the command and class files, will have an -h (Help option) that will show display a help message for that particular program.  The help message will usually consist of a description, usage, arugments to the program, example, notes about the program, and any known bugs not yet fixed.  To run the help command:

```
{Python_Project}/check-log/check_log.py -h
```


# Testing:

# Unit Testing:

### Installation:

Install the project using the procedures in the Installation section.

### Testing:

```
cd {Python_Project}/check-log
test/unit/check_log/unit_test_run.sh
```

### Code Coverage:

```
cd {Python_Project}/check-log
test/unit/check_log/code_coverage.sh
```


# Integration Testing:

### Installation:

Install the project using the procedures in the Installation section.

### Testing:

```
cd {Python_Project}/check-log
test/integration/check_log/integration_test_run.sh
```

### Code Coverage:

```
cd {Python_Project}/check-log
test/integration/check_log/code_coverage.sh
```


# Blackbox Testing:

### Installation:

Install the project using the procedures in the Installation section.

### Testing:  

```
cd {Python_Project}/check-log
test/blackbox/check_log/blackbox_test.sh
```

