# Xen-Orchestra (Community Edition) Installer

Xen-Orchestra (Community Edition) allows you to administer Citrix XenServer and XCP-ng as well as backup any VM's running on these systems. 

The single line installation script allows you to go from a bare-minimal installation of Ubuntu or Debian (Server) to fully operational XOCE server. Run the following steps from a root shell. 

    sudo bash
    <password>
    sudo curl https://raw.githubusercontent.com/Jarli01/xenorchestra_installer/master/xo_install.sh | bash
    <password>
    
The default username and password are applied, admin@admin.net and admin for the password
    
If you don't want NFS capabilities run ```sudo apt-get remove nfs-common```.

* Do not use LAMP
* SSH Access is optional, but highly recommended

## SSL Settings and Details

To configure SSL with this installation script you'll want to look in the following path for the YAML configuration file, we name it ```.xo-server.yaml``` it can be found in ```/opt/xen-orchestra/packages/xo-server/```. 

For details on how to configure this please review the documentation here: https://xen-orchestra.com/docs/configuration.html#https

# Goals/Backstory for this script

I'm often asked "why can't this be run on CentOS or Fedora" to which my only reply is and has ever been: The goal was to be the XCP-ng of XS. Which means I wanted a solution that offered as much as XOA offers, while using what is available freely and from open sources. Without restrictions. 

That isn't to say that this installation script won't work on other distributions, please contribute and help us to spread XOCE to other platforms. 

Initially my goal was to simply setup and start using XOCE for a tiny production shop to be able to use an open source hypervisor (Citrix XenServer at the time) and have a management tool/backup solution. Which was initially NAUBackup and XenCenter, when I found XOA and that there was an open source management solution and backup solution that wasn't script based I jumped for it, taking the manuall installation process provided by Olivier and his team and automating it. 

That goal transformed into the desire to assist the developers of XOA by using and hopefully finding any bugs or quirks that needed to be worked out while staying in line with the original goal of being as nearly compatibile as possible to XOA.

While the goal initially was to have a solution as close to XOA as possible, with the script came the ability and goal to automate the installation. This is a big deal for these scripts today, while providing an as near-match solution to XOA as possible. 

