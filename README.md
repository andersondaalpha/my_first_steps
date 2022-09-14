https://github.com/andersondaalpha/my_first_steps.git
Cliquei com botão direito na pasta do meu computador e cliquei em Git bash, então o programa já abriu no diretório em questão.
Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial
$ git init
Initialized empty Git repository in I:/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial/.git/

Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git remote add orig https://github.com/andersondaalpha/my_first_steps.git

Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git remote -v
orig    https://github.com/andersondaalpha/my_first_steps.git (fetch)
orig    https://github.com/andersondaalpha/my_first_steps.git (push)

Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git add ola_mundo.txt


Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git commit -n "Primeiro arquivo"
error: pathspec 'Primeiro arquivo' did not match any file(s) known to git

Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git commit -m "Primeiro arquivo"
[master (root-commit) b1481f0] Primeiro arquivo
 1 file changed, 4 insertions(+)
 create mode 100644 ola_mundo.txt

Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git push orig master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 347 bytes | 8.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/andersondaalpha/my_first_steps.git
 * [new branch]      master -> master

Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ cat >".gitignore"
serei_ignorado.txt

Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git add .gitignore

Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git commit -m "Adicionando arquivo que ignora outros arquivos"
[master e59b32e] Adicionando arquivo que ignora outros arquivos
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore

Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git push
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream orig master

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Anderson@DESKTOP-6PS65PD MINGW64 /i/Meu Drive/Estudo/Alpha/Aula 6/Git_inicial (master)
$ git push --set-upstream orig master
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 329 bytes | 10.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/andersondaalpha/my_first_steps.git
   b1481f0..e59b32e  master -> master
branch 'master' set up to track 'orig/master'.