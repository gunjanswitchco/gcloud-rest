Contributing to ``gcloud-rest``
===============================

Thanks for contributing to ``gcloud-rest``! We appreciate contributions of any
size and hope to make it easy for you to dive in. Here's the thousand-foot
overview of how we've set this project up.

Testing
-------

Tests are run with `nox`_. See ``noxfile.py`` for the scaffolding and the
``tests/unit`` and ``tests/integration`` folders for the actual test code.

You can get nox with ``pip install nox`` and run the project's tests with
``nox``.

Local Development
~~~~~~~~~~~~~~~~~

We recommend using ``nox``, as described above, but this library supports using
more standard workflows as well. For more convenient local development, or if
you don't want to use ``nox``, you can run the tests using pytest:

- create and activate a virtual environment: ``python -m venv venv && source venv/bin/activate``
- install test dependencies: ``pip install pytest``
- install library from local path: ``pip install -e .``

Then, you can run any tests manually with:

.. code-block:: console

    python -m pytest tests/unit/<your favourite test>

Submitting Changes
------------------

Please send us a `Pull Request`_ with a clear list of what you've done. When
you submit a PR, we'd appreciate test coverage of your changes (and feel free
to test other things; we could always use more and better tests!).

Please make sure all tests pass and your commits are atomic (one feature per
commit).

Always write a clear message for your changes. We think the
`conventional changelog`_ message format is pretty cool and try to stick to it
as best we can (we even generate release notes from it automatically!).

Roughly speaking, we'd appreciate if your commits looked like this:

.. code-block:: console

    feat(taskqueue): implemented task queue manager

    Created gcloud.rest.taskqueue.TaskManager for an abstraction layer around
    renewing leases on pull-queue tasks. Handles auto-renewal.

The first line is the most specific in this format; it should have the format
``type(project): message``, where:

- ``type`` is one of ``feat``, ``fix``, ``docs``, ``refactor``, ``style``, ``perf``, ``test``, or ``chore``
- ``project`` is ``auth``, ``bigquery``, ``datastore``, etc.
- ``message`` is a concise description of the patch and brings the line to no more than 72 characters

Coding Conventions
------------------

We use `pre-commit`_ to manage our coding conventions and linting. You can
install it with ``pip install pre-commit`` and set it to run pre-commit hooks
for ``gcloud-rest`` by running ``pre-commit install``. The same linters get run
in CI against all changesets.

You can also run ``pre-commit`` in an ad-hoc fashion by calling
``pre-commit run --all-files``.

Other than the above enforced standards, we like code that is easy-to-read for
any new or returning contributors with relevant comments where appropriate.

Releases
--------

If you are a maintainer looking to release a new version, see our
`Release documentation`_.

.. _conventional changelog: https://github.com/conventional-changelog/conventional-changelog
.. _nox: https://nox.readthedocs.io/en/latest/
.. _pre-commit: http://pre-commit.com/
.. _Pull Request: https://github.com/talkiq/gcloud-rest/pull/new/master
.. _Release documentation: https://github.com/talkiq/gcloud-rest/blob/master/.github/RELEASE.rst

Thanks for your contribution!

With love,
TalkIQ
