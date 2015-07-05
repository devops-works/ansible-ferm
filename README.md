# Ansible ferm role

This role is a stripped down version of
[debops.ferm role](https://github.com/debops/ansible-ferm).

[ferm](http://ferm.foo-projects.org/) is a wrapper around `iptables` and
`ip6tables` commands which lets you manage host firewall in an easy and
Ansible-friendly way. This role can be used to setup firewall rules
directly from inventory, or it can be used as a dependency by other roles
to setup firewall rules for other services.

### Installation

This role requires at least Ansible `v1.7.0`. To install it, run:

    ansible-galaxy install leucos.ferm

### Documentation

More information about `debops.ferm` can be found in the
[official debops.ferm documentation](http://docs.debops.org/en/latest/ansible/roles/debops.ferm.html).

### Authors and license

`ferm` role was written by:
- Maciej Delmanowski | [e-mail](mailto:drybjed@gmail.com) | [Twitter](https://twitter.com/drybjed) | [GitHub](https://github.com/drybjed)

and adapted by
- Michel Blanc | [Twitter](https://twitter.com/b9m) | [GitHub](https://github.com/leucos)

License: [GPLv3](https://tldrlegal.com/license/gnu-general-public-license-v3-%28gpl-3%29)


