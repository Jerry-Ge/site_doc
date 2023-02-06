---
title: "Commands"
description: "Some common cmd scripts for setting up a server."
lead: "Some common cmd scripts for setting up a server."
date: 2023-02-05T20:48:57+00:00
lastmod: 2023-02-05T20:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "server_setup"
weight: 100
toc: true
---

## Create a New User
{{< alert text="sudo adduser $user_name" />}}

## Change Password
{{< alert text="sudo passwd $user_name" />}}

## Enable SSH Password Authentication
{{< alert text="vim /etc/ssh/sshd_config "/>}}
Change from No to Yes
{{< alert text="PasswordAuthentication yes"/>}}
Restart the SSH service
{{< alert text="sudo service ssh restart"/>}}

## Add a SSH Key
Generate the key
{{< alert text="ssh-keygen -t rsa"/>}}
Copy the id_rsa.pub file
{{< alert text="cat ~/.ssh/id_rsa.pub"/>}}
On the remote server, create the authorized_keyes file
{{< alert text="mkdir -p ~/.ssh"/>}}
{{< alert text="touch ~/.ssh/authorized_keyes"/>}}

<!-- ```cpp
int main() {
  int y = SOME_MACRO_REFERENCE;
  int x = 5 + 6;
  cout << "Hello World! " << x << std::endl();
}
``` -->

