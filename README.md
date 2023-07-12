# Docker and Jekyll

![Make Jekyll Great Again](./assets/repository-docker-jekyll.png)

The template that takes you from zero to a deployed Jekyll blog starter in 4 steps 🚀

1. Use this template to create your own repo and clone your repo 👽
2. Set up GitHub pages to use "from action" (BETA) 🤞
3. Run shell scripts 🐚
4. Push all your new code to your remote repo and wait for your new site 🧙‍♂️

Inspired by [Bill Raymond](https://github.com/BillRaymond) thank you so much!

## About

A personal project to explore the use case of Docker and `.devcontainer` environment for using jekyll!

## Why?

Turns out, running Jekyll and ruby and gems and bundler and... as a sudo root user is a bit of PIA, so I was searching for a different way.

Enter Docker and containerized development.

With Docker, we can create a 'computer' and install our development environment inside that 'computer'.

Allowing local editing and development without cluttering your host.

Also, with GitHub Actions it is possible to automate the deployment process down to just YOLO pushing. `One push === site update`.

## Prerequisites

- VSCode
- Docker
- Docker Desktop
- Docker and Dev Containers extension for VSCode

## Steps:

- This is a template repo, you will need to use the template and clone it to your local machine
- Open VSCode
- Hit the command palette `ctrl+shift+p`
- and select `open folder in container`

### THIS WILL TAKE A WHILE 🕐

While you are waiting...Do this if you would like to use GH pages (recommended) ⬇️

> **Turn on deployment from actions (beta) in:**
>
> `Settings -> Pages -> Deploy From Action (in the drop menu)`

1. **RUN ONLY ONCE** :smile:

```shell
sh init-jekyll.sh
```

2. **OPTIONAL:** If you would like to expose the theme files (do not run this if you haven't chosen a theme) run: 🤔

```shell
sh load-theme.sh
```

3. Run the site either or both!:

#### Run the site locally with: 👨‍💻

```shell
bundle exec jekyll serve --livereload
```

#### Github Pages 👏

- Add all the newly created files and push the code to your remote repo
- Your site will be deployed automatically if you have chosen the `github action workflow`
  - You will have a folder `.github`
  - With a `workflow` directory
  - Containing a `.yml` file that will automatically deploy directly to GitHub pages
