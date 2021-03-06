Contributing to Trusted Firmware-A
==================================

Getting Started
---------------

-  Make sure you have a Github account and you are logged on
   `developer.trustedfirmware.org`_.
-  Create an `issue`_ for your work if one does not already exist. This gives
   everyone visibility of whether others are working on something similar.

   -  If you intend to include Third Party IP in your contribution, please
      raise a separate `issue`_ for this and ensure that the changes that
      include Third Party IP are made on a separate topic branch.

-  Clone `arm-trusted-firmware-a`_ on your own machine as suggested on the
   `User Guide`_.
-  Create a local topic branch based on the `arm-trusted-firmware-a`_ ``master``
   branch.

Making Changes
--------------

-  Make commits of logical units. See these general `Git guidelines`_ for
   contributing to a project.
-  Follow the `Coding Guidelines`_.

   -  Use the checkpatch.pl script provided with the Linux source tree. A
      Makefile target is provided for convenience (see the "Checking source code
      style" section in the `User Guide`_).

-  Keep the commits on topic. If you need to fix another bug or make another
   enhancement, please create a separate `issue`_ and address it on a separate
   topic branch.
-  Avoid long commit series. If you do have a long series, consider whether
   some commits should be squashed together or addressed in a separate topic.
-  Make sure your commit messages are in the proper format. If a commit fixes
   an `issue`_, include a reference.
-  Where appropriate, please update the documentation.

   -  Consider whether the `User Guide`_, `Porting Guide`_, `Firmware Design`_
      or other in-source documentation needs updating.
   -  Ensure that each changed file has the correct copyright and license
      information. Files that entirely consist of contributions to this
      project should have a copyright notice and BSD-3-Clause SPDX license
      identifier of the form as shown in `license.rst`_. Files that contain
      changes to imported Third Party IP files should retain their original
      copyright and license notices. For significant contributions you may
      add your own copyright notice in following format:

      ::

          Portions copyright (c) [XXXX-]YYYY, <OWNER>. All rights reserved.

      where XXXX is the year of first contribution (if different to YYYY) and
      YYYY is the year of most recent contribution. <OWNER> is your name or
      your company name.
   -  If you are submitting new files that you intend to be the technical
      sub-maintainer for (for example, a new platform port), then also update
      the `Maintainers`_ file.
   -  For topics with multiple commits, you should make all documentation
      changes (and nothing else) in the last commit of the series. Otherwise,
      include the documentation changes within the single commit.

-  Please test your changes. As a minimum, ensure that Linux boots on the
   Foundation FVP. See `Running the software on FVP`_ for more information. For
   more extensive testing, consider running the `TF-A Tests`_ against your
   patches.

Submitting Changes
------------------

-  Ensure that each commit in the series has at least one ``Signed-off-by:``
   line, using your real name and email address. The names in the
   ``Signed-off-by:`` and ``Author:`` lines must match. If anyone else
   contributes to the commit, they must also add their own ``Signed-off-by:``
   line. By adding this line the contributor certifies the contribution is made
   under the terms of the `Developer Certificate of Origin (DCO)`_.

   More details may be found in the `Gerrit Signed-off-by Lines guidelines`_.

-  Ensure that each commit also has a unique ``Change-Id:`` line. If you have
   cloned the repository with the "`Clone with commit-msg hook`" clone method
   (as advised on the `User Guide`_), this should already be the case.

   More details may be found in the `Gerrit Change-Ids documentation`_.

-  Submit your changes for review at https://review.trustedfirmware.org
   targeting the ``integration`` branch.

   -  The changes will then undergo further review and testing by the
      `Maintainers`_. Any review comments will be made directly on your patch.
      This may require you to do some rework.

   Refer to the `Gerrit Uploading Changes documentation`_ for more details.

-  When the changes are accepted, the `Maintainers`_ will integrate them.

   -  Typically, the `Maintainers`_ will merge the changes into the
      ``integration`` branch.
   -  If the changes are not based on a sufficiently-recent commit, or if they
      cannot be automatically rebased, then the `Maintainers`_ may rebase it on
      the ``master`` branch or ask you to do so.
   -  After final integration testing, the changes will make their way into the
      ``master`` branch. If a problem is found during integration, the merge
      commit will be removed from the ``integration`` branch and the
      `Maintainers`_ will ask you to create a new patch set to resolve the
      problem.

--------------

*Copyright (c) 2013-2019, Arm Limited and Contributors. All rights reserved.*

.. _developer.trustedfirmware.org: https://developer.trustedfirmware.org
.. _issue: https://developer.trustedfirmware.org/project/board/1/
.. _arm-trusted-firmware-a: https://git.trustedfirmware.org/TF-A/trusted-firmware-a.git
.. _Git guidelines: http://git-scm.com/book/ch5-2.html
.. _Coding Guidelines: ./docs/coding-guidelines.rst
.. _User Guide: ./docs/user-guide.rst
.. _Porting Guide: ./docs/porting-guide.rst
.. _Firmware Design: ./docs/firmware-design.rst
.. _license.rst: ./license.rst
.. _Acknowledgements: ./acknowledgements.rst
.. _Maintainers: ./maintainers.rst
.. _Running the software on FVP: ./docs/user-guide.rst#user-content-running-the-software-on-fvp
.. _Developer Certificate of Origin (DCO): ./dco.txt
.. _Gerrit Uploading Changes documentation: https://review.trustedfirmware.org/Documentation/user-upload.html
.. _Gerrit Signed-off-by Lines guidelines: https://review.trustedfirmware.org/Documentation/user-signedoffby.html
.. _Gerrit Change-Ids documentation: https://review.trustedfirmware.org/Documentation/user-changeid.html
.. _TF-A Tests: https://git.trustedfirmware.org/TF-A/tf-a-tests.git/about/
