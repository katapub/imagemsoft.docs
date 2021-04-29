# Installing Smile CDR
 
Smile CDR can be deployed to a server as an application by extracting the Smile CDR application archive file or as a Docker service by importing the Smile CDR Docker image. Once deployed, the initial installation of Smile CDR should be as simple as editing the configuration file and starting the software. We believe that software should be easy to configure, and should come with sane configuration out-of-the-box.

The following sections will provide a general overview of the basic installation process along with details for deploying Smile CDR as an application. Additional details about deploying Smile CDR as a Docker service are available at this page.

## Installing to Linux / OSX
 
The following instructions will focus on deploying the software in a Linux/OSX environment.

1. Create a service account that the Smile CDR application will run under

        sudo adduser --system --no-create-home --disabled-login --group smile

2. Extract the archive

        # Navigate to the directory you wish to install to
        cd /opt/

        # Extract the Downloaded Archive
        sudo tar xf /path/to/smilecdr-2021.05.PRE

        # Reassign the install directory to the smile user
        sudo chown -R smile:smile smilecdr

3. Navigate to the smilecdr directory

        $ cd smilecdr

You will now see the following directories in your target folder:

* bin/ – contains the script used to start and stop Smile CDR's server process
* classes/ – contains configuration files
* lib/ – contains the application itself (you should not need to interact with this directory)