THIS IS README!

Start by making yourself a user on github, if you do not already have one:
https://github.com/join?source=header-home

Setting up git identity on your own machine, and even change which editor is your core editor.

git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor vim

On windows you will need to do a bit more specific:
Consult : https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup

Speeding up the workflow, by adding a fingerprint to your computer.
In short it means that you allow your computer to hold a key, for which github can recognize when you interact with github.

generate ssh key
https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/
Make the passphrase the same as your github account.

adding to git
https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/

Once added ssh in with:
Log in with passphrase to your github.
ssh -T git@github.com


So once we have a user, we wish to create a project (repository).
Let us make a repository, which can be done from the main page.

With our newly created github repository, we can start working.
First off we need to clone the project to our machine, by using:

git clone <repo>

Example:
git clone https://github.com/Grymer92/git

This will download the complete repository to the current directory in which you stand.
And everything comes in one wrapped directory, meaning you will not see files flushed down into your "Documents" directory.

EDITTING:

There are 5 core commands you will want to know:

| 1) git status |
2) git pull |
3) git add/rm <filename> |
4) git commit [flags] "optional message" |
5) git push |

1) Gives you an overview of files that have been modified, deleted or created.
   It also makes you aware if they have been added, or have yet to be added.

2) Pulls most recent version of the repository, meaning that if any changes have been made you will download them with this command.
   This comes in handy because you might be working on different computers, or maybe you are not the only person working on this repo.
   In order to pull, you need to add and commit all modified files prior to making a pull request (It ensures your changes will not be deleted).

3) When you wish to start updating your repository, adding files is done prior to making what we call git commit.
   If you accidentally added a file you did not wish to push, then simply use git rm <filename>.

   Example:
   git add mastermind.fsx ||
   git rm  mastermind.fsx

4) Committing is a way to keep a track record of the overall changes you made during editting,
   and it is adviced to commit frequently when things work.
   The only one you really need before becoming a git master is "-m" which indicates you are committing files with an attached message.
   Once we have committed, we can both pull the repository to fix potential merges.
   And then we are ready to push the changes.

   Example:
   git commit -m "We implemented mastermind I/O in mastermind.fsx"

5) This pushes your commit to the repository, and you can see the updates instantly when you made the push request.
   Once this is done, it allows other or yourself to download the most recently update version on another machine.
   
   