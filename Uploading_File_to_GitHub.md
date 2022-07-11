Uploading File to GitHub using Git

(https://zhuanlan.zhihu.com/p/136355306)

- Install the xcode tool https://stackoverflow.com/questions/52522565/git-is-not-working-after-macos-update-xcrun-error-invalid-active-developer-pa
```
shuozhen@Bun Downloads % xcode-select --install
```
- Generate SSH key and upload to GitHub
  - Check if there's already a SSH (I used the same one for farnam)
  ```
  cd ~/.ssh
  ls
  cat 
  ```
  - Generate a public key if there's no existing one
    - Generate for GitHub directly （https://docs.ycrc.yale.edu/clusters-at-yale/access/ssh/）
    ```
    ssh-keygen
    ```
    - Generate first and upload to GitHub via setting
- Initiate a branch in local
```
cd working_directory
git init
```
- Upload the folder or file
```
git add ./scRNA-CNV 
git commit -m "%comments"
```
- Correlates the local branch with the repository

  - Check the existing remotes
  ```
  git remote -v
  ```
  - Change the remotes if needed
  ```
  git remote set-url origin https://github.com/USERNAME/REPOSITORY.git
  ```
  - copy the SSH link under the repository
```
git remote add origin git@github.com:Shuozhen/DBiT-Advanced.git
```  
- Upload the file
```
git push -u origin master
```
