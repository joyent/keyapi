---
title: KeyAPI
markdown2extras: wiki-tables, code-friendly
apisections: tokenize, detokenize
---
<!--
    This Source Code Form is subject to the terms of the Mozilla Public
    License, v. 2.0. If a copy of the MPL was not distributed with this
    file, You can obtain one at http://mozilla.org/MPL/2.0/.
-->

<!--
    Copyright (c) 2014, Joyent, Inc.
-->

# KeyAPI

KeyAPI is a simple library to create and unpackage opaque encrypted tokens
for services that require user authentication

## Usage:

KeyAPI is created as an object with constructor argument object that must
contain at minimum ufds connection options ( as per the constructor for
sdc-clients.UFDS ) and may optionally include a bunyan logger object

# token
take a javascript object and encrypt it, returning a javascript object
containing a hash, key version, keyid and data payload

# detoken
take a keyapi generated token as a javascript object (if received from
your application as a string you must convert it to javascript) and
return the originally encrypted js object
