# fathym.io_ParticleDev
Download the fathym.io library folder to develop for Fathym on the Particle Photon
## About
[Fathym](http://fathym.com) is a platform that let's you create powerful, social, front-end apps and dashboards for your IoT projects. Now with the fathym.io library native to Particle, it's incredibly easy to create dashboards and notifications, and even control your Photon from your own Fathym app! 
# Tutorial
## Getting up and running
1. **Download the [Fathym.io (fix link)](http://fathym.io) zip folder from this repo and unzip**
2. **Open the Particle Dev Desktop app and add the Fathym.io folder**
![Particle Dev](https://40.media.tumblr.com/85a6b84ac6a20005769c38cf79ea9c55/tumblr_o58dv5IR7S1qcz8h1o1_1280.jpg "Particle Dev")
  - Download the [Particle Dev Environment](https://www.particle.io/dev) if you haven't already
  - Inside Particle Dev: File -> Add Project Folder -> Find the fathym.io folder
5. **Select your device, save, complie, flash**
  - The .ino should get random test data flowing to Fathym exactly as is, so we'll test everything before messing with the code
6. **Create a new Photon Part in your Fathym Homespace**
![Fathym Home](https://41.media.tumblr.com/101c284e6b4c640957cbaa86e444fe32/tumblr_o58dv5IR7S1qcz8h1o2_1280.jpg "Fathym Home")
  - Create an  account at [community.fathym.com](http.//community.fathym.com) if you haven't already
  - From your homespace, click the plus "+" button to get to the catalog of addable parts
  - Choose the Particle Photon part
  - Add your Photon deviceID, which you can find on your [Particle Dashboard](https://dashboard.particle.io/user/devices)
8. **Enter your Photon Part on Fathym and add visualizations**
![Inspector](https://36.media.tumblr.com/e783e4d513003a6dc328c38347a4fa51/tumblr_o58dv5IR7S1qcz8h1o3_1280.jpg "Inspector")
  - From inside your Particle Photon Part, click the plus "+" button to get to the catalog of addable parts
  - Start by adding the inspector display
  - Save and watch your data flow through!

## Customizing

1. **Inside Particle Dev, open the fathym.io-photon.ino file**
![ino](https://40.media.tumblr.com/31879b26805e0ddac21e0a97e9fbe36e/tumblr_o58dv5IR7S1qcz8h1o4_1280.jpg "ino")
  - You'll see commented instructions about how and where to add code for your sensors
  - Note that fathym.set("attribute name", value, "units of measurement") formats the JSON to send to Fathym
2. **Open the Fathym.Build.h file**
![build.h](https://40.media.tumblr.com/7ec2caa15654a3f089cb182301aefcbd/tumblr_o58dv5IR7S1qcz8h1o5_1280.jpg "build.h")
  - Edit the attributes that are automatically sent along with your payload by setting each item to true or false 
  - Note that the Fathym.io library includes support Photon battery power - enable battery support by uncommenting the code at the bottom of the FathymBuild.h file
3. **Add additional dashboard visualizations for your device in Fathym**
![Fathym Dashboard](https://36.media.tumblr.com/447b4d8abf0869768b89b0411e377eae/tumblr_o2crfxZXFf1qcz8h1o2_1280.jpg "Fathym Dashboard")
  - From inside your Particle Photon part, click the plus "+" button to get to the catalog of addable parts
  - Try a Historc Value part
    - Fill out the "Property Name" field with one of the attributes you're sending from your Photon (the attribute name must be an exact, case-sensitive match). Leave this field blank to create a generic graph with dropdown menu of the attributes you're sending so you can switch the attribute on the fly.   
4. **Create a Fathym Notification**
![Notification Rule](https://40.media.tumblr.com/1a61ec7a1eb745816795d509af0f044f/tumblr_o58dv5IR7S1qcz8h1o6_1280.jpg "Notification Rule")
  - From inside your Particle Photon part, click the config "cog wheel" button
  - Enter the "Add Ons" part
  - Enter the "Publish Subscription" part
  - Again, click the config "cog wheel" button
  - Enter the "Responses" part
  - Click the plus "+" button to get to the catalog of addable parts
  - Select the "Check" part
  - Name the Check Part and add a "Message Evaluation" 
    - Ensure that the property name you use is an exact match to one you're sending from your Photon
  - Save the Check part and then Enter into the Check part you just created
  - Click the plus "+" button to get to the catalog of addable parts
  - Add an "Email Response" for email or "Twillio Respoonse" for sms and configure as desired
