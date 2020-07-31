# oss-gradle-template

This project template sets up your Maven-based project to be published to Maven Central.

## Building

```
./mvnw install
```

## Publishing to Artifactory

```
./gradlew artifactoryPublish
```

## CI 

This project contains a [GitHub Actions workflow file](.github/workflows/branch.yml) that:

* runs the build on every push to any branch
* publishes to Artifactory on every push to the `release` branch.

To make that work, add these secrets to your GitHub project:

* `GH_EMAIL`: the email you want to associate with the commits the Maven release plugin does to update the version number
* `GH_USERNAME`: the username you want to associate with the commits the Maven release plugin does to update the version number
* `GH_ACCESS_TOKEN`: the Github access token to authenticate for the commits the Maven release plugin does to update the version number
* `SIGNING_KEY`: the private key that is used for signing the artifacts
* `SIGNING_PASSWORD`: the password to the private key

