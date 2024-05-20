# genesys-git

1.	VERSION CONTROL
A version control system is used to track modifications made to documents, software, big websites, and other information collections. It's especially important in software development, where several individuals work together on the same codebase.

In summary, version control is a vital tool that helps to manage project changes, facilitates teamwork, preserves a thorough record of work, and makes sure a project may grow effectively and seamlessly over time.
2.	THE DIFFERENCE BETWEEN GIT AND GITHUB
When it comes to software development and version control, Git and GitHub are closely connected, yet they have different uses. 

o	Git is a distributed version control system made to work quickly and effectively on any size project, from tiny to massive; while 

o	GitHub is an online platform that offers a graphical user interface for version control and collaboration, in addition to hosting Git repositories.

THE KEY DIFFERENCES ARE THAT IN:
	Scope, while GitHub is a platform that offers additional collaborative tools and hosts Git repositories, Git is a version control technology.

	In operation, GitHub functions as an online cloud service, while Git runs locally on your computer.

	And in functionality, Git offers version control's essential features, whereas GitHub expands on them with social coding, project management, and collaboration capabilities.




3.	THREE OTHER GITHUB ALTERNATIVES
•	GitLab
•	Bitbucket
•	SourceForge

4.	THE DIFFERENCE BETWEEN GIT FETCH AND GIT PULL
Introduction:	You may update your local repository with changes from a remote repository using the commands git fetch and git pull, although they accomplish distinct tasks and have different uses.

GIT FETCH

Definition:	Git fetch downloads files, references, and commits into your local repository from a remote repository. It does not, however, combine these modifications with your active files. 
Functionality:Obtains the most recent information from the remote repository. 
Updates the origin/main branch, one of your remote-tracking branches. 
Does not change the working directory or branch you are currently in.
Use Case:	When you wish to check the changes made in the remote repository before merging them into your local branch, use git fetch. You can inspect the modifications without having to make any changes to your working directory.

GIT PULL
Definition:	In essence, git pull is the result of combining two commands: git fetch and git merge. It attempts to merge changes into the current branch as soon as it retrieves them from a remote repository.
Functionality:Pulls the most recent information from the remote repository. 
Fetches the commits that were fetched into your current branch. 
If there are modifications that conflict between the remote branch and your local branch, it could lead to merge conflicts.
Use Case:	When you're ready to incorporate the modifications from the remote repository into your local branch, use git pull. Using this method, you can quickly apply the most recent changes from the remote repository to your local branch.

KEY DIFFERENCES:
Scope of Action:	Git fetch: Does not modify the working directory; it only updates the remote-tracking branches. 

Git pull: Merges changes to update the working directory and local branch.

Conflict Handling:	Git fetch: As no merging occurs, there is no chance of merge conflicts. 

Git pull: There may be merge conflicts that need to be resolved during the merging process.
Usefulness:	Git fetch: Perfect for checking changes and making sure you're up to date on all updates before merging. 

Git pull is a useful command for rapidly updating your branch with changes made in the remote branch.

NOTE:	Knowing these distinctions can help you select the right command depending on whether you want to update your local branch directly or examine changes first.

5.	EXPLANATION IN SIMPLE TERMS OF GIT REBASE AND THE COMMAND FOR IT
WHAT IS GIT REBASE?
Consider a project where several individuals are concurrently working on various features. These features may eventually deviate from the primary project branch (commonly referred to as main or master). You must synchronize your work with the most recent changes from the main branch when attempting to merge your modifications back into the main project. Here's when git rebase is useful.

SIMPLE EXPLANATION:

Consider git rebase as "moving" your modifications to the top of the most recent project modifications.

PROCESS:

	Your modifications are temporarily set aside by git rebase. 
	It upgrades your branch to reflect the target branch's (typically main) most recent state. 
	It then overlays this new state with your modifications once again.


NOTE:	This procedure produces a project history that is more linear and organized, making it potentially simpler to read and comprehend.

COMMAND FOR GIT REBASE:
Here’s how you use it in a simple scenario:
1.	Make sure you’re on your feature branch:

‘git checkout your-feature-branch’
2.	Rebase onto the main branch:
‘git rebase main’.
NOTE:	Maintaining a clear and structured project history through the use of git rebase makes it simpler for everyone to comprehend how the project has changed over time. 

6.	EXPLANATION IN SIMPLE TERMS GIT CHERRY-PICK AND THE COMMAND FOR IT.
WHAT IS GIT CHERRY-PICK?
Suppose you are working on a project and you make a specific change (a commit) in one branch and then you realize this change would also work well in another branch. To apply that particular commit to the other branch, use git cherry-pick rather than duplicating the changes by hand. It is analogous to plucking a cherry and planting it on another tree.
SIMPLE EXPLANATION:

1.	Cherry-picking is the process of applying a particular commit from one branch to another. 

2.	Procedure: 

•	Choose the commit that you wish to use. 
•	The commit can be applied to your current branch by using the git cherry-pick command.


GIT CHERRY-PICK COMMAND: 

Here's how to apply it in a straightforward example: 

      1.  Find the commit hash: Get the identifier (hash) of the commit you want to cherry-pick. This you can find by looking at the commit history using:

				‘git log’

The commit hash looks something like a1b2c3d4.


2.	Checkout the target brach: Switch to the branch where you want to apply the commit.

‘git checkout target-branch’


3.	Cherry-pick the commit:  Use the git cherry-pick command with the commit hash.

‘git cherry-pick a1b2c3d4’


