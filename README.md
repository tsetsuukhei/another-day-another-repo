# Creating an Aircampi Auth Image on Docker

## Prerequisite
Make sure you have installed the following applications on your development machine:
- ### [Download Docker](https://docs.docker.com/get-docker/)
  
- ### [Download Postman](https://www.postman.com/downloads/)

## Creating a Personal Access Token (PAT) on Github

1. Sign into your Github account, click on your profile on the upper-right corner, and go to **Settings**. 

![alt text](https://github.com/tsetsuukhei/E-Mongo1ia/blob/main/tutorial/github-1-settings.png?raw=true)

2. In the left sidebar, click on **Developer settings**.

![alt text](https://github.com/tsetsuukhei/E-Mongo1ia/blob/main/tutorial/github-2-developer-settings.png?raw=true)

3. In the left sidebar, click on **Personal access tokens**.

![alt text](https://github.com/tsetsuukhei/E-Mongo1ia/blob/main/tutorial/github-3-pat.png?raw=true)

4. Click on **Generate new token**.

![alt text](https://github.com/tsetsuukhei/E-Mongo1ia/blob/main/tutorial/github-4-new-token.png?raw=true)

5. Give your token a name. E.g. "Work Mac".

![alt text](https://github.com/tsetsuukhei/E-Mongo1ia/blob/main/tutorial/github-5-note.png?raw=true)

6. On the expiration drop-down menu, select **No expiration**.

![alt text](https://github.com/tsetsuukhei/E-Mongo1ia/blob/main/tutorial/github-6-expiration.png?raw=true)

7. On Select Scopes, click on **repo** and **write:package**.

![alt text](https://github.com/tsetsuukhei/E-Mongo1ia/blob/main/tutorial/github-7-scope.png?raw=true)

8. Click **Generate token**.

![alt text](https://github.com/tsetsuukhei/E-Mongo1ia/blob/main/tutorial/github-8-generate.png?raw=true)

9. **Copy your token that starts with "ghp..."**

## Exporting PAT

1. Open your Terminal and type in the following commands to export your PAT


  ```
  vi ~/.zprofile
  ```
Press **i** to insert

  ```
  export PAT=<your PAT>
  ```

Press **esc** to stop inserting

Press **shift+q** to exit

Type in **wq** to save or !q to not save 

2. Check your PAT

  ```
  echo $PAT
  ```
  
If it prints your PAT, you have successfully exported your PAT.
  
## Login with Docker

Type in the following command on your terminal

  ```
  echo $PAT | docker login ghcr.io --<username> phanatic --password-stdin
  ```

## Compose with Docker

1. Create a new folder on your computer and download the following files into the folder
2. 
[Download docker-compose.yml](https://drive.google.com/file/d/1TqsxFnW-t2mMnvF6OpqPhDw4wuuRz7Tp/view?usp=sharing)

[Download nginx.conf](https://drive.google.com/file/d/106KN2EVwn780wVUK-e8PrAuEtye-9kew/view?usp=sharing)


2. Open up your terminal and go to your working directory where you downloaded the files.

3. Type in the following commands

  ```
  docker compose up
  ```

