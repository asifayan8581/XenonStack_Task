# XenonStack_Task


# Xenonstack

## Task 1

## Linux

A custom linux command internsctl was given by a customer for performing operations.

## Features
1. Using `$man internsctl` you can see the command's manual page so that you see the full documentation of the command similar to $man ls.
2. Using `$internsctl --help` you can see the help document.
3. Using `$internsctl --version` you can see the version of the command.
4. Using `$internsctl cpu getinfo` you get cpu information of the server like the `lscpu` command.
5. Using `$internsctl memory getinfo` you can get memory information of the server like the `free` command.
6. Using `$internsctl user create <username>` you can create a new user on the server.
7. Using `$internsctl user list` you can list all the regular users present on the server.
8. Using `$internsctl user list --sudo-only` you can list all the users with sudo permissions on the server.
9. Using `$internsctl file getinfo <file-name>` you can get some information about a file.
10. Using `$internsctl file getinfo [options] <file-name>` in case you only want some specific information then you have a provision to use options like: `--size`, `-s` to print size; `--permissions`, `-p` print file permissions; `--owner`, `o` print file owner; `--last-modified`, `m`.

## Task 2
## A website
A website on something

## Project Structure
The project is divided into three main pages:

1. Page (index.html)
2. Login Page (login.html)
3. Contact Us Page (contact.html)

## Setup and Installation
Follow these steps to set up and run the project locally:

Clone the Repository: git clone `https://github.com/your-username/my-website.git cd my-website`

Install Dependencies: `npm install`

Database Setup: A. Ensure that you have MongoDB installed and running. B. Configure the database connection in server.js.

Run the Server: node server.js

Access the Website: Open your web browser and go to `http://localhost:3000` to view the website.


