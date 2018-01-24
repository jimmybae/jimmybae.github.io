---
layout: post
title: "git remote change"
description: "git remote change & config"
date: 2018-01-17
categories: DEVELOP
tags: [mac, git, github, configuration]
comments: true
share: true
---
### 1. git remote change
```
$ cd ~/bgs/data/node-project/cli-prototype
$ zip -r .git.zip .git
$ rm -rf .git
```
https://github.com  
Create a new repository
```
$ git init
$ git add .
$ git commit -m "first commit"
$ git remote add origin https://github.com/......
$ git push -u origin master
```

### 2. Permission denied
```
$ git push -u origin master
remote: Permission to jimmy***/cli-prototype.git denied to bird**.
fatal: unable to access 'https://github.com/jimmy***/cli-prototype.git/': The requested URL returned error: 403
```
- mac
    1. open Keychain Access App
    2. Search 'git'
    3. Get Info
    4. Account modify
    5. Save Changes

### 3. git config
```
$ git config --global --list
credential.helper=osxkeychain
user.name=jimmy***
user.email=mywind****@gmail.com

$ git config --local --list
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
core.ignorecase=true
core.precomposeunicode=true
remote.origin.url=https://github.com/jimmy***/cli-prototype.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.master.remote=origin
branch.master.merge=refs/heads/master
```
```
$ git config --global user.name "jimmy***"
$ git config --global user.email "mywind****@gamil.com"
```
