<h1 align="center">My Git Book</h1>
<h6 align="center">Commands and reminders</h6>

---


- ##### Original Git Book
[![N|Solid](https://git-scm.com/images/logos/logomark-black@2x.png)](https://git-scm.com/book/en/v2)

- **[What is git?][df1]** Git is a free and open source distributed version control system.

[//]: # (Comment: Just learning Markdown 😁 )

---

## 1. List of commands
#### In my opinion the most used in the daily basis

| Command &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;| Description |
| ------ | ------ |
| git init | initialization of a git repository (repo) in the current directory  |
| git status | reports the status of the repo |
| git add . | adds file(s) to the staging area|
| git commit -m | commits the file(s) that are in the staging area to the repo, with a specific message that was to be added with ""|
| git log (--oneline) | --oneline represents an optional subcommand to show the log messages in oneline; log, lists all the changes (commits) made in the repo|
| git commit --ammend | allows to change the last made commit, the commit message or the the files that were added or changed  |
| git branch | lists the existing branch's in the repo |
| git branch branch_name | creates a branch from the branch we currently are without changing the HEAD pointer, we stay in the branch we are right now |
| git switch branch_name / git checkout branch_name| changes the current branch to the branch_name we put in the command (changes the pointer HEAD)|
| git switch - c branch_n / git checkout -b branch_n | creates a new branch and changes at the same time the HEAD pointer to the branch we just create |
| git branch -d / git branch -D / git branch -m new_n| -d -> deletes a branch; -D -> force delete to a branch; -m -> changes the name to the currently branch|
| git diff | lists all the changes from staging area to work directory, only if they are in the unstaged area of the repo |
| git diff HEAD | lists all the changes from staged and unstaged area of the repo |
| git diff --staged | list all the changes already staged |
| git diff branch1_n..branch2_n | list all the changes from branch1 to branch2 |
| git diff commit1_id..commit2_id | lists all the changes between two commits |
| git stash | stashes all the uncommitted changes in the current branch |
| git stash pop | removes from the stash all the stashed changes |
| git stash list | lists all the stashed changes |

---

## 2. Basic UNIX commands
This UNIX commands can be helpful if we work in the git bash directly instead of a service that use's git.

| Command | Description |
| ------ | ------ |
| ls | lists all the files and directory's of the current directory |
| ls -a | lists all the files and directory's including hidden files/directory's of the current directory |
| clear | cleans the terminal |
| pwd | print's the current work directory |
| cd directory_name | change us from the current directory to the directory_name |
| cd .. | get us back on directory from the directory path |
| start . | open's the GUI (Graphical User Interface) of the current directory for Windows |
| open . | open's the GUI (Graphical User Interface) of the current directory for Mac/Linux |
| touch file_name | creates a file |
| mkdir dir_name | creates a directory with the dir_name name |
| rm -rf dir_name | removes a directory called dir_name |
| rm file_name | removes a file or files permanently |

---

## 3. Configure Git

* Configure the username in git associated to the repo's:
```sh
git config --global user.name "name"
```
* Configure the email associated to the user:
```sh
git config --global user.email email@email.com
```
* Configure the git editor:
```sh
git config --global core.editor <code>`
```

---

## 4. Graphical User Interface for Git
GUI for Git is not only reliable, efficient, visually pleasing and stylish to use, it also makes Git operations more understandable and enjoyable. Its interface is intuitive, as it allows users to quickly perform basic actions. It even has a drag and drop feature to make your life easier. More than that, you can easily fix errors with just one click. Here are some of the GUI's for Git:
* GitKraken (recommended)
* GitHub Desktop
* Source Tree
* Tower
* Ungit

---

## 5. The process of Committing

Here's a workflow to represent the process of committing:

![](images/comitting-process.png)

In the image below it is represented a image to exemplify the structure of various commits in one branch of a repo.

![](images/operations-committing.png)

---

## 6. Ignoring files
Git ignore's everything inside the .gitignore file.
<br />
E.g.:
* .DS_Store -> ignores every file with the extension DS_Store
* foldername/ -> ignores the entire folder
* .log -> ignores every file with the extension .log

---

## 7. Branching

Here's a workflow to represent the process of branching:

![](images/operations-branching.png)

In the image above we can see that from commit 2, the tree starts having more than just 1 branch to have 3 branches.

---

## 8. Merging

Here's a workflow to represent branching and merging, because there's no merging without a "little" branching before:

![](images/operations-branching-merging.png)

In the above image we can see two operations of merging, from commit 4 to commit 8 and commit 6 to commit 8 again, that is, a merge from the two branches existing in the tree to the branch master (also called main).

---





---
---

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.



## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
