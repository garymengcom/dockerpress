# Docker for WordPress
> One website one environment.


## How to use
1. Clone this repository and go to the directory:
    ```bash
    git clone https://github.com/yeszao/dockerpress.git
    cd dockerpress
    ```
2. Copy `docker-compose.yml.sample` to `docker-compose.yml`:
    ```bash
    cp docker-compose.yml.sample docker-compose.yml
    ```
   Customize the `docker-compose.yml` file as needed.
   E.g. nginx expose port `80` to host default, change it to another one if it was occupied.
4. Download WordPress and unzip files to `src` directory.
    ```bash
   curl -s https://wordpress.org/latest.zip -o /tmp/latest.zip \
       && unzip -q /tmp/latest.zip -d /tmp \
       && mv /tmp/wordpress/* src/ \
       && rm -rf /tmp/wordpress /tmp/latest.zip
   ```
5. Run the following command:
    ```bash
    docker compose up -d
    ```
6. Open your browser and access [http://localhost](http://localhost).
7. The MySQL configurations default are (all of the values can be modified in `docker-compose.yml` file):
   - **Host**: `mysql`
   - **Port**: `3306`
   - **DB Name**: `wordpress`
   - **Username**: `root`
   - **Password**: `12345678`
   
