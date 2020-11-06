# Flares 🔥

Flares is a CloudFlare DNS backup tool, it dumps your DNS table to the screen or exports it as BIND formatted zone 
files.

[![BSD License](https://img.shields.io/badge/license-BSD-blue.svg?style=flat)](LICENSE) 
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Flfaoro%2Fflares.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Flfaoro%2Fflares?ref=badge_shield)
[![Go Report Card](https://goreportcard.com/badge/github.com/lfaoro/flares)](https://goreportcard.com/report/github.com/lfaoro/flares)

![Docker Pulls](https://img.shields.io/docker/pulls/lfaoro/flares.svg?logo=docker&style=popout-square)
[![PayPal](https://img.shields.io/badge/paypal-contribute-blue.svg?style=popout-square&logo=paypal)](https://www.paypal.com/pools/c/8fm4OKBYMa)

Currently using it for simple backups. This version can utilize a cloudflare token with read-only acl
flares --token "<readonly cloudflare token>" --export --all
