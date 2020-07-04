# cloudlog-docker #
docker-compose for [cloudlog](https://github.com/magicbug/Cloudlog)

## Requirements ##
- git
- docker/docker-compose


## Setup ##
1. Clone this repo

   ```bash
   git clone `https://github.com/red-coracle/cloudlog-docker.git
   cd cloudlog-docker
   git submodule update --init --recursive
   ```
2. Modify server_name in `cloudlog.conf` to be the domain you will be accessing it on.
3. Modify `docker-compose.yml` to change the port (if desired) and mysql passwords.
4. Bring up the stack with `docker-compose up -d`.
5. Access `http://{your domain}/install` to begin the cloudlog installation process.
   Use `db` when prompted for the database hostname.
6. After completing the installation you can modify `cloudlog/application/config/config.php` 
   with any configuration changes. Since nginx will rewrite the URL, you can 
   set `index_page` to an empty string.
