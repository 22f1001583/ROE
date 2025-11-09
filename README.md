# Matrix Build with Artifacts — Demo

This repository contains a GitHub Actions workflow that demonstrates:
- A matrix build with 3 Node variants (14, 16, 18).
- Parallel execution of matrix jobs.
- Each job generates a build artifact and uploads it with the prefix `build-6a802fd`.

Owner / Contact:
- Email: 22f1001583@ds.study.iitm.ac.in

How to run:
1. Make sure this repository is pushed to GitHub and the workflow is present at `.github/workflows/build-matrix.yml`.
2. Replace `you@example.com` above with your real email and commit.
3. Trigger the workflow by:
   - Pushing a commit to `main` or `master`, OR
   - Using the **Actions** tab → select "Matrix Build with Artifacts" → **Run workflow** (workflow_dispatch).

Verification:
- In the Actions tab select the latest workflow run.
- Confirm there are **at least 3 successful jobs** (one per matrix variant).
- Open any job → go to **Artifacts** (right side) and confirm three uploaded artifacts:
  - `build-6a802fd-v14`
  - `build-6a802fd-v16`
  - `build-6a802fd-v18`
- Download each artifact and confirm the file inside (e.g. `output-v14.txt`) is **non-empty** and contains the text `Build: node <version>`.

Notes:
- If your repository uses `main` as the default branch, use `main`. If `master`, use `master`. Both are supported by the workflow triggers.
