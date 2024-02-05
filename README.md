## Bookmarks

Welcome to our Image Sharing Platform! This project allows users to discover, bookmark, and share images encountered
during their web browsing adventures. Whether you stumble upon a captivating photo or a visually stunning piece of art,
this platform is your go-to for bookmarking and sharing those images with the community.

## Features

* **Bookmarking**: Users can easily bookmark any image found on the Internet and create a curated collection of their
  favorites.
* **Sharing**: Share your bookmarked images with other users and explore a world of visual inspiration.
* **Activity Tracking**: Stay in the loop by monitoring the on-platform activities of users you follow. See what images
  they're discovering and engaging with.
* **Preference Expression**: Express your opinions on images by liking or disliking them. Contribute to the platform's
  community-driven curation.

## Authentication

* **User Registration**: Easily sign up for an account on our platform to start bookmarking and sharing your favorite
  images.
* **Social Authentication**: Seamlessly log in with your Google or Facebook account for a hassle-free authentication
  process.
* **Password Recovery**: Forgot your password? No worries! Utilize our password recovery feature to regain access to
  your account.

## Usage of Redis

* **Image Views**: Redis is employed to keep track of the number of views each image receives, providing insights into
  their popularity.
* **Image Ratings**: Redis is also used to store and manage the ratings given by users to images on the platform.

## Installation:

1. #### Clone the repository and set up required dependencies and environment

```console
# clone the repo
$ git clone https://github.com/karim3487/bookmark_project

# change the working directory to bookmark-project
$ cd bookmark_project

# create python virtual enviroment and activate it
$ python -m venv venv
$ source venv/bin/activate

# change the working directory to bookmark
(venv) cd bookmarks
```

2. #### Installing Redis storage

```console
# get the Redis image of the Docker platform
$ docker pull redis

# run a Docker container for Redis
$ docker run -it --rm --name redis -p 6379:6379 redis
```
3. Edit your machine's `hosts` file by adding the following below
   line
```console
127.0.0.1 bookmarks-site.com
```
4. #### Run the application locally and start exploring and sharing images
```console
# make migrations and migrate it
(venv) python manage.py make migrations
(venv) python manage.py migrate
(venv) python manage.py runserver_plus --cert-file cert.crt`
```
