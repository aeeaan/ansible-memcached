correcthorse.memcached
=========

An ansible role for installing memcached.

Role Variables
--------------

| Variable                              | Default                       | Notes                                         |
| :---                                  | :---                          | :---                                          |
| memcached_port			| 11211				| 	  	       		    		|
| memcached_open_port			| false				|						|
| memcached_user			| memcached			|						|
| memcached_maxconn			| 1024				|						|
| memcached_cachesize			| 64				|						|
| memcached_options			| ''				|						|
| memcached_disable_default		| false				| disable default memcache instance, useful if you want all your instances named |

    memcached_extra_instances:
      instance2:
        port: 11212 (required)
        open_port: true (optional, default false, never make assumptions about firewall rules)
        user: memcached (optional, default memcached_user)
        maxconn: 1024 (optional, default memcached_maxconn)
        cachesize: 64 (optional, default memcached_cachesize)
        memcached_options: (optional, default memcached_options)

Dependencies
------------

* correcthorse.common

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: correcthorse.memcached }

License
-------

MIT

Author Information
------------------

* [Joshua Rusch](https://correct.horse/)
