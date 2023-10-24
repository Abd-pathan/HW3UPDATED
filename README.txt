The code of homework 3 is basically an updated version of homework 2.
In this we have implemented 2 more options '-e' and '-E'.

The -e option allows you to execute a single command for each matching file. For example, if you want to List all files that have the substring “jpg” in their
filename with depth <=3 relative to the current
directory and size <= 1024, and execute the command
"wc -l" on each file , you can use the following command: 
./search -s 1024 -f jpg 3 -e "wc -l"

The -E option allows you to execute a command with a list of matching files as an argument. For example, you can create a tar archive of all text files in the specified directory with the following command:

./search-f txt 2 -E "tar cvf txt.tar"

basic implementation is done using the fork() parent child process and the system function is used to run the constructed command, and the exit status is captured and checked for success or failure.

