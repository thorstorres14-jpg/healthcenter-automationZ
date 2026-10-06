# RHU Health Center System

Static web app (GitHub Pages) + Firebase Auth + Firestore.

## Setup
1. Firebase Console: create a project. Firestore: region `asia-southeast1`, production mode.
2. Authentication: enable Email/Password.
3. Project settings: add a Web app and copy the config into `firebase-config.js`.
4. Firestore > Rules: paste `firestore.rules` and publish.
5. Authentication > Settings > Authorized domains: add `<username>.github.io`.
6. Push these files to a GitHub repo. Settings > Pages > deploy from the main branch (root).
7. Open the site right away. On first run it asks you to create the administrator account.
   Do this immediately after deploying, before anyone else visits.
8. Admin > Users: create the other staff accounts and choose their roles.

## Notes
- Use test data only until the LGU data privacy requirements are settled.
- Clinical data lives in `visits` and `prescriptions`, which Security Rules limit by role.
- Patient registration needs an internet connection. Reads work offline from the cache.
