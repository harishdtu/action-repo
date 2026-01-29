# action-repo
# action-repo

This repository is used to generate GitHub events required for the TechStaX Developer Assessment.

## Purpose
The purpose of this repository is to trigger GitHub webhook events such as:
- Push
- Pull Request
- Merge (bonus)

These events are sent to the webhook endpoint implemented in the `webhook-repo`.

## How it works
- Any push to this repository triggers a **push** event
- Creating a pull request triggers a **pull_request** event
- Merging a pull request triggers a **merge** event (handled as a closed + merged pull request)

## Webhook Configuration
A GitHub webhook is configured with:
- Payload URL pointing to the Flask `/webhook` endpoint
- Content type: `application/json`
- Events selected:
  - Push
  - Pull requests

## Notes
This repository does not contain application logic.  
It exists only to simulate real GitHub activity for webhook testing.

---


