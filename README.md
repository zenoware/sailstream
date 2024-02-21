# Sailstream

## Overview

Clone this starter project if you're in a hurry to spin up a Laravel project with Sail + Jetstream for the UI scaffold.

I created this repo because it's onerous to keep on scaffolding the same things over and over when I'm trying to do a demo or starter project.

## Requirements

A working understanding of how Laravel, Sail, and Jetstream work together.

It has _all_ Sail services enabled by default (except for MariaDB and Postgres). PHPMyAdmin was added on for easy DB viewing. 
Take care of possible port collisions yourself.

## Nuances

- Default MySQL DB host port has been changed to `3307`. Change `FORWARD_DB_PORT` if needed.
- AWS-prefix env var defaults have been changed to Minio.

## Installation

### Clone

    git clone git@github.com:Zenoware/sailstream.git

or

    composer create-project zenoware/sailstream --prefer-dist

### Set environment variables

    cp .env.example .env

### Install composer dependencies

    composer install

### Run

    ./vendor/bin/sail up

### Migrate

    ./vendor/bin/sail artisan migrate

### Build front-end

    ./vendor/bin/sail npm install
    ./vendor/bin/sail npm run dev

### Symlink storage

    ./vendor/bin/sail artisan storage:link

### (Optional) SSH into the app container

    ./vendor/bin/sail shell

## Quick links

- [Laravel](http://localhost)
- [Telescope](http://localhost/telescope)
- [PHPMyAdmin](http://localhost:8080)
- [Minio](http://localhost:9000) (don't forget to add a `local` bucket with R/W permissions)
- [Mailpit](http://localhost:1025)
