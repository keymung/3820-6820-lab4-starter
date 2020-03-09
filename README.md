# Starter repo for first ansible automation lab

## Please clone this repo in the home directory on the ansible node

After all files are cloned you'll edit two files:

1. Edit the my_inventory file to add the IP addresses of your target hosts under respective group(s)

2. Edit the roles/webapp/defaults/main.yml file and add your repository address for the sample website you made in previous assignment as the value to the repository variable (*that file has an example on how this will look like, simply replace the example repo link with your repo link.*)

## Running the deploy-everything.yml playbook

**Navigate to the cloned directory to make it easier to run playbook or else specify correct paths to files.** To run all tasks and associated roles (and tasks within those roles):
`ansible-playbook deploy-everything.yml -i my_inventory` (*this is the only step required for assignment*)

To run only a tagged task: `ansible-playbook deploy-everything.yml -i my_inventory --tags "common_configuration"`, for example, to run the task with the tag "common_configuration" (see deploy-everything.yml playbook for other tags.)
