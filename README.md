# efundi-sync
Shell script made for syncing University modules from eFundi to local machine

## Windows

For Windows local machine the program [Cyberduck](https://cyberduck.io/) was used.

## Linux

For Linux local machine the library [Rclone](https://rclone.org/) was used. The file ```efundi.sh``` was ran when sync was needed.

## Rclone Setup

From the rclone documentation the following command was ran to install the library:

```curl https://rclone.org/install.sh | sudo bash```

Thereafter the following was ran to initialise the configuration:

```rclone config```

To add a new remote the following option was chosen

```n) New remote```

After a name was specified, the following option for storage type was chosen

```
37 / Webdav
   \ "webdav"
```

The url was pasted next without any "quotes". This was taken from the eFundi module(s) page(s) under ```Resources > Transfer files```

For the "Vendor" option the following was chosen:

```
 4 / Other site/service or software
   \ "other"
```

The username was filled in next (which was the student number) without any "quotes"

For the password the following option was chosen

```
y) Yes type in my own password
```

For the "Bearer token" the default option was chosen

For the "Edit advanced config? (y/n)" option the default was chosen

```
n) No (default)
```

Thereafter the following option was chosen to finish the new remote setup

```
y) Yes this is OK (default)
```

The config can now be closed by selecting the option

```
q) Quit config
```

## Future improvements

- [ ] [cron](https://man7.org/linux/man-pages/man8/cron.8.html) jobs can be implemented to carry out sync automatically on a predefined schedule
