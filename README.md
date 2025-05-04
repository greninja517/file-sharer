# file-sharer
This is the helm chart Source code of file sharing application.
File Sharing Application Source Code:
https://github.com/greninja517/file-sharing-application.git

# Publishing the Helm Chart through github Pages
First, you have to create a new branch(gh-pages) that will contain only two files.i.e.
i. .tgz file
ii. index.yaml file

Step 1: Packaging
```bash
helm package <chart_path>
```

Step 2: Generate the index file
```bash
helm repo index . --url https://<your-username>.github.io/<repo-name>
```

Step 3: Push the Changes to Github and then go to Settings -> Pages . Select the 
branch-name and directory to serve. And, done.


Now, you can locally run:
```bash
helm repo add <local-repo-name> https://<your-username>.github.io/<repo-name>/
helm install my-release <local-repo-name>/<chart-name>
```
And, the application runs. BOOM !!!
