# Development when forking this repository

# setup an environment for github actions
The environment must be called `he`.
Set it up in your github repository settings.
It must contain the following three environment variables:

| Variablename | Purpose |
| :----------- | :------ |
| HE_USERNAME  | username for login into free dns service of HE |
| HE_PASSWORD  | password for login into free dns service of HE |
| HE_TEST_ZONE_NAME | zonename fqdn for test that is configured in your HE account |

Those variables should contain your login information to the free dns service
of Hurricane Electric.
The zone must be a zone that you have configured as a zone in the free dns
service, because the webhook creates a TXT record in the zone.

You can use the action rules without the tests, if you don't want to store this
information in the github account, but you will have to change the action rules
yourself :) .
