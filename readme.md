# Codeanywhere MySQL Setup Instructions

- Sign up for a free Codeanywhere account at [https://codeanywhere.com/signup](https://codeanywhere.com/signup)
- Verify your email
- Open the Editor
- When prompted by the connection wizard, name the connection anything you like (e.g., 'mysql') then search for and use the **Node - Ubuntu 14.04** template
- Once the container has been deployed open up the SSH Terminal by right clicking the terminal name from the left hand menu and selecting SSH Terminal
- With the terminal open, run the following:
- `/usr/bin/mysql_secure_installation`
- You'll be prompted to enter a root user password, intially there won't be one so press enter and when prompted set your own password and confirm it
- Run through all of the questions and answer 'Y' to each of them
- When the setup is complete run the following snippet in the terminal:

```
echo 'alias cli="mysql -u root -p"
alias start="sudo service mysql start"
alias stop="sudo service mysql stop"' > ~/.bash_profile
```

- Now run `source ~/.bash_profile`
- You will now be able to access the mysql shell with `cli` (you will be prompted for the password that you created above) and you will be able to start and stop the mysql service with `start` and `stop`