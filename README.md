----
Description
----
The "slackhistory" script will display the entire message history of a slack
channel (via *stdout*), but not the message content itself. This can be useful
if you want to pull user metrics.

The output of this script will be in the following format for each message:
```
<timestamp> <user_real_name> <channel_name>
```

----
Prerequisites
----

This was tested on PHP 5.5+. It may work on earlier versions, however.

----
Configuration
----
**Required:**
The Slack API token should be stored as an environment variable called
SLACK_API_TOKEN

For example, add the following to your .bash_profile file:
```
export SLACK_API_TOKEN="<token_value>"
```

**Optional, but highly recommended:**
You must set the timezone or PHP timezone warnings may appear. You can set your
time zone as an environment variable called SLACK_TIMEZONE (A list of timezones
can be found at http://php.net/manual/en/timezones.php).

For example, add the following to your .bash_profile file:
```
export SLACK_TIMEZONE="America/Chicago"
```

----
Usage
----
Execute the "slackhistory" file directly:
```
./slackhistory <channel_id>
```

For example:
```
./slackhistory U12345678
```

Another example but saving the output to a file:
```
./slackhistory U12345678 >> output.txt
```
