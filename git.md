# Oppgave 3

## GIT
```javascript
// Sette opp git lokalt
// Sette opp nytt repo i Github
$ git init
$ touch .gitignore && echo "node_modules" > .gitignore
$ git add .gitignore
$ git commit -m "initial commit"
$ git remote add origin https://github.com/Aricin86/Leksjon-3.git
$ git push -u origin master

// Lage dev branch lokalt
$ git checkout -b dev

// Lage fil i dev branch lokalt (hiof.js fil med console.log("hiof"))
$ touch hiof.js && echo "console.log(\"hiof\");" > hiof.js

// Commite disse
$ git commit -am "initial dev commit" // Fikk beskjed om å "adde". Fulgte det Marius gjorde i filmen met "set-upstream"

// Pushe endringene til repo
$ git push --set-upstream origin dev
// Så i git status at hiof.js ikke var commited, så gjorde det på nytt:
$ git add hiof.js
$ git commit -m "initial dev commit"
$ git push

// Lage en fil i dev branch remote
// Hente endringene lokalt
$ git fetch
$ git pull

// Merge filene fra dev i master
$ git checkout master
$ git merge dev
$ git add .
$ git commit -m "merged dev branch with master"
$ git push

// Samarbeide med en kollega eller en annen konto du har for å få til merge conflict
$ touch conflict.js && echo "const y = \"Let's make a merge conflict! \";" > conflict.js
$ git add .
$ git commit -m "making a merge conflict"
$ git push

// Resolve merge conflict
$ git fetch
$ git pull
$ git add .
$ git commit -m "fixed merge conflict"
$ git push
```
