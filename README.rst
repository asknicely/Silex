Silex, a simple Web Framework
=============================

This is AskNicely's fork of silex/silex, which was abandoned in June
2018. Read more on `Symfony's blog <https://symfony.com/blog/the-end-of-silex>`_.

Silex is a PHP micro-framework to develop websites based on `Symfony
components`_:

As part of forking, we also took on our own versioning of silex to match the
Symfony components Silex will support. v4.x for Symfony 4 components, v5.x for
Symfony 5 components etc. The last version of silex/silex was 2.2.4 and
supported Symfony 3 and PHP 7.4.

Version 4+ of this fork also support PHP 8

.. code-block:: php

    <?php

    require_once __DIR__.'/../vendor/autoload.php';

    $app = new Silex\Application();

    $app->get('/hello/{name}', function ($name) use ($app) {
      return 'Hello '.$app->escape($name);
    });

    $app->run();

Silex works with PHP 7.1.3 or later.

Installation
------------

The recommended way to install Silex is through `Composer`_:

.. code-block:: bash

    composer require silex/silex "^4.0"

Alternatively, you can download the `silex.zip`_ file and extract it.

More Information
----------------

Read the `documentation`_ for more information and `changelog
<doc/changelog.rst>`_ for upgrading information.

Tests
-----

To run the test suite, you need `Composer`_ and `PHPUnit`_:

.. code-block:: bash

    composer install
    phpunit

Support
-------

If you have a configuration problem use the `silex tag`_ on StackOverflow to ask a question.

If you think there is an actual problem in Silex, please `open an issue`_ if there isn't one already created.

License
-------

Silex is licensed under the MIT license.

.. _Symfony components: https://symfony.com
.. _Composer:           https://getcomposer.org
.. _PHPUnit:            https://phpunit.de
.. _silex.zip:          https://silex.symfony.com/download
.. _documentation:      https://silex.symfony.com/documentation
.. _silex tag:          https://stackoverflow.com/questions/tagged/silex
.. _open an issue:      https://github.com/silexphp/Silex/issues/new
