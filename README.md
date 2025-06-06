# 24Fire API CLI

A command-line interface tool for interacting with the 24Fire hosting service API. This tool allows you to fetch and display information about your KVM servers, webspaces, and domains in a user-friendly format.

## Features

- 🔥 Interactive service selection
- 🎨 Colorized terminal output
- 📊 Support for KVM, Webspace, and Domain services
- 🔐 Secure API key management via environment variables
- 📋 Clean, formatted data display

## Prerequisites

- Python 3.6 or higher
- A valid 24Fire API key

## Installation

1. Clone this repository:
```bash
git clone https://github.com/SyncWide-Solutions/24fire-api-cli.git
```

2. Navigate to the project directory:
```bash
cd 24fire-api-cli
```

3. Install required dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root:
```bash
touch .env
```

5. Add your 24Fire API key to the `.env` file:
```
FIRE_API_KEY=your_api_key_here
```

## Usage

Run the CLI tool:
```bash
python main.py
```

The tool will:
1. Display the 24Fire CLI logo
2. List all your available services with numbered options
3. Prompt you to select a service by entering its number
4. Fetch and display detailed information about the selected service

### Example Output

```
 .d8888b.     d8888  .d888d8b                   .d8888b. 888     8888888 
d88P  Y88b   d8P888 d88P" Y8P                  d88P  Y88b888       888   
       888  d8P 888 888                        888    888888       888   
     .d88P d8P  888 888888888888d888 .d88b.    888       888       888   
 .od888P" d88   888 888   888888P"  d8P  Y8b   888       888       888   
d88P"     8888888888888   888888    88888888   888    888888       888   
888"            888 888   888888    Y8b.       Y88b  d88P888       888   
888888888       888 888   888888     "Y8888     "Y8888P" 888888888888888 

1. My KVM Server
2. My Webspace
3. example.com
Enter the number to fetch the infos from: 1
```

## API Endpoints

The tool interacts with the following 24Fire API endpoints:

- **Services List**: `GET /api/account/services`
- **KVM Status**: `GET /api/kvm/{internal_id}/status`
- **Webspace Info**: `GET /api/webspace/{internal_id}`
- **Domain Info**: `GET /api/domain/{internal_id}`

## Configuration

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `FIRE_API_KEY` | Your 24Fire API key | Yes |

### Getting Your API Key

1. Log in to your 24Fire management panel
2. Navigate to API settings
3. Generate or copy your API key
4. Add it to your `.env` file

## Dependencies

- `requests` - HTTP library for API calls
- `python-dotenv` - Environment variable management

Create a `requirements.txt` file with:
```
requests>=2.25.1
python-dotenv>=0.19.0
```

## Error Handling

The tool includes comprehensive error handling for:
- Missing or invalid API keys
- Network connectivity issues
- Invalid service selections
- API response errors

## Color Coding

The CLI uses ANSI color codes for better readability:
- 🔵 **Blue**: Service names and keys
- 🟢 **Green**: Logo and success messages
- 🟡 **Yellow**: User prompts
- 🔴 **Red**: Error messages
- 🟦 **Cyan**: Section headers

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

**NOTE**: New code without Comments will not be approved. Reason: Not everyone can understand others code easiely.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support with the 24Fire API, please contact [24Fire Support](https://cp.24fire.de/tickets).

For issues with this CLI tool, please open an issue on GitHub.

## Changelog

### v1.0.0
- Initial release
- Support for KVM, Webspace, and Domain services
- Interactive service selection
- Environment variable configuration

### v1.1.0
 - Output Formating
 - Exeption Handling for 401 and 404 or API_KEY not found
 - Environment variable configuration Example
 - Colorful Output

### v1.1.5
 - Bug Fixes
 - Extras Tab for Account, Donation and Affiliate Information
 - Better Formating

---

**Note**: This is an unofficial tool and is not affiliated with 24Fire GmbH. Use at your own discretion.
