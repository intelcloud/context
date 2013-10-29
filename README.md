Intel Cloud Services Plugin - Context - Phonegap
=====================

Documentation
=====================

Context functions
=====================

<center><h2>context.service</h2></center>

This object contains the following properties: <i>name</i> and </i>urn</i> 

<center><h2>context.initCallbacks(onReceivedItem, onError)</h2></center>

Initialize the callbacks for context services. This function receives the following parameters:

- <b>onReceivedItem</b>: This parameter is a function defined by one parameter: <i>type</i>. This last parameter will contain the urn (in string format) of the item received on context services (for example, contacts or battery types).

- <b>onError</b>: This parameter is a function defined by one parameter: <i>error</i>. This last parameter will contain all errors received from context services api.

<center><h2>context.getServices(services, errorCallback)</h2></center>

This function returns the allowed services for the current platform. For example, in android the "messages service" is allowed, but not on iOS.

- <b>services</b>: Collection of services objects. Each object contains "name" and "urn" properties.

Note: In the context.init method, must be specified "context.services" objects. The collection received by parameter in this function is not the same as context.services objects.

- <b>errorCallback</b>: This function will be executed if occurs an error while the services was getting. The returned parameter in this function is the error.

<center><h2>context.init(services, callback, errorCallback)</h2></center>

This function initializes the list of services passed by the first parameter (must be a collection of context.services objects). 

- <b>services</b>: The list of services to initialize.

- <b>callback</b>: This function will be executed if the specified services have been initialized properly.

- <b>errorCallback</b>: This function will be executed if occurs an error while the services was starting. The returned parameter in this function is the error.

<center><h2>context.stop(services, callback, errorCallback)</h2></center>

This function stops all the working providers at this moment.

- <b>callback</b>: This function will be executed if the specified services have been stopped properly.

- <b>errorCallback</b>: This function will be executed if occurs an error while the services was stopping. The returned parameter in this function is the error.

<center><h2>context.checkStatus(callback, errorCallback)</h2></center>

This function gets the actual status of context service.

- <b>callback</b>: This function returns one parameter with the status of the context services. If the state (parameter returned by this function) is true, then the context service is already enabled, otherwise the service context is not enabled yet.

- <b>errorCallback</b>: This function will be executed if occurs an error while was getting the status of the context service. The returned parameter in this function is the error.