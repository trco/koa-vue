===========
Koa & Vue
===========

Koa backend & Vue frontend

Run
===

Run docker and visit http://localhost:8080::

    $ docker-compose up

How to build it from scratch?
=============================

1. Create project folder::

    $ mkdir koa-vue
    $ cd koa-vue

2. Create Koa backend app, install dependencies::

    $ koa2 back
    $ cd back
    $ npm install

3. Change default port from ``3000`` to ``8000`` in ``bin/www``.

4. Install ``koa2-cors``::

    $ npm install koa2-cors --save

5. Add ``koa2-cors`` to app.js::

    const cors = require('koa2-cors')
    app.use(cors());

6. Install ``vue client``::

    $ npm install -g @vue/cli

7. Create Vue frontend app in project folder, install dependencies::

    $ vue create front

8. Fetch data from Koa backend through "http://localhost:8000/<path>" inside .vue files.

9. Create separate ``Dockerfile`` in back and front apps and ``docker-compose.yml`` in project folder.
