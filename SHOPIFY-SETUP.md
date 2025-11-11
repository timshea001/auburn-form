# Shopify Setup Instructions

## Overview

This form will work perfectly in Shopify. The email functionality remains unchanged - all submissions will still go to tim@claredigital.co via Web3Forms.

## Setup Steps

### 1. Get Web3Forms Access Key (Required)

1. Go to [Web3Forms](https://web3forms.com/)
2. Click "Get Started Free"
3. Enter email: **tim@claredigital.co**
4. Check your email and verify the address
5. Copy your Access Key
6. Open `shopify-form.html`
7. Find line 249 and replace `YOUR_ACCESS_KEY_HERE` with your actual key:
   ```html
   <input type="hidden" name="access_key" value="your-actual-access-key">
   ```

### 2. Add Form to Shopify (Choose One Method)

#### **Method A: Custom Liquid Section (Recommended)**

Best for: Reusable form that can be added to any page

1. In Shopify Admin, go to **Online Store > Themes**
2. Click **Actions > Edit code**
3. In the left sidebar under **Sections**, click **Add a new section**
4. Name it: `auburn-event-form`
5. Delete the default code
6. Copy and paste the entire contents of `shopify-form.html`
7. Click **Save**

**To use the section:**
1. Go to any page editor (Pages > [Your Page] > Customize)
2. Click **Add section**
3. Find and select **auburn-event-form**
4. Save and publish

#### **Method B: Custom Page Template**

Best for: Dedicated form page

1. In Shopify Admin, go to **Online Store > Themes**
2. Click **Actions > Edit code**
3. Under **Templates**, click **Add a new template**
4. Select **page** as the template type
5. Name it: `event-form`
6. In the template file, add:
   ```liquid
   {% section 'auburn-event-form' %}
   ```
7. Click **Save**
8. First create the section using Method A above
9. Create a new page: **Online Store > Pages > Add page**
10. In the page settings (right sidebar), under **Theme template**, select `page.event-form`
11. Save the page

#### **Method C: Direct HTML in Page (Quick & Easy)**

Best for: Quick setup, single page use

1. Go to **Online Store > Pages**
2. Create a new page or edit an existing one
3. Click the **Show HTML** button (< > icon)
4. Paste the entire contents of `shopify-form.html`
5. Click **Save**

**Note:** Some Shopify themes may strip custom HTML. If this happens, use Method A or B.

### 3. Test the Form

1. Visit your page in the live store
2. Fill out all required fields
3. Submit the form
4. Check tim@claredigital.co for the email notification

## Customization for Client's Branding

### Update Colors

Find these sections in the code to match the client's brand:

```css
/* Header gradient */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Button gradient */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Focus color */
border-color: #667eea;
```

Replace the hex color codes with the client's brand colors.

### Update Text

You can modify:
- Form title (line 260)
- Form description (line 261)
- Success message (line 268)
- Error message (line 271)

## Important Notes

### ✅ What Works in Shopify:
- All form fields and validation
- Email submissions via Web3Forms
- Phone number confirmation
- Responsive design
- Success/error messages
- All JavaScript functionality

### 🔄 Form Handling:
- **Does NOT impact form submissions** - The form uses Web3Forms API directly
- No Shopify backend required
- Works exactly the same as the GitHub Pages version
- Emails still go to tim@claredigital.co

### 🎨 Styling:
- All styles are prefixed with `.auburn-` to avoid conflicts with Shopify theme
- Form is self-contained and won't break theme styling
- Fully responsive for mobile devices

## Troubleshooting

### Form doesn't submit:
- Verify Web3Forms access key is correct
- Check browser console for JavaScript errors
- Ensure all required fields are filled

### HTML gets stripped when saving:
- Use Method A (Custom Liquid Section) instead
- Some themes don't allow raw HTML in pages

### Form looks broken:
- Check if theme CSS is conflicting
- Try adding `!important` to critical styles
- Use Method A for better isolation

### Not receiving emails:
- Verify Web3Forms access key
- Check spam folder
- Confirm tim@claredigital.co is verified in Web3Forms

## Support

For additional help:
- Web3Forms Documentation: https://docs.web3forms.com/
- Shopify Theme Development: https://shopify.dev/themes

---

**Quick Start Checklist:**
- [ ] Get Web3Forms access key for tim@claredigital.co
- [ ] Add access key to the form code (line 249)
- [ ] Choose installation method (A, B, or C)
- [ ] Add form to Shopify
- [ ] Test form submission
- [ ] Verify email received at tim@claredigital.co
