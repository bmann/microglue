# microglue

A small glue API server to create a micropub endpoint that can publish to Jekyll and other static sites via git

# Bounty

The intention is to post a bounty for the initial build out / base features of the microglue server.

# Micropub to Git Server

[micro.blog](http://micro.blog) is a decentralized [micro blog](https://en.wikipedia.org/wiki/Microblogging) / [tumblelog](https://kottke.org/05/10/tumblelogs)  service. You sign up at the centralized server and it manages a global namespace for accounts (e.g. @boris is at [micro.blog/boris](http://micro.blog/boris)).

It has an [iOS app](https://itunes.apple.com/us/app/micro-blog/id1253201335) that allows for creating and publishing content from mobile. It also supports many [third party clients](http://help.micro.blog/2017/micropub-clients/).

The iOS app supports WordPress, MetaWeblog and Micropub formats, so you can publish to third party hosting environments.

Jekyll and other static site generators who store content in Git don't have an easy way to publish from mobile.

Rather than running a single API server that has to be supported, we want to make it possible to self-host a simple glue API server that receives Micropub-compatible posts on one side, and pushes to git repos that are the source for static sites on the other side.

## Base Features

See the [Base Features milestone](https://github.com/bmann/microglue/milestone/1)

* micro.blog compatible Micropub endpoint
* Github authentication
* Jekyll templates with default [front matter](https://jekyllrb.com/docs/frontmatter/)
* Deploy to Heroku configuration

## Extended Features

### Static Site Supported
* Configurable templates per blog / per post type

### Deployment targets
* Amazon Lambda
* glitch
* zeit

### Git host support
* Gitlab
