# Contributing

The easiest way to get started with contributing to the project is to get started with the VS Code install.

## Getting Started

1. Install [Docker](https://docs.docker.com/get-docker/) for your system
1. Fork it (<https://github.com/Open-SGF/portal-to-work-api/fork>)
1. Create your feature branch (`git checkout -b feature/fooBar`)
1. Commit your changes (`git commit -am 'Add some fooBar'`)
1. Push to the branch (`git push origin head`)
1. Create a new Pull Request

## VS Code Setup

1. Install & Open up VS Code
2. Install extension: `ext install ms-vscode-remote.remote-containers`
3. Open this workspace (by navigating to this project folder in system)

Project Setup:

4. Run `cp .env.example .env`
5. Edit the .env file, specfically these option(s):

	DB_PASSWORD

6. Open new terminal window, or new terminal in VS Code

If not using VS Code's terminal

7. Run `docker-compose build`
8. Run `docker-comose up`
9. Open a new terminal window
10. Run `docker exec -ti app bash`
11. Go to step 12

If using VS Code's Terminal & Connected to remote container

12. Run `php artisan key:generate`
13. Run `php artisan migrate`
14. Run `php artisan db:seed`
15. Run `exit`

Your app is installed and setup at the location defined in `APP_URL` at port 8080 or [http://localhost:8080](http://localhost:8080) when using mostly defaults.