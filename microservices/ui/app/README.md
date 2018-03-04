# zapier-backup

## What is it?

Zapier backup is used to upload your files to Hausra server and trigger a backup for the same file on Google Drive.
The drive link where all the backups get saved is: https://drive.google.com/open?id=1pYSTjW7pooVf3_kUXm_vj-cZVAVt9JSb

## How it works?

### Workflow

You follow the following steps to upload your file:

1. Login/Sign-Up at http://ui.akin49.hasura-app.io/
2. You will be taken to upload page.
3. Drag and drop the file you want to upload.
4. Click the upload button, to upload the file and trigger backup.

### Internal Implementation

1. When the user uploads the file, the file is sent to the backend.
2. Various validations are performed like valid type of file etc.
3. If all validations succeed, the backend pushes the file to Hasura infra.
4. As soon as the the backend receives the response from Hasura about successful file upload, it triggers a backup to save the file to Google Drive using Zapier Zap.

## What does it use?

1. [Hasura](https://hasura.io)
2. [Zapier](https://zapier.com/)


## How to build on top of this?

The backend is written in Python using the Flask framework. The source code lies in `microservices/app/src` directory. `server.py` is where you want to start modifying the code.

Frontend uses React-JS and the source code lies in ``microservices/ui/app/src``

## Support

If you happen to get stuck anywhere, please contact us at vikasprasad.prasad@gmail.com or amalchandrandev@gmail.com

You can create pull requests for any contribution.
