## Generate release notes for a Github milestone

To generate markdown release notes that comprise the list of bugs
and issues in a GitHub milestone follow these steps:

- Clone this project
- Configure the application with the following properties:
```
releasenotes
  github:
    organization:
    repository:
    username:
    password:
```

NOTE: When generating release notes for a public repository, the `username` and `password` properties are optional. However, specifying them ensures that you don't hit [Github's rate limit](https://developer.github.com/v3/?#rate-limiting) easily.

- Run the following commands:

```
$ ./mvnw clean install

$ java -jar target/github-release-notes-generator.jar <milestone> <path_to_generate_file>
```

NOTE: The `<milestone>` may either refer to the milestone number or a name.
