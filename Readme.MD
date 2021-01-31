IF you have problem error like this one :

E: The repository 'http://apt.postgresql.org/pub/repos/apt ulyssa-pgdg Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.

Change on /etc/apt/sources.list.d/pgdg.list 

deb http://apt.postgresql.org/pub/repos/apt ulyssa-pgdg main

to be like this :
deb http://apt.postgresql.org/pub/repos/apt focal-pgdg main

*note focal fossa is ubuntu 20.04 LTS
and Linux mint is based on from ubuntu 20.04 LTS 
i hope your understand :)

And then save, type : sudo apt update

And after update if you have problem :
N: Skipping acquire of configured file 'main/binary-i386/Packages' as repository 'http://apt.postgresql.org/pub/repos/apt focal-pgdg InRelease' doesn't support architecture 'i386'

Please Change on /etc/apt/sources.list.d/pgdg.list ,to be like this:

deb [arch=amd64] http://apt.postgresql.org/pub/repos/apt focal-pgdg main


typing again :
sudo apt update && sudo apt-get -y install postgresql







