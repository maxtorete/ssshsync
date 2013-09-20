ssshsync
========

Symfony SSH sync


This small script is intended to be used on SpartUp as a deploy automating tool on our first project alpha state. With it, you can deploy a Symphone application on an limited server (as a shared one like 1and1, etc.) with only one command, all you need is ssh access to the remote server and git, ssh and a mysql server on your workstation.

On each deploy, it will generate a new clean installation (be careful, because it will delete previous data if a database or directory with the same name exists) on your workstations from a git repository, and will upload and deploy it on the remote server.

The usage is really simple, if you don't pass any of the arguments, you will be asked for it on runtime:

<pre>
$ ssshsync [arguments]

Arguments:

-n <name> Project name  
-t <tag> Git tag to be deployed  
-g <url> Git host url  
-p <protocol> Git protocol  
-u <username> Git username  
-U <username> Local database user  
-r <username> Local database user with CREATE and DROP database permissions  
-H <host> Remote database host  
-d <name> Remote database name  
-R <username> Remote database username  
-S <host> SSH host  
-s <username> SSH username  
-f <directory> SSH destination directory  
-x Loads fixtures  
-c Clean local project generated files and database
</pre>
