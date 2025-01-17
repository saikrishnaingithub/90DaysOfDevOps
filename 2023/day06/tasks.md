# Day 6 Task: File Permissions and Access Control Lists

### Today is more on Reading, Learning and Implementing File permissions

 The concept of Linux File permission and ownership is important in Linux. 
 Here, we will be working on Linux permissions and ownership and will do tasks on
 both of them. 
 Let us start with the Permissions.

1) Create a simple file and do `ls -ltr` to see the details of the files [refer to Notes](https://github.com/LondheShubham153/90DaysOfDevOps/tree/master/2023/day6/notes)
 
 Each of the three permissions are assigned to three defined categories of users. The categories are:
-	   owner   —   The owner of the file or  application.
-	"chown" is used to change the ownership permission of a file or directory.
-	   group   —   The group that owns the file or application.
-	"chgrp" is used to change the group permission of a file or directory.
-	   others  —   All users with access to the system. (outside the users are in a group)
-	"chmod" is used to change the other users permissions of a file or directory.

    As a task, change the user permissions of the file and note the changes after `ls -ltr`

2) Write an article about File Permissions based on your understanding from the notes.

- 	Highest permission is : 7 — (4+2+1)
	Maximum permission -  777, but effective 666 incase of a file for security reason in linux, no user will get execute permission.
	For directory case effective permission is 755
	Lowest permission is –000 not recomended
	Minimum permission – effective permission 644 incase of a file 	        * [   (umask [UNIX MASK] value- 022 )    ]
	For directory case default permission is execute permission.

Each of the three permissions are assigned to three defined categories of users. The categories are:
	   owner   —   The owner of the file or  application.
	"chown" is used to change the ownership permission of a file or directory.
	   group   —   The group that owns the file or application.
	"chgrp" is used to change the gropu permission of a file or directory.
	   others  —   All users with access to the system. (outised the users are in a group)
	"chmod" is used to change the other users permissions of a file or directory.


3) Read about ACL and try out the commands `getfacl` and `setfacl`

-   Standard file permissions are satisfying when files are used by only a single ownner and a single designated group. However, If we want to give access to a user or group which not listing on default file permission, then ACL will come in use.
With ACL, you can grant permission to multiple users and groups, identified by user name, group name, UID, GID. using the same permission flags used with regular file permission: read, write and execute.

-   setfacl -m u:vagrant:rw test	  ## Hear we have set read and write permission for vagrant user, who dont have access to the file before.
 
In case of any doubts, post it on [Discord Community](https://discord.gg/hs3Pmc5F)

Happy Learning