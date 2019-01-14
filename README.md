**Warning** this is an experimental buildpack and is provided as-is without any
promise of support.

# Heroku Buildpack: SonarQube Scanner

This experimental [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks)
vendors Sonar Scanner into the dyno. It is intended for use with Heroku CI or any
other environment where vendoring sonar into the dyno is acceptable (i.e. dev, test).

## Usage

This is intended to be transparent to your application. No service is started - Sonar Scanner
will only execute when invoked. For example, in the test-setup script in your Heroku CI
configuration in [app.json](https://devcenter.heroku.com/articles/heroku-ci##specifying-custom-test-commands-the-scripts-key).

By default, the buildpack provides the latest Sonar Scanner version that is available. 

You can specify a `SONAR_VERSION` in the `env` section of your
[app.json](https://devcenter.heroku.com/articles/heroku-ci#environment-variables-env-key)
to use a different version. This feature is experimental and subject to change.