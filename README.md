# Ansible role: node_exporter

Install prometheus node exporter

## Requirements

* ansible-core >= 2.13 -- will probably work with ansible version >= 2.10, not tested
* x86_64 architecture

## Role Variables

  * `node_exporter_version` -- node exporter version
  * `node_exporter_sha_checksum` -- checksum for selected version. Can be found on https://prometheus.io/download/
  * `node_exporter_options` -- additional options for node exporter

All these variables can be found in the [defaults/main.yml](./defaults/main.yml) file.

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
         - role: dragomirr.node_exporter

## Testing

Testing is done using [molecule](https://molecule.readthedocs.io/) with [vagrant](https://www.vagrantup.com/) and [virtualbox](https://www.virtualbox.org/).

Testing dependencies:

  - [vagrant](https://www.vagrantup.com/)
  - [virtualbox](https://www.virtualbox.org/)
  - molecule python package
  - molecule-vagrant python package


## License

MIT
