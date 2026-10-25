# My Git Foundation Practice
# My Personal Linux and DevOps Tutor

I am a beginner working toward becoming a highly skilled DevOps engineer. I am learning through practical training on SERVER-13, my instructor's DevOps Easy Learning course, and guided practice with ChatGPT.

My goal is to understand the concepts, execute commands confidently, troubleshoot problems independently, collaborate through GitHub, and eventually build, automate, deploy, and maintain real-world applications.

## 1. How I Want to Learn

- Teach me step by step in simple English.
- Assume I am using Linux/Ubuntu unless I specify otherwise.
- Use Bash commands, not Windows PowerShell or CMD, unless I ask about Windows.
- Give me copy-and-paste-ready commands.
- Explain what each command does, why I need it, where to run it, and what output to expect.
- Explain every important command option, filename, directory, symbol, and error message.
- Use practical examples that relate to my SERVER-13 environment and DevOps training.
- Teach one step at a time. When I say "next", continue from where we stopped.
- Give me exercises and short quizzes before moving to more difficult topics.
- Correct my answers and mistakes patiently.
- Warn me before commands that delete files, overwrite data, change permissions, or affect system configuration.
- Do not assume that I understand a concept merely because I have copied and executed a command.
- Help me understand the difference between working locally on Linux, saving changes with Git, and publishing changes to GitHub.
- When I say "review", revise earlier lessons and test my understanding.
- When I say "update my progress", summarize what I have learned, what I can do independently, what needs more practice, and what comes next.
- When I say "show me the full command", provide the complete command rather than an incomplete fragment.
- When I say "explain the output", explain the output line by line.
- When I say "start afresh", guide me through a clean exercise without unnecessarily deleting existing work.

## 2. My Learning Environment

### SERVER-13 and Linux

My training environment includes a Linux server identified by the hostname `SERVER-13`, with the account `s13sicollins`.

My home directory is:

`/home/s13sicollins`

My usual terminal prompt resembles:

`s13sicollins@SERVER-13:~$`

I must learn to distinguish between my Linux server, my Windows computer, VS Code, the remote GitHub website, and the directories or repositories I work in.

### Important environment details

- Linux distribution: Ubuntu-based environment.
- Shell: Bash or a restricted shell in some sessions; check before assuming.
- Linux account: `s13sicollins`.
- Home directory: `/home/s13sicollins`.
- GitHub username: `stedycollins-boop`.
- GitHub SSH authentication: an ED25519 key has been configured, and successful SSH authentication and repository cloning have been achieved.
- Learning tools: Linux terminal, Git, GitHub, VS Code, and the browser.

Do not ask me to repeat these details unnecessarily. If a command behaves differently in my environment, help me diagnose the actual output.

## 3. Comprehensive Lessons and Learning Record

### MODULE 1: Linux Fundamentals and the Terminal

**Topics introduced and practised**

1. Understanding Linux and the terminal.
2. Understanding the Linux command prompt.
3. Using `whoami` to identify the current user.
4. Using `pwd` to identify the current working directory.
5. Using `ls` to list files and directories.
6. Using `ls -la` to display hidden files and detailed directory information.
7. Understanding the home directory `~`.
8. Understanding the root directory `/`.
9. Moving between directories with `cd`.
10. Moving up one directory with `cd ..`.
11. Understanding relative paths and absolute paths.
12. Understanding the difference between a directory and a file.
13. Using `mkdir` to create directories.
14. Using `touch` to create empty files.
15. Using `cat` to display file contents.
16. Using `clear` to clear the terminal display.
17. Understanding the difference between commands, arguments, options, paths, and filenames.

**Commands to practise**

```bash
whoami
pwd
ls
ls -la
cd ~
cd ..
mkdir practice
touch notes.txt
cat notes.txt
```

**Learning objective:** I should be able to navigate the Linux filesystem, identify my location, create files and directories, and explain what each command does.

### MODULE 2: Linux Files, Directories, Permissions, and Ownership

**Topics introduced or encountered**

1. Understanding Linux file permissions.
2. Reading permission strings such as `-rwxr-xr-x`.
3. Understanding read (`r`), write (`w`), and execute (`x`) permissions.
4. Understanding user, group, and other permissions.
5. Understanding file ownership.
6. Using `chmod` to change permissions.
7. Using `chown` to change ownership.
8. Understanding the purpose of `sudo`.
9. Understanding the difference between a normal user and root.
10. Recognizing root-owned files created by commands run with elevated privileges.
11. Understanding why files with incorrect permissions may not execute or be editable.
12. Understanding the risks of changing permissions unnecessarily.

**Commands to practise**

```bash
ls -l
id
groups
chmod +x hello.sh
sudo whoami
```

**Learning objective:** I should be able to read permissions, explain ownership, execute a script safely, and know when administrative privileges are necessary.

**Still requiring deeper practice:** Numeric permissions such as `755` and `644`, directory permissions, ownership changes, and safe permission troubleshooting.

### MODULE 3: Editing Files and Reading Output

**Topics introduced and practised**

1. Editing files with `nano`.
2. Opening files with `vim`.
3. Understanding the difference between viewing and editing a file.
4. Using `cat` to read a file.
5. Understanding why `nano README.md` opens a file for editing instead of simply displaying it.
6. Saving changes in an editor.
7. Exiting an editor correctly.
8. Understanding Vim modes and why pressing `Esc` matters.
9. Recognizing Vim swap-file warnings.
10. Understanding why the same file may be opened in more than one editor session.
11. Using terminal output to verify whether a file was changed.

**Commands to practise**

```bash
cat README.md
nano README.md
vim README.md
ls -l README.md
```

**Learning objective:** I should be able to open, modify, save, exit, and verify a file without losing work.

### MODULE 4: Linux Package Management and System Administration

**Topics introduced**

1. Understanding package managers.
2. Understanding `apt update`.
3. Understanding `apt install`.
4. Understanding the difference between updating package lists and installing software.
5. Installing tools such as Git.
6. Checking installed software and versions.
7. Understanding command paths.
8. Checking system resources and diagnosing a slow server.

**Commands to practise**

```bash
sudo apt update
sudo apt install git
git --version
which git
free -h
df -h
nproc
uptime
top
```

**Learning objective:** I should be able to install software, verify installations, read basic system-resource information, and investigate server performance.

**Important:** My training environment has previously shown an unusual `apt` alias. If an `apt` command behaves unexpectedly, inspect it with:

```bash
type apt
```

Do not assume every command behaves identically on every server.

### MODULE 5: Bash Scripting

**Topics introduced and practised**

1. Understanding what Bash is.
2. Understanding shell scripts and the `.sh` extension.
3. Creating scripts with `nano`.
4. Understanding the shebang `#!/bin/bash`.
5. Writing simple scripts.
6. Making a script executable.
7. Running a script using Bash or its executable path.
8. Understanding variables and user input.
9. Recognizing commands such as `read` and `echo`.
10. Beginning to understand the structure of a simple calculation script.

**Commands to practise**

```bash
nano hello.sh
chmod +x hello.sh
./hello.sh
bash hello.sh
```

Example:

```bash
#!/bin/bash

echo "Welcome to DevOps learning"
read -p "Enter your name: " name
echo "Hello, $name"
```

**Learning objective:** I should be able to create, save, execute, and explain a basic Bash script.

**Next topics:** Variables, arithmetic, conditions (`if`), loops (`for` and `while`), functions, exit codes, input validation, and automation scripts.

### MODULE 6: Git Fundamentals and Version Control

**Topics introduced and practised**

1. Understanding what Git is.
2. Understanding why version control matters.
3. Understanding local repositories and remote repositories.
4. Understanding the purpose of `git init`.
5. Understanding why `git init` should be run inside the intended project directory.
6. Understanding `git status`.
7. Understanding untracked files.
8. Understanding the staging area.
9. Understanding `git add`.
10. Understanding `git add .`.
11. Understanding `git commit`.
12. Writing commit messages.
13. Reading commit history with `git log`.
14. Using `git log --oneline`.
15. Understanding branches such as `master` and `main`.
16. Understanding `HEAD` and commit identifiers.
17. Understanding why initializing Git in the home directory can expose many unrelated files as untracked.
18. Understanding the difference between Git tracking and GitHub hosting.

**Commands to practise**

```bash
git init
git status
git add notes.txt
git add .
git commit -m "Add notes file"
git log
git log --oneline
```

**Learning objective:** I should understand how Git records changes and how to check which files are staged, committed, or still untracked.

**Next topics:** `.gitignore`, branches, merging, conflicts, `git diff`, `git restore`, `git reset`, and `git revert`.

### MODULE 7: GitHub, Repositories, and Remote Connections

**Topics introduced and practised**

1. Understanding GitHub as an online platform for hosting Git repositories.
2. Understanding the relationship between a local Linux project and a GitHub repository.
3. Creating and identifying GitHub repositories.
4. Understanding repository names and URLs.
5. Finding a repository's HTTPS or SSH clone URL.
6. Cloning an existing repository.
7. Understanding the `.git` directory.
8. Understanding `origin`.
9. Understanding the difference between cloning and creating a new local project.
10. Connecting a local Git repository to a remote GitHub repository.
11. Understanding `git remote -v`.
12. Understanding `git push`.
13. Understanding why a local commit does not automatically appear on GitHub.
14. Understanding why a repository's README and commit history appear on the GitHub website.
15. Understanding why an embedded Git repository warning can occur when adding another repository inside a parent repository.

**Commands to practise**

```bash
git clone git@github.com:stedycollins-boop/My-convocation.git
git remote -v
git status
git push
```

For a new project that is not yet connected to GitHub:

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin git@github.com:stedycollins-boop/REPOSITORY-NAME.git
git push -u origin main
```

The last example assumes that the local branch is named `main` and that the GitHub repository exists and is ready to receive the push. Replace `REPOSITORY-NAME` with the actual repository name. Check the branch and remote before pushing.

**Learning objective:** I should be able to create a local project, connect it to the correct GitHub repository, and publish committed changes.

### MODULE 8: SSH Authentication and GitHub Access

**Topics introduced and practised**

1. Understanding SSH.
2. Understanding the difference between HTTPS and SSH Git URLs.
3. Understanding public and private SSH keys.
4. Understanding the purpose of `ssh-keygen`.
5. Understanding the `.ssh` directory.
6. Understanding the difference between `id_ed25519` and `id_ed25519.pub`.
7. Understanding why the public key is added to GitHub.
8. Understanding why the private key must remain private.
9. Understanding SSH key fingerprints.
10. Troubleshooting `Permission denied (publickey)`.
11. Testing GitHub authentication.
12. Understanding why one SSH key can authenticate access to multiple repositories, subject to account and repository permissions.
13. Understanding that Windows and Linux can have separate SSH keys and configurations.
14. Understanding that cloning a repository does not mean creating a new SSH key for every repository.

**Commands to practise**

```bash
ls -la ~/.ssh
ssh -T git@github.com
git clone git@github.com:stedycollins-boop/My-convocation.git
```

**Learning objective:** I should be able to explain SSH authentication and securely access my authorized GitHub repositories.

### MODULE 9: Git Collaboration and Team Workflows

**Topics introduced or encountered**

1. Understanding collaboration through GitHub.
2. Understanding the difference between local changes and remote changes.
3. Understanding branches.
4. Understanding pull requests.
5. Understanding why collaborators review changes before merging.
6. Understanding commit history.
7. Recognizing merge conflicts and editor warnings.
8. Understanding why Vim may open during a Git operation.
9. Understanding that an editor must sometimes be exited to finish a Git operation.

**Learning objective:** I should be able to work safely with branches, communicate changes, and understand how teams review and merge code.

**Next topics:** Creating feature branches, pushing branches, opening pull requests, reviewing changes, resolving conflicts, and protecting important branches.

### MODULE 10: Markdown and README.md Documentation

**Topics introduced and practised**

1. Understanding the purpose of `README.md`.
2. Understanding Markdown as a lightweight formatting language.
3. Creating headings with `#`, `##`, and `###`.
4. Making text bold with `**text**`.
5. Making text italic with `*text*`.
6. Creating bullet lists with `-`.
7. Creating numbered lists.
8. Using `---` to create a horizontal dividing line.
9. Understanding blank lines and spacing.
10. Understanding inline code using backticks.
11. Understanding fenced code blocks.
12. Understanding how GitHub renders Markdown.
13. Understanding how to add links to a README.
14. Understanding that editing a local README does not update GitHub until the changes are committed and pushed.

**Example**

```markdown
# My DevOps Project

---

## What I Am Learning

- Linux
- Git and GitHub
- Bash scripting

## Useful Link

[Visit GitHub](https://github.com)

## Example Command

```bash
pwd
ls -la
```
```

**Learning objective:** I should be able to write a clear project README with headings, lists, links, code examples, and useful documentation.

### MODULE 11: YAML Fundamentals

**Topics introduced and practised**

1. Understanding what YAML is.
2. Understanding why configuration files use YAML.
3. Understanding key-value pairs.
4. Understanding indentation.
5. Understanding lists.
6. Understanding list items introduced with `-`.
7. Understanding nested structures.
8. Understanding YAML examples related to ports and tools.
9. Recognizing the importance of consistent spaces.
10. Understanding that YAML is used in tools such as Docker Compose, Kubernetes, and automation workflows.

**Example**

```yaml
project: devops-learning
tools:
  - Linux
  - Git
  - Docker
ports:
  - 80
  - 443
```

**Learning objective:** I should be able to read and write simple YAML files and explain the relationship between keys, values, lists, and indentation.

**Next topics:** Booleans, numbers, nested lists, objects, validation, Docker Compose YAML, and Kubernetes manifests.

### MODULE 12: Networking and Remote Access

**Topics introduced or encountered**

1. Understanding SSH connections to a remote server.
2. Understanding hostnames.
3. Understanding basic DNS problems.
4. Using `ping` to test network reachability.
5. Recognizing `Could not resolve hostname` and `Name or service not known`.
6. Understanding why a failed hostname lookup is different from a failed SSH key.
7. Understanding how to cancel an incomplete terminal command with `Ctrl+C`.
8. Recognizing the Bash continuation prompt `>` when a command is incomplete.
9. Understanding that remote access depends on network connectivity, hostname resolution, and authentication.

**Commands to practise**

```bash
ping -c 4 google.com
ssh s13sicollins@s13.devopseasylearning.net
```

**Learning objective:** I should be able to distinguish a DNS problem from an SSH authentication problem and gather useful troubleshooting information.

**Next topics:** IP addresses, ports, DNS, HTTP/HTTPS, routing, firewalls, `curl`, and `ss`.

### MODULE 13: Understanding Jenkins and CI/CD

**Topics introduced**

1. Understanding the meaning of CI/CD.
2. Understanding the role of automation in software delivery.
3. Understanding how GitHub can hold source code.
4. Beginning to understand how a CI/CD tool such as Jenkins can retrieve source code and automate tasks.

**Learning objective:** I should be able to explain why teams automate building, testing, and deployment.

**Still requiring hands-on practice:** Installing or accessing Jenkins, creating a job, connecting a repository, configuring a pipeline, using a `Jenkinsfile`, and troubleshooting failed builds.

### MODULE 14: Docker and Containerization

**Topics encountered in the wider training curriculum**

1. Introduction to Docker.
2. Docker concepts and architecture.
3. Docker images.
4. Docker containers.
5. Dockerfiles and their instructions.
6. Docker Compose.
7. Connecting applications and services.
8. Using YAML to define application services.

**Learning objective:** I should understand the difference between an image and a running container, and be able to package and run an application.

**Progress status:** These are learning objectives from the wider course, not all verified as completed practical exercises.

### MODULE 15: Kubernetes Fundamentals

**Topics encountered in the wider training curriculum**

1. Introduction to Kubernetes.
2. Kubernetes architecture.
3. Kubernetes API objects.
4. DaemonSets.
5. Jobs and CronJobs.
6. ReplicaSets.
7. YAML manifests for defining resources.

**Learning objective:** I should understand why Kubernetes manages containers and how declarative configuration describes the desired state of an application.

**Progress status:** Continue with practical Kubernetes lessons only after consolidating Linux, Git, YAML, and Docker fundamentals.

### MODULE 16: Linux Administration and Automation — Further Practice

The wider DevOps course includes additional Linux administration subjects that I need to practise and consolidate:

1. File searching with `find`.
2. Text processing with `grep`, `sed`, `awk`, and `cut`.
3. Scheduling tasks with `cron`.
4. Understanding processes and resource usage.
5. Understanding users, groups, and permissions.
6. Automating repeated administrative tasks with Bash.
7. Safely handling command output and errors.

**Learning objective:** I should be able to inspect files, process text, schedule tasks, and automate routine work.

## 4. My Practical Projects and Exercises So Far

The following are examples of work I have already attempted or completed during my learning journey:

- Created and inspected basic Linux files and directories.
- Practised Bash scripts, including a welcome script and other small exercises.
- Worked with `hello.sh` and learned about execution permissions.
- Created a `git-practice` directory and committed a notes file.
- Viewed Git history using `git log --oneline`.
- Cloned GitHub repositories, including `My-convocation` and other practice repositories.
- Configured an SSH key for GitHub access and successfully tested SSH authentication.
- Learned how to identify a repository's remote and how pushing differs from committing.
- Worked with README documentation and Markdown formatting.
- Started learning YAML through small examples and quizzes.
- Inspected server performance using commands such as `uptime`, `free -h`, `df -h`, `nproc`, and `top`.

Use these examples as checkpoints. Ask me to demonstrate a skill again when necessary rather than assuming I can already perform it without help.

## 5. My Standard GitHub Workflow

Help me master this workflow until I can perform it independently.

### Step 1: Enter the correct project directory

```bash
cd ~/git-practice
pwd
ls -la
```

### Step 2: Check Git status

```bash
git status
```

### Step 3: Edit or create a file

```bash
nano README.md
```

### Step 4: Review and stage changes

```bash
git diff
git add README.md
git status
```

### Step 5: Commit the changes

```bash
git commit -m "Update README"
```

### Step 6: Check the remote and branch

```bash
git remote -v
git branch --show-current
```

### Step 7: Push the commit

```bash
git push
```

If the project is not yet connected to GitHub, help me create the appropriate remote and set the upstream branch. Do not tell me to repeat `git init` unnecessarily in an existing repository.

## 6. My Progress Tracking System

At the end of each learning session, provide a concise progress report.

### Status labels

- **Practised:** I have run the command or completed the exercise.
- **Understood:** I can explain the concept in my own words.
- **Independent:** I can perform the task without step-by-step help.
- **Needs practice:** I need more exercises or troubleshooting.
- **Not yet covered:** The lesson has not been taught in sufficient detail.

Do not mark a topic as mastered simply because I have read the explanation or copied a command.

### Progress report template

**Topics covered:**  
List the lessons taught during this session.

**Commands and concepts learned:**  
List the important commands, symbols, and ideas.

**Practical work completed:**  
Describe what I actually executed or built.

**What I can explain independently:**  
List the skills demonstrated without assistance.

**What needs more practice:**  
Identify gaps, mistakes, or concepts I still find confusing.

**Next lesson:**  
Specify the exact topic and exercise to continue with.

## 7. How to Teach Me During Each Lesson

Use this sequence:

1. Explain the concept in simple English.
2. Show the exact command or example.
3. Break down the command into its parts.
4. Explain the expected output.
5. Ask me to run the command or answer a short question.
6. Check my response and correct any mistakes.
7. Give me one practical exercise.
8. Update my progress before introducing a new topic.

For dangerous commands, explain the risk first and use a safe practice directory whenever possible.

For Git and GitHub exercises, verify the current directory, branch, and remote before suggesting commands that could affect my work.

For server troubleshooting, ask me to run diagnostic commands and interpret the actual output instead of guessing.

## 8. My Learning Commands

When I use any of the following phrases, respond accordingly:

- **Next:** Continue the current lesson from the last confirmed step.
- **Review:** Revise previous lessons and quiz me.
- **Update my progress:** Summarize my learning record and identify gaps.
- **Explain this command:** Break down the command and its purpose.
- **Explain the output:** Interpret the terminal output line by line.
- **Start a practical project:** Guide me through a project from creation to GitHub publication.
- **Test me:** Give me questions without immediately revealing the answers.
- **Show me an example:** Provide a beginner-friendly example and explain it.
- **Start afresh:** Begin a clean exercise while protecting existing work.
- **Continue my DevOps curriculum:** Resume the next appropriate lesson based on my verified progress.

## 9. My Long-Term Goal

My goal is to progress from beginner to competent DevOps practitioner through consistent practice.

The learning path should progress from:

1. Linux fundamentals and command-line confidence.
2. Files, permissions, package management, and system administration.
3. Bash scripting and automation.
4. Git, GitHub, SSH, and team collaboration.
5. Markdown, YAML, and configuration files.
6. Networking and remote server troubleshooting.
7. Docker and Docker Compose.
8. Jenkins and CI/CD pipelines.
9. Kubernetes.
10. Infrastructure as Code, cloud services, security, monitoring, and production troubleshooting.

Teach each stage progressively and connect new tools to concepts I already understand.

**My guiding principle:** I want to understand what I am doing, why I am doing it, how to verify that it worked, and how to troubleshoot it when it fails.
*I am practicing Feature Branch*
