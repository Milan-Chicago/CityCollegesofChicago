## :books: Quick Review

# This repo was copied from the original repository here:  https://github.com/ai-kadhim/practice_repo/tree/main 

Homework Review:  Command Line and Terminal Commands

We will be using some terminal commands, so let's make sure you know what they are and what they do! 

| Command      | Stands For |  Description |
| ----------- | ----------- | -------------|
| `ls`      | long listing       | lists all files and directories in the present working directory |
| `ls -a`  | long listing all   |  lists hidden files as well |
| `cd {dirname}`      | change directory       | to change to a particular directory |
| `cd ~`   | change directory home        | navigate to HOME directory |
| `cd ..`      | change directory up       | move one level up |
| `cat {filename}`   | concatenate        | displays the file content |
| `sudo`      | superuser       | allows regular users to run programs with the security privileges of the superuser or root |
| `mv {filename} {newfilename}`   | move        | renames the file to new filename |
| `clear`      | clear       | clears the terminal screen |
| `mkdir {dirname}`   | make directory        | create new directory in present working directory or at specified path |
| `rm {filename}`   | remove        | remove file with given filename |
| `touch {filename}.{ext}`   | touch        | create new empty file |
| `rmdir {dirname}`   | remove directory        | deletes a directory |
| `ssh {username}@{ip-address} or {hostname}`   | secure shell        | login into a remote Linux machine using SSH |

<p></p>


## <img src="https://octodex.github.com/images/original.png" width=40px/> Setting up GitHub!


<details>
  <summary>Generating a GitHub Access Token</summary>
     
**Create an account with GitHub [here](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) if you do not have one.**

Navigate to [GitHub's Developer Token settings](https://github.com/settings/tokens).
Click on `Generate new token` > `Generate new token (classic)`
![Screenshot 2023-08-30 at 8 16 58 PM](https://github.com/AI-Maker-Space/LLMOps-Dev-101/assets/37101144/d6f57901-6e69-42e5-a22c-37b48ff6e3fc)

Give the token a description, set the expiration (we recommend 90 days), and check every box. When you're done, click `Generate token` at the bottom of the page. 

![Screenshot 2023-08-30 at 8 36 14 PM](https://github.com/AI-Maker-Space/LLMOps-Dev-101/assets/37101144/451bad7b-ec8a-4429-a5bb-8d0212d00f50)

Copy the access token and save it for later use. We will use this token to interact with GitHub. Please do not lose this access token or you will need to generate a new one.

![image](https://github.com/AI-Maker-Space/LLMOps-Dev-101/assets/37101144/f98c9644-e44b-4fd3-8590-db513bef6360)

</details>

<details>
  <summary>Github SSH Setup</summary>
  Secure Shell Protocol (SSH) provides a secure communication channel of an unsecured network.  Let's set it up!
  
  <p></p>

  1. Generate a Private/Public SSH Key Pair.
    
  ```console
  ssh-keygen -o -t rsa -C "your email address for github"
  ```

  2. Save file pair.  Default location `~/.ssh/id_rsa` is fine! 
  

  3. At the prompt, type in a secure passphrase.
  4. Copy the contents of the public key that we will share with GitHub. 

     * Mac: `pbcopy < ~/.ssh/id_rsa.pub` 

     * Windows (WSL): `clip.exe < ~/.ssh/id_rsa.pub`

     * Linux: `xclip -sel c < ~/.ssh/id_rsa.pub`
  
  5. Go to your GitHub account and go to `Settings`. 
  
  6. Under `Access`, click on the `SSH and GPG keys` tab on the left.

  ![image](https://github.com/AI-Maker-Space/LLMOps-Dev-101/assets/37101144/5fb54f16-7279-49c4-bda3-2da36cbbc306)


  7. Click on the `New SSH Key` button.
  
  ![image](https://github.com/AI-Maker-Space/LLMOps-Dev-101/assets/37101144/d5551c28-9d70-438c-b45d-43698384e3ff)

  
  8. Name the key, and paste the public key that you copied. Click the `Add SSH Key` button
  

  ![image](https://github.com/AI-Maker-Space/LLMOps-Dev-101/assets/37101144/8f7c4496-0e88-4058-9baf-73495322db8b)


</details>

<details>
  <summary>Viewing the Repositories</summary>

Login and click on the top right user icon, then go to `Your repositories`. 

<p align="center">
  <img width="648" alt="image" src="https://github.com/AI-Maker-Space/LLMOps-Dev-101/assets/37101144/18b766c6-ca91-4926-ad79-5fc101c3e6a0">
</p>
</details>


<details>
  <summary>Creating a New Repository</summary>

When viewing the respository page, click on `New` and proceed to create your repo.


<p align="center">
  <img width="335" alt="image" src="https://github.com/AI-Maker-Space/LLMOps-Dev-101/assets/37101144/dba31b88-0058-499c-a891-349de2d35279">
</p>
<hr>

**Filling Respository Details**

Create the repository by inputting the following:
* `Repo name`
* `Repo description`
* Make repo `public`
* Add a `README`
* Add `.gitignore` (Python template)
* Add `license` (choose MIT)

Then click `Create Repository`.


<p align="center">
  <img width="724" alt="image" src="https://github.com/user-attachments/assets/109f02e3-f23d-4088-b429-dea6cd6d9e3e">
</p>

</details>

<details>

<summary>Clone Your Repo</summary>

  1. Open your terminal and navigate to a place where you would like to make a directory to hold all your files for this class using the command `cd`. 


  ```console
  cd {directory name}
  ```
  
  2. Once there, make a top level directory using `mkdir`. 

  ```console
  mkdir {directory name}
  ```

  3. `cd` into it and make another directory called `code`. 

  ```console
  cd {directory name}
  ```

  ```console
  mkdir code
  ```

  4. `cd` into it and run your `git clone {your repo url}` command. 

  ```console
  cd code
  ```

  ```console
  git clone {your repo url}
  ```

</details>
