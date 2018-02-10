Example using CirclCI and protecting master.

Clone https://github.com/davezuko/react-redux-starter-kit.git to a new repo.

Configure for CircleCI:
  - push your repo to GitHub
  - create a free account on CircleCI
  - configure CircleCI to build and run tests on your repo.
    - on PROJECTS
      - click Add Project
      - find your repo, click Setup project
      - on Operating System choose Linux
      - on Language choose Node
      - create .circleci/config.yml in your repo
      - copy/paste contents of Sample .yml File to config.yml
      - click Start building

Configure GitHub to protect master, require code review and passing tests before allowing merge to master:
  - go to Settings -> Branches
    - in Protected branches
      - click Choose a branch... master
    - in Branch protection for master
      - check Protect this branch
      - check Require pull request reviews before merging
      - check Require status checks to pass before merging
        - check Require branches to be up to date before merging
        - check ci/circleci
      - check Include administrators
