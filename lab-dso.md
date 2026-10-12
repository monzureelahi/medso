ubuntu 24

Checking os
cat /etc/os-release

Checking hostname
hostname
ls
ls -l

mkdir my-directory
rmdir my-directory

long-running operation (Installing Ansible)
pip3 install ansible==9.13.0 ansible-lint==4.3.7

Try a long-running operation in the background, E.g.: Installing Ansible
pip3 install ansible==9.13.0 ansible-lint==4.3.7 &

there is another command called nohup that is used along with the ampersand (&), you can explore it yourself
https://stackoverflow.com/questions/15595374/whats-the-difference-between-nohup-and-ampersand

Working with Files and Directories
mkdir new-directory
ls new-directory
pwd
cd new-directory
ls
cd ..
rmdir new-directory
ls

##Working With Files and Directories

Understanding Files
Everything is a file in Linux, text files, configurations, services, etc., However, Linux is so powerful there are many ways of doing the same operation.

If you wish to create a file, you can use any text editor of your choice. We will use nano and cat in this exercise.


nano myfile

Once you are in the editor, add some text and save the file using control + O (letter o) and hit Enter or the return.

You can exit the editor using control + X

Another option is you can also copy-paste some text into the terminal, for example:

nano myfile

Click this text below to copy:

Click anywhere to copy

Hello world!
Then you can save the file using control + X (letter x), hit Y (letter y) and hit Enter or the return.
If a file exists already, you can explore the contents of a file using the nano utility.

nano myfile

Do not forget to exit the editor using control + X.

Or you can also use the cat command (remember multiple ways of doing the exact same thing?).
cat command reads the content of a given file and displays it as output.

cat myfile

If you wish to rename a file, you can use the mv (move) command.

mv myfile newfile

You can see that myfile is renamed to newfile using the ls command.

ls

You can delete a file with rm.


rm newfile

##Here Documents
The cat command is mostly used to read a file; however, using a command line magic (read as command line hack), we can even create a file in a non-interactive way (ideal for CI/CD systems).

cat > filename <<EOL

Some text content
Some text content 2
Some text content 3

EOL

There are three parts to this command.

The filename, here its filename
The here document, the << symbols are a special code block. It allows you to redirect anything between EOL into a command
The cat command, if it’s followed by >, allows you to create a file
More info is available at https://www.cyberciti.biz/faq/save-file-in-linux-using-cat-command/

Do not forget to try an ls to view the new file, and a cat filename to review the contents of the file.
