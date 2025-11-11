# Auburn Jewelry - Private Event Form

A professional web form for collecting private permanent jewelry event inquiries, hosted on GitHub Pages.

## Setup Instructions

### 1. Configure Web3Forms (Email Delivery)

To receive form submissions at tim@claredigital.co:

1. Go to [Web3Forms](https://web3forms.com/)
2. Click "Get Started Free"
3. Enter your email: **tim@claredigital.co**
4. Verify your email address
5. Copy your Access Key
6. Open `index.html` and replace `YOUR_ACCESS_KEY_HERE` with your actual access key:
   ```html
   <input type="hidden" name="access_key" value="your-actual-access-key">
   ```

### 2. Deploy to GitHub Pages

1. Commit and push the changes:
   ```bash
   cd auburn-form
   git add .
   git commit -m "Initial commit: Auburn Jewelry event form"
   git push origin main
   ```

2. Enable GitHub Pages:
   - Go to your repository settings: https://github.com/timshea001/auburn-form/settings/pages
   - Under "Source", select "Deploy from a branch"
   - Select branch: `main`
   - Select folder: `/ (root)`
   - Click "Save"

3. Your form will be live at: `https://timshea001.github.io/auburn-form/`

## Form Features

- **All fields from the original Google Form** including:
  - Contact information (name, email, phone)
  - Event details (date, time, location, guest count)
  - Pricing preferences (bulk vs. individual)
  - Event description and occasion
  - Referral source tracking

- **Enhanced UX:**
  - Phone number confirmation validation
  - Responsive design for mobile and desktop
  - Modern gradient design
  - Success/error message handling
  - Form validation

- **Email Notifications:**
  - All submissions sent to tim@claredigital.co
  - Formatted email with all form data

## Testing

After setup, test the form by:
1. Filling out all required fields
2. Submitting the form
3. Checking tim@claredigital.co for the email notification

## Customization

- Colors and styling can be adjusted in the `<style>` section of `index.html`
- Form fields can be added or modified in the HTML structure
- Email subject line can be changed in the hidden `subject` field

## Support

For issues or questions, contact the development team or create an issue in this repository.
