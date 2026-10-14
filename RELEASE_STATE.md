# BUILDWISE Site Updates — Release State

## Current release gate
- Gate: **4B — BLOCKED**
- Staging commit: `2bb07d1a53e2ed1024ee27844fefd59cc0cc80aa`
- Staging deployment: succeeded
- Production: **v123 FROZEN**
- Production deployment: **NOT ALLOWED**
- UAT: **NOT STARTED**

## Confirmed
- Host SSO: passed
- Staging DB/R2 read-only checks: passed
- ERP dashboard: deferred from the Staging core-flow
- RBAC: owner/admin only; every new SSO user is default-deny until explicitly mapped

## Only blocker
Five real UAT identities must be granted access to the private Staging Site, log in once through ChatGPT SSO, then be mapped by the owner in **ตั้งค่าสมาชิก**:
- PM
- Engineer
- Inspector
- Contractor
- Viewer

Do not record passwords, tokens, cookies, secrets, or unmasked resource IDs in this repository.

## Workflow
1. Update the linked Gate issue with evidence after each completed action.
2. Never claim a gate passes without reproducible evidence.
3. Do not deploy or modify Production v123 without recorded approval, backup verification, and rollback approval.
