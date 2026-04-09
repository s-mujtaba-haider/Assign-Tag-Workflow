# Assign-Tag-Workflow
This workflow starts with a webhook that receives a request containing an email address, a tag, and an action (add/remove). It first validates whether the email is provided; if not, it returns an error. If the email exists, it fetches the corresponding contact from Mautic and checks whether the contact actually exists, otherwise returning an appropriate error response.

Once the contact is confirmed, the workflow retrieves all available tags from Mautic and checks if the requested tag already exists. If the tag does not exist, it creates a new tag and assigns it to the contact. If the tag already exists, it proceeds to assign or remove the tag based on the requested action.

Additionally, the workflow includes logic to handle special conditions between tags like MQL and SQL. For example, it prevents assigning an MQL tag if the contact already has an SQL tag, and ensures proper removal or replacement of conflicting tags. Finally, it updates the contact in Mautic and returns a success message describing the action performed.
