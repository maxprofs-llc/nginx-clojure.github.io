Core Features
=================

The latest release is v0.2.5, more detail changes about it can be found from [Release History](downloads.html).

1. Compatible with [Ring](https://github.com/ring-clojure/ring/blob/master/SPEC) and obviously supports those Ring based frameworks, such as Compojure etc.
1. Use Clojure / Java / Groovy to write simple handlers for http services.
1. Use Clojure / Java / Groovy to write a simple nginx rewrite handler to set var or return errors before proxy pass or content ring handler
1. Non-blocking coroutine based socket which is Compatible with Java Socket API and works well with largely existing java library such as apache http client, mysql jdbc drivers. 
With this feature  one java main thread can handle thousands of connections.
1. Handle multiple sockets parallel in sub coroutines, e.g. we can invoke two remote services at the same time.
1. Asynchronous callback API of socket/Channel(**_NEW_**) for some advanced usage
1. **_NEW_**: Long Polling & Server Sent Events
1. **_NEW_**: More easier to archive  Sub/Pub services with broadcast events API
1. Run initialization clojure code when nginx worker starting
1. Support user defined http request method
1. Compatible with the Nginx lastest stable version 1.6.0. (Nginx 1.4.x is also ok, older version is not tested and maybe works.)
1. One of  benifits of [Nginx](http://nginx.org/) is worker processes are automatically restarted by a master process if they crash
1. Utilizes lazy headers and direct memory operation between [Nginx](http://nginx.org/) and JVM to fast handle dynamic contents from Clojure or Java code.
1. Utilizes [Nginx](http://nginx.org/) zero copy file sending mechanism to fast handle static contents controlled by Clojure or Java code.
1. Supports Linux x64, Linux x86 32bit, Win32, Win64(**_NEW_**) and Mac OS X. 


License
=================
Copyright © 2013-2014 Zhang, Yuexiang (xfeep) and released under the BSD 3-Clause license.

This program uses:
* Re-rooted ASM bytecode engineering library which is distributed under the BSD 3-Clause license
* Modified Continuations Library Written by Matthias Mann  is distributed under the BSD 3-Clause license