# Keith's Aquascaping & Aquarium Maintenance

Welcome to the Keith's Aquascaping & Aquarium Maintenance website project! This project is designed to showcase the services offered by Keith's Aquascaping, providing an elegant and responsive web experience.

## Project Structure

The project is organized as follows:

```
keiths-aquascaping-website
├── src
│   ├── index.html          # Main HTML document for the website
│   ├── css
│   │   ├── style.css       # Main styles for the website
│   │   └── utilities.css    # Utility classes for reusable styles
│   ├── fonts
│   │   └── gabriel-sans.woff2 # Font file for typography
│   └── js
│       └── main.js         # JavaScript for interactive features
├── README.md               # Project documentation
```

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Custom Font: Gabriel Sans

## Color Palette

- Background: White
- Text: Black
- Accent: Light Blue
- Highlight: Bright Yellow

## Setup Instructions

1. Clone the repository to your local machine.
2. Open the `index.html` file in your web browser to view the website.
3. For development, you can edit the CSS files in the `css` directory and the JavaScript in the `js` directory.

## Features

- Responsive design that adapts to various screen sizes.
- Clean and modern aesthetic with a focus on aquascaping services.
- Interactive elements powered by JavaScript.

## Contribution

Feel free to contribute to this project by submitting issues or pull requests. Your feedback and suggestions are welcome!

## License

This project is open-source and available under the MIT License.

## Contact Form Email Setup (EmailJS)

The website includes a contact form that sends emails using EmailJS. Follow these steps to set up the email functionality:

### 1. Create an EmailJS Account

1. Sign up for a free account at [EmailJS.com](https://www.emailjs.com/)
2. Verify your account through the confirmation email

### 2. Connect Your Email Service

1. Log in to your EmailJS dashboard
2. Go to "Email Services" and click "Add New Service"
3. Choose your email provider (Gmail, Outlook, etc.)
4. Follow the authentication steps to connect your email account
5. Once connected, you'll receive a **Service ID** (save this for later)

### 3. Create an Email Template

1. In the EmailJS dashboard, go to "Email Templates" and click "Create New Template"
2. Give your template a name (e.g., "Keith's Aquascaping Contact Form")
3. Set the subject line (e.g., "New Contact Form Submission from Keith's Aquascaping Website")
4. Design your email content using the variables below:
   ```
   Name: {{from_name}}
   Email: {{reply_to}}
   Phone: {{phone_number}}
   
   Message:
   {{message}}
   ```
5. Save the template and note the **Template ID** provided

### 4. Update the Website Code

1. Open `index.html` in a code editor
2. Locate the EmailJS initialization code (around line 193)
3. Replace `"YOUR_USER_ID"` with your EmailJS **User ID** (found in the Integration section of the dashboard)
4. Find the `emailjs.send()` function (few lines below)
5. Replace `'service_id'` with your actual **Service ID** from step 2
6. Replace `'template_id'` with your actual **Template ID** from step 3

Example:
```javascript
// Initialize EmailJS
emailjs.init("abc123xyz"); // Replace with your User ID

// Inside the submit handler:
emailjs.send('gmail', 'contact_form', templateParams) // Replace with your Service ID and Template ID
```

### 5. Test the Form

1. Open the website in your browser
2. Fill out the contact form and submit it
3. Check your email account to verify that you received the submission
4. If you encounter any issues, check the browser console for error messages

### 6. EmailJS Free Plan Limitations

- The free plan allows 200 emails per month
- For higher volumes, consider upgrading to a paid plan at [EmailJS.com](https://www.emailjs.com/pricing/)