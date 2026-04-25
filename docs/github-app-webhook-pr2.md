# GitHub App Webhook PR #2 Smoke

This test PR exists to trigger a real `pull_request.opened` webhook delivery to qaestro's gateway.

Expected smoke path:

- GitHub creates a pull request event.
- The GitHub App signs the webhook with the configured secret.
- `qaestro-gateway` receives `POST /webhooks/github`.
- The gateway verifies the signature and returns `202` for a supported PR event.
