.. index:: Release notes


==================
Release Notes v0.7
==================

SlimerJS 0.7 has not been released yet.

It is usable, although its API is not yet 100% compatible with PhantomJS.

Improvements
------------

- Implements phantom.args and phantom.scriptName

Fixed bugs
----------

- The leading "-" of command line options were troncated and loose their values
- Modules loader doesn't freeze any more module objects, so they can be extensible


Missing APIS
------------

Here are the PhantomJS APIs that are missing in SlimerJS 0.7. Of course, their
implementation is planed in future releases.

- most of options for the command line are not supported
- no API to manage HTTP cookies, although cookies are supported (they are stored
  automatically)
- no API to manage HTTP headers
- no support of the ``window.callPhantom()`` function in web pages
- no support of the navigation locking
- no support of the ``webpage.offlineStorage*`` properties, although offlineStorage
  is supported natively and usable by a web page
- no API to manage child windows
- no support of settings on the webpage and phantomjs object
- ``webpage.open()`` only supports an url and a callback as parameter
- no support of file uploading in web page (``webpage.uploadFile()``, ``webpage.onFilePicker``..)

You can read the `compatibility table <https://github.com/laurentj/slimerjs/blob/master/API_COMPAT.md>`_ to know details.


Known issues
------------

- CommonJS modules: you cannot alter objects (they are `freezed <https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Object/freeze>`_ )
  returned by the ``require()`` function. This is a "feature" of the CommonJS
  modules system of the Mozilla Addons SDK (used by SlimerJS).


