We'll be running our code today using DDEV. If you have an existing PHP environment you would like to use, feel free to use that -- however please note that we won't be able to help with environment troubleshooting during the class due to time contraints.

To set up DDEV, you must first install Docker if you don't already have it.


## Installing Docker

### Docker for Mac OS:
(Instructions taken from https://docs.docker.com/docker-for-mac/install/)

1.  Download the latest stable release:
https://download.docker.com/mac/stable/31259/Docker.dmg

2. Double-click Docker.dmg to open the installer, then drag Moby the whale to the Applications folder.

![Install Docker app](https://docs.docker.com/docker-for-mac/images/docker-app-drag.png)

3. Double-click Docker.app in the Applications folder to start Docker. (In the example below, the Applications folder is in “grid” view mode.)

![Docker app in Hockeyapp](https://docs.docker.com/docker-for-mac/images/docker-app-in-apps.png)

You are prompted to authorize Docker.app with your system password after you launch it. Privileged access is needed to install networking components and links to the Docker apps.

The whale in the top status bar indicates that Docker is running, and accessible from a terminal.

![Whale in menu bar](https://docs.docker.com/docker-for-mac/images/whale-in-menu-bar.png)

4. If you just installed the app, you also get a success message with suggested next steps and a link to this documentation. Click the whale (whale menu) in the status bar to dismiss this popup.

![Startup information](https://docs.docker.com/docker-for-mac/images/mac-install-success-docker-cloud.png)

### Docker for Windows:
(Instructions taken from https://docs.docker.com/docker-for-windows/install/)

1. Download the latest stable release of the Window installer: https://download.docker.com/win/stable/31259/Docker%20for%20Windows%20Installer.exe

2. Double-click Docker Desktop for Windows Installer.exe to run the installer.
It typically downloads to your Downloads folder, or you can run it from the recent downloads bar at the bottom of your web browser.

3. Follow the install wizard to accept the license, authorize the installer, and proceed with the install.
You are asked to authorize Docker.app with your system password during the install process. Privileged access is needed to install networking components, links to the Docker apps, and manage the Hyper-V VMs.

4. Click **Finish** on the setup complete dialog to launch Docker.

5. Docker may not start automatically after installation. To start it, search for Docker, select **Docker Desktop for Windows** in the search results, and click it (or hit Enter).

![search for Docker app](https://docs.docker.com/docker-for-windows/images/docker-app-search.png)

When the whale in the status bar stays steady, Docker is up-and-running, and accessible from any terminal window.

![whale on taskbar](https://docs.docker.com/docker-for-windows/images/whale-icon-systray.png)

If the whale is hidden in the Notifications area, click the up arrow on the taskbar to show it.

If you just installed the app, you also get a popup success message (shown below) with suggested next steps, and a link to this documentation.

**NOTE** You do **NOT** need to login or create an account at Docker.com. Click the x to close the window.

![Startup information](https://docs.docker.com/docker-for-windows/images/docker-app-welcome.png)


## Installing DDEV

### DDEV for Mac

(Instructions taken from the DDEV site at https://www.drud.com/get-started/)

1. For macOS/Linux users, we recommend downloading, installing, and upgrading via Homebrew/Linuxbrew.

`brew tap drud/ddev && brew install ddev`

## DDEV for Windows

Download the installer and run it:
https://github.com/drud/ddev/releases/download/v1.9.1/ddev_windows_installer.v1.9.1.exe

## Get a local copy of the repository

The code used in our exercises is stored in GitHub. Clone (or download a ZIP file) from the repository:

Weather App: https://github.com/debugacademy/basic-drupal

### Cloning the repository:
1. If you would like to clone the repository, go to the command line and CD into the directory where you would like to put the repository. 

2. Enter 
`git clone https://github.com/debugacademy/basic-drupal.git`

**If** you already have SSH set up with GitHub, you can run
`git clone git@github.com:debugacademy/basic-drupal.git`

### Downloading a ZIP file:
1. If you'd prefer, you can also download a ZIP file and expand it into your preferred directory location.

ZIP file location: https://github.com/debugacademy/basic-drupal/archive/master.zip

Once you have cloned or expanded the ZIP file, you should now have a new directory named `weather-app` containing the exercise files.


## Starting your PHP environment

Once Docker and DDEV have been installed, you need to start them up in order to execute PHP code.

1. Make sure Docker is running -- look for the whale icon in the top status bar (Mac) or on the taskbar (Windows)
![Whale in menu bar](https://docs.docker.com/docker-for-mac/images/whale-in-menu-bar.png)
![whale on taskbar](https://docs.docker.com/docker-for-windows/images/whale-icon-systray.png)

2. CD into the `basic-drupal` directory and start DDEV from the command line:
`ddev start`

3. `ddev ssh`  
`ddev site-install`  
`drush sqlc < db_export.sql`  
`drush cr`  
