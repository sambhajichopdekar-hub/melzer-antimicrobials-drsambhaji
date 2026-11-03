NETLIFY FORMS DEPLOYMENT INSTRUCTIONS

This version removes FormSubmit and posts the enquiry form to Netlify Forms.

1. In Netlify site dashboard, ensure form detection is enabled (Forms settings).
2. Commit and push these files to the GitHub production branch connected to this Netlify site.
3. Wait for the production deploy.
4. Open Netlify > Forms and verify that "industry-enquiry" is detected.
5. Configure Forms > Submission notifications > Add notification.
   Netlify email notification recipients must be active members of the Netlify team. If the target mailbox is not a team member, invite it or use an approved webhook/other notification route.
6. Test with a real submission. Confirm it appears in Verified submissions, inspect Spam submissions, and verify email notification delivery.
7. The form uses Netlify Akismet spam filtering, a honeypot, and Netlify reCAPTCHA.
8. Test /thank-you after successful submission.

DOMAIN:
The canonical URL, robots.txt and sitemap use https://antimicrobial.melzerspeciality.com/. Only publish with this domain once DNS and HTTPS are active. If not yet connected, temporarily change those URLs to your working Netlify URL and update them after domain connection.

SECURITY:
Form posts to the same Netlify site, not FormSubmit. _headers adds security headers. These reduce common risks but do not guarantee the site is virus-free. Secure GitHub and Netlify with MFA and restrict repository/team access.
