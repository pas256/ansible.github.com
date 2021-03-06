.. _git:

git
```

Deploys software (or files) from git checkouts.

+--------------------+----------+---------+----------------------------------------------------------------------------+
| parameter          | required | default | comments                                                                   |
+====================+==========+=========+============================================================================+
| repo               | yes      |         | git, ssh, or http protocol address of the git repo                         |
+--------------------+----------+---------+----------------------------------------------------------------------------+
| dest               | yes      |         | absolute path of where the repo should be checked out to                   |
+--------------------+----------+---------+----------------------------------------------------------------------------+
| version            | no       | HEAD    | what version to check out -- either the git SHA, the literal string        |
|                    |          |         | 'HEAD', branch name, or a tag name.                                        |
+--------------------+----------+---------+----------------------------------------------------------------------------+
| remote             | no       | origin  | name of the remote branch                                                  |
+--------------------+----------+---------+----------------------------------------------------------------------------+

Example action from Ansible :doc:`playbooks`::

    git repo=git://foosball.example.org/path/to/repo.git dest=/srv/checkout version=release-0.22
