.. spelling::

  geotagging

Welcome to Open Data Kit Tool Suite X's (ODK-X) documentation!
==============================================================

.. _odk-2-introduction:

The :dfn:`ODK-X Tool Suite` is a new set of ODK tools that will co-exist with the existing ODK Tool Suite. It targets advanced users who find themselves limited by the ODK data collection workflows. It provides:

- **Fully customizable layout of prompts on the Android device**. The ODK-X tools use HTML, JavaScript, and CSS to specify the layout of nearly all the screens viewed by the data collectors. This enables individuals and organizations with basic web development skills to modify and customize the appearance of their surveys and workflow. At the same time, we retain the easy-to-use spreadsheet-based definition of the survey questions (however, this XLSX Converter mechanism is not cross-compatible with XLSForm).
- **More flexible, user-directed, navigation of a survey**. The ODK-X tools do not impose a strict sequential advancement through a form like ODK Collect. Form designers can allow users to traverse a form in any order, yet impose validation of collected data prior to traversing into subsequent steps in a workflow.
- **Improved treatment of repeat-groups**. In the ODK-X tools, we have eliminated the concept of a repeat-group. In its place, we provide prompts that enable you to open and edit other surveys with links back to the originating survey (if desired). These prompts can describe a sub-form (nested) relationship among the surveys (for example: household and household-member) or they can represent arbitrary relational linkages across your data (for example: tea-houses and tea-types).
- **Bi-directional synchronization of data across devices**. The ODK-X tools support the collaborative sharing of survey data across devices, as well as the updating and submission of changes to previously collected data (for example: follow-up surveys) via a bi-directional synchronization protocol. This contrasts with the unidirectional device-to-server submission pathway of ODK Collect / ODK Aggregate / ODK Briefcase.
- **Data curation and visualization on the device**. ODK Tables gives organizations the ability to investigate and visualize entire datasets directly on the Android devices through graphical and non-graphical displays and through filtered views.
- **Row-level access filters**. The visibility of the data and the ability to edit and/or delete data can be restricted for different users and groups.

.. note::

  The ODK-X tool suite is targeted at advanced users who are unable to complete their workflows with the ODK tools. If you find that the ODK tools meet your needs then there is no reason to switch.

ODK-X is a platform that will run your :dfn:`data management applications`. With ODK you create survey forms that ODK Collect renders and are used to collect data and submit it to the ODK Aggregate server. In ODK-X, you create `data management applications` that consist of survey forms (similar to those used in Collect) as well as Javascript based web apps that allow you to render a fully customized user interface and implement business logic in order to collect, manage, and visualize data all on the Android device.

.. _odk-2-intro-learn-more:

Learn More
--------------
View a brief feature comparison in the guide for :doc:`select-tool-suite`.

.. _odk-2-perspectives:

Perspectives
---------------

The ODK-X documentation is organized into different perspectives to allow readers to focus on the sections most relevant to their needs.

These perspectives are:

  - :dfn:`User`: A user of the data management application running on the Android tools. This person collects and interacts with data on the Android device. Examples include field workers, clinic staff, and census workers.
  - :dfn:`Deployment Architect`: An author of a data management application or a consumer of collected data. This person might create forms and edit Javascript on their computer to deploy to the Android device. Or they might download data from the server and use Excel to perform analysis. Examples include technical staff and data analytics staff.
  - :dfn:`System Administrator`: The person or team that manages the web servers in the cloud. This person might want to ensure high availability of the server or coordinate across multiple regions.
  - :dfn:`Platform Developer`: A programmer that intends to modify the source code of the ODK-X tools themselves. This person might want to add a new view type or a fix a bug.

.. note::

  We expect most organizations to have users, deployment architects, and system administrators (though these roles might overlap). But most organizations can safely ignore the platform developer sections.

.. _odk-2-intro-list-of-tools:

List of Tools
---------------
The ODK-X Tool Suite consists of:

  - :doc:`survey-intro` - a data collection application based upon HTML, CSS, JavaScript.
  - :doc:`tables-intro` - a data curation and visualization application running on your mobile device.
  - :doc:`services-intro` - an application for handling database access, file access, and data synchronization services between all the ODK-X applications. It allows you to synchronize data collected by the ODK-X Android tools with a cloud endpoint.
  - :doc:`app-designer-intro` - a design environment for creating, customizing, and previewing your forms, data curation, and visualization applications. This is a good place to start the process of learning how to use ODK tools.
  - :doc:`cloud-endpoints-intro` - a cloud server to host data and application files, and to support bi-directional data synchronization across disconnected mobile devices.
  - :doc:`suitcase-intro` - a desktop tool for synchronizing data with a cloud endpoint.

  These tools are used in application design, which consists of:

  - designing the forms used in data collection (by ODK Survey)
  - designing the HTML landing pages and screens used for navigating, curating, and visualizing that data on your Android device (within ODK Tables).
  - customizing the look-and-feel of both of these via customized images, logos, and CSS rules.
  - designing mark-sense forms for paper-based data entry (by ODK Scan)
  - synchronizing database access, file access, and data synchronization services between all the ODK 2 applications (using ODK Services). This happens behind the scenes, but you will need to install ODK Services as a prerequisite to using the other ODK 2 tools.

.. tip::
  The tools operate independently -- you are not required to use all the tools, or even install them on your device. If you are only interested in data collection, you may only want ODK Survey. Or if you are only interested in data dissemination and visualization, you might only want ODK Tables.

  Simply select the combination or individual tool that fits your needs. However, all of these tools require ODK Services to access the database, sync to a server, and vend HTML files.

.. _odk-2-intro-trying-it-out:

Trying It Out
----------------

The first step to get a feel for the ODK-X tools and how they fit together is to do the :doc:`getting-started-2-user`. This guide walks you through the process of using a basic geotagging application and submitting data to the server. After this is completed, the guide provides a list of :ref:`user-odk2-next` for the user.

Deployment Architects should follow this up with the :doc:`getting-started-2-architect` to get an introduction into revising and editing their own forms. That guide walks you through modifying the *Geotagger* demo application to add a new field to it. Similar to the user guide, this guide provides a list of :ref:`architect-odk2-next` for the Deployment Architect.

System Administrators should learn about :doc:`cloud-endpoints-intro`.

Platform Developers should already be familiar with everything from the User and Deployment Architect sections, and can learn more in the :doc:`advanced-topics-developer` documentation.


.. toctree::
  :maxdepth: 1
  :hidden:

  select-tool-suite
  getting-started-2-user
  getting-started-2-architect

.. toctree::
  :maxdepth: 2
  :hidden:
  :caption: Mobile Tools

  survey-intro
  tables-intro
  services-intro
  scan-intro

.. toctree::
  :maxdepth: 2
  :hidden:
  :caption: Desktop and Server Tools

  app-designer-intro
  cloud-endpoints-intro
  suitcase-intro

.. toctree::
  :maxdepth: 2
  :hidden:
  :caption: Application Building

  build-app
  xlsx-converter-intro
  tables-web-pages
  injected-interfaces
  scan-form-designer-intro
  reference-apps

.. toctree::
  :maxdepth: 2
  :hidden:
  :caption: Advanced Topics

  advanced-topics-architect
  advanced-topics-developer

.. toctree::
  :maxdepth: 2
  :hidden:
  :caption: Contributing

  contributing

.. toctree::
  :maxdepth: 2
  :hidden:
  :caption: Reference
