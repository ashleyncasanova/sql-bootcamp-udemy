### <span style="color:hotpink">Installing MySQL</span>

In this section we will install the MySQL server for mac. We can interact with
our database through the terminal or through the MySQL workbench.

Through the MySQL workbench, we can write and save query's in files to execute
when ready.

Install MySQL Server using link: https://dev.mysql.com/downloads/mysql/

> Note: you will be prompted to set a password.

\
Now we need to tell our computer about our server so we can access it through the
terminal:

Step 1: Open bash_profile using the following command

```terminal
open ~/.bash_profile
```

Step 2: Add path to sql to our bash_profile using

```
export PATH=${PATH}:/usr/local/mysql/bin
```

Step 3: Save and close file.

> Note: Newer versions of macOS are now using the zsh terminal instead of the
> bash terminal by default. You can use this command to check which terminal
> your macOS is running:

```terminal
echo $SHELL
```

If you see zsh in the output of that command, then editing the ~/.bash_profile
file won't work. Instead, you need to edit your ~/.zshrc file.

Instead of manually opening and editing the mentioned terminal configuration
file, you can just run this as a single terminal command and it should add the
necessary configuration to the ~/.zshrc file to make the mysql command work in
your zsh terminal:

```terminal
echo "export PATH=\${PATH}:/usr/local/mysql/bin" >> ~/.zshrc
```

After that, completely exit your terminal app, then start a brand new terminal
window, and try the command:

```terminal
mysql -u root -p
```

Which should prompt you to enter your password.

> Note: Your server should be running (apple icon > system settings > MySQL >
> start MySQL server).

> Note: For the Mac OS Sonoma you may have to edit the MySQL configurations by
> turning off the `Keyring Data File`. To do this go to the apple icon > system
> settings > MySQL > Configuration > uncheck Keyring Data File.

To exit SQL in our terminal use the command:

```terminal
quit;
```

---

### <span style="color:hotpink">Install MySQL Workbench</span>

Graphical interface where we can write and execute queries without having to
work within the command line.

Link to download MySQL Workbench: https://dev.mysql.com/downloads/workbench/

Go through installation process and open in applications directory. There should
be a connection already in place. We can open that and enter the root password
we created when we set up MySQL.
