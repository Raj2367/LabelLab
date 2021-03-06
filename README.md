# LabelLab
LabelLab is an image analyzing and classification platform. The application should allow users to upload batches of images and classify them with labels. It will also have the features to run classifications against a trained model. LabelLab also has a user project management component as well as an image analyzing component.

## User Guide

#### How to Setup

Clone the repository.

`git clone https://github.com/scorelab/Labellab.git`

#### Set up react server

Run npm install in labellab-client folder.

```
 cd labellab-client/
 npm install
 ```
 
#### Set up MongoDB Backend

Run npm install in labellab-server folder.

```
 cd labellab-server/
 npm install
 ```
    
#### How to Use

Use two terminals, one for labellab-server and the other for labellab-client. <br/> <br/>
First you need to create a `.env` file in both labellab-server folder and labellab-client folder and fill it with the template provided in the file `.env.example` which is present in both the folders.<br/> <br/>
For client side `.env` file:
```
REACT_APP_HOST=localhost
REACT_APP_SERVER_ENVIORNMENT=dev
REACT_APP_SERVER_PORT=4000
```
For server side `.env` file:
```
HOST=localhost
PORT=4000
```
`JWT_SECRET` can be any word your choice. For the next 5 fields visit `mlab.com` and create a MongoDB database and find a URI of your database and fill the values accordingly.<br/><br/>

Run the Node server in the labellab-server folder:
    
`$ npm start`

Run the Nodemon server in the labellab-server folder:

`$ npm run dev`

> **NOTE**: Before starting the server create a file named `.env` same as `.env.example` and add your **OAUTH** and **DATABASE** credentials in the file.

start the npm server in labellab-client directory.

`npm start`

And use [localhost:3000](https://) to browse.


> **NOTE**: This version is only supporting for Chrome and Firefox browser. And make sure to instal the extension -> Redux Dev Tools in chrome extension library.

#### How to Use (Mobile)
Run the Node server in the labellab-server directory (if not already done):

`npm start`

In a new terminal navigate to `labellab_mobile` directory.

Configure the `lib/config.dart` using the format provided in `lib/config_example.dart`.
<br><br>
Application needs `google-services.json` issue from firebase to run google sign in option.To obtain the file,

1. Sign in to https://console.firebase.google.com/.
2. Click **Add Project** and necessary information about the project.
3. Agree to the terms and click **Create Project**.
4. After creating the project, click **Add Firebase to your android app**.
5. Go to project location and open `android/app/src/main/AndroidManifest.xml`.Copy the package name(**org.scorelab.labellab_mobile**) and paste in the package name field
6. Get the **SHA1 fingerprint** by following the instruction and paste it in the SHA1 fingerprint field.
7. click next and download the `google-services.json`.
8. paste the file in location `android/app/` folder.

Build flutter the application

`flutter build apk`

> **NOTE**: Use 'ios' instead of 'apk' to build for iOS

or run the flutter application

`flutter run`

> **NOTE**: A device with USB debugging enabled or virtual device is required
