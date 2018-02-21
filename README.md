# Example CirclCI Howto #
## and protect master branch howto ##

[![CircleCI](https://circleci.com/gh/stuheiss/example-circleci-react-redux.svg?style=shield)](https://circleci.com/gh/stuheiss/example-circleci-react-redux)

### An example how to use CircleCI and protect the master branch ###

1. Clone [react-redux-starter-kit](https://github.com/davezuko/react-redux-starter-kit.git) to a new repo.

2. Configure for [CircleCI](https://circleci.com/):
	- push your repo to [GitHub](https://github.com/)
	- create a free account on [CircleCI](https://circleci.com/)
	- configure [CircleCI](https://circleci.com/) to build and run tests on your repo.
		- on PROJECTS
			- click Add Project
			- find your repo, click Setup project
			- on Operating System choose Linux
			- on Language choose Node
			- create .circleci/config.yml in your repo
			- copy/paste contents of Sample .yml File to config.yml
			- click Start building

3. Configure [GitHub](https://github.com/) to protect master, require code review and passing tests before allowing merge to master:
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
