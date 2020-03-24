mtail setup
=========

This playbook installs mtail binary from github release page.

Requirements
------------

Only systemd-based systems are supported for now. Pull-requests are welcome.


Role Variables
--------------

| Variable | Description | Type | Default | Mandatory |
|----------|-------------|------|---------|-----------|
| mtail_version | mtail release version, defaults to newest version in the [page](https://github.com/google/mtail/releases). | string | v3.0.0-rc35 | true |
| mtail_args | Raw argument to `mtail` program | string |  | false |
| mtail_logs_list | Logs argument to `mtail` program | list | ['/var/log/syslog'] | true |
| mtail_progs_path | Progs argument to `mtail` program | string | /etc/mtail.d | true |
| mtail_download_path | Path to save binary | string | /opt/mtail | true |
| mtail_binary_path | Path to link executable binary | string | /usr/local/bin/ | true |


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
      - role: leboncoin.mtail
        mtail_version: v3.0.0-rc35

Add mtail files like [examples](https://github.com/google/mtail/tree/master/examples) in `files` directory in side of your playbook

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
