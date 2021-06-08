

https://tupleblog.github.io/use-git-part1/

pi@raspberrypi:~ $ pwd
/home/pi
pi@raspberrypi:~ $ cd home
bash: cd: home: No such file or directory
pi@raspberrypi:~ $ ls
 Adafruit_Python_GPIO   Downloads   Public                            Videos
 Bookshelf              git         Templates
 Desktop                Music      'udo systemctl enable mosquitto'
 Documents              Pictures    venv
pi@raspberrypi:~ $ cd Ducuments
bash: cd: Ducuments: No such file or directory
pi@raspberrypi:~ $ cd Documents 
pi@raspberrypi:~/Documents $ cd .. && pwd
/home/pi
pi@raspberrypi:~ $ pwd
/home/pi
pi@raspberrypi:~ $ ^C
pi@raspberrypi:~ $ cd Documents
pi@raspberrypi:~/Documents $ ls
GitHub  GitSync
pi@raspberrypi:~/Documents $ cd GitHub
pi@raspberrypi:~/Documents/GitHub $ mkdir Project-MicroSmart
pi@raspberrypi:~/Documents/GitHub $ cd Project-MicroSmart
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ touch readme.md
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ ls
readme.md
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ cd ..
pi@raspberrypi:~/Documents/GitHub $ git clone https://github.com/GridsRasPi/Project-MicroSmart.git
fatal: destination path 'Project-MicroSmart' already exists and is not an empty directory.
pi@raspberrypi:~/Documents/GitHub $ git clone https://github.com/GridsRasPi/Project-MicroSmart.git
Cloning into 'Project-MicroSmart'...
remote: Enumerating objects: 17, done.
remote: Counting objects: 100% (17/17), done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 17 (delta 1), reused 6 (delta 0), pack-reused 0
Unpacking objects: 100% (17/17), done.
pi@raspberrypi:~/Documents/GitHub $ cd Project-MicroSmart
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ git init
Reinitialized existing Git repository in /home/pi/Documents/GitHub/Project-MicroSmart/.git/
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ ls
circleci  README.md
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ ls -a
.  ..  circleci  .git  .github  README.md
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ git remote -v
origin	https://github.com/GridsRasPi/Project-MicroSmart.git (fetch)
origin	https://github.com/GridsRasPi/Project-MicroSmart.git (push)
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ git add .
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ git commit -m "initial commit"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ git log
commit 6e9af85d0eb74e71381b1e12b0499904bdde7ad1 (HEAD -> main, origin/main, origin/HEAD)
Author: Grids Jivapong <69285464+GridsMicro@users.noreply.github.com>
Date:   Fri Jun 4 16:10:12 2021 +0700

    Create blank.yml

commit 0f0482e631415c368d6918fe2dafb3d922a2e3df
Author: GridsDev <Grids@microtronic.biz>
Date:   Fri Jun 4 15:53:10 2021 +0700

    Create config.yml

commit cfe6ce95d2b226623eb6cd80906535dd3bec8434
Author: GridsDev <Grids@microtronic.biz>
Date:   Fri Jun 4 15:52:34 2021 +0700

    edit by windows pc

commit 24ac7a704c989193c8b9799f6bdfe84ad1326e2b
Author: Grids Jivapong <69285464+GridsMicro@users.noreply.github.com>
Date:   Fri Jun 4 15:47:54 2021 +0700

pi@raspberrypi:~/Documents/GitHub/Project-MicroSmart $ 
