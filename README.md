# Docker container image with "headless" VNC and browser

docker image is installed with the following components:

* Desktop environment [**IceWM**](http://www.icewm.org/)
* VNC-Server (default VNC port `5901`)
* [**noVNC**](https://github.com/kanaka/noVNC) - HTML5 VNC client (default http port `6901`)
* Browsers:
  * Chromium

## Usage

Build a image:

docker build -t consol/centos-xfce-vnc centos-xfce-vnc

Run container

docker run -it -p 5901:5901 -p 6901:6901 vnc chromium-browser https://coldstorage.com

=> connect via __VNC viewer `localhost:5901`__, default password: `vncpassword`

