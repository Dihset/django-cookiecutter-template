DC=docker-compose


.PHONY: create-network
create-network:
	docker network create {{cookiecutter.project_name}}-network
	
.PHONY: up-storages
up-storages:
	${DC} -f docker-compose/storages.yml up -d
