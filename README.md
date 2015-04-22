# Middleman Build Pack

Originally forked from [heroku-buildpack-prismic](https://github.com/hashicorp/heroku-buildpack-middleman) this is a build pack for [Middleman](http://middlemanapp.com) and [middleman-prismic](https://github.com/kollegorna/middleman-prismic) that will
create your static site and fetch your content from Prismic.

It is cleaner than most Middleman build packs out there because it
takes advantage of the [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi)
buildpack to separate out the Ruby and Middleman specific components.

## Usage

This build pack is meant to be used with the
[heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi)
buildpack. Setup generally goes like this with an existing Heroku app:

```
$ heroku config:add BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi.git
...
$ cat .buildpacks
https://github.com/heroku/heroku-buildpack-ruby.git
https://github.com/hashicorp/heroku-buildpack-middleman.git
```

Then just push!
