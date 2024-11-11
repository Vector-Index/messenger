# Web-Based Messenger App Manual
[English](messenger.en.md) | [简体中文](messenger.zh-CN.md)

Welcome to the user manual for your web-based messenger app. This guide will help you understand all the available settings and features, so you can make the most out of your messaging experience.

## Settings Overview

This section explains the various settings options available in your web-based messenger app.

### Username
- **Description**: The username field allows you to set or update your current username. This is the name that other users will see when interacting with you.
- **Usage**: Enter your desired username in the input field.

### Cache (Number of Messages)
- **Description**: This setting determines how many messages are stored locally on your device. The messages are saved in `localStorage` to provide persistency, meaning your chat history will still be available even after refreshing or closing the app.
- **Usage**: Enter the number of messages (e.g., 20) that you want to cache. The default value is `20` messages.

### Hide Encrypted Messages
- **Description**: This option allows you to completely hide messages that are encrypted.
- **Usage**: When checked, encrypted messages will be hidden from the user interface. Uncheck this option to view encrypted messages, though they will be unreadable without the correct decryption key.

### Generate Key Pair
- **Description**: Generate a public/private key pair for end-to-end encryption, which allows for secure communication between users.
- **Usage**: Click on the key icon (🔑) to generate a new key pair. The generated key pair is not saved and must be generated each time you start the messenger if you wish to use end-to-end encryption. The key pair is essential for ensuring privacy and secure communication.

### Choose a User (Secure Channel)
- **Description**: This setting allows you to select which user you want to communicate with using a secure channel.
- **Usage**: The dropdown menu contains a list of users who have already generated key pairs in the current chatroom. By selecting a specific user, you will use their public key to encrypt your message. Alternatively, if you choose "Use public channel," your message will use the shared symmetric encryption key for the entire chatroom. Users who have the shared key can decrypt your messages.

### Choose a Theme
- **Description**: Allows you to change the appearance of the application to fit your preferences.
- **Usage**: Use the dropdown menu to select the desired theme. By default, the "Default" theme is selected. Click on "Add more themes" (🎭) if you want to browse and add more theme options.

### Enable Eval
- **Description**: This option enables the `eval()` function, which allows you to evaluate your own messages as JavaScript code before sending.
- **Usage**: When checked, the app will evaluate the message using `eval(msg)` before sending it. Note that security considerations are not in place for this feature, and enabling it may expose you to risks. This is why the option is marked with an exclamation mark (⚠) to caution users.

### Proxy Setting
- **Description**: This setting allows you to configure a proxy URL to relay API requests. This is primarily used when the "Enable eval" setting is activated, and the app needs to make CORS-enabled requests.
- **Usage**: Enter the proxy URL in the text field provided. The default URL is `https://api.codetabs.com/`. If left blank, the system might not work as expected, depending on the browser's security restrictions.

## Using the App

### Sending Messages
1. **Enter Your Message**: Type your message in the text input field.
2. **Encrypt Your Message** (Optional): If you have generated a key pair, you can encrypt your message before sending it. Select the recipient from the "Choose a user" dropdown to use their public key for encryption.
3. **Send Your Message**: Click the "Send" button to transmit your message.

### Attaching Files
- Use the "Choose Files" button to select a file from your local system and attach it to your message.
- Once a file is chosen, click "Send" to transmit both the message and the attached file.

### Encryption Options
- The app provides both end-to-end encryption (public/private key pair) and a symmetric encryption mode for group chats. Make sure to generate a key pair to enable secure communication.

## Security Considerations
- **Encryption**: The app supports browser-to-browser encryption using a public/private key pair. Users are responsible for generating their key pairs to enable this functionality.
- **Eval Function**: Enabling the eval function is a potential security risk, as it allows message evaluation as code. It is recommended to use this feature only if you are fully aware of the implications and potential risks.

## FAQ

### What happens if I close my browser?
- The messages you cached (up to the number set in "Cache") will remain available in your `localStorage` for the next session.

### Can I recover my key pair?
- No, key pairs are not saved or stored in any form. You need to generate a new key pair for each session.

### How do I enable secure messaging?
- Generate a key pair using the "Generate key pair" option, and select the intended recipient from the "Choose a user" dropdown. The message will be encrypted using the recipient's public key.

## Troubleshooting

### Unable to Send Messages
- **Check Your Internet Connection**: Make sure you have a stable internet connection.
- **Encryption Issues**: Verify that you have generated a key pair if you are trying to send encrypted messages. Also, confirm that the target user is available in the secure channel dropdown.

### Messages Not Appearing
- If encrypted messages are not visible, make sure the "Hide encrypted messages" setting is unchecked.

## Contact Support
If you have any additional questions or issues, feel free to contact our support team through the "Help" button available in the app's main interface.

---

Thank you for using our web-based messenger app! We hope this manual helps you navigate and utilize all the available features effectively. Stay secure and happy chatting!

