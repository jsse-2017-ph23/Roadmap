# JSSE roadmap
This roadmap describes each module in this organization, their responsibility, implementation
methods and some references.

## Web Client
[Github repository](https://github.com/jsse-2017-ph23/web-frontend)

Hosted on [Firebase Hosting]. Built with [React].

Connect to [Firebase realtime database] and [Firebase storage]

[Firebase Hosting]: https://firebase.google.com/docs/hosting/
[React]: https://facebook.github.io/react/
[Firebase realtime database]: https://firebase.google.com/docs/database/
[Firebase storage]: https://firebase.google.com/docs/storage/web/download-files

## Rpi button module
Node JS

Connect to Firebase realtime database using [Admin SDK]. Also include [offline detection]

Remember to set client ID to `worker-rpi`

[GPIO library for Node JS]

[Admin SDK]: https://firebase.google.com/docs/database/admin/start
[offline detection]: https://firebase.google.com/docs/database/web/offline-capabilities
[GPIO library for Node JS]: https://github.com/fivdi/onoff

## Rpi streaming module
[Github repository](https://github.com/jsse-2017-ph23/rpi-streaming)

Python

[Take photo] -> [upload] to GCloud cloud storage

[Take photo]: http://picamera.readthedocs.io/en/release-1.13/recipes1.html
[upload]: https://cloud.google.com/storage/docs/object-basics#storage-upload-object-python

## Firebase functions
[Github repository](https://github.com/jsse-2017-ph23/firebase-functions)

[Cloud functions docs]
 - [x] Create status log from status change
 - [x] [Cloud messaging] when status change 
 - [x] Remove old images [periodically]
 - [x] Clean up logs periodically
 - [x] Sync Firebase Storage photo url to realtime database

[Cloud functions docs]: https://firebase.google.com/docs/functions/
[Cloud messaging]: https://firebase.google.com/docs/cloud-messaging/admin/send-messages
[periodically]: https://firebase.googleblog.com/2017/03/how-to-schedule-cron-jobs-with-cloud.html

## App engine
[Github repository](https://github.com/jsse-2017-ph23/app-engine)

App engine is needed to trigger cron job in firebase functions

Code deployed to app engine are copied directly from [functions-cron].

[functions-cron]: https://github.com/firebase/functions-cron