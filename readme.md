# Let's Start GithubAction Concepts
 
1. Create a Repository in GitHub called CICDPipeLine-GithubAction
2. Create a Folder Called GithubAction (you can create with any name) and open it in VSCode
3. Install Nodejs and check the version using node -v and npm -v command
4. In VSCode Add the extension GitHub Action from GitHub, GitHub Co-pilot
5. Initialize the git local Repo and push the code to remote repo 
6. Create test.html file and commit it locally and then push to the remote repo







name: CI pipeline
on: push
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Printing a message
        run: echo "Hello, World!"
      - name: Show Current time
        run: date
      - name: List files
        run: ls -la
      - name: Print Workflow event
        run: echo "${{ github.event_name }}"
      - name: Show GitHub workspace
        run: echo "${{ github.workspace }}"
      - name: Show Runner OS
        run: echo "${{ runner.os }}"
      - name: Show Github Repository
        run: echo "${{ github.repository }}"