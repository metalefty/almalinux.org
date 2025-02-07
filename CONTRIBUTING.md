# Contributing

If you are interested in making a contribution there are a few ways you could help out the project.

## Contributing a blog post

We welcome blog posts of almost any kind from our community! We accept content that covers topics that relate to AlmaLinux OS, the AlmaLinux OS Foundation. If you aren't sure if your blog post topic would be a good one, feel free to create an issue on this repo and ask! You can also join our chat and ask in the Marketing room. 

### Process

- Before you begin writing the blog post, we strongly recommend that you search existing open and closed issues [and existing blog posts](https://github.com/AlmaLinux/almalinux.org/tree/master/content/blog) for similar content, to prevent duplication. 
- We also recommend that you open an issue on the repo to propose your blog post before you begin writing it, to ensure that your blog post would be appropriate for the AlmaLinux blog.
- Please fork the [almalinux.org](https://github.com/AlmaLinux/almalinux.org) repo and submit a pull request with your blog post addition from there. 
- Once you submit your pull request, tag @bennyvasquez for a review. 

#### The content of your .md file

Our website is built in Hugo and served using CloudFlare pages, so you may find some quirks. To add a blog post successfully to the website, take the steps below, and reach out in [~marketing](https://chat.almalinux.org/almalinux/channels/marketing) on our chat server if you have any problems.

**The blog file**

Blog content is served using the `layouts/blog/single.html` format. Note: if you would like to suggest changes to this format, they should be submitted in a PR outside the PR of your blog post.

- create a new file in `./content/blog` named what you'd like the slug (URL) to be, with a file extension of '.md'. For example, the blog post at [almalinux.org/blog/celebrating-500k-docker-pulls](almalinux.org/blog/celebrating-500k-docker-pulls) is in a file named ``./content/blog/celebrating-500k-docker-pulls.md``.

**The Meta data**

- The top of your file should be the metadata for your post. The meta information should be updated to include your posts information. The content is defined and further explained below.

```
---
title: ""
type: blog
author: 
 name: ""
 bio: ""
 image: /users/
date: ''
post:
	title: ""
	image: /blog-images/
---
```

- The **title** is what you'd like displayed at the top of the post.
- The **type** should always be blog.  
- The **name** listed should be yours (either legal name or chosen name or moniker) 
- Your **bio** will be displayed directly under your name, so please keep this to 60 characters or less. If you would like to leave this blank, you may do so. 
- Your author **image** should be appropriate for an all-audiences website and added to `./static/users/` in .png format. The file will serve from `/users/`, so do not change the beginning of this path. 
- The **date** is the date (in YYYY-MM-DD format) you want to see the blog post published, but we cannot always guarantee a publishing timeline. 
- The post **title** should match the above.
- A post **image** should be included, and will be displayed both on the [almalinux.org/blog/](almalinux.org/blog/) feed, and as the header image on the full-page blog post. Use this tempalte to get started: `./static/blog-images/blog_images_template.svg`
  - Your image should not violate any trademarks or copyrights, and should be relevant to blog content. Once created, a PNG version of your image should be placed in `./static/blog-images/` The file will serve from `/blog-images/`, so do not change the beginning of this path. 

**The meat of your post**

- Below the --- of the metadata block, you should place the content of your blog post. This content should be in markdown format, and any images you want to include in your post can be added to `./static/blog-images/` and will serve from `/blog-images/`.
- Before submitting your PR, please test that your content loads correctly by building the site locally with the command `hugo serve`


### Some notes about content

- define all terms used (especially acronyms) so that all readers may understand your content. 
- content submitted to the AlmaLinux blog should be unique and not posted elsewhere on the internet.
- by submitting content to the AlmaLinux website, you acknowledge that you are aware of our [license policy](https://almalinux.org/p/the-almalinux-os-licensing-policy/), are affirming that you own all rights to publish said content.
- external links are allowed, but links to paywalled websites or obvious use of a blog post on the AlmaLinux site as an SEO builder for another website is prohibited. By default, external links should include a '[nofollow](https://en.wikipedia.org/wiki/Nofollow)' value. Exceptions can be requested in your pull request.

## Filing issues

You are free to use [GitHub issues](https://github.com/AlmaLinux/almalinux.org/issues) to submit bugs and for discussions related to the codebase.

### Reporting a Bug

Good bug reports can be very helpful. A bug is a demonstrable problem with the code or functionality.

Please use the [GitHub issues](https://github.com/AlmaLinux/almalinux.org/issues) and check if the issue has already been reported.

A good bug report should be as detailed as possible, so that others won't have to follow up for the essential details.

- Submit a bug in [GitHub issues](https://github.com/AlmaLinux/almalinux.org/issues)

### Requesting a Feature

1. [Search the issues](https://github.com/AlmaLinux/almalinux.org/issues) for any open requests for the same feature, and give a thumbs up or +1 on existing requests.
1. If no previous requests exist, create a new issue. Please be as clear as possible about why the feature is needed and the intended use case.

- Request a feature in [GitHub issues](https://github.com/AlmaLinux/almalinux.org/issues)

## Contributing code
If you plan to propose code changes it is required you create
an [issue](https://github.com/AlmaLinux/almalinux.org/issues) with a brief proposal and discuss it with us first.

This is necessary to avoid more than one contributor working on the same feature/change and to avoid someone from spending time on feature/change that would not be merged for any reason.

For smaller contributions use this workflow:

* Create an [issue](https://github.com/AlmaLinux/almalinux.org/issues) describing the changes.
* Await confirmation from contributors.
* Fork the project.
* Create a branch for your feature or bug fix.
* Add code changes, relevant documentation, etc.
* Send a pull request.  All PRs should be made against the `master` branch.  A dev site will be automatically created based on the PR.  Localization will not be fully working as this pipeline does not run the localization scripts.

After one of the contributors has checked and approved the changes, they will be merged into master branch and will be included in the next deployment.

### Styling Guide

Please adhere to the styling guidelines listed below when contributing to the codebase.

#### Code/Syntax Highlighting

Code/Syntax highlighting is achieved by the builtin [Hugo syntax highlighting](https://gohugo.io/content-management/syntax-highlighting/) feature, which utilizes [Chroma](https://github.com/alecthomas/chroma).

While Hugo supports two syntaxes, we use traditional code fencing for code samples:

````plaintext
```go
package main

import "fmt"

func main () {
    fmt.Println("AlmaLinux is neat-o!")
}
```
````

Supported highlighting languages can be found [here](https://gohugo.io/content-management/syntax-highlighting/#list-of-chroma-highlighting-languages).

## Approval of changes

Before any changes can be merged:

- All minor or cosmetic changes (typos, minor styling, etc) can be approved and merged by any contributor with master merge rights
- All non-cosmetic changes to the website requires the approval of the Marketing lead
