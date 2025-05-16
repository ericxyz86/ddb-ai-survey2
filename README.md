# DDB Generative AI Survey Form

This directory contains an interactive HTML survey form based on the provided markdown document.

## Files

- `index.html`: The main survey form.
- `style.css`: Basic styling for the survey form.
- `survey.md`: The original markdown survey questions.

## Deployment to Netlify

This survey form is ready to be deployed to Netlify, which offers free static site hosting and form handling.

### Steps:

1.  **Sign up or Log in to Netlify:**
    Go to [https://www.netlify.com/](https://www.netlify.com/) and create an account or log in if you already have one.

2.  **Deploy the site:**
    You can deploy your site in a few ways:

    *   **Drag and Drop (Easiest for a quick test):**
        *   On your Netlify dashboard (usually under the "Sites" tab), you'll find a section to deploy a new site by dragging and dropping a folder.
        *   Drag the entire `/Users/ep/Desktop/ddb_ai_survey` folder into this area.
        *   Netlify will upload your files and assign a unique URL to your site (e.g., `random-name-12345.netlify.app`).

    *   **Connect to a Git Repository (Recommended for ongoing projects):**
        *   If you initialize a Git repository in this folder (`/Users/ep/Desktop/ddb_ai_survey`) and push it to GitHub, GitLab, or Bitbucket, you can connect Netlify to your Git provider.
        *   In Netlify, click "Add new site" -> "Import an existing project".
        *   Connect to your Git provider and select the repository.
        *   Deployment settings:
            *   **Build command:** Leave this blank (as it's a static site with no build step).
            *   **Publish directory:** Leave this blank or set to `/` (or the name of your survey folder if it's a subfolder in the repo). Netlify is usually smart enough to detect `index.html` in the root.
        *   Click "Deploy site".

3.  **Enable Netlify Forms:**
    *   The `index.html` file already includes the `data-netlify="true"` attribute in the `<form>` tag and an `<input type="hidden" name="form-name" value="ai-survey" />`. This tells Netlify to process submissions for this form.
    *   After deploying, go to your site's dashboard in Netlify.
    *   Navigate to "Forms". You should see your "ai-survey" form listed there (it might take a minute or two after the first deployment for Netlify to detect it).
    *   Submissions will appear in this section. You can also set up notifications (e.g., email alerts for new submissions).

4.  **Test Your Form:**
    *   Visit the URL Netlify provided for your deployed site.
    *   Fill out and submit the survey to ensure submissions are being captured in your Netlify Forms dashboard.

### Important Notes for Netlify Forms:

*   **Form Name:** The `name` attribute on your `<form>` tag (`ai-survey` in this case) is how Netlify identifies your form. If you change it, update it in Netlify's settings if needed.
*   **Hidden Input:** The `<input type="hidden" name="form-name" value="ai-survey">` is crucial if you have multiple forms or want to be explicit.
*   **Spam Filtering:** Netlify includes a honeypot field (`netlify-honeypot="bot-field"` and the hidden `bot-field` input) by default to help prevent spam. This is already included in the `index.html`.
*   **AJAX Submissions:** For a more seamless user experience without a page reload, you could implement AJAX form submission. However, the current setup uses standard HTML form submission, which will show a default Netlify success page.

Your survey should now be ready for deployment!
