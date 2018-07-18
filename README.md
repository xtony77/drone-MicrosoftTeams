# drone-MicrosoftTeams

Drone plugin for sending Microsoft Teams notifications.

```
pipeline:
	MicrosoftTeams:
    	image: xtony77/drone-microsoftteams
    	webhook: https://outlook.office.com/webhook/...
    	when: 
    		status: [ failure, success ]
```

Example configuration with custom secrets:

```
pipeline:
	MicrosoftTeams:
	    image: xtony77/drone-microsoftteams
 	    secrets:
    		- source: ${custom_secret_name}
	    	  target: plugin_webhook
    	when:
			status: [ failure, success ]
```
