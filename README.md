# Dockerfiles for the local development setup of Artemis

Hosts the Dockerfiles that are used for the local setups for Artemis.
The main reason for the existance of this repository is that the official Docker images of the tools in this repository only offer x64 images. As arm64 CPUs become more common (especially in the Artemis develper team) it is beneficial to have native images for these processors.

Currently this repository contains Dockerfiles for the following tools:

- **Bitbucket** (adapted from <https://bitbucket.org/atlassian-docker/docker-atlassian-bitbucket-server/src/master/>)
- **Bamboo** (adapted from <https://bitbucket.org/atlassian-docker/docker-bamboo-server/src/7.2.5/>)
- **Jira** (adapted from <https://bitbucket.org/atlassian-docker/docker-atlassian-jira/src/master/>)
- **GitLab** (adapted from <https://gitlab.com/gitlab-org/omnibus-gitlab/-/tree/master/docker>)
- **Jenkins** (adapted from <https://github.com/jenkinsci/docker>)

## Building the images

Each push to main (or merge into), will trigger a re-build of the images.

> __Please note:__ Only those images that have changes in either their `Dockerfile` or `RELEASE`-file will be rebuilt!

To prevent an image from being built at all, simply change the `BUILD=yes` line to `BUILD=no` in the corresponding `RELEASE`-file.

### Change versions built

To change the version of the images being built, edit their version in the corresponding `RELEASE`-file.
