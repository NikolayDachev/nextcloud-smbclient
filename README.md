# nextcloud-smbclient
nextcloud docker-compose with smbclient build

Based on nextcloud:fpm, for some reason smbclient pkg is not include, which not allow external smb share to be provided via nextcloud 

deploy: Any customisaztion will work, no real diffrent from origian docker-compose  

1. set sql db password

nextcloud-smbclient/db/db.env
MYSQL_PASSWORD={NEXTCLOUD_USER_SQL_PASS}

2. set sql root pwd  

nextcloud-smbclient/docker-compose.yml
- MYSQL_ROOT_PASSWORD={MYSQL_ROOT_PWD}

3. set public ip for nextcloud service
 - {MY_PUBLIC_IP_ADDRESS}:80:80

4. run
docket-compose up -d
