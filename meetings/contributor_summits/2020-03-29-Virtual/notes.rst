********
Overview
********


.. contents::
   :local:

Main links
==========

* `Videos <https://www.youtube.com/playlist?list=PL0FmYCf7ocraJzcnE3-VwVozQ0Zt7vm7z>`_
* Contributors Summit `summary <https://meetbot.fedoraproject.org/ansible-community/2020-03-29/ansible_contributor_summit_2020.2020-03-29-10.50.html>`_, `full log <https://meetbot.fedoraproject.org/ansible-community/2020-03-29/ansible_contributor_summit_2020.2020-03-29-10.50.log.html>`_
* Hackathon `summary <FIXME>`_,  `full log <FIXME>`_


Contributors Summit
===================

Welcome and Introductions
-------------------------

* This was the 8th Ansible Contributors Summit, and the first 100% virtual one
* Everybody that attended got the chance to introduce themselves, their interest in Ansible and what they were hoping to get from the day



Overview of Ansible Collections
-------------------------------

The majority of the day was spent talking about Ansible Collections. To help give context on these discussions some time was spent given to set the scene.

* `Where we want to get to <https://github.com/ansible-collections/overview/blob/master/README.rst#where-we-ve-come-from-and-where-we-are-going>`_
* `Collections user guide <https://docs.ansible.com/ansible/latest/user_guide/collections_using.html>`_
* `Collections developer guide <https://docs.ansible.com/ansible/latest/dev_guide/developing_collections.html>`_
* `Collections overview <https://github.com/ansible-collections/overview/blob/master/README.rst#where-we-ve-come-from-and-where-we-are-going>`_
* `Collections development and contributor status <https://github.com/ansible-collections/overview/blob/master/status.rst>`_
* Ansible (prior to 2019) was a single repo, and single deliverable
* Collections allow developers to move at their own speed, but users just want a simple way to consume content without worrying about collection release cycles
* With collections, there is no longer a single global namespace for modules, now each collection has its own namespace


Collection
  A packaging format for bundling and distributing Ansible content: plugins, roles, modules. Can be released independent of other collections or ``ansible-base`` so features can be made available sooner to users. Installed via ``ansible-galaxy collection install <namespace.collection>``.

Ansible Base
  The codebase that will be contained in github.com/ansible/ansible for the Ansible 2.10 release. Contains a minimal amount of modules and plugins, allows other collections to be installed. Similar to Ansible 2.9 though without any content that has since moved into a collection. A work in progress can be found in `ansible-base <https://github.com/ansible-collection-migration/ansible-base/>`_ repository.


Ansible Galaxy
  An online hub for finding and sharing Ansible community content.  Also, the command-line utility that lets users  install individual Ansible Collections. `galaxy.ansible.com <https://galaxy.ansible.com/>`_.

Fully Qualified Collection Name (FQCN)
  The full definition of a module, plugin, or role hosted within a collection, in the form ``namespace.collection.content_name``. Allows a Playbook to refer to a specific module or plugin from a specific source in an unambiguous manner, for example, ``community.grafana.grafana_dashboard``. The FQCN is required when you want to specify the exact source of a module and multiple modules with the same name are available. Can always be identified in a playbook; ideally not necessary in most playbooks, but in cases in which users have multiple collections installed with similar content, the FQCN will always be the explicit and authoritative indicator of which collection to use for content. Example: ``cisco.ios.ios_config`` would be the FQCN, and the playbook would generally call "ios_config" when this is required.

Namespace
  The first part of a Fully Qualified Collection Name, the namespace usually reflects a functional content category. Example: in ``cisco.ios.ios_config``, “Cisco” is the Namespace. Namespaces are reserved and distributed by Red Hat at Red Hat’s discretion. Many, but not all, namespaces will correspond with vendor names.

Collection name
  In the second part of a Fully Qualified Collection Name, the collection name further divides the functional characteristics of the collection content and denotes ownership.  For example, the cisco namespace might contain  ``cisco.ios``, ``cisco.ios_community``, and ``cisco.ios_prc``, containing content for managing ios network devices maintained by Cisco.

The community.general collection
  A special collection managed by the Ansible Community Team containing all the modules and plugins which shipped in Ansible 2.9 that don't have their own dedicated Collection. A work in progress can be found in `community.general <https://github.com/ansible-collection-migration/community.general/>`_ repository. At least initially there are no Long Term Support (LTS) plans, though we will see how the need for that grows over time.

Repository
  The location of the source code included in a collection. Contributors make suggestions, fix bugs, and add features through the repository. Collection owners can host repositories on GitHub, Gerrit, or any other source code repository platform they choose.

See also the `full list of Collection Terminology <https://github.com/ansible-collections/overview/blob/master/README.rst#terminology>`_

Molecule
--------

Sorin Sbarnea (IRC: zbr, GitHub: ssbarnea) is the maintainer of the `Molecule <https://molecule.readthedocs.io/en/latest/>`_ project, and does a short presentation on Molecule.

* Molecule project is designed to aid in the development and testing of Ansible roles. Molecule provides support for testing with multiple instances, operating systems and distributions, virtualization providers, test frameworks and testing scenarios
* `Molecule documentation <https://molecule.readthedocs.io/en/latest/`>_
* `Slides <https://sbarnea.com/slides/molecule/#/>`_
* Molecule has many drivers they can be found at `<https://github.com/ansible-community?q=molecule`>_

Call to Action:
* If you are interested in Molecule feel free to join ``#ansible-molecule`` on IRC
* 


Community Data
--------------

ansible-lint
------------

Collections: User Experience
-----------------------------

Collections: Development and contribution process
--------------------------------------------------

Collections: Development Status
-------------------------------


Routing and redirection support in ansible-base 2.10
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

https://github.com/ansible/ansible/pull/67684

Collections: Documentation
--------------------------

The new ansible package (ACD) build process)
--------------------------------------------

Cloud Collections
------------------

Community process for Collections
---------------------------------



Hackathon
=========
