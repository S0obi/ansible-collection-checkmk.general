# Checkmk Ansible Collection

Checkmk already provides the needed APIs to automate and 
configure your monitoring. With this project we want to create
and share modules and roles for Ansible to both simplify your first steps
with automating Checkmk and keep your daily operations smooth and efficient.

---

## Here be dragons!

This repository is provided as is and we cannot guarantee stability at this point.
Additionally, there is no commercial support whatsoever!
This is an open source endeavour, which we want to share and progress with the community.

[![Ansible Sanity Tests](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ansible-sanity-tests.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ansible-sanity-tests.yaml)
[![Ansible Integration Tests for all Modules](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-tests-full.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-tests-full.yaml)
<!-- [![Ansible Unit Tests](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ansible-unit-tests.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ansible-unit-tests.yaml) -->

## Dependencies
 - [ansible.posix](https://github.com/ansible-collections/ansible.posix)
 - [community.general](https://github.com/ansible-collections/community.general)

Although the Ansible project notes, that collections should have no or very little dependencies, we want to make sure the  collection works for you out-of-the-box. Currently we only depend on very basic collections, which are most likely already installed in your environment. For version constraints, see [galaxy.yml](galaxy.yml).

## Getting help

For documentation on the [included modules](#modules), run the following
command substituting the `$MODULE_NAME`:

    ansible-doc checkmk.general.$MODULE_NAME

For any form of support queries or requests refer to [SUPPORT.md](SUPPORT.md).

## Repository Structure

For information about the structure and organization of this repository
have a look at [STRUCTURE.md](docs/STRUCTURE.md).

You can find playbooks, demonstrating several aspects of this collection in the folder [playbooks/demo/](playbooks/demo/).

## Included content

<!--start collection content-->
<!-- ### Inventory plugins
Name | Description
--- | ---
[checkmk.general.ec2](https://github.com/Checkmk/ansible-collection-checkmk.general/tree/main/docs/checkmk.general.ec2_inventory.rst)|EC2 inventory source

### Lookup plugins
Name | Description
--- | ---
[checkmk.general.account_attribute](https://github.com/Checkmk/ansible-collection-checkmk.general/tree/main/docs/checkmk.general.account_attribute_lookup.rst)|Look up Checkmk account attributes.
-->

### Modules
Name | Description | Tests
--- | --- | ---
[checkmk.general.activation](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/activation.py)|Activate changes.|[![Integration Tests for Activation Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-activation.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-activation.yaml)
[checkmk.general.bakery](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/bakery.py)|Bake and sign agents.|[![Integration Tests for Bakery Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-bakery.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-bakery.yaml)
[checkmk.general.contact_group](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/contact_group.py)|Manage contact groups.|[![Integration Tests for Contact Group Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-contact_group.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-contact_group.yaml)
[checkmk.general.discovery](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/discovery.py)|Discover services on hosts.|[![Integration Tests for Discovery Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-discovery.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-discovery.yaml)
[checkmk.general.downtime](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/downtime.py)|Manage downtimes.|[![Integration Tests for Downtime Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-downtime.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-downtime.yaml)
[checkmk.general.folder](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/folder.py)|Manage folders.|[![Integration Tests for Folder Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-folder.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-folder.yaml)
[checkmk.general.host_group](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/host_group.py)|Manage host groups.|[![Integration Tests for Host Group Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-host_group.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-host_group.yaml)
[checkmk.general.host](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/host.py)|Manage hosts.|[![Integration Tests for Host Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-host.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-host.yaml)
[checkmk.general.rule](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/rule.py)|Manage rules.|[![Integration Tests for Rule Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-rule.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-rule.yaml)
[checkmk.general.service_group](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/service_group.py)|Manage service groups.|[![Integration Tests for Service Group Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-service_group.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-service_group.yaml)
[checkmk.general.tag_group](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/tag_group.py)|Manage tag groups.|[![Integration Tests for Tag Group Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-tag_group.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-tag_group.yaml)
[checkmk.general.user](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/plugins/modules/user.py)|Manage users.|[![Integration Tests for User Module](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-user.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/ans-int-test-user.yaml)
### Roles
Name | Description | Tests
--- | --- | ---
[checkmk.general.agent](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/roles/agent/README.md)|Installs Checkmk agents.| [![Molecule Tests for Agent Role](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/molecule-role-agent.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/molecule-role-agent.yaml)
[checkmk.general.server](https://github.com/Checkmk/ansible-collection-checkmk.general/blob/main/roles/server/README.md)|Installs Checkmk servers.|[![Molecule Tests for Server Role](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/molecule-role-server.yaml/badge.svg)](https://github.com/Checkmk/ansible-collection-checkmk.general/actions/workflows/molecule-role-server.yaml)
<!--end collection content-->

## Additional content
We love to see the community build things on top of this collection.  
Check out [COMMUNITY.md](COMMUNITY.md) for a listing of interesting projects that build upon this collection in some way.

## Installing this collection
Please refer to the [official Ansible documentation](https://docs.ansible.com/ansible/latest/collections_guide/collections_installing.html) on how to install this collection. The most basic way is this:

    ansible-galaxy collection install checkmk.general

## Using this collection

You can either call modules by their Fully Qualified Collection Namespace (FQCN),
such as `checkmk.general.activation`, or you can call modules by their short name
if you list the `checkmk.general` collection in the playbook's [`collections`](https://docs.ansible.com/ansible/devel/user_guide/collections_using.html#using-collections-in-playbooks) keyword:

```yaml
---
- hosts: all

  collections:
    - checkmk.general

  tasks:
    - name: "Run activation."
      activation:
        server_url: "http://localhost/"
        site: "my_site"
        automation_user: "automation"
        automation_secret: "$SECRET"
        force_foreign_changes: 'true'
        sites:
          - "my_site"
```
### More information about Checkmk

* [Checkmk Website](https://checkmk.com)
* [Checkmk Documentation](https://docs.checkmk.com/)
* [Checkmk Community](https://forum.checkmk.com/)

## Getting Involved

See [CONTRIBUTING](CONTRIBUTING.md).

## Release notes
<!--Add a link to a changelog.rst file or an external docsite to cover this information. -->
See [CHANGELOG.rst](CHANGELOG.rst).

## Roadmap
<!-- Optional. Include the Roadmap for this collection, and the proposed release/versioning strategy so users can anticipate the upgrade/update cycle. -->
This is merely a collection of possible additions to the role.
Please do **not** consider a concrete planning document!

- Modules
  - Monitoring
    - Acknowledgement
  - Setup
    - Agents
    - BI
    - Distributed Monitoring
    - Notification Rules
    - Time Periods
- Lookup Plugins
  - Version
  - Rules

## More information about Ansible

- [Ansible Collection overview](https://github.com/ansible-collections/overview)
- [Ansible User guide](https://docs.ansible.com/ansible/latest/user_guide/index.html)
- [Ansible Developer guide](https://docs.ansible.com/ansible/latest/dev_guide/index.html)
- [Ansible Community code of conduct](https://docs.ansible.com/ansible/latest/community/code_of_conduct.html)

## Licensing
See [LICENSE](LICENSE).
