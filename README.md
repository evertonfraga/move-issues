# Move Issues

[![npm](https://badge.fury.io/js/probot-move-issues.svg)](https://www.npmjs.com/package/probot-move-issues)


Move Issues is a GitHub App built with [Probot](https://github.com/probot/probot)
that moves issues to a different repository.

<p>
  <img width="420" src="assets/source-issue.png">
  <img width="420" src="assets/target-issue.png">
</p>

## Supporting the Project

Move Issues is an MIT-licensed open source project. Its ongoing
development is made possible thanks to the support of awesome backers.
If you'd like to join them, please consider contributing with
[Patreon](https://goo.gl/qRhKSW), [PayPal](https://goo.gl/5FnBaw)
or [Bitcoin](https://goo.gl/uJUAaU).

## Usage

1. **[Install the GitHub App](https://github.com/apps/move)**
2. Create `.github/move.yml` based on the template below
3. Move an issue by creating a comment with the command: `/move to <repo>`

#### Configuration

Create `.github/move.yml` in the default branch to enable the app.
The file can be empty, or it can override any of these default settings:

```yml
# Configuration for move-issues - https://github.com/dessant/move-issues

# Delete the command comment. Ignored when the comment also contains other content
deleteCommand: true
# Close the source issue after moving
closeSourceIssue: true
# Lock the source issue after moving
lockSourceIssue: false
# Set custom aliases for targets
# aliases:
#   r: repo
#   or: owner/repo
```

#### Command Syntax

```sh
/move [to ][<owner>/]<repo>
```

###### Examples:

```sh
/move to repo
/move to owner/repo
/move repo
/move owner/repo
```

## Deployment

See [docs/deploy.md](docs/deploy.md) if you would like to run your own
instance of this app.

## License

Move Issues is released under the terms of the MIT License.
Please refer to the [LICENSE](LICENSE) file.
