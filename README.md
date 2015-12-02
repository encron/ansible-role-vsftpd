# Vsftpd

An Ansible role for installing and configuring vsftpd on CentOS/RHEL 7.  

## Requirements

- SELinux is expected to be running
- Users and groups should already be created

## Role Variables

`vars/main.yml`

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| vsftpd_shares_root | /srv/shares | The default ftp directory where your shares will be placed |
| vsftpd_shares | -      | List of dicts defining the ftp shares that need to be created (see example below) |

## Dependencies

This role has no depencies and will work on its own.

## Defining shares

To define a share, you start with giving it a name:

```Yaml
vsftpd_shares:
  - name: readonlyshare
```
Because of the default settings of the other variables, this will create a share with only read access for registered users.  
To further define permissions and group ownership, you'll have to specify the variables directory_mode and group, as shown in this example:

```Yaml
vsftpd_shares:
  - name: exampleshare
    group: pirates
    directory_mode: u=rwx,g=rwx,o=rwx
```

## License

MIT
