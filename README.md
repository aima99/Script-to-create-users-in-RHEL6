# Script-to-create-users-in-RHEL6
#!/bin/bash
# create-users.sh

# Define an array of usernames
username=("aima1" "aima2" "aima3" "aima4" "aima5")

# Create the user account
for username in "${username[@]}"
do
    useradd "$username"

    chage -d 0 "$username"
done
