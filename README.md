correcthorse.memcached
=========

An ansible role for installing memcached.

Role Variables
--------------

| Variable                              | Default                       | Notes                                         |
| :---                                  | :---                          | :---                                          |
| memcached_port			| 11211				| 	  	       		    		|
| memcached_user			| memcached			|						|
| memcached_maxconn			| 1024				|						|
| memcached_cachesize			| 64				|						|
| memcached_options			| ''				|						|

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
