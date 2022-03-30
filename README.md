# qBittorrent to Rclone 

This web application downloads your torrent-files or magnet links or torrent http links and uploads directly to your any rclone drive instantly.
Here qBittorrent-nox (Linux) is used as web UI And Rclone is used as Uploader with the help of Docker.


![Demo](demo/Screenshot%202022-01-09%20180328.png)


## How To Deploy ?
### Step 1
* Create a [Heroku](https://dashboard.heroku.com/login) Free account
* Log in to Heroku in any browser
* Click on the Rapid deployment button [![Deploy](https://heroku.com/deploy?template=https://github.com/TheCaduceus/QBitorrent-Web-Ui) and deploy app
### Step 2 (setting Config Vars)
* Go to deployed application in heroku
* Switch to application settings.
* Scroll down to see `config vars` > click `Reveal Config Vars`.

#### i) RCLONE_CONFIG_IN_RAW_URL

* Generate rclone.conf file from any terminal or cmd or termux or by using RCX android.
* Make sure you have a valid config and the `remote name` shouldn't have spaces in it. eg- `[devanaz]`
* You can't use Multiple cloud drive accounts in single rclone.conf file, if you done that your first config is only taken for upload.
* We need any text/code hosting website, Use [gist-github](https://gist.github.com) github account needed.
* Open rclone.config file using any text editors and copy all text inside rclone.conf and paste it in gist
* Choose any file name and save it by clicking `Create secret gist`.
* Then Click RAW button and copy the url (RAW is important)
* Paste your config Url in the heroku 'RCLONE_CONFIG_IN_RAW_URL' Section 
* note : Don't share this url to anyone

#### ii) WEBUSER
* Type Your new Username in `WEBUSER` section

#### iii) WEBPASSWORD
* Type Your New Password in `WEBPASSWORD` section

##### iv) SELFPING (Optional hidden config var)
 This config var is hidden and can be activated by 
* Go to deployed application in heroku
* Switch to application settings.
* Scroll down to see `config vars` > click `Reveal Config Vars`.
* use key as `selfping` and corresponding value as `your-deployed-app-name` 
* example [image here](demo/-4962988908900100631_121.jpg)
##### v) PINGDOMAIN (Optional hidden config var)
 This config var is hidden and can be activated by 
* Use config var , key `PINGDOMAIN` and corresponding value `http://your.custom.domain.com`
* example [image here](https://user-images.githubusercontent.com/71500526/160111418-220d1420-ac47-4c6d-8bc2-faf26457483b.jpg)

## Common Errors
* If  `This page isn’t workingIf the problem continues, contact the site owner. HTTP ERROR 401` is shown in browser change your browser url from `https://myapp.herokuapp.com` to `http://myapp.herokuapp.com/` . ie., change https to http

## SCREENSHOTS


![demoo](demo/Screenshot%202022-01-09%20181831.png)
![demoo](demo/image.png)



