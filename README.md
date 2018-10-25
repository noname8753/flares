# Flares 🔥

Flares is a CloudFlare DNS backup tool: every time it runs, dumps your DNS table to the screen.

Optionally exports the data into (BIND formatted) zone files.

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE) [![Go Report Card](https://goreportcard.com/badge/github.com/lfaoro/flares)](https://goreportcard.com/report/github.com/lfaoro/flares)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Flfaoro%2Fflares.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Flfaoro%2Fflares?ref=badge_shield)

![flaredns_demo](static/flaredns_demo.gif)

## Quick Start - docker (painless)
```bash
# CloudFlare auth key is here: https://dash.cloudflare.com/profile ->
# Global API Key -> View
$ docker run -it --rm \
-e CF_AUTH_KEY="" \
-e CF_AUTH_EMAIL="" \
lfaoro/flares domain1.tld domain2.tld
```

## Quick Start - compile (full control)
Golang must be installed: https://golang.org/dl/
```bash
# flaredns
$ go get -u github.com/lfaoro/flares/cmd/flaredns
$ cd $GOPATH/src/github.com/lfaoro/flares/
# flarelogs (TODO: coming soon)
# $ go get -u github.com/lfaoro/flares/cmd/flarelogs
```
### Set the API key and account email address.
```bash
$ flaredns auth # (TODO: coming soon) opens the dashboard at https://dash.cloudflare.com/profile
$ export CF_API_KEY=abcdef1234567890
$ export CF_API_EMAIL=someone@example.com
# alternatively you can provide a `.flaredns` file in your
# $HOME directory with the above variables or specify its path
# with `--config <filePath>`
```
### Run the app
```bash
$ make install
$ flaredns -h
$ flaredns domain.tld
$ flaredns export -d /tmp/tables/ domain.tld
```

# Contributing
> Any help and suggestions are very welcome and appreciated. Start by opening an [issue](https://github.com/lfaoro/flares/issues/new).

- Fork the project
- Create your feature branch `git checkout -b my-new-feature`
- Commit your changes `git commit -am 'Add my feature'`
- Push to the branch `git push origin my-new-feature`
- Create a new pull request against the master branch

## TODO
- [ ] use https://github.com/spf13/cobra for the CLI interface
- [ ] add the flarelogs command
- [ ] add `all` keyword to export all the domains available in the account
- [ ] add `auth` command, automatically opens CloudFlare dashboard

## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Flfaoro%2Fflares.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Flfaoro%2Fflares?ref=badge_large)
