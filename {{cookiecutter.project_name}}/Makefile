DC=docker-compose


.PHONY: create-network
create-network:
	docker network create {{cookiecutter.project_name}}-network
	
.PHONY: up-storages
up-storages:
	${DC} -f docker-compose/storages.yml up -d

.PHONY: setup-dev
setup-dev:
	./manage.py runserver 0.0.0.0:8000

.PHONY: testing
testing:
	{% if cookiecutter.testing == "pytest" -%}
	pytest
	{% elif cookiecutter.testing == "unittest" -%}
	./manage.py test
	{% endif %}