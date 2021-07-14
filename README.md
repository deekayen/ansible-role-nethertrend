Nether Trend
============
![CI](https://github.com/deekayen/ansible-role-nethertrend/workflows/CI/badge.svg?branch=main) [![Project Status: Concept – Minimal or no implementation has been done yet, or the repository is only intended to be a limited example, demo, or proof-of-concept.](https://www.repostatus.org/badges/latest/concept.svg)](https://www.repostatus.org/#concept) ![BSD 3-Clause license](https://img.shields.io/badge/license-BSD%203--Clause-blue) ![Windows platform](https://img.shields.io/badge/platform-windows-lightgrey)

Uninstall Trend Micro Deep Security Agent advanced host-based protection, registry keys, and remove files using Ansible.

https://success.trendmicro.com/solution/1096150-manually-uninstalling-deep-security-agent-relay-and-notifier-from-windows

Role Variables
--------------

    # Reboot after uninstall.
    allow_reboot: false

    # Override to disable self-protection when the Management dashboard is unavailable.
    dsa_control_password: ""


Example Playbook
----------------

    - name: Uninstall Trend Micro Deep Security Agent.
      hosts: platform_windows

      vars:
        allow_reboot: true

      roles:
         - deekayen.nethertrend


Requirements
------------

The control machine should have `pywinrm` and one of `requests-ntlm`, `requests-kerberos`, and/or `requests-credssp` installed by `pip`.

Dependencies
------------

None.

License
-------

BSD
