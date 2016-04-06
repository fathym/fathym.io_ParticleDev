# fathym.io_ParticleDev
Download the fathym.io library folder to develop for Fathym on the Particle Photon
## About
[Fathym](http://fathym.com) is a platform that let's you create powerful, social, front-end apps and dashboards for your IoT projects. Now with the fathym.io library native to Particle, it's incredibly easy to create dashboards and notifications, and even control your photon from your own Fathym app! 
# Tutorial
## Getting up and running

**1. Download the [Fathym.io (fix link)](http://fathym.io) zip folder from this repo and unzip**

**2. Open the Particle Dev Desktop app and add the Fathym.io folder**

  - Download the [Particle Dev Environment](https://www.particle.io/dev) if you haven't already
  - Inside Particle Dev: File -> Add Project Folder -> Find the fathym.io folder
**5. Select your device, save, complie, flash**

  - The .ino should get random test data flowing to Fathym exactly as is, so we'll test everything before messing with the code
**6. Create a new Photon Part in your Fathym Homespace**

  - Create an  account at [community.fathym.com](http.//community.fathym.com) if you haven't already
  - From your homespace, click the plus "+" button to get to the catalog of addable parts
  - Choose the Particle Photon part
  - Add your Photon deviceID, which you can find on your [Particle Dashboard](https://dashboard.particle.io/user/devices)
**8. Enter your Photon Part on Fathym and add visualizations**
  - From inside your Particle Photon Part, click the plus "+" button to get to the catalog of addable parts
  - Start by adding the inspector display
  - Save and watch your data flow through!
## Customizing
**1. Inside Particle Dev, open the fathym.io-photon.ino file**
  - You'll see commented instructions about how and where to add code for your sensors
  - Note that fathym.set("attribute name", value, "units of measurement") formats the JSON to send to Fathym
**2. Open the Fathym.Build.h file**
  - Edit the attributes that are automatically sent along with your payload by setting each item to true or false 
  - Note that the Fathym.io library includes support Photon battery power - enable battery support by uncommenting the code at the bottom of the FathymBuild.h file
**3. Add additional dashboard visualizations for your device in Fathym**
  - From inside your Particle Photon part, click the plus "+" button to get to the catalog of addable parts
  - Try a Historc Value part
    - Fill out the "Property Name" field with one of the attributes you're sending from your Photon (the attribute name must be an exact, case-sensitive match). Leave this field blank to create a generic graph with dropdown menu of the attributes you're sending so you can switch the attribute on the fly.   
**4. Create a Fathym Notification**
  -

