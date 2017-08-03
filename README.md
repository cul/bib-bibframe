# Bibframe Editor
This repo contains a local installation of `bfe`, customized for use at the Columbia University Libraries. The `bfe` (https://github.com/lcnetdev/bfe) codebase is contained within a git submodule. The submodule points to an older version of `bfe` that is currently still in use at CUL. For more information about `bfe`, please visit their [README](https://github.com/lcnetdev/bfe/blob/master/README.md).

## Repository Setup
This the site content is at `/public`.

`/public`   - contains all the js/css/html files necessary for the site

`/bfe`      - git submodule which contains the bfe source code used

`/lib`      - could include Capistrano tasks, if necessary

`/config/*` - Capistrano configuration

`/Capfile`  - list all the Capistrano requirements

`/Gemfile*` - Gemfile and Gemfile.lock for use with Bundler

## Deploying
1. Locally clone this repository

   `git clone --recursive git@github.com:cul/bib-bibframe.git`
2. Install ruby

   _Deploy was tested with `ruby 3.3.3`._
3. Install bundler

   `gem install bundler`
  
4. Install all gems required
  
   `bundle install`
   
5. Deploy
   
   `cap {environment} deploy`
   
   _Note: You will be prompted for a branch, by default deploys the local branch._

## Making changes to repository
1. Make the changes locally commit them to a branch, push to the remote repository.
2. Deploy using the instructions above.

## Plan to update `BFE`
In order to update our local version of bfe, the git submodule within this repo would need to be updated to point at the desired commit of the remote bfe repository.
