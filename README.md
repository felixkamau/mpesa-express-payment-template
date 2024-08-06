Template code for M-pesa daraja-api

---

# M-Pesa Express Merchant Initiated Online Payment API

This project provides a Node.js script to initiate M-Pesa Express payments using Safaricom's Daraja API. The script uses Axios for HTTP requests and dotenv for environment variable management.

## Prerequisites

- Node.js and npm installed.
- An active Safaricom account with access to the Daraja API.
- Environment variables set up for Safaricom API credentials.

## Setup

1. **Clone the Repository**

   ```bash
   git clone <repository_url>
   cd <repository_directory>
   ```

2. **Install Dependencies**

   Make sure you have `axios` and `dotenv` installed:

   ```bash
   npm install axios dotenv
   ```

3. **Create Environment File**

   Create a `.env` file in the root directory of your project and add the following environment variables:

   ```env
   BASE_URL=https://sandbox.safaricom.co.ke
   CONSUMER_KEY=your_consumer_key
   CONSUMER_SECRET=your_consumer_secret
   SHORT_CODE=your_shortcode
   PASSKEY=your_passkey
   CALLBACK_URL=your_callback_url
   ```

   Replace the placeholder values with your actual Safaricom API credentials.

## Code Overview

The script contains two main functions:

1. **`getAccessToken`**

   Retrieves an access token using the Consumer Key and Consumer Secret.

2. **`mpesaExpress`**

   Initiates a payment request to the M-Pesa API.

### Example Usage

To use the `mpesaExpress` function, replace the phone number and amount in the example:

```javascript
import { mpesaExpress } from './path_to_your_script';

mpesaExpress('+254708374149', 1)
  .then(response => console.log('Payment Response:', response))
  .catch(error => console.error('Payment Error:', error));
```

## Running the Script

To run the script, use the following command:

```bash
node your_script.js
```

## Error Handling

Ensure that your API credentials and environment variables are correct. Common issues might include:

- Incorrect or expired API credentials.
- Incorrect endpoint URLs.

Check the response from the API and consult the Safaricom Daraja API documentation for further troubleshooting.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



---

Feel free to adjust the details to better fit your project specifics!
