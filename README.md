# MacAdminsConf2026-mSCPWorkshop
Quick repo for items related to our workshop
<b>mSCP 2.0: The Quest for More Compliance</b>
John Mahlman IV, Matt Woodruff, Cody Keats
Tuesday, July 7 • 09:00AM - 04:30PM
Workshop, Intermediate • Deans Hall 2
Session Info: https://sched.co/2CY5u
Feedback: https://bit.ly/psumac26-1147827

Pre-Workshop Items
Thank you all for picking our workshop on mSCP 2.0. While we don’t have any major pre-requisites, we are asking that you do some things before coming to the workshop, just to ensure the network is not taxed. We will cover this during the workshop, but the goal is to save bandwidth.

Download and install the Apple Container subsystem
Head to the download page: https://github.com/apple/container/releases/tag/1.0.0 and install the PKG
Once installed, open a Terminal and run the command:
container system start
This starts the subsystem but will also ask you to install the kernel, answer Y when asked to download the recommended kernel, and let that complete

Note that you can use Docker if you prefer, all commands will be supported in both.

Download the mSCP Container (and optionally, the code)
After installing the container subsystem or Docker, you can then pull the mSCP container using one of the following commands:
Apple Container:
mkdir -p ~/Desktop/mscp/custom
container run -it --volume ~/Desktop/mscp:/mscp/build --volume ~/Desktop/mscp/custom:/mscp/custom ghcr.io/usnistgov/mscp_2.0:latest


Docker:
mkdir -p ~/Desktop/mscp/custom
docker run -it --volume ~/Desktop/mscp:/mscp/build --volume ~/Desktop/mscp/custom:/mscp/custom ghcr.io/usnistgov/mscp_2.0:latest

This will ensure that the container is already downloaded locally to your system. After running this, you will be dropped into the mSCP container, you can just type `exit` or press control+d.
(Optional but helpful) If you would like to also have the mSCP code base handy in another local folder, you can clone the git repo to a local folder: 
cd ~/Downloads; git clone https://github.com/usnistgov/macos_security.git


We also ask that you have your preferred code editor handy, just to inspect documents with highlighting. We recommend Microsoft Visual Studio Code for free.

We’re looking forward to seeing you!
