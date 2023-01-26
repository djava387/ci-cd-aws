# CI CD Jenkins -> AWS

## Demo

## CI

![](CI-Jenkins-github.gif)

## CD

![](CD-Jenkins-aws.gif)

## How have you use Jenkins to add Continuous integration with this project?

-Giving Jenkins acces to github repo to make automated build and tests after making changes to it and configuring execute shell for build.

### How did you allow Jenkins access to the Github repo?

- Adding Jenkins public keys, through Deploy Keys feature in github

### How did you get the Github repo to trigger the build?

-Added a new webhook with Jenkins url(ip)/github-webhook/

---

## How have you use Jenkins to add Continuous delivery with this project?

-Giving Jenkins access to EC2 instance for automated deployment after a succes build from CI
-Running execute shell for environment.

### How did you allow Jenkins access to the EC2 instance?

- EC2 instance ssh key i.e adding it into Jenkin's new project at SSH agent (access to deployment)

### How did you get the CI project to trigger the CD build?

Added a post-build action in ci to trigger cd build, only if the build is stable

---
