# How to make a new lesson

This repository describes how to create
a new lesson website in `github.com/clemsonciti`.
The template for lessons is defined in the repository
[https://github.com/clemsonciti/lesson-template](https://github.com/clemsonciti/lesson-template).

We strongly recommend using Mac OS X or Linux for development
(a virtual machine or docker container will serve fine).
You can also develop using Windows,
but we do not provide any instructions for setting up the required software.

1.  Clone the lesson-template repository and rename the resulting folder.

    ~~~
    $ git clone -o upstream https://github.com/clemsonciti/lesson-template
    $ mv lesson-template test-lesson
    ~~~

2.  One-time setup

    You will need to have [pip](https://pip.pypa.io/en/stable/) installed.
    Additionally, you will need to install [Pandoc](http://pandoc.org).
    Finally, you will have to install a few Python packages:

    ~~~
    $ cd test-lesson
    $ pip install -r requirements.txt
    ~~~

3.  Prepare the lesson materials (markdown files)

    All the lesson material can be organized in Markdown files
    named `00-intro.md`, `01-files.md`, etc.,
    These will automatically be rendered into HTML files
    `00-intro.html`, `01-files.html`, etc.,
    You should also create an `index.md` that will link to all these HTML files.

4.  Preview locally and commit

    Run `make preview` to build the HTML files,
    which you can preview using a web browser.
    If you're happy with these files, you can `git add` and `git commit` them.

5.  Create your lesson's repository and push

    Create a repository on Github under the `clemsonciti` organization,
    for example, `https://github.com/clemsonciti/test-lesson`.
    Add this repository as a remote:

    ~~~
    $ git remote add origin https://github.com/clemsonciti/test-lesson
    ~~~
    
6.  Finally, push your lesson materials to the new remote:

    ~~~
    $ git push origin gh-pages
    ~~~
