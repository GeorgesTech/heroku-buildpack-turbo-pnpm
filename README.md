# HEROKU BUILDPACK TURBO YARN

Buildpack for prune project with yarn and turborepo.

This buildpack use `yarn dlx turbo prune --scope $BUILD_SCOPE` and move the ***out*** folder in the root of the project.

# usage

1. Write a bunch of apps and scatter them through out your code base.
2. Create a bunch of Heroku apps.
3. For each app, set `BUILD_SCOPE=scope`, and of course:
   `heroku buildpacks:add -a <app> https://github.com/GeorgesTech/heroku-buildpack-turbo-yarn`
4. For each app, `git push git@heroku.com:<app> master`
