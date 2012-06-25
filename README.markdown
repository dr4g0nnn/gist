Gist: The Script
================

Works great with Gist: The Website.

Installation
------------

[homebrew](http://mxcl.github.com/homebrew/):

```bash
$ brew install gist
$ gist -h
```

RubyGems:

```bash
$ gem install gist
$ gist -h
```

Old school:

```bash
$ curl -s https://raw.github.com/defunkt/gist/master/gist > gist &&
$ chmod 755 gist &&
$ mv gist /usr/local/bin/gist
```

Ubuntu:

```bash
$ sudo apt-get install ruby
$ sudo apt-get install rubygems
$ sudo apt-get install libopenssl-ruby
$ sudo gem install gist
$ sudo cp /var/lib/gems/1.8/bin/gist /usr/local/bin/
$ gist -h
```

Use
---

```bash
$ gist < file.txt
$ echo secret | gist --private # or -p
$ echo "puts :hi" | gist -t rb
$ gist script.py
$ gist script.js notes.txt
$ pbpaste | gist -p # Copy from clipboard - OSX Only
$ gist -
the quick brown fox jumps over the lazy dog
^D
```

Authentication
--------------
Authentication is a simple process:
```bash
$ gist --login
Obtaining OAuth2 access_token from github.
Github username: dr4g0nnn
Github password: 
Success! https://github.com/settings/applications
$
```

This fetches an OAuth token from GitHub and stores it in '~/.gist';
your username and password are not stored and are only ever
transmitted over HTTPS.

Defaults
--------

You can set a few options in your git config (using git-config(1)) to
control the default behavior of gist(1).

* gist.private - boolean (yes or no) - Determines whether to make a gist
  private by default

* gist.extension - string - Default extension for gists you create.

* gist.browse - boolean (yes or no) - Whether to open the gist in your
  browser after creation. Default: yes

Proxies
-------

Set the HTTP_PROXY env variable to use a proxy.

```bash
$ HTTP_PROXY=host:port gist file.rb
```

Manual
------

Visit <http://defunkt.github.com/gist/> or use:

```bash
$ gist -m
```

Bugs
----

<https://github.com/defunkt/gist/issues>
