# A simple To-Do Flet app

An example of a minimal Flet app.

## Install libraries
```bash
pip3 install -r requirements
```


## Run app as desktop app

```bash
flet run [app_directory]
```

## Run it as web app

Based on [Web Self Hosting](https://flet.dev/docs/publish/web/dynamic-website/hosting/self-hosting)

### Make a Flet service

Edit and make a link to flet.service file 
```bash
cd /etc/systemd/system
sudo ln -s ${absolute-path-to}/flet-app/documentation/flet.service
sudo systemctl start flet
sudo systemctl enable flet
sudo systemctl status flet
```

### Add a proxy in Nginx

**Note**: Have Nginx installed

Copy conf file to Nginx configs 

```bash
sudo cp ${absolute-path-to}/flet-app/documentation/todo.conf /etc/nginx/sites-available/todo
```

Start nginx
```bash
sudo service nginx start
```

