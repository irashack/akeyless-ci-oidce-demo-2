# Akeyless CI/CD OIDC demo

A GitHub Actions workflow that reads a secret from Akeyless with no stored
credential. The job asks GitHub for an OIDC token, Akeyless verifies it against
GitHub's public keys, and the role association releases the secret only to this
repository's `main` branch.

Run **Actions → deploy → Run workflow** with the access ID and secret path your
facilitator gives you. Run it again on `feature/try-prod` to watch Akeyless
refuse the same code from another branch.

The Akeyless side (JWT auth method, role, sub-claims) is provisioned per
workshop by the `ci-oidc` module of the Akeyless workshop.
