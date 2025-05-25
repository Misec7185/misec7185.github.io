# A simple static website for misec.us

To reduce expenses, we decided to move from the old site to a static site.
Plain HTML content with some flavor added via BlumaCSS.

# Contributing

## Setting up an SSH key for github

1. Gain access to misec's organization
2. Set up SSH key 
  - `ssh-keygen -t ed25519 -C "your-org-email@example.com" -f ~/.ssh/id_ed25519_org` Use a unique filename to avoid personal ssh keys
  - `ssh-add ~/.ssh/id_ed25519_org`
  - Copy the public key to github settings on your profile
  - `nano ~/.ssh/config` Add the following, match the hostname to ssh file name
    ```
    Host github.com-org
        HostName github.com
        User git
        IdentityFile ~/.ssh/id_ed25519_org
        IdentitiesOnly yes
    ```
  - SSH key and an alias for github.com is now created and used locally
3. Set up git config
  - `git clone git:github.com-org:Misec7185/misec7185.github.io.git misec-static`
  - `cd misec-static`
  - `git config user.name "Your Org Username"`
  - `git config user.email "your-org-email@misec.us"`

# References

  - https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
