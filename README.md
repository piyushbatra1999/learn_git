# Demo

Repo for the seminar I conducted to teach git and GitHub.

## Installation

For windows download from [here](https://gitforwindows.org/).

For MacOs use this [link](https://sourceforge.net/projects/git-osx-installer/files/).

For Ubuntu:
```bash
sudo apt-get install git
```
Configure your name and email address
```bash
git config --global user.name "Name"
```
```bash
git config --global user.email "email@example.com"
```
To generate ssh for authentication:

```bash
#Create an ssh key
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
#change the key name if you want to
# Add a paraphrase if you want to
```
Execute the command below then copy the public ssh key and paste it into your GitHub account under Settings>SSH and GPG keys.

```bash
cat ~/.ssh/id_rsa.pub
```


In your local machine, check if the ssh-agent is running by executing:
```bash
eval "$(ssh-agent -s)"
```
Add ssh key to local ssh agent:
```bash
ssh-add ~/.ssh/id_rsa
```
Done.

# Basics

- clone
- add
- commit
- status
- reset
- revert
- checkout
- push
- pull
- diff
- merge (to demonstrate: master and features)

# Workflow
- master (main branch to merge all the features and issues)
  - feature branches
- qa ( perform tests before merge into staging)
- prod (Real production workload)
  - hotfixes ( quick fixes on production code)
- staging ( - duplicate of prod for blue/green deployment)
