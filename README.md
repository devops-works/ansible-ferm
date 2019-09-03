***MOVED TO https://github.com/devops-works/ansible-ferm/**

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

    ansible-galaxy install https://github.com/leucos/ansible-ferm.git

### Documentation

You can use this role as a simple dependency:

    dependencies:
      - role: ansible-ferm
        name: ansible-ferm
        src: https://github.com/leucos/ansible-ferm.git
        ferm_input_group_list:
          - type: 'dport_accept'
            dport: [ '80' ]
            saddr: '{{ some_ansible_group }}'
            weight: '50'
            filename: 'gluster_accept'

If you need more control, you can skip the `ferm_input_group_list` part
and push specific templates from your role.

See [ansible-pxc](https://github.com/leucos/ansible-pxc.git) role for this.

### Issues

This role is WIP and lacks tests.

### Authors

This role is based on `ferm` role written by [Maciej Delmanowski](https://github.com/drybjed) of [DebOps](https://github.com/debops) fame.

Adapted by Michel Blanc ([Twitter](https://twitter.com/b9m) | [GitHub](https://github.com/leucos)

### Licence

License: [MIT](http://opensource.org/licenses/MIT)


