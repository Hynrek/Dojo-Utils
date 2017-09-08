<h1>Dojo XHR-Manager</h1>
<p>
This module should simplify the use of HTTP-Requests and also should make them more readable sice you can use Objects instead of strings.
</p>

<p>
 * DESCRIPTION:
 * 
 * How to use a request (PUT/POST/GET/DELETE are used the same way)
 * 
 * @param {String} service - Mostly this contains a HOST + SERVICE (E.g. localhost/myService.json)
 * @param {object} parameter - If your request needs to be parameterized, use a key/value object to automatically add it to the request.
 * @param {object} header - Key/Value object which will be inserted to the request.
 * Request specific headers you could set to change the request behaviour:
 * 		-isSychron (Default: false)
 * 			-False: Non blocking asynchronous requests
 * 			-True: BLOCKING synchronous requests
 * 		-preventCache (Default: false)
 * 			-False: Nothing happens
 * 			-True: A parameter will be added to the request to advice the server to NOT send cached values
 * 		-handleAs: (Default: text)
 * 			-Standard handlers are: text, json, javascript and xml
 * 			-More info and how to create your own handlers are found here: "dojo/request/handlers"
 * 
 * @return {object : deferred} deferred - A dojo object which allows easier asynchronous handling.
 * 		How to use it:
 *		x.getRequest(service, requestParams, requestHeader).then(function(success){
 *		}, function(error){
 *		});
</p>

