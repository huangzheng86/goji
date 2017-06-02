goji
====

[![Build Status](https://travis-ci.org/kylef/goji.png?branch=master)](https://travis-ci.org/kylef/goji)

goji is a minimal command line client for JIRA.

**NOTE**: This is in early development, not fully ready yet.

## Usage

### login

Authenticate with a JIRA server.

```bash
$ goji login

Email: delisa@example.com
Password:
```

### show

Show detailed information about an issue.

```bash
$ goji show GOJI-1
-> GOJI-1
  As a user, I would like to view an issue status

  - Status: Closed
  - Creator: Kyle Fuller (kylef)
  - Assigned: Kyle Fuller (kylef)
  - URL: https://cocode.atlassian.net/browse/GOJI-1

  Related issues:
  - Relates to: GOJI-2 (Closed)
```

### open

Opens an issue in your browser.

```bash
$ goji open GOJI-1
```

### assign / unassign

Assigns yourself or another user to an issue.

```bash
$ goji assign GOJI-1
You have been assigned to GOJI-1.
$ goji assign GOJI-1 sam
sam has been assigned to GOJI-1.
$ goji unassign GOJI-1
GOJI-1 has been unassigned.
```

### comment

Add a comment to an issue, editing text in your `$EDITOR`

```bash
$ goji comment GOJI-1
```

### search

Search issues using
[JQL](https://confluence.atlassian.com/jiracoreserver073/advanced-searching-861257209.html)

```bash
$ goji search "project=GOJI AND assignee=sam"
GOJI-21 Update core metrics
GOJI-40 Remove expired food from fridge
```

### change-status

Change the status of an issue

```bash
$ goji change-status GOJI-311
Fetching possible transitions...
0: To Do
1: In Progress
2: Done
Select a transition: 1
Okay, the status for GOJI-311 is now "In Progress".
```

## License

goji is released under the BSD license. See [LICENSE](LICENSE).

