# Git - First Commands

`> git init`  

Command to initialize your git local repository. This command must be issued on the repo path.

`> git status`  

Show the status of your current repository and watched files.

Example output:

On branch master

    No commits yet

    Untracked files: (use "git add <file>..." to include in what will be committed)
                testfile.txt

    nothing added to commit but untracked files present (use "git add" to track)

`> git remote add origin <repo-address>`  
You may choose one of the two connection modes to Git repository (https or SSH).

- This will associate the directory to the repository.

> git remote add origin git@github.ibm.com:CIO-Q2C-GI-IP-Software-MQ/ansible.git

> git remote -v
    origin  https://github.ibm.com/CIO-Q2C-GI-IP-Software-MQ/ansible.git (fetch)
    origin  https://github.ibm.com/CIO-Q2C-GI-IP-Software-MQ/ansible.git (push)

> git add .
    - Will add all files to the staging phase, from the current path to below.

> git commit -m "inital commit"
    - Move files from staging status to commit, already updating the repository.

        Example output:

        [master (root-commit) 6e2ff19] inital commit
         1 file changed, 0 insertions(+), 0 deletions(-)
         create mode 100644 qqcoisa.txt

> git status
    - Check current git status.

        Example output:

        On branch master
        nothing to commit, working tree clean

`> git log`  

Show commit logs and further details.
Example output:

        commit 6e2ff193ba15cd38dd0a8fdefb383b2a6b643087 (HEAD -> master)
        Author: Alexandre Kazuo Sato <aksato@br.ibm.com>
        Date:   Thu Oct 1 17:15:16 2020 -0300

            inital commit

`> git push origin master`  

Push all commited files to Master (repository).

Example output:

        remote: Password authentication is not available for Git operations.
        remote: You must use a personal access token or SSH key.
        remote: See https://github.ibm.com/settings/tokens or https://github.ibm.com/settings/ssh
        fatal: unable to access 'https://github.ibm.com/CIO-Q2C-GI-IP-Software-MQ/ansible.git/': The requested URL returned error: 403
        aksato@aksato-2 ansible % git push origin master
        remote: Anonymous access denied
        fatal: Authentication failed for 'https://github.ibm.com/CIO-Q2C-GI-IP-Software-MQ/ansible.git/'

        Example output 2:

        The authenticity of host 'github.ibm.com (169.60.70.162)' can't be established.
        ECDSA key fingerprint is SHA256:ZkDIk3kbswojRjqiSBsXS6xOHF+y+9nzcbZypokADKA.
        Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
        Warning: Permanently added 'github.ibm.com,169.60.70.162' (ECDSA) to the list of known hosts.
        Enumerating objects: 3, done.
        Counting objects: 100% (3/3), done.
        Writing objects: 100% (3/3), 223 bytes | 111.00 KiB/s, done.
        Total 3 (delta 0), reused 0 (delta 0)
        remote: detect-secrets-stream (beta) ver=164-1ac7e673b9acf31ed1ba86a8422cf59cb8a848be FAQ: https://ibm.biz/detect-secrets-stream-faq
        remote:
        remote: Successfully send push metadata.
        remote: Push info collect pre-receive hook finished within 3 seconds.
        To github.ibm.com:CIO-Q2C-GI-IP-Software-MQ/ansible.git
         * [new branch]      master -> master



Desde o Release 2.9.0, o Git parou de permitir o merge automático de projetos que possuem
históricos Git diferentes. O erro `fatal: refusing to merge unrelated histories` geralmente
acontece quando você tenta fazer o git pull de um repositório remoto, mas o seu repositório
local possuí um histórico de commits, branches, etc, diferente do que está no repositório remoto.

Para permitir que o Git faça o merge de dois projetos com históricos diferentes, é só passar
o parâmetro `--allow-unrelated-histories` quando for fazer o pull, assim:

`> git pull origin master --allow-unrelated-histories`
