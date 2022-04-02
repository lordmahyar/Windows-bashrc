# Windows-bashrc
Set your custom Commands in .bashrc

## Create .bashrc in Windows

1. Open `Git Bash` and paste the following commands

2. Clone this repository

   ```bash
   git clone https://github.com/lordmahyar/Windeows-bashrc.git
   ```

3. Copy `.bashrc` to user directory C:\\Users\\`USERNAME`\\

   ```bash
   cp .bashrc $HOME
   ```

4. Restart Git Bash to apply changes
   
   ```bash
   bash
   ```

5. Run `dj` to see your custom commands

   ```bash
   $ dj
   [HELP]:

    dj-req
    dj-run
    dj-shell
    dj-mig [APP_NAME]
    dj-admin [USER_NAME]
    dj-user USER_NAME
    dj-env ENVIROMENT_DIR
    dj-app APP_NAME
    dj-clean
    dj-pip PACKAGE_NAME
   ```

## Check .bashrc

Check if `.bashrc` exists in the user directory

```bash
[ -f $HOME/.bashrc ] && echo ".bashrc exists in $HOME"
```
you should get above existence message if `.bashrc` exists in the user directory.

## Read/Write on .bashrc

1. Read `.bashrc`

   ```bash
   cat $HOME/.bashrc
   ```

2. Write on `.bashrc`

   ```bash
   # using nano
   nano $HOME/.bashrc

   # using vim
   vim $HOME/.bashrc

   # using your editor
   start $HOME/.bashrc
   ```

## Get/Set `DEFAULT_PASSWORD` variable in .bashrc

1. Get `DEFAULT_PASSWORD`

   ```bash
   echo $DEFAULT_PASSWORD
   ```

2. Set Temporary `DEFAULT_PASSWORD`

   ```bash
   export DEFAULT_PASSWORD="New_Password"
   ```

3. Set Permanent `DEFAULT_PASSWORD`  
   set your new password in `.bashrc` line 4.

## Notes
### Set alias commands :

```bash
alias COMMAND_NAME="COMMAND"

# Example
alias dj-run="python manage.py runserver"
```

This means when you run `dj-run` it will run `python manage.py runserver`, so you don't need to type many words and arguments.

### Set functional commands :

```bash
FUNCTION_NAME(){
    COMMAND
}

# Example
dj-run(){
    python manage.py runserver
}

# Example with an argument
dj-pip(){
    python -m pip install "$1"
}
```

This means when you run `dj-pip django` it will run `python -m pip install django`, so you don't need to type many words and arguments.


echo $DEFAULT_PASSWORD
export DEFAULT_PASSWORD="Password"