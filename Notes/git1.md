~/.ssh/config

Host 10.168.0.129

 Hostname 10.168.0.129

 IdentityFile ~/.mykeys/gitkey


-------------

git config http.sslVerify false

-----------

GIT_SSH_COMMAND="ssh -i ~/.ssh/id_rsa_example" git clone xxxxxx

----------------

git config core.sshCommand "ssh -i ~/.mykeys/gitkey -F /dev/null"

-------

  git config --global user.email "cccccc"

  git config --global user.name "cccccc"

--------
https://stackoverflow.com/questions/4565700/how-to-specify-the-private-ssh-key-to-use-when-executing-shell-command-on-git


---------------

git config

[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
	sshCommand = ssh -i ~/.ssh/KEYS -F /dev/null
[remote "origin"]
	url = ssh://git@DOMAIN:SSH_PORT/GIT_USER/GIT_REPO.git
	fetch = +refs/heads/*:refs/remotes/origin/*
	url = git@github.com:GIT_USER/GIT_REPO.git
[pull]
	rebase = false
[branch "main"]
	remote = origin
	merge = refs/heads/main
