# What is this repository and who is it for?
The purpose of this repository is to provide a simple and streamlined local development experience.
It provides a MariaDB database and a phpMyAdmin web interface to manage the database.
This should be all you need to set up a local development environment, but you are free to extend it as needed.

# Setting it up
1. Clone this repository to your computer.
2. Enter your desired database password in the `.env` file. By default it is `foobar`.
3. Run `docker network create localdev` to create a new local Docker network on your machine.
4. Enjoy the simplicity of using your new local database.

# Running the containers
To start the containers, navigate to the path where you cloned the files and then simply run `docker-compose up -d` to start them. To stop them, run `docker-compose down`. The files of the containers will be saved relative to the path where your `docker-compose.yml` file is located.

# Accessing the database
Since we have created an `external` network for the services that is available system-wide, you can use the hostname of the container (`mariadb` by default) to connect to the database. Using `localhost` or `127.0.0.1` should work just as well.

# Accessing phpMyAdmin
Accessing the database via phpMyAdmin is as easy as visiting <a href="http://127.0.0.1:8080">`http://127.0.0.1:8080`</a> in your browser.