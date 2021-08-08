# How to Contribute Your Code
Only PRs corresponding to an existing, approved, and assigned issue will be considered.

If an issue does not exist for what you want to update, please create an issue for it, make your plan known, and indicate you'd like to take on that responsibility.

Let's talk about the various tests that your idea and contribution would require.

The idea is to keep PRs small and focused to a single objective. The smaller and more focused, the better.

## The Workflow
1. Make sure to not the corresponding issue, letting everyone know it's been assigned to you.
2. Fork the repository to your GitHub account.
3. Clone your fork.
4. Set up the development environment, as described in the project's README.md file.
5. Set up your fork as your git remote origin and this repository as the git remote upstream.
6. Two options:
  1. If developing documentation, create a documentation branch, document, add, commit changes. Jump to step \#9.
  2. Create a development branch and branch that to second branch that matches the work.
    * \<issue-id\>-feature-\<feature-slug\>
        * ex: 3-feature-site-search
        * for developing new features for an upcoming or future release
        * exists as long as the feature is in development.
    * \<issue-id\>-bugfix-\<bugfix-slug\>
        * ex: 3-bugfix-pagination
        * used for bug/defect fixes
    * \<issue-id\>-hotfix-\<hotfix-slug\>
        * ex: 3-hotfix-wrong-title-fonts
        * for unplanned production releases
        * used for maintenance or patches after of the latest release
    * \<issue-id\>-documentation-\<document-slug\>
        * ex: 3-documentation-readme
        * used for documentation
7. Create your tests.
8. Code your solution, add, commit and merge onto your local development branch.
9. Push to your fork and create the PR from there.

There are three project-level branches:
* main
* release
* staging
* development

### documentation Branch
Documentation PRs will be visually checked.

If approved, they will be merged directly onto main/master branch.

### Code Change Branches
GitHub Actions will immediately run tests and check linting for all non-documentation PRs.

If PR passes all automated tests, it sit idle, await a visual code check. Conversations might be had if there are any concerns, but once the code changes are approved, the branch will be merged onto the repository's staging branch.

CI will spin up an mirrored instance to that of production. The site will undergo visual and usability testing.

Once approved, the PR will be merged onto the repository's release branch. This will execute deploying onto production.

To document changes, the release tag and information will be updated on GitHub. Once documented, the PR will be merged onto the main/master branch.
