Google App Engine dashboard
https://console.cloud.google.com/appengine

Create a new code repository:
Google Cloud Platform -> Development -> Source code

Add Google Cloud source repository
--------
https://cloud.google.com/source-repositories/docs/adding-repositories-as-remotes

$ gcloud init

$ git config credential.helper gcloud.sh

$ git remote add google \
  https://source.developers.google.com/p/fuzzylizbot/r/lizbot

Push changes from local rep to google cloud
--------
https://console.cloud.google.com/code/develop/repo?project=fuzzylizbot

$ git add ...
$ git commit -m "...."
$ git push --all google



Deploy app:
--------
$ gcloud app deploy app.yaml --project fuzzylizbot -v <version_id> --verbosity=info

Open app in the browser:
$ gcloud app browse

Read logs from default application:
$ gcloud app logs read --service default --limit 10


Delete old app versions
--------
List all versions:
$ gloud app versions list

Delete vesions:
$ gcloud app versions delete v1 v2

From GUI:
http://stackoverflow.com/questions/34597576/cli-400-error-deploying-to-google-app-engine

Request logs from logger module
--------
https://cloud.google.com/appengine/docs/standard/python/tools/downloading-logs
https://console.cloud.google.com/logs?_ga=1.195045804.1680263653.1487352034
