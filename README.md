# WeatherForecasting-AR-App

<h2>Downloading and installing Unity</h2>
Download and install the Unity Editor from the Unity download page. The installer uses a Download Assistant and has detailed instructions to follow. If you want to download the Unity Editor using a torrent or install several versions of Unity at once, see Torrent Download, below.

<h3>Unity Download Assistant</h3>
The Unity Download Assistant is a small executable program (approximately 1 MB in size) which lets you select which components of the Unity Editor you want to download and install.

If you’re not sure which components you want to install, leave the default selections, click Continue, and follow the installer’s instructions.

<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/UnityDownloadAssistant_v52_75.png">
Unity Download Assistant (leave the default selections if youre not sure which to choose)
Unity Download Assistant (leave the default selections if you’re not sure which to choose)
Note that on PC there is Microsoft Visual Studio Community 2015.


<h2>Setting up your Project for Vuforia</h2>
<p>Setting up your project to develop Vuforia AR or MR mobile applications is very similar to the set-up process for building with Unity for a mobile platform. The Unity Installer includes the Vuforia SDK. Follow the instructions for downloading and installing Unity on the InstallingUnity manual page. Vuforia provides a selection of Prefabs designed to be dropped into a Scene to provide feature functionality to your application. These are all available from inside the Unity Editor.</p>
<p>You should adhere to the same performance considerations as required for developing regular mobile games. For information on optimising for mobile devices, see Unity documentation on mobile optimisation.</p>
<p>To get Vuforia set up with Unity:</p>
<ul>
<li>Install the latest version of Unity, and in the Unity component selection section of the installer, select Vuforia Augmented Reality Support, along with either the iOS Build Support or Android Build Support packages.</li></ul><br>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/installing_vuforia.png"><br>
<small>Installing Vuforia Augmented Reality support through Unity Installer</small>
<p><b>Note:</b>Most AR and MR applications target mobile devices, so the focus of this guide is development for Android and iOS. See guides for enabling build support for Android and iOS devices in the Getting Started documentation for Android and iOS.<br></p>
<ul>
<li>Create a Vuforia developer account from the Vuforia registration page. This account gives you access to the tools you need to make AR and MR applications with Vuforia in Unity.</li>
<li>If you have not already created a Unity ID, then do so from the Unity registration page. You need a Unity ID to download any packages from the Unity Asset Store.</li>
<li>Open Unity and create a new 3D Project (make sure the 3D option is selected next to the Add Asset Package button). Name your Project, then click the Create project button.</li>
</ul>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/new_project.png"></body><br>
<small>Creating a new 3D project</small>
<p><b>Tip:</b>Download the Vuforia AR+VR Sample package from the Unity Asset Store. This package provides useful example Scenes demonstrating important features. You will not need this for following this guide, but it is useful to have for further learning later.</p>
<h2>Activating Vuforia in Unity</h2>
<p>To activate Vuforia in your Unity project, access the Player Settings from <b>Edit</b> > <b>Project Settings</b> > <b>Player</b> and select the tab for the mobile device you are building to. Under <b>XR Settings</b>, tick the <b>Vuforia Augmented Reality Support checkbox</b>.</p>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/vuforia_ar_support.png"><br>
<small>Enabling Vuforia Augmented Reality Support in Unity Player Settings</small>
<p>Your Scene now contains two GameObjects: a main Camera, and a directional light. You need to add a new AR Camera to the Scene in order to enable AR functionality, and you need to delete the current <b>Main Camera</b> GameObject from the Scene.</p>
<p>To delete the Camera GameObject, select it in the <b>Hierarchy window</b> and press the delete key on your keyboard, or right click it and select <b>Delete</b>.</p>
<p>For more information on the individual settings in the XR Settings window, see the <u>Vuforia Platform Configuration page of this manual</u>.</p>
<h2>Adding a Vuforia AR Camera and other GameObjects</h2>
<p>To add an AR Camera to your scene, go to <b>GameObject</b> > <b>Vuforia</b> > <b>AR Camera</b>.</p>
<p>If this is the first Vuforia GameObject added to your Scene then Unity also prompts to import your Vuforia Assets. Select <b>Import</b>, and Unity imports all necessary Vuforia files into your project.</p>
<p>The <b>Project window</b> displays 4 new folders, one of which is called <b>Vuforia</b>. The code and Assets in this folder provide the main AR and MR functionality. The other folders provide sample Scenes, resources, tools, and plugins so that you can develop AR and MR applications for a variety of devices.</p>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/Importing_assets.png"><br>
<small>Empty project with all imported Vuforia assets</small>
<p>Create a new folder in your project. To do this, navigate to the Project window, click the <b>Create</b> button, and select <b>Folder</b>. Name this new folder Scenes and save a <u>new Scene</u> inside this folder.</p>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/New_folder.png"><br>
<small>Creating an empty folder and naming it Scenes</small>
<p>This process also adds a new ARCamera GameObject in your Scene hierarchy.</p>
<h2>Creating a Vuforia license key</h2>
<p>The last step in the setup process is to create a license key from the <u>License Manager section</u> of the Vuforia Developer Portal. You need to enter this into Unity’s Vuforia configuration settings in order to build and test your application with Unity.</p>
<p>Visit the <u>Vuforia Developer Portal</u> and log in (or create a new account). Navigate to the <b>License Manager</b> in the <b>Develop</b> section and click the <b>Get Development Key</b> button to open the <b>Add License Key</b> page.</p>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/creating_dev_key.png"><br>
<small>Creating a Vuforia Development Key</small>
<p>On the <b>Add License Key</b> page, enter a name for your app. Accept the terms and conditions, then click the <b>Confirm</b> button to generate a new license key.</p>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/vuforia_dev_key_details.png"><br>
<small>Confirming Vuforia development key details</small>
<p>On the next page, agree to the Vuforia Developer conditions (tick the box) and then click the <b>Confirm</b> button. This brings you back to the <b>Licence Manager</b> page where you can see your newly created license in a list where its status is <b>Active</b>. Click on the name of your App to view the license details. This allows you to retrieve your development license key.</p>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/license_manager.png"><br>
<small>License Manager</small>
<p>Copy the license key to the clipboard and navigate back to your Unity Project.</p>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/copying_license_key.png"><br>
<small>Copying your Vuforia License key</small>
<p>Select the <b>ARCamera</b> GameObject from the <b>Hierarchy window</b> and, in the Inspector window, navigate to the the <b>Vuforia Behaviour(Script)</b> component and click the <b>Open Vuforia configuration</b> button.</p>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/config_settings.png"><br>
<small>Accessing Vuforia configuration settings</small>
<p>The <b>Inspector window</b> displays a list of <b>Vuforia Configuration</b> options. Paste your Vuforia Development key into the <b>App License Key</b> text box under the Vuforia section and then click the <b>Add License</b> button.</p>
<img src="https://docs.unity3d.com/2017.3/Documentation/uploads/Main/entering_key.png"><br>
<small>Entering your Vuforia development key in the Vuforia Configuration settings</small>
<h2>Testing your set-up</h2>
<p>To test Vuforia apps in the Unity Editor, you need to have a webcam connected to your PC or laptop. As a final step to make sure Vuforia is now installed properly in your Unity Project, press the <b>Play</b> button to test your Scene. If Vuforia is set up correctly, a video feed from your webcam appears in the Editor Game View.</p>
<p>Now you are ready to set up Image Targets and add AR functionality to your Project.</p>
