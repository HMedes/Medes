Medes
=====

Medes is a distributed actor polyglot framework which acts as a toolkit for writing application services with any language such as Erlang, Java, C, and etc.

Architecture
-----

```
        Node#1                                Node#2
+-------------------+                  +-------------------+
|                   |  remote message  |                   |
|  +--> actor#1.1 <--------------------------+ actor#2.1   |
|  |                |                  |                   |
|  | local message  |   +----------+   |                   |
|  |                |   |          |   |                   |
|  +--> actor#1.2   |   | nodetool |   |                   |
|                   |   |          |   |                   |
+-------------------+   +----------+   +-------------------+

+----------------------------------------------------------+
|                                                          |
|               Distributed Process Registry               |
|                                                          |
+----------------------------------------------------------+

```

Node
-----
- name
- config
- language
- visibility

Nodetool
-----
- code boilerplate
- bootstrap
- monitor
- control
- config

Actor
-----
- node
- name
- config
- visibility
- handler

Handler Callbacks
-----
- init
- handle call
- handle cast
- handle info
- terminate

Languages
-----
- [Erlang Node](https://github.com/medes-project/medes-erlang)
- [C Node](https://github.com/medes-project/medes-c)
- [Java Node](https://github.com/medes-project/medes-java)
