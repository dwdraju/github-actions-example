# SSH Based Deployment

### Create a new ssh key
```
ssh-keygen -t rsa
```
Give a new path for the key if you don't want to use default location or replace.

### Create a new Github secrets
Create a secret **CD_SSH_KEY** for the repository where you want to use the deployment.

### Add ssh public key
Append the newly generated ssh public key inside `~/.ssh/authorized_keys` file.

### Adjust ssh username and host
On the `cd.yaml` file, adjust this line: `ssh user@your-server` with ssh user and host.

### Time for actions !
Copy the `cd.yaml` file inside `.github/workflows` folder

Push to `master` branch and you are all done !

[Make sure the ssh port is open to the world !]
