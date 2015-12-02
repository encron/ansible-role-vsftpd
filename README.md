# vsftpd
Vsftpd ansible role for RedHat.  
This role installs and configures vsftpd.

## Dependencies

This role has no depencies and will work on its own.

## Role Variables

`vars/main.yml`

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| vsftpd_shares_root | /srv/shares | The root folder where your shares will be placed |
| vsftpd_shares | undefined       | Define your ftp shares here that need to be created |


## License

MIT
