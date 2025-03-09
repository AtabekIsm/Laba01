┌──(root㉿kali)-[~]
└─#  export GITHUB_USERNAME=AtabekIsm           
                                                                             
┌──(root㉿kali)-[~]
└─# export GIST_TOKEN=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
                                                                             
┌──(root㉿kali)-[~]
└─# alias edit=nano              
                                                                             
┌──(root㉿kali)-[~]
└─# mkdir -p ${GITHUB_USERNAME}/workspace
                                                                             
┌──(root㉿kali)-[~]
└─# cd ${GITHUB_USERNAME}/workspace
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# pwd

/root/AtabekIsm/workspace
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# cd ..
                                                                             
┌──(root㉿kali)-[~/AtabekIsm]
└─# pwd
/root/AtabekIsm
                                                                             
┌──(root㉿kali)-[~/AtabekIsm]
└─# mkdir -p workspace/tasks/
                                                                             
┌──(root㉿kali)-[~/AtabekIsm]
└─# mkdir -p workspace/projects/
                                                                             
┌──(root㉿kali)-[~/AtabekIsm]
└─# mkdir -p workspace/reports/
                                                                             
┌──(root㉿kali)-[~/AtabekIsm]
└─# cd workspace
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2025-03-09 05:11:32--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Resolving nodejs.org (nodejs.org)... 104.20.22.46, 104.20.23.46, 2606:4700:10::6814:172e, ...
Connecting to nodejs.org (nodejs.org)|104.20.22.46|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9356460 (8.9M) [application/x-xz]
Saving to: ‘node-v6.11.5-linux-x64.tar.xz’

node-v6.11.5-linux- 100%[================>]   8.92M  17.6MB/s    in 0.5s    

2025-03-09 05:11:33 (17.6 MB/s) - ‘node-v6.11.5-linux-x64.tar.xz’ saved [9356460/9356460]

                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# tar -xf node-v6.11.5-linux-x64.tar.xz
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# rm -rf node-v6.11.5-linux-x64.tar.xz
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# mv node-v6.11.5-linux-x64 node
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# ls node/bin
node  npm
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/games:/usr/games
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# export PATH=${PATH}:`pwd`/node/bin
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/games:/usr/games:/root/AtabekIsm/workspace/node/bin
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# mkdir scripts
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# cat > scripts/activate<<EOF
heredoc> export PATH=\${PATH}:`pwd`/node/bin
heredoc> EOF
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# source scripts/activate
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# gem install gist
Fetching gist-6.0.0.gem
Successfully installed gist-6.0.0
Parsing documentation for gist-6.0.0
Installing ri documentation for gist-6.0.0
Done installing documentation for gist after 0 seconds
1 gem installed
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# export LAB_NUMBER=01
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Cloning into 'tasks/lab01'...
remote: Enumerating objects: 74, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 74 (delta 0), reused 1 (delta 0), pack-reused 71 (from 1)
Receiving objects: 100% (74/74), 945.07 KiB | 1.73 MiB/s, done.
Resolving deltas: 100% (20/20), done.
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# mkdir reports/lab${LAB_NUMBER}
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace]
└─# cd reports/lab${LAB_NUMBER}

┌──(root㉿kali)-[~/AtabekIsm/workspace/reports/lab01]
└─# edit REPORT.md

zsh: suspended  edit REPORT.md
                                                                             
┌──(root㉿kali)-[~/AtabekIsm/workspace/reports/lab01]
└─# gist REPORT.md
https://gist.github.com/AtabekIsm/7b11ffed33a8bf548b867af2bc48743f
