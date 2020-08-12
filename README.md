# Updated August 2020

I've updated my process and this is another option for folks that might want to use a staging account. I use an API call along with some other scripting methods to collect the user data during the build (based on email address) and then replace the staging account with that user. Process is faster and requires less interaction by the person building the system. The API call I make in the script is documented at your tenant's address then end with /api/help and WS1 doc is here: https://docs.vmware.com/en/VMware-Workspace-ONE-UEM/services/macOS_Platform/GUID-AWT-SINGLESTAGINGFLOWWITHAPI.html Keep in mind that you must have your DEP profile setup with the staging account as mentioned in the above doc. 

# DEPNotify 1.1.5 with Workspace One

DEPNotify is a great splash screen program to notify macOS users during the build process about whats happening on their system. I've decided to use this time to
give a little history lesson about our company and while installing applications in the background. All credit for this program goes to Joel Rennich and the folks
that help support it on the macadmins slack channel. I wanted to create a proper workflow for those folks that use Workspace One as an MDM. I was fortunate enough
to present at the Penn State mac admins conference in 2019. You can see that here: https://www.youtube.com/watch?v=HbKZ66F58qo

# The main application - DEPNotify

DEPNotify works with several MDM's and allows you to "tail" the log files of these MDM's to report back what's installing. Please download the main application and extract
the DEPNotify.app before creating your deployment package. latest build for 1.1.5 is in a package and can be found here: https://files.nomad.menu/DEPNotify.pkg

You can use -jamf, -filewave, -munki. 

If you want to tail the AirWatch or WS1 log file, follow these instructions from VMware:
https://github.com/vmware-samples/euc-samples/tree/master/macOS-Samples/BootstrapPackage/WS1-DEPNotify-Standard#customize-the-depnotify-settings (Thanks to Mathijs de Ruiter for the heads up!)
