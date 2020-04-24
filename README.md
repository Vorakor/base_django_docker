# Interiori Core Django App

This is the core Interiori app that will run various modules as we build them.

Go here for markdown syntax: [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

**Eric & Aubrey** - use this markdown sheet to detail anything from your standpoint that we may need to add to the core project.

## Launch Dev Environment

These are some instructions for how to get the dev environment up and running at the moment. Granted though, there isn't much to see just yet.

This first section is just a summary, then it goes into more detail.

### Summary Instructions

First you will need to get and install Git so you can pull all the necessary code to your machine, Google it honestly because it's very easy to do. You will also need docker and docker-compose, there's a GUI to do this available at [Docker for Windows](docs.docker.com/docker-for-windows/install/) and [Docker for Mac](docs.docker.com/docker-for-mac/install/), this should install the necessary tooling to do the job.

Next you need to pull down the code via Git and then you will be running the docker commands and targeting the files in the directory.

### In Detail - Terminal Style

Caution: if you aren't familiar with terminal or the windows equivalent command prompt, don't try to use it, dangerous stuff can happen when you play with them and it can seriously mess up your machine.

## TODO

- Create executables and or other types of graphical scripting that will allow you to simply double click and it will run and launch all the necessary code and commands.
- At some point in the future create shell scripts to run commands like "**interiori up**" or "**interiori up --env=dev**" as well as commands like "**interiori down**" and "**interiori restart**".
- Don't forget the docker commands to run for prod:
  - docker-compose -f docker-compose.prod.yml up -d --build
  - docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
  - docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear
