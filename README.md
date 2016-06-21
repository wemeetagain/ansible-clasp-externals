Clasp Externals
=========

Ansible Role to install Clasp dependencies.

Requirements
------------

Currently Archlinux or Ubuntu

Role Variables
--------------

- `externals_clasp_dir` - where to clone the externals-clasp to
locally, default: /home/vagrant/externals-clasp
- `externals_clasp_repo_url` - git repo url of externals-clasp,
default: https://github.com/drmeister/externals-clasp
- `externals_clasp_version` - the branch, commit, tag to use, default:
  master
- `externals_clasp_target` - the make target to invoke, default: all
- `pjobs` - the number of parallel jobs to use for C/++ compilation,
default: 2
- `gcc_toolchain` - defines the root directory where gcc binaries can
be found (gcc_toolchain/bin/gcc exists), default: /usr
- `gcc_executable` - default: "{{ gcc_toolchain }}/bin/gcc"
- `gxx_executable` - default: "{{ gcc_toolchain }}/bin/g++"


Example Playbook
----------------

    - hosts: servers
      roles:
         - clasp-externals

License
-------

MIT
