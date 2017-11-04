# HUGO Conference Website Code
This REPO holds a HUGO generated Website with the config template to update and generate it.
+ Tested on OSX 10.12.6
## Install Hugo
+ $ brew install hugo
+ $ hugo

## Instructions for Building The Website off specific Template
+ $ cd gitHub/
+ $ hugo new site my-conference
+ $ cd my-conference
+ $ git init
+ $ git clone https://github.com/jweslley/hugo-conference themes/hugo-conference
+ $ cp themes/hugo-conference/exampleSite/config.yml .
+ NOTE: Change "baseurl:" parameter to "/" in config.yml so all static content will be referneced with realtive paths.
+ $ edit ./config.yml  (NOTE: Modify the ~/github/my-conference/config.yml)
+ $ hugo server -t hugo-conference --watch   (NOTE:  TEST the template site locally)
+ $ hugo -t hugo-conference  (NOTE: This will generate a local copy of the site in /public folder inside the REPO folder)

## To Move the generated Website to our GO Project folder in the /public folder/
+ $ rm -rf ./public    (NOTE: To clean out older builds)
+ $ cp -R ./public ~/Documents/go-workspace/src/github/demo-app/

## Run the site from Go net/http Module
+ $ cd /Users/kraust/Documents/go-workspace/src/github/demo-app
+ $ go run conference-app.go

## Test
+ Note the PORT the server is Listening on:
+ Open Chrome and navigate to http://localhost:<port>  Defaults to :8080 
