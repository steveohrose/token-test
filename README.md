# Design System Tokens

GitHub Sync
Storing tokens on GitHub makes a lot of sense. It's version controlled, allows you to work in different branches (think of a brand refresh that lives on a different branch than the current live version) and gives you varying access levels such as Read or Write access. Also you can integrate GitHub Actions which will allow you to create a token pipeline with Style Dictionary or other tools.

Already have a GitHub account with a repository? Great, skip to step 3

1. Create a GitHub account
Go to https://github.com/signup and create an account.

2. Create a new repository
Go to https://github.com/new and create a new repository. Give it any name you like, make it public or private and initialize it with a README.

3. Generate your Personal Access Token
Go to the Personal Access Tokens section by clicking here, or click on your Avatar in the top right, go to Settings > scroll down to Developer Settings > Personal Access Tokens and generate a new token and select scope repo, decide for yourself when that token should expire. Scroll down and click Generate token.

Copy that token, you'll need it in a second and won't see it again if you close the page.

Also, never share this token with anyone who shouldn't have access to your repository. The token I shared in the video above was deleted already, treat it like your personal password.

4. Add a new GitHub sync to your Tokens file.
Go to the Sync tab and select GitHub. Add a new item

Add any name (this is only used for the plugin UI)
Add your Personal Access Token which we just copied.
Add your GitHub repository (e.g. six7/figma-tokens)
Add your default branch (probably main)
Specify a file path where your tokens should be stored, e.g. data/tokens.json or just tokens.json
5. Push your initial set of tokens
The plugin will now ask you to push your currently stored tokens to the repository.

Add a commit message, e.g. "Initial commit"

If you're adding a repository that already contains tokens, the plugin will ask you if you want to pull the latest tokens. This will overwrite your locally stored tokens, so make sure to back these up if you don't want them to get removed.

6. Push or pull changes
Whenever you make a change in Figma Tokens, you have to manually hit Push to GitHub to push your local changes to the remote. Anytime you do that you have to supply a commit message. You can choose the branch you want to push your changes to, so you could just try new tokens out without overwriting the currently live ones.

If you only want to pull the latest changes, hit Pull from GitHub. The plugin will let you know when your local changes differ from the ones stored on the remote by showing a blue dot.
