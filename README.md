Setting Up AWS Code Commit
---
Note: This is for Mac/Linux users.

```
cd $HOME/.ssh
ssh-keygen
[here just create the name codecommit_rsa and leave all fields blank *just click enter*]
touch config
chmod 600 config
```

Now we need to enter our codecommit_rsa.pub into IAM.

```
nano config

Host git-codecommit.*.amazonaws.com
  User [YOUR_SSH_KEY_ID_FROM_IAM]
  IdentityFile /Users/andrewpuch/Desktop/codecommit/
```

Now lets test to verify it works.

```
ssh git-codecommit.us-east-1.amazonaws.com
```

You should see.
---
You have successfully authenticated over SSH. You can use Git to interact with AWS CodeCommit. Interactive shells are not supported.Connection to git-codecommit.us-east-1.amazonaws.com closed by remote host.
