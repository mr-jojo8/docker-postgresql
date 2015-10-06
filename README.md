Docker-postgresql
=================

Usage
-----

	docker build -t duruu/postgresql .

	docker run -d -p 5432:5432 duruu/postgresql

	docker logs <CONTAINER_ID>
	
Setting a specific password for the admin account
-------------------------------------------------

If you want to use a preset password instead of a random generated one, you can
set the environment variable `POSTGRES_PASS` to your specific password when running the container:

	docker run -d -p 5432:5432 -e POSTGRES_PASS="mypass" --name postgresql duruu/postgresql 