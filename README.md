## Assignment 3 Part 1

#### ip address for digital ocean droplet: 64.23.162.3

### Setting Up A New Server

#### Step 1: Create a System User

We will create a new system user called `webgen` using the command below:

```bash
sudo useradd --system -d /var/lib/webgen -s /usr/sbin/nologin webgen
```
`--system`: This option creates a system user (UID below 1000) instead of a regular user
`-d`: This option specifies the home directory of the new user
`-s`: This option specifies the login shell of the new user (in this case we will set nologin because it is a system user)

Now we will create the sub-directories inside of the new users home directory using the commands below:

```bash
sudo mkdir /var/lib/webgen/HTML
sudo mkdir /var/lib/webgen/bin
```

And finally we will change the ownership of the newly created directory using the command below:

```bash
sudo chown -R webgen:webgen /var/lib/webgen
```

`-R`: This option means the ownership will be applied recursively which means it will change the ownership of the /var/lib/webgen directory as well as all its subdirectories (such as bin and HTML). 

#### Step 2: Configure the generate_index script

#### Step 3: Configure the systemd service file and timer file

#### Step 4: Configure the nginx configuration files

#### Step 5: Configure UFW
