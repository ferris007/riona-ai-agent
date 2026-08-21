## Riona-AI-Agent 🌸

Riona-AI-Agent is an AI-powered automation tool designed to interact with various social media platforms, including **Instagram**, **Twitter**, and **GitHub**. It leverages advanced AI models to generate engaging content, automate interactions, and manage social media accounts efficiently.

You can personalize the agent by training it with various data sources to match your desired personality and style.

## Features

- **Instagram Automation**: Automatically log in, post photos, like posts, and leave thoughtful comments.
- **Twitter Automation**: (Coming soon) Automatically tweet, retweet, and like tweets.
- **GitHub Automation**: (Coming soon) Automatically manage repositories, issues, and pull requests.
- **AI-Powered Content Generation**: Use Google Generative AI to create engaging captions, comments, and tweets.
- **Proxy Support**: Use proxies to manage multiple accounts and avoid rate limits.
- **Cookie Management**: Save and load cookies to maintain sessions across restarts.

## Installation

1. **Clone the repository**:

   ```sh
   git clone https://github.com/ferris007/Riona-AI-Agent.git
   cd Riona-AI-Agent
   ```

2. **Install dependencies**:

   ```sh
   npm install
   ```

3. **Set up environment variables**:
   Create a `.env` file in the root directory (you can rename the `.env.example` file) and add your credentials.

   ```dotenv
   # Instagram credentials
   IG_USERNAME=your_instagram_username
   IG_PASSWORD=your_instagram_password 
   
   # Twitter credentials
   X_USERNAME=your_twitter_username
   X_PASSWORD=your_twitter_password

   # MongoDB URI
   MONGODB_URI=mongodb://localhost:27017/riona-ai-agent
   ```

## MongoDB Setup (Using Docker)

1.  **Install Docker**:
    If you don't have Docker installed, download and install it from the [official website](https://www.docker.com/products/docker-desktop/).

2.  **Run MongoDB using a Docker Container**:

    ```sh
    docker run -d -p 27017:27017 --name riona-ai-mongodb -v mongodb_data:/data/db mongodb/mongodb-community-server:latest
    ```
    This command will keep your data even if the container is stopped or removed.

3.  **Verify the connection**:
    Open a new terminal and run `docker ps`. You should see the `riona-ai-mongodb` container running.

### Docker Commands (Optional)

-   To stop the container: `docker stop riona-ai-mongodb`
-   To start the container: `docker start riona-ai-mongodb`
-   To remove the container: `docker rm riona-ai-mongodb`
-   To remove the container and its data: `docker rm -v riona-ai-mongodb`

## Usage

1. **Run the agent**:
   ```sh
   npm start
   ```

The default agent is Instagram. You can change the agent in the configuration.

**Upcoming Commands:**

- **Run the Twitter agent** (Coming soon):

  ```sh
  npm run start:twitter
  ```

- **Run the GitHub agent** (Coming soon):
  ```sh
  npm run start:github
  ```

## Project Structure

- **src/client**: Contains the main logic for interacting with social media platforms.
- **src/config**: Configuration files, including logger setup.
- **src/utils**: Utility functions for various tasks.
- **src/Agent**: Contains the core AI agent logic and training scripts.
- **src/schema**: Database models and schemas.
- **src/test**: Test files and data.

## Logging

Logs are stored in the `logs` directory, managed by a custom logger.

## Error Handling

The application includes robust error handling to catch and log unhandled exceptions and promise rejections.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.

## Acknowledgements

- [Google Generative AI](https://ai.google/tools/)
- [Puppeteer](https://github.com/puppeteer/puppeteer)
- [puppeteer-extra](https://github.com/berstend/puppeteer-extra)
