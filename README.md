# git JIRA

Generate git branch names based on JIRA Issues

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes

### Prerequisites

* curl
* [jq](https://github.com/stedolan/jq)

#### For development only

* [shellcheck](https://github.com/koalaman/shellcheck)

### Installing

To install into your $HOME/bin directory, which I assume is in your $PATH

```
$ make install
```

## Configuration

1) Ensure there is a [~/.netrc](https://www.gnu.org/software/inetutils/manual/html_node/The-_002enetrc-file.html) entry for the host of your cloud hosted atlassian account eg. for example.atlassian.net

```
machine example.atlassian.net
  password <my password>
  login <my login>
```

2) Configure that same host for use within git jira

```
$ git config --global git.jira example.atlassian.net
```

That's it!

## Usage

```
$ git jira <issue number>
```

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md)
