Philosophy
----------

Since Ximera is built on LaTeX source, we want to use LaTeX as a
method of validating the code authors write. Hence, if you want to
write a Ximera online activity, the first step is constructing LaTeX
documents.

Once you have the LaTeX documents, and you have checked them for
typos, accuracy, etc, the fact that they compile should be reasonable
evidence that they will display correctly in Ximera.

Directions for download
-----------------------

### Register for a GitHub account

This step is required if you are going to publish your activities to Ximera website.
If you only need to compile activities to `pdf`, you can skip this step step.
If you already have a GitHub account, you can go on to the next step.
Otherwise go to:

[https://github.com/](https://github.com/)

and create an account. Choose the free plan, and no organization is
needed.


### Obtain a git client

For Linux and OS X console clients are available.

For Windows, download git [here](https://git-scm.com/downloads).


### Clone the ximeraLatex repository

Depending on your operating system, these command may be different. 

##### For OS X

Run the following commands in terminal:

- `mkdir -p ~/Library/texmf/tex/latex/`
- `cd ~/Library/texmf/tex/latex/`
- `git clone https://github.com/XimeraStevens/ximeraLatex.git`
- `cd ximeraLatex`
- `git checkout develop`

##### For Windows

Run `git bash` and perform the following steps:

- `mkdir -p C:\localtexmf\tex\latex\`
- `cd C:\localtexmf\tex\latex\`
- `git clone https://github.com/XimeraStevens/ximeraLatex.git`
- `cd ximeraLatex`
- `git checkout develop`

For MiKteX to notice `C:\localtexmf\tex\latex\` directory, go to:

1. Start -> All programs -> MiKTeX Folder -> Maintenance (Admin) Folder -> Settings (Admin).
2. Now select the tab "Roots."
3. Click "Add" because you are going to add a path.
4. Find `C:\localtexmf\` and click "OK."
5. Click "apply" then "OK."
6. Reopen Miktex Settings (Admin). Click Refresh FNDB.

This will allow all of your documents to find ximera.cls. Note, it is
important that none of the directories containing ximeraLatex have
spaces in their names.

##### For Linux


Run the following commands in terminal:

- `mkdir -p ~/texmf/tex/latex/`
- `cd ~/texmf/tex/latex/`
- `git clone https://github.com/XimeraStevens/ximeraLatex.git`
- `cd ximeraLatex`
- `git checkout develop`


Writing an activity
-------------------

You should create your courses (set of activities) in you own GitHub repo.
All activities should be in their own directory,
with all supporting documents also in this directory.
This will provide maximum flexibility and modularity of
your activity.
Also, you will be able to compile each activity on its own, or
as a collection.


Staying up-to-date
------------------

While we hope to solidify the ximera.cls file, at this point we are
still in development stages.

To keep your `ximera.cls` file up-to-date, you may need to periodically update it.
Go to `ximeraLatex` directory (i.e. where you cloned `ximeraLatex` repo) and run

- `ximeraLatex$ git fetch --all`
- `ximeraLatex$ git reset --hard origin/develop`
