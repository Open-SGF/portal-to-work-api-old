# Contributing

The easiest way to get started with contributing to the project is to get started with the VS Code install.

## Project Setup for Development

### Perquisites

1. Basic understanding of [Laravel 6.x](https://laravel.com/docs/6.x)
1. Install [Docker](https://docs.docker.com/get-docker/) for your system
1. Install [VS Code](https://code.visualstudio.com/docs/setup/setup-overview) for your system
1. Fork this project (<https://github.com/Open-SGF/portal-to-work-api/fork>)
1. Install project by cloning your forked repository to a location on your file system.

### VS Code Setup

1. Open up VS Code
2. Install the "Remote Containers" (ms-vscode-remote remote-containers)
3. Open the workspace for this project by navigating to `path/to/project/workspace.code-workspace`
4. Open a [terminal Window](https://code.visualstudio.com/docs/editor/integrated-terminal) for the project
5. Type in terminal: `cp .env.example .env` or if on Windows type: `copy .env.example .env` instead

   This makes a local copy of _your_ environment settings that you're free to modify for this project.

6. Edit the `.env` file, specifically these option(s):

	**DB_PASSWORD** - This will be your database password, so please provide one.

7. Open the [VS Code command palette](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette) and type the command `Remote-Containers: Rebuild and Reopen in Container` and hit enter.

   This will re-launch VS Code to work off a container environment. This environment contains all the tools you'll need to develop for this project. This step may take a while.

8. When container is open, open up a [terminal Window](https://code.visualstudio.com/docs/editor/integrated-terminal)

9. Run `composer install`

   This will install all the PHP dependencies for the project. This may take a while.

10. Run `php artisan key:generate`

    This creates a project key used for authentication security.

11. Run `php artisan migrate`

    This creates the tables, views, etc... for the database.

12. Run `php artisan db:seed`

    This fills the database with fake data.

Your app is installed and setup at the location defined in `APP_URL` at port 8080 or [http://localhost:8000](http://localhost:8000) depending on your `.env` file settings.

### Closing down the containers

Make a habit of closing down the project after finishing some work. This will save some computer resources.

1. Open the [VS Code command palette](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette)

2. Type and run: `Remote: Close remote Connection`

   This will close down the Docker connections.

To resume work after shutting down

1. Open VS Code

2. Navigate to the project

3. Open the [VS Code command palette](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette)

4. Type and run: `Remote-Containers: Open Workspace in Container`

## Create a PR

1. Create your feature branch (`git checkout -b feature/fooBar`)
1. Commit your changes (`git commit -am 'Add some fooBar'`)
1. Push to the branch (`git push origin head`)
1. Create a new Pull Request