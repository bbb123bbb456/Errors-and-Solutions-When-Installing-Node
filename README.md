# Errors-and-Solutions-When-Running-Node

Error 1: Error: invalid character 'o' looking for beginning of value

When you get this error, you should enter the following command as a solution

    sudo su


Error 2: command not found

With this command we do the following. ---> cp [source directory] [destination directory]

    cp /root/go/bin/nodeidd /usr/local/bin
    systemctl restart nodeidd
    
Where nodeidd is written, we will write as follows. (That is, we will add the letter d to the end of the node name we set up.)

For example: rebusd for rebus, strided for stride, stafihubd for stafihub, teritorid for teritori

For example; We can fix the error in the image above for the Rebus node with the following command;

    cp /root/go/bin/rebusd /usr/local/bin
    systemctl restart rebusd



Error 3: Make: *** [Makefile:101: install] Error 127

We usually encounter this error when performing an update. The solution is also quite simple, we will reinstall go.
Go installation commands;

    cd $HOME
    wget -O go1.18.2.linux-amd64.tar.gz https://go.dev/dl/go1.18.2.linux-amd64.tar.gz
    rm -rf /usr/local/go && tar -C /usr/local -xzf go1.18.2.linux-amd64.tar.gz && rm go1.18.2.linux-amd64.tar.gz
    echo 'export GOROOT=/usr/local/go' >> $HOME/.bashrc
    echo 'export GOPATH=$HOME/go' >> $HOME/.bashrc
    echo 'export GO111MODULE=on' >> $HOME/.bashrc
    echo 'export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin' >> $HOME/.bashrc && . $HOME/.bashrc
    go version

After typing these commands, you can enter the update commands again.


Error 4: Exit code

You may get angry while reading this title. You are right because this error is the trouble of all of us most of the time. :D

However, this exit code error does not have a specific solution, so there are multiple solutions. What we need here is to find out what is causing the error, so we will use the following command.

    systemctl stop nodeismid 
    nodeidd start 
    
Where nodeidd is written, we will write as follows. (That is, we will add the letter d to the end of the node name we set up.)

e.g. rebusd for rebus, strided for stride, stafihubd for stafihub, teritorid for teritori

After entering this command, there will be an expression in the first line of the output that tells us why the error is caused, according to the error written there, we will take action on the node and get rid of the nuisance called exit code.


    account sequence mismatch, expected X, got X: incorrect account sequence
When you get this error, add the --sequence X command to the end of the command you entered.

(Add a number to the part that says X, but not a number from the head, of course, for example, we will enter whatever is written where expected is written in the image. )

Error 5: No journal files were found

After doing Ctrl + C, let's enter the following command;

    systemctl restart systemd-journald
  
This command will not give you any output, do not think that the command did not work because it does not give output. After entering this command, check the log again.

