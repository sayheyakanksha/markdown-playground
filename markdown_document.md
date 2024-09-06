# Getting started with Git Lab
## Instructions
In this lab, we'll be going through some basic tasks you'll need to do as you manage the GitHub repository for your CollectionBuilder site. The questions below are designed to help you learn and remember what you need to do to perform these tasks, as well as where you can go to look for help. 

## Creating your repository and editing files
**What did you click on to create a new repository in the web interface of Github (i.e., on Github.com)?**  
I clicked on the "New" button next to "Top repositories" on the [GitHub dashboard](https://github.com/) which took me to ["Create a new repository"](https://github.com/new) webpage.  

**What is the difference between a private and a public repository?**  
A *private repository* can only be seen and accessed by the person who created the repository and the people they invite to collaborate with. No one else can access it without any given permission. A *public repository* can be seen and copied by anyone on the internet, no matter who created it. We don't need any special permission to be able to access it. 

**Once your repository has been made and has at least one file, what button do you need to click on the web interface in order to create a new file in your repository?**  
On my main [markdown-playground](https://github.com/sayheyakanksha/markdown-playground) repository page, I clicked on the "Add file" button which opened a dropdown menu and then I selected "+ Create new file" option from that menu to create a new file in my repository. 

**Describe the steps you took to clone your repository on Github Desktop**  
I took the following steps to clone my repository on Github Desktop:
- *Step 1:* Opened GitHub Desktop application.
- *Step 2:* Signed in to my GitHub account.
- *Step 3:* In my GitHub Desktop app, I clicken on "File" and selected "Clone repository" option from the drop down menu.
- *Step 4:* In the "Clone a Repository" pop-up, I selected [markdown-playground](https://github.com/sayheyakanksha/markdown-playground) repository from the list of repositories shown under "Your Repositories" list. 
- *Step 5:* Made sure to choose the correct local path on my system.
- *Step 6:* Finally, clicked on "Clone" button to clone the repository. 

**What is the title of GitHub documentation?**  
The title of GitHub documentation is **[GitHub Docs](https://docs.github.com/en)**.

**What is the URL for GitHub documentation on creating your first repository?**  
This is the URL for GitHub documentation on creating your first repository: https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository.

**Where is your local repository versus the remote repository?**  
The *local repository* is stored on our local machines, where we make changes to the files directly. If we are cloning a repository from somewhere else, it won't affect the data on that unless we push it back to that main repository. The *remote repository* is hosted on GitHub's servers (or another version control server). It provides an option for people to sync their data remotely. Overall, we can communicate with both the respositories by pushing and pulling changes between the two. 

**What happens when you fetch?**  
When we fetch the origin, we retrieve the latest commits and changes from the remote repository to our local repository to see what all changes have been made, but it doesn't automatically merge them into our working directory. It updates the information without modifying our own files.

**What happens when you pull changes/commits?**  
When we pull, we fetch changes from the remote repository and then merge them into our current branch in the local repository. It is a bit more of an aggressive way to merge changes to our current respository. The safest way would be to fetch all the changes first, compare everything then we can safely pull changes/commits accordingly. 

**When working on GitHub Desktop, what order should you generally perform push, pull, and fetch?**  
The general order is:
1. We fetch to see if there are any changes/updates on the origin. 
2. We then pull to get those changes/updates and merge them into our local repository.
3. We should then push to send our commits to the remote repository, in case we make any changes.

**What happens when you push commits from your local repository?**  
When we push commits from our local repository, we upload all the changes/updates from our local branch to the origin/corresponding branch in the remote repository, making them available to other collaborators depending on who the repository is shared with.

**What is the URL for the Github glossary?**  
This is the URL for the GitHub glossary: https://docs.github.com/en/get-started/quickstart/github-glossary.

**Where can you find a list of your commits?**  
We can go to our main repository page on Github.com and click on the "Commits" button on the right side, which also shows the number of commits made next to it. It then opens up a page which shows us the entire commits' history. We can also click on a branch name separetly to view its commits history/all activity.

Github desktop client also has a separate section called "History" which shows us a list of all our commits. 

**What is the URL for documentation on reverting a commit?**  
This is the URL for documentation on reverting a commit: https://docs.github.com/en/desktop/managing-commits/reverting-a-commit-in-github-desktop.

**How do you revert a commit?**  
We can follow these steps to revert a commit: 
1. *Step 1:* Click on "History" on Github Desktop.
2. *Step 2:* Right-click on the commit that we want to revert. 
3. *Step 3:* From the dropdown menu, we can select "Revert Changes in Commit".

## Git-flavored markdown
**What is the name of the page or URL in GitHub documentation where there's information on how to format your Markdown for GitHub?**  
This is the name of the page: **[Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#GitHub-flavored-markdown)**.  

**What precedes a second-level heading in Github markdown?**  
Two hash symbols (##).

**How do you indicate text that has been struckthrough?**  
To indicate text that has been struckthrough in markdown, we need to wrap the text in double tilde symbols (~~).  
For example:  
~~This is a struckthrough text.~~

**How do you create a hyperlink in your markdown?**  
To create a hyperlink in markdown, we need to wrap the text in square brackets and add the URL in small brackets() after the link text.  
For example:  
[This is a hyperlink. Click on it!](https://github.com)

**How do you link to a section in the same or another markdown file?**  
To link to a section in the same file, we need to use the # hashtag symbol followed by the section heading in lowercase with dashes instead of spaces (if multi-word).    
For example:   
[This is an anchor link for *heading 1* on this page](#getting-started-with-git-lab). 

To link to a section in another markdown file, we need to write the file's name in URL field (./filename.md) followed by the section heading in lowercase with dashes instead of spaces (if multi-word).  
For example:   
[This is an anchor link for *heading 4* on the markdown_exercise page in my repository](./markdown_exercise.md#level-4-(h4)-heading).

**What are the three possible symbols for indicating an unordered list?**  
The three possible symbols for indicating an unordered list in Markdown are:  - (hyphen), * (asterisk), + (plus sign)

For example:   
Unordered list using hyphen symbol: 
- Resident Evil 1
- Resident Evil 2
- Resident Evil 3

Unordered list using asterisk symbol:  
* The Last of Us Part I
* The Last of Us Part II

Unordered list using plus sign:  
+ Dark Souls I
+ Dark Souls II
+ Dark Souls III

**Format the following text into a footnote:**  
Main text: Alex Wingate went to William and Mary.(place footnote here)  
Footnote text: William and Mary is a university in Williamsburg, VA founded in 1693.  
Bonus: make "William and Mary" a hyperlink to W&M's website.   

**Footnote example:** 

Alex Wingate went to William and Mary.[^1]
[^1]: [William and Mary](https://www.wm.edu/) is a university in Williamsburg, VA founded in 1693.
