# WebRTC.org website (*** This repository is deprecated ***)

The documentation to contribute to native code is available at https://webrtc.googlesource.com/src/+/refs/heads/master/docs/native-code/index.md

Info about the WebRTC project and Web API's is available at https://webrtc.org


# The [webrtc.org](https://webrtc.org) website #

This is the repo for [webrtc.org](http://webrtc.org), home of the WebRTC project.

For more information about WebRTC, we maintain a list of
[WebRTC Resources](/start/). If you've never worked with WebRTC, we recommend you
start with the 2013 Google I/O
[WebRTC presentation](http://www.youtube.com/watch?v=p2HzZkd2A40).

We welcome corrections, updates and additions!

See [CONTRIBUTING](CONTRIBUTING.md) for instructions. All contributors must
sign a contributor license agreement before code can be accepted. Please
complete the agreement for an
[individual](https://developers.google.com/open-source/cla/individual) or a
[corporation](https://developers.google.com/open-source/cla/corporate) as
appropriate.


## Add or Edit Content

The [webrtc.org](https://webrtc.org) site is built from Markdown files, using
the [Jekyll](https://jekyllrb.com/) tool.

The default branch for the
[webrtc.org repo](https://github.com/webrtc/webrtc-org) is **gh-pages**.

You can review your changes (after you've pushed them) on the
[GitHub Pages](https://pages.github.com/) site for your fork. For example, if
your username is _foobar_ and you edited the **Contributing Fixes** page, you
can view your updated version online at
_foobar.github.io/webrtc-org/contributing_. A GitHub Pages site is
automatically generated by GitHub for every repo that has a _gh-pages_ branch.

You can also build and serve the site locally in order to check your work. See
the instructions below.


### Where are the Files?

Each page on the site corresponds to an _index.md_ file in a directory of the
repository's gh-pages branch. For example, the **Development** page at
[webrtc.org/native-code/development](https://webrtc.org/native-code/development/)
corresponds to
[github.com/webrtc/webrtc-org/tree/gh-pages/native-code/development/index.md](https://github.com/webrtc/webrtc-org/tree/gh-pages/native-code/development).

To simplify URLs, many pages are at the top level of the site rather than in a
subdirectory. For example, the **Release Notes** page is at
[webrtc.org/release-notes](https://webrtc.org/release-notes/) even though it
lives under the site's **About** menu. (The corresponding Markdown file is
[github.com/webrtc/webrtc-org/tree/gh-pages/release-notes/index.md](https://github.com/webrtc/webrtc-org/tree/gh-pages/release-notes).)


### Make a Correction or update

For minor content changes, fork the repo and make a pull request from your
GitHub account.

For major or ongoing changes, create a branch and issue pull requests from
that. Please delete the branch once you’ve finished working on it.

Find out more in our
[Developer's Guide](https://docs.google.com/document/d/1tn1t6LW2ffzGuYTK3366w1fhTkkzsSvHsBnOHoDfRzY/edit#heading=h.fqhc83uuzrcb).


### Add a New Page

  1. Create a new directory in your local repo, either at the top level of the
     site or in an existing directory.

  2. Copy an existing _index.md_ file into the new directory you created.

  3. At the start of the new _index.md_ file, adjust the
  [YAML front matter](https://jekyllrb.com/docs/frontmatter/) that is used by
  the Jekyll build tool. For example, the following front matter will cause
  Jekyll to create a page with the title _Android_ at
  _webrtc.org/native-code/android/index.html_:

         ---
         layout: default
         title: Android
         permalink: /native-code/android/
         ---

  4. Edit the content of _index.md_: files are in
     [Markdown format](http://daringfireball.net/projects/markdown/).

     Images are added with markup like the following example (from the
     [Architecture](https://raw.githubusercontent.com/webrtc/webrtc-org/gh-pages/architecture/index.md) page):
     ```markdown
     ![]({{ site.baseurl }}/assets/images/webrtc-public-diagram-for-website.png)
     ```

     Add code snippets like this:

         ~~~~~ bash
         export JAVA_HOME=<location of OpenJDK 7>
         ~~~~~

  5. Commit and push your work.

  6. Review your changes locally or from the GitHub Pages site for your fork
     (for example, _usename.github.io/webrtc-org_).

  7. Make a pull request.


## Build and Serve the Site Locally

These steps are optional, and require familiarity with managing gem
dependencies. If you're only interested is previewing changes before making a
pull request, see [Add or Edit Content](#add-or-edit-content), above.

  1. If necessary, install Ruby.

  2. Navigate to your webrtc-org repo directory.

  3. Run the following command:

         bundle exec jekyll serve

     HTML files are generated in the _site directory and regenerated automatically when you make changes.

  4. View the modified site in a browser at
     [http://0.0.0.0:4000/webrtc-org](http://0.0.0.0:4000/webrtc-org/).

More information is available from
[Using Jekyll With Pages](https://help.github.com/articles/using-jekyll-with-pages)
(but **do not** run the Setting up Jekyll step!)
