---
layout: page
title: "Releasing"
description: "Steps involved to publish a new Home Assistant release."
date: 2016-07-13 17:00
sidebar: true
comments: false
sharing: true
footer: true
---

This page describes the steps for publishing a new Home Assistant release.

### {% linkable_title GitHub %}

1. Create a pull request from `dev` to `master` with the upcoming release number as title.
2. Merge `master` into `dev` to make the PR mergable. PR message contains intro, highlighting major changes, and an overview of all changes tagging each author.
3. Merge pull request.
4. Go to [releases](https://github.com/home-assistant/home-assistant/releases) and tag a new release on the `master` branch. Tag name and title name are version number. Release description is text from PR.

### {% linkable_title Website %}

1. Create a blog post and base it on the PR text. Add images, additional text, links, etc. if it adds value. Tag each platform/component in message to documentation.
2. Create missing documentation as stumbs.
3. Create a pull request from `next` to `master` with the upcoming release number as title.
4. Merge `master` into `next` (`git checkout next && git merge master`) to make the PR mergable.
5. Update the link on the frontpage (`source/index.html`) to link to the new release blog post and version number.
6. Merge blog post and updated frontpage to `master` (`git merge next`).

### {% linkable_title Python Package Index %}

Checkout `master` branch and run `script/release` to publish the new release on [Python Package Index](https://pypi.python.org)

### {% linkable_title Social media %}

1. Create a [tweet](https://twitter.com/home_assistant) announcing blog post linking to release notes.
2. Publish a link to the tweet/release blog post for the [Google+ Community](https://plus.google.com/b/110560654828510104551/communities/106562234893511202708).

