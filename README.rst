workspace_hq
============

Manage my workspace by git


General
-------

A web service that get my github information, including repos(self created and starred), gists etc,
and store these data.

Manage them by tagging and annotation.

Organize ``workspace`` by place repos under tree folder structure. Record its changes.

View by searching all the related informations.

Create CLI tools, which use HTTP API to access service data. Funtions include:

- quickly clone the whole workspace

- show status of the workspace, there are only two statuses:

  + synced

  + unsynced

  retrieve each repos under workspace, in conditions:

  + multiple branches

  + uncommitted changes or untracked files in any branch

  notice user to manually done them(if in sync mode).

- sync. execute show status process, after all changes have been committed,
  push each repo and prompt failed pushes at the end.

- generate a configuration file, user can modify it and sync by it.

  exampe::

    workspace
        archive
            repo1
        current
            repo2
            repo3
            user@domain.com:/repos/repo4.git repo4-new
        lab
            repo5
            repo6
