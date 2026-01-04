# Software Development Chatbot

A web-based chatbot application powered by OpenAI's GPT-3.5 API for answering software development questions and providing coding assistance.

## Features

- Real-time chat interface
- Integration with OpenAI's GPT-3.5 Turbo model
- Clean and responsive UI
- Express.js backend server
- Error handling and API response validation

## Prerequisites

Before running this project, make sure you have:

- [Node.js](https://nodejs.org/) (v14 or higher)
- An [OpenAI API key](https://platform.openai.com/account/api-keys)
- npm (comes with Node.js)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Nobelgalido/software-dev-chatbot.git
cd software-dev-chatbot
```

2. Install dependencies:
```bash
npm install
```

3. Set up your API key:
   - Copy `config.example.js` to `config.js`:
   ```bash
   cp config.example.js config.js
   ```
   - Open `config.js` and replace `YOUR_API_KEY_HERE` with your actual OpenAI API key:
   ```javascript
   module.exports = {
       OpenAIAPIKey: 'sk-your-actual-api-key-here'
   };
   ```

## Usage

1. Start the server:
```bash
node server.js
```

2. Open your browser and navigate to:
```
http://localhost:3000
```

3. Start chatting with the AI assistant!

## Project Structure

```
software-dev-chatbot/
├── public/
│   ├── index.html      # Main HTML page
│   ├── style.css       # Styling
│   └── main.js         # Client-side JavaScript
├── server.js           # Express server setup
├── openai.js           # OpenAI API integration
├── config.js           # API key configuration (not tracked by git)
├── config.example.js   # Example configuration file
├── package.json        # Project dependencies
└── README.md          # This file
```

## Configuration

The application uses port 3000 by default. You can change this by setting the `PORT` environment variable:

```bash
PORT=8080 node server.js
```

## API Configuration

This chatbot uses OpenAI's GPT-3.5 Turbo model with the following settings:
- Model: `gpt-3.5-turbo-1106`
- Max tokens: 150

You can modify these settings in `openai.js`.

## Security Notes

- Never commit your `config.js` file containing your actual API key
- The `.gitignore` file is configured to exclude `config.js`
- Use `config.example.js` as a template for sharing configuration structure
- Consider using environment variables for production deployments

## Troubleshooting

### "Insufficient quota" error
- Check your OpenAI account billing at https://platform.openai.com/account/billing
- Ensure you have a valid payment method set up
- Verify you haven't exceeded your usage limits

### "Invalid API key" error
- Make sure you've copied your API key correctly to `config.js`
- Verify the API key is active in your OpenAI dashboard

### Server won't start
- Ensure port 3000 is not already in use
- Check that all dependencies are installed with `npm install`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Powered by [OpenAI API](https://openai.com/api/)
- Built with [Express.js](https://expressjs.com/)