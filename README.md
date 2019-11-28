## EWS Exchange Web Service
Exchange Web Service client for golang

### usage:
```
func main() {

	client := ews.NewClientWithConfig(
		"https://outlook.office365.com/EWS/Exchange.asmx",
		"email@myexchangeserver",
		"my password",
		&ews.Config{Dump: true},
	)

	err := ews.SendEmail(c,
        []string{"mhewedy@gmail.com", "someone@else.com"},
        "An email subject",
        "The email body, as plain text",
    )

	if err != nil {
		log.Fatal("err: ", err.Error())
	}

	fmt.Println("mail sent")
}
```

### Supported Feature matrix:

| Category                         	| Operation            	| Supported        	|
|----------------------------------	|----------------------	|------------------	|
| eDiscovery operations            	|                      	|                  	|
| Exchange mailbox data operations 	|                      	|                  	|
|                                  	| CreateItem operation 	| Email & Calendar 	|
| Availability operations          	|                      	|                  	|
|                                  	| GetUserAvailability  	| WIP              	|
| Bulk transfer operations         	|                      	|                  	|
| Delegate management operations   	|                      	|                  	|
| Inbox rules operations           	|                      	|                  	|
| Mail app management operations   	|                      	|                  	|
| Mail tips operation              	|                      	|                  	|
| Message tracking operations      	|                      	|                  	|
| Notification operations          	|                      	|                  	|
| Persona operations               	|                      	|                  	|
| Retention policy operation       	|                      	|                  	|
| Service configuration operation  	|                      	|                  	|
| Sharing operations               	|                      	|                  	|
| Synchronization operations       	|                      	|                  	|
| Time zone operation              	|                      	|                  	|
| Unified Messaging operations     	|                      	|                  	|
| Unified Contact Store operations 	|                      	|                  	|
| User configuration operations    	|                      	|                  	|


#### Reference:
https://docs.microsoft.com/en-us/exchange/client-developer/web-service-reference/ews-operations-in-exchange