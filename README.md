⚠️ Not so safe to use, some issue with permission?

In the heroku build logs:
```
thread 'main' panicked at 'called `Result::unwrap()` on an `Err` value: Os { code: 13, kind: PermissionDenied, message: "Permission denied" }'
```

# HEROKU BUILDPACK TURBO PNPM

A buildpack to prune project with pnpm and turborepo.

This buildpack use `turbo prune --scope $BUILD_SCOPE` and move the `/out` folder content to the root build folder.

# Usage

1. Write a bunch of apps and scatter them throughout your code base.
2. Create a bunch of Heroku apps.
3. For each app, set `BUILD_SCOPE=scope`, and of course:
   `heroku buildpacks:add -a <app> https://github.com/GeorgesTech/heroku-buildpack-turbo-pnpm`
4. For each app, `git push git@heroku.com:<app> master`
