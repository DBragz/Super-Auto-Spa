# Super Auto Spa

## Generate GitHub Access Token

1. Sign in to your GitHub account at [github.com](github.com).
   
2. Click on your profile picture in the upper right corner, and select **"Settings."**

3. In the left sidebar, click on **"Developer settings."**

4. Under **"Developer settings,"** select **"Personal access tokens."**

5. Click on **"Tokens (classic)"** if you want to generate a classic token.

6. Click the **"Generate new token"** button.
   
7. In the form that appears, give your token a descriptive name and select the scopes or permissions you'd like to grant this token. For basic access, you might select:

- `repo` (to access your private repositories),
- `workflow` (to access GitHub Actions workflows),
- any other necessary scopes based on your needs.

8. After configuring the permissions, click **"Generate token."**

9. Copy the generated token and store it securely. You will not be able to see it again once you navigate away from the page.

Make sure you keep your token secure, as it provides access to your GitHub account based on the scopes you selected. Use this token as a password when prompted during Git operations.

## Add Secret to Replit Workspace

1. Open the **Tools** pane and select **Secrets**.

2. Click + **New Secret**.

3. Use the same key name as your Account Secret.

4. Copy the value from your Account Secret and paste it into the Value field.

5. Click **Add Secret**.

## Use GitHub Access Token as Secret

1. Open the **Shell** tool from the Tools pane in Replit.

2. **Configure Git** (if you haven’t already):

- Set your username and email:

    ```shell
    git config --global user.name "Your Name"
    git config --global user.email "your.email@example.com"
    ```

3. Add your remote repository:

- Use your GitHub access token from the secret you created. Replace `your-username` with your GitHub username, `your-repo` with your repository name, and `YOUR_SECRET_NAME` with the name of your secret:

    ```shell
    git remote add origin https://your-username:$(echo             $YOUR_SECRET_NAME)@github.com/your-username/your-repo.git
    ```

## Requirements

- [Node.js 20.18.1+](https://nodejs.org/)

## Installation

1. Install web application dependencies.

    ```shell
    npm install
    ```

## Development

1. Start the development server.

    ```shell  
    npm dev
    ```

## Build

1. Build the web application.

    ```shell
    npm build
    ```

## Preview

1. Run the production version of application locally.

    ```shell
    npm preview
    ```

## Authors

- [Daniel Ribeirinha-Braga](https://github.com/DBragz)
- [Editor](https://github.com/replit) - AI Code Assistant
