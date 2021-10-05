Base Docker Compose for Odoo
############################

:code:`docker-compose.yml` is to be used as a base for all Odoo containers, where :code:`prod.yml` and :code:`stage.yml` are to be used as a supplement for specific types of environments. :code:`dev.yml` is intended to be used for local development.

Examples
========

To run it in specific project, use :code:`docker-compose` :code:`--project-directory` argument, so all relative paths are resolved from that directory instead of default, which is location of :code:`docker-compose.yml`.

Like: :code:`docker-compose --project-directory . -f ~/src/docker-compose-odoo/docker-compose.yml -f ~/src/docker-compose-odoo/dev.yml down && docker-compose --project-directory . -f ~/src/docker-compose-odoo/docker-compose.yml -f ~/src/docker-compose-odoo/dev.yml up`, which means use current working directory for relative paths resolving and take specified compose files.
