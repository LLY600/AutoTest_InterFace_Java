Administrator@SC-201810141340 MINGW64 /e
$ mkdir muke


Administrator@SC-201810141340 MINGW64 /e
$ cd muke/


Administrator@SC-201810141340 MINGW64 /e/muke
$ git init
Initialized empty Git repository in E:/muke/.git/


Administrator@SC-201810141340 MINGW64 /e/muke (master)
$ git clone git@github.com:LLY600/AutoTest_InterFace_Java.git
Cloning into 'AutoTest_InterFace_Java'...
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.
Please make sure you have the correct access rights
and the repository exists.


Administrator@SC-201810141340 MINGW64 /e/muke (master)
$ ssh-keygen -t rsa -C '18380430509@163.com'
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/Administrator/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/Administrator/.ssh/id_rsa.
Your public key has been saved in /c/Users/Administrator/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:aV7EJghphMUJajcv59IhP9CU1FWOC1vMxQZ13ZkKj00 18380430509@163.com
The key's randomart image is:
+---[RSA 2048]----+
|  .*++. .o=+ .. +|
| .. *..oo.++.E +.|
|.. + o...==.* .  |
|. . =   +=.. +   |
|   + = .S..      |
|    O .o .       |
|   . =  .        |
|    . .          |
|                 |
+----[SHA256]-----+

Administrator@SC-201810141340 MINGW64 /e/muke (master)
$ git clone git@github.com:LLY600/AutoTest_InterFace_Java.git
Cloning into 'AutoTest_InterFace_Java'...
Warning: Permanently added the RSA host key for IP address '52.74.223.119' to the list of known hosts.
warning: You appear to have cloned an empty repository.

Administrator@SC-201810141340 MINGW64 /e/muke (master)
$ cd AutoTest_InterFace_Java/


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ vim test.txt

Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ cat test.txt
test

Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        test.txt

nothing added to commit but untracked files present (use "git add" to track)



Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git add test.txt
warning: LF will be replaced by CRLF in test.txt.
The file will have its original line endings in your working directory

Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   test.txt


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git commit -m "增加测试文件"
[master (root-commit) 5d71790] 增加测试文件
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt



Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git push
Warning: Permanently added the RSA host key for IP address '13.229.188.59' to the list of known hosts.
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 232 bytes | 46.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:LLY600/AutoTest_InterFace_Java.git
 * [new branch]      master -> master


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git pull
Already up to date.


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git branch
* master


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git branch -a
* master
  remotes/origin/master


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git checkout -b localbranch
Switched to a new branch 'localbranch'

Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git branch
* localbranch
  master


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$  git status
On branch localbranch
nothing to commit, working tree clean

Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ vim test.txt

Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ cat test.txt
test
add comtent



Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git add test.txt


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git commit -m "增加add comtent"
[localbranch efc9c24] 增加add comtent
 1 file changed, 3 insertions(+)


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git push
fatal: The current branch localbranch has no upstream branch.
To push the current branch and set the remote as upstream, use
    git push --set-upstream origin localbranch


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git push --set-upstream origin localbranch
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 265 bytes | 66.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'localbranch' on GitHub by visiting:
remote:      https://github.com/LLY600/AutoTest_InterFace_Java/pull/new/localbranch
remote:
To github.com:LLY600/AutoTest_InterFace_Java.git
 * [new branch]      localbranch -> localbranch
Branch 'localbranch' set up to track remote branch 'localbranch' from 'origin'.


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git status
On branch localbranch
Your branch is up to date with 'origin/localbranch'.
nothing to commit, working tree clean


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git branch
* localbranch
  master

Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git branch -a
* localbranch
  master
  remotes/origin/localbranch
  remotes/origin/master


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git checkout master
FETCH_HEAD           master               origin/master
HEAD                 ORIG_HEAD
localbranch          origin/localbranch

Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (localbranch)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git branch -d localbranch
warning: deleting branch 'localbranch' that has been merged to
         'refs/remotes/origin/localbranch', but not yet merged to HEAD.
Deleted branch localbranch (was efc9c24).


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git branch
* master


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git branch -a
* master
  remotes/origin/localbranch
  remotes/origin/master



Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git branch -r -d origin/localbranch
Deleted remote-tracking branch origin/localbranch (was efc9c24).


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git branch -a
* master
  remotes/origin/master


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git push origin:localbranch
ssh: Could not resolve hostname origin: Name or service not known
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.


Administrator@SC-201810141340 MINGW64 /e/muke/AutoTest_InterFace_Java (master)
$ git push origin :localbranch
To github.com:LLY600/AutoTest_InterFace_Java.git
 - [deleted]         localbranch
