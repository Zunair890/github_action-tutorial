Common Git Workflows:

    Feature Branch Workflow

        Create a new branch (git checkout -b feature-x) for each feature/bugfix.

        Commit changes (git commit -m "message") and push to the remote branch.

        Open a Pull Request (PR) or Merge Request (MR) for code review.

        After approval, merge into main/master or develop branch.

    GitFlow (More structured)

        Uses long-lived branches:

            main/master (production-ready code).

            develop (integration branch).

            Feature, release, and hotfix branches.

    Trunk-Based Development (Simpler)

        Developers commit directly to main (or short-lived branches).

        Relies heavily on CI/CD for stability.

2. CI/CD Pipeline (Automation)

Once code is merged, CI/CD pipelines automate testing, building, and deployment.
Continuous Integration (CI)

    Trigger: Code push/merge to main/develop.

    Actions:

        Run automated tests (unit, integration).

        Build artifacts (e.g., Docker images, binaries).

        Static code analysis (SonarQube, ESLint).

Continuous Delivery/Deployment (CD)

    Continuous Delivery: Manual trigger to deploy to production.

    Continuous Deployment: Automatic deployment after CI passes.

    Stages:

        Deploy to Staging (Test environment).

        Run E2E/UI tests.

        Deploy to Production (Canary, Blue-Green, or Rolling updates).
