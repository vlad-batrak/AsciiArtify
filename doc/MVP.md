# Minimum viable product (MVP)

## Automate deployment of Ambassador application by the Argo CD service

1. Setting up the CD conveyor in Argo CD

![Setup new App](img/ArgoCD_newApp-1.PNG)

![Setup new App](img/ArgoCD_newApp-2.PNG)

![Setup new App](img/ArgoCD_newApp-3.PNG)

2. Result

![Setup new App](img/ArgoCD_newApp-4.PNG)

![Setup new App](img/ArgoCD_newApp-5.PNG)

3. Synchronization with the repository

![Setup new App](img/ArgoCD_newApp-6.PNG)

4. Let's create a fork of the original repository and change the application settings of the **REPO URL** and **AUTO SYNC POLICY** is **"Enabled"**.

![Setup new App](img/ArgoCD_newApp-7.PNG)

5. Сhange the file /helm/values.yaml in the repository and make a commit

![Setup new App](img/ArgoCD_newApp-8.PNG)

6. After 3 minutes, Argo CD will compare the git-repository with the application configuration and begin auto synchronization

![Setup new App](img/ArgoCD_newApp-9.PNG)


### Demo

Gif-demo

![Demo MVP](img/demo3.gif)

or asciicast

[![asciicast](https://asciinema.org/a/psj8TY9PKagLMg9SYOdXCt0vh.svg)](https://asciinema.org/a/psj8TY9PKagLMg9SYOdXCt0vh)

