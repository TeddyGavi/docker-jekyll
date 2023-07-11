# Docker and Jekyll

Template for setup of Docker and jeykll

Inspired by [Bill Raymond](https://github.com/BillRaymond) thank you!

## About

A personal project to explore the use case of Docker and `.devcontainer` environment for using jekyll!

## Prerequisites
- VSCode
- Docker
- Docker Desktop
- Docker and Dev Containers extension for VSCode

## Steps:

- This is a template repo, you will need to use the template and clone to your local machine
- `open folder in container` from command pallette will get you started `ctrl+shift+p`
- Run
> **DEPLOYMENT** This is the recommonded use case. Turn on deployment from actions (beta) in: 
> 
>`Settings -> Pages -> Deploy From Action (in the drop menu)` 

1. **RUN ONLY ONCE** :smile:

```shell
sh init-jekyll.sh
```

2. **OPTIONAL:** If you would like to expose the theme files (do not run this if you haven't chosen a teme) run:

```shell
sh load-theme.sh
```
3. Run the site either or both!: 
#### Run the site locally with:

 ```shell
 bundle exec jekyll serve --livereload
 ```
#### Github Pages
- Add all the newly created files and push the code to your remote repo
- Your site will be deployed automatically if you have chosen the `github action workflow` 
  - You will have a folder `.github`
  - With a `workflow` directioy
  - Containing a `.yml` file that will automatically deploy directly to GitHub pages