# Assign-Tag-Workflow
This workflow starts with a webhook that receives a request containing an email address, a tag, and an action (add/remove). It first validates whether the email is provided; if not, it returns an error. If the email exists, it fetches the corresponding contact from Mautic and checks whether the contact actually exists.
