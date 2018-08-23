ansible-role-pyenv
==================

[![Apache-2.0 License](https://img.shields.io/github/license/bluk/ansible-role-pyenv.svg)](https://github.com/bluk/ansible-role-pyenv/blob/master/LICENSE) [![Build Status](https://travis-ci.org/bluk/ansible-role-pyenv.svg?branch=master)](https://travis-ci.org/bluk/ansible-role-pyenv)

An [Ansible](https://www.ansible.com) role to install [pyenv](https://github.com/pyenv/pyenv).

Requirements
------------

1. Add `pyenv` to your `$PATH` after install.

```
echo 'export PATH="$HOME/.pyenv/bin:$PATH"' >> ~/.bash_profile
```

2. Run the following:

```
~/.pyenv/bin/pyenv init
```

Role Variables
--------------

* `pyenv_install_path` - The path to install `pyenv`.

* `pyenv_git_url` - The git URL to clone `pyenv` from.

* `pyenv_git_update` - If the cloned `pyenv` git repository should be updated.

* `pyenv_virtualenv_git_url` - The path to the `python-build` plugin for `pyenv`.

* `pyenv_virtualenv_git_update` - If the cloned `python-build` git repository should be updated.

Dependencies
------------

No dependencies.

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: bluk.pyenv }
```

License
-------

Apache 2.0
