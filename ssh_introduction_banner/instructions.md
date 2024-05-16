## Instructions for creation of an introduction banner for SSH servers

1. modify the SSH daemon configuration file located at /etc/ssh/sshd_config. Here's how you can do it:
Open the SSH daemon configuration file using a text editor like `nano` or `vim`.

For example: 

```sh
sudo vim /etc/ssh/sshd_config

```
2. Scroll down or search for the Banner directive in the file. If it's commented out (with a # at the beginning), uncomment it by removing the #, or add it if it's not present. 

It should look like this:

```
Banner /path/to/your/banner/file

```
3. Create a text file containing your personalized greeting. For example, you can create a file named ssh_banner.txt in a directory of your choice, such as /etc/ssh/. 

You cand do it by running the following command:

```sh
sudo touch /etc/ssh/sh_banner.txt

```
4. Add your personalized greeting message to the file. if you want you can create a banners, like the one in the file `ssh_banner.txt` of this repository in sites like the one below: 


```
https://manytools.org/hacker-tools/ascii-banner/

```
5. Make sure the file is readable by all users by running the command below:

```sh
sudo chmod a+r /path/to/your/banner/file

```
6. Restart the SSH service to apply the changes with the command:

```sh
sudo systemctl restart sshd

```
7. Ready! Now, when users connect to your server via SSH, they will see your personalized greeting message before the login prompt.
