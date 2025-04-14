# Changing-File-Permissions-in-Linux

## In this exercise we are going to change permissions in linux of a couple of files and a directory.

![image](https://imgur.com/hN4zpay.png)

First we verify the permissions that are currently in place in the directory that we are working.

![image](https://imgur.com/VebjXcF.png)

We also need to know if there are hidden files in case we need to work with some of them.

![image](https://imgur.com/dJ1Yrkx.png)

![image](https://imgur.com/QL60I2D.png)

We need to find what files have write permissions for the other group. We found tha the project_k.txt is the file in question.

![image](https://imgur.com/eeRA1BS.png)

We then removed the write permissions of the file from the "others" group using the command chmod o-w projects_k.txt, the result now shows the file with only read permissions from the "others" group marked in red.

![image](https://imgur.com/7zxcTfZ.png)

Now to the next excercie.

![image](https://imgur.com/ctPVfpw.png)

Here we can see that the project_m.txt has read permissions for group, we need to remove those permissions since this file should only be readable or writeable by anyone else but the user.

![image](https://imgur.com/WEk7ZkK.png)

After using the command to remove permissions chmod g-r project_m.txt and then check file permissions again we can see that the file now only has read and write permissions from the user as it should be.

![image](https://imgur.com/wqTSPyi.png)

![image](https://imgur.com/rh79nXX.png)

Now after knowing that the file .project_x.txt is a hidden file we need to change the permissions of the file so that both the user and the group can read, but not write to the file.

After using the command chmod u=r,g=r .project_x.txt we end with the following result. (Keep in mind we need to use the . before the name of the file in order to tell the system that the file we want is a hidden file)

![image](https://imgur.com/K1wvQTx.png)

For the final task we are going to change the permissions of a directory as explained below.

![image](https://imgur.com/sUXCeKn.png)

These are the innitial permissions of the draft directory, it is easier to spot it since it is marked in blue.

![image](https://imgur.com/x3yXkIr.png)

Now after using the command chmod g-x drafts and checking the permissions again we can see that the group execute permissions are gone from the directory and only the user permissions remain.

![image](https://imgur.com/o33sPMZ.png)

With this we conclude this simple exercise of changing permissions in Linux.
