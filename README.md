# linux_practice-idm-ldap-lab
a local FreeIPA (IdM) lab you can spin up on your laptop with VirtualBox/Vagrant, join a couple of Linux clients to the domain, and then automate user/group management with Python. This maps directly to: LDAP/Kerberos/SSSD, token-based auth, config mgmt, and RHEL admin
<!-- -- testing if I set up my keys correctly awhile ago -- -->
Intended file structure:
idm-lab-freeipa/
├─ README.md
├─ vagrant/
│  ├─ Vagrantfile
│  ├─ bootstrap_ipa.sh
│  ├─ bootstrap_client.sh
│  └─ hosts.yaml                 # (generated inventory for convenience)
├─ ansible/                      # optional (roles if you prefer Ansible)
│  └─ ...                        # (for future automations)
├─ python/
│  ├─ requirements.txt
│  ├─ ipa_cli.py                 # user/group/sudo/HBAC admin CLI
│  ├─ ipa_api.py                 # tiny wrapper over FreeIPA JSON-RPC
│  └─ examples/
│     └─ seed_users.yaml
├─ tests/
│  └─ test_ipa_cli.py
└─ docs/
   ├─ architecture.md
   └─ troubleshooting.md
