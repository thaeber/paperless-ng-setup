# paperless-ng-setup

A simple setup for paperless-ng using a sqlite database on a Synology NAS

## Installation

Paperless is a simple and fast document management system (DMS) mostly for personal use cases. The original repo can be found here: <https://github.com/jonaswinkler/paperless-ng>.

- Got to `Package Center` and install the `Docker` package.

- Open `File Station` and create a folder named `paperless` directly under the existing  `docker` folder.

- Enable SSH access in the `Control Panel` if you have not already done so.

- SSH into the NAS and execute `sudo -i` to become root.

- Go to the `paperless` folder just created. Clone this repository into the `paperless` folder or, if `git` is not installed, upload all files of the repository using the `File Station`.

- Run `docker-compose up -d` and wait for docker to pull the images and the main container to run.

- Run `docker-compose run --rm webserver createsuperuser` to create a user and password with administration privileges. Make sure to remember the user name and password. ;-)

