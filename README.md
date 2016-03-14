# StackRiot-Labs
Boilerplate Meteor app deployed using [dokku](http://dokku.viewdocs.io/dokku/).

### Clone
```
git clone https://github.com/sethbergman/stackriot-labs.git && cd stackriot-labs
```
### Create Dokku App
You will need to ssh into the dokku host for this step.
```
dokku apps:create app-name
```
### Add Remote Deploy Target
```
git remote add dokku dokku@your-dokku-host.com:app-name
```
### Configure ROOT_URL
This is specific to Meteor in regards to Dokku.
```
dokku config:set ROOT_URL=http://app-name.your-dokku-host.com
```
### Deploy Your App :rocket:
```
git push dokku master
```
