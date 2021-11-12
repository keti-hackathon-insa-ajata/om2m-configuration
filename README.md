# OM2M Configuration

OM2M configuration files for in-cse and mn-cse

## Central server : in-cse
Most important lines in /configuration/config.ini : 
```ini
org.eclipse.om2m.dbReset=false

org.eclipse.om2m.cseBaseAddress=192.168.43.171
org.eclipse.equinox.http.jetty.http.port=8080
org.eclipse.om2m.cseBaseId=in-cse
org.eclipse.om2m.cseBaseName=in-name
```

Configuration : 
  * Adjust cseBaseAddress with the IP address of the central server
  * Choose a unique cseBadeId and cseBaseName 
  * dbReset can be set to true to reset the in-cse when starting om2M

## Local Raspberry Pi : mn-cse
Most important lines in /configuration/config.ini : 
```ini
org.eclipse.om2m.dbReset=false

org.eclipse.om2m.cseBaseAddress=192.168.43.139
org.eclipse.equinox.http.jetty.http.port=8282
org.eclipse.om2m.cseBaseId=mn-cse-raspi
org.eclipse.om2m.cseBaseName=mn-raspi

org.eclipse.om2m.remoteCseAddress=192.168.43.171
org.eclipse.om2m.remoteCsePort=8080
org.eclipse.om2m.remoteCseId=in-cse
org.eclipse.om2m.remoteCseName=in-name
```

Configuration : 
  * Adjust cseBaseAddress with the IP address of the Raspberry Pi
  * Choose a unique cseBadeId and cseBaseName
  * Adjust remoteCseAddress and remoteCsePort with the IP address and port of the central server
  * Adjust remoteCseId and remoteCseName with the id and name of the in-cse of the central server
  * dbReset can be set to true to reset the mn-cse when starting om2M (for example when we change the in-cse's address)
