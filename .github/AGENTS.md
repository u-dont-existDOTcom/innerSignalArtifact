# `.github/` Agent Instructions

- Treat release, ownership, artifact provenance, and repository-policy changes as privileged integrity changes.
- Declare explicit least-privilege workflow `permissions`; begin with `contents: read` and grant write scopes only to the smallest release job that needs them.
- Pin remote actions and reusable workflows to reviewed full 40-character commit SHAs; retain release tags only as comments.
- Never execute untrusted pull-request code in a privileged `pull_request_target` context.
- Keep signing credentials, model/API credentials, private user data, and secret values out of workflows, logs, artifacts, prompts, and state files.
- Do not hand-edit generated artifacts. A release must record the canonical source repository, exact source commit, version, generator command, checksums, and verification result.
- Separate artifact generation from publication and protect publication credentials with an environment/approval gate when activated.
- CODEOWNERS does not prove branch protection. Do not claim rulesets or hosted scanning controls are enabled without GitHub settings/API evidence.
