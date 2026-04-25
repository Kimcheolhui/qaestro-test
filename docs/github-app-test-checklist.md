# GitHub App Test Checklist

Use this quick checklist when validating a GitHub App integration in this test repository.

## Before testing

- Confirm the app is installed on this repository.
- Verify the webhook URL is reachable from GitHub.
- Store the webhook secret in the app runtime environment.
- Review repository permissions and subscribe only to required events.

## Pull request smoke test

- Push a small branch to this repository.
- Open a pull request against `main`.
- Confirm the app receives the expected pull request webhook events.
- Check app logs for successful signature verification and event handling.

## After testing

- Remove unused test branches.
- Rotate temporary secrets if they were shared during debugging.
- Document any missing permissions or webhook events before retesting.
