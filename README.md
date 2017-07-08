# JSSE roadmap
This roadmap describes each module in this organization, their responsibility, implementation
methods and some references.

## Web Client
Hosted on [Firebase Hosting]. Built with [React].

Connect to [Firebase realtime database] and [Firebase storage]

Currently missing in UI: Show previous images from Cloud Storage

[Firebase Hosting]: https://firebase.google.com/docs/hosting/
[React]: https://facebook.github.io/react/
[Firebase realtime database]: https://firebase.google.com/docs/database/
[Firebase storage]: https://firebase.google.com/docs/storage/web/download-files

## Rpi button module
Node JS in docker

Connect to Firebase realtime database using [Admin SDK]. Also include [offline detection]

Remember to set client ID to `worker-rpi`

[GPIO library for Node JS]

[Admin SDK]: https://firebase.google.com/docs/database/admin/start
[offline detection]: https://firebase.google.com/docs/database/web/offline-capabilities
[GPIO library for Node JS]: https://github.com/fivdi/onoff

## Rpi streaming module
Python in docker

[Take photo] -> [upload] to GCloud cloud storage

[Take photo]: http://picamera.readthedocs.io/en/release-1.13/recipes1.html
[upload]: https://cloud.google.com/storage/docs/object-basics#storage-upload-object-python

## Firebase functions
[Cloud functions docs]

Create status log from status change

[Cloud messaging] when status change

Remove old images

[Cloud functions docs]: https://firebase.google.com/docs/functions/
[Cloud messaging]: https://firebase.google.com/docs/cloud-messaging/admin/send-messages
