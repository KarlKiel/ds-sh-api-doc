# Notifications

## Websocket Notifications based Notifications

2 Types of Notifications are available:

- Apartment State Change: Something has happened (A state variable has changed)
- Apartment Structure Change: A structural change has been done
- 
pros: Quite fast, all nearly all status changes are detected
cons: seems to get slower when server has high loads, no information on channel output or sensor value changes

## Subscribe: Open Websocket Connection to:

No authentication is required for receival of these type of Notifications.

### Connect:

ws://<dss-host>:8090/api/v1/apartment/notifications

with payload:
"{'protocol':'json','version':'1'}"

### Received Notfication Nessages:
#### Apartment Status change:
"{"type":1,"target":"event","arguments":[{"type":"apartmentStatusChanged"}]}"

#### Apartment Structure change
"{"type":1,"target":"event","arguments":[{"type":"apartmentStructureChanged"}]}"

# Application Token handling
An application Token is required for both json as well as Rest - API usage.

Generate the token for an API client:


T
