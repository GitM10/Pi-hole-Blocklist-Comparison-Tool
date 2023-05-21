# Raspberry

This is a tool that can help you decide whether to use a blocklist in Pi-hole.

The script prompts the user to enter the link to a blocklist.
It downloads the blocklist using wget and saves it as user_blocklist.txt.
The path to the Pi-hole blocklists directory is defined as blocklist_dir.
An empty array called unique_domains is created to store unique domains.
The script iterates through each file in the Pi-hole blocklists directory, skipping directories.
It compares the user-provided blocklist with each Pi-hole blocklist, finding unique domains.
The unique domains found in each blocklist are stored in the unique_domains array.
The total number of unique domains is calculated by joining, sorting, and counting the lines in the unique_domains array.
The script prints the number of unique domains found in the user-provided blocklist but not in the Pi-hole blocklists.
The user-provided blocklist file is removed to clean up.

In summary, the script allows the user to input a blocklist, compares it with the Pi-hole blocklists, and reports the number of unique domains present in the user-provided blocklist but not in the Pi-hole blocklists.
