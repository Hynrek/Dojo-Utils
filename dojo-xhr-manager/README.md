<h1>Dojo XHR-Manager</h1>
<p>
This module should simplify the use of HTTP-Requests and also should make them more readable sice you can use Objects instead of strings.
</p>

<p>
	<h2> DESCRIPTION: </h2>
	How to use a request (PUT/POST/GET/DELETE are used the same way) </br>
	<ul>
		<li>@param {String} service - Mostly this contains a HOST + SERVICE (E.g. localhost/myService.json)</li>
		<li>@param {object} parameter - If your request needs to be parameterized, use a key/value object to automatically add it to the request.</li>
		<li>@param {object} header - Key/Value object which will be inserted to the request. </li>
		<ul>
			<li><b>Request specific headers you could set to change the request behaviour:</b></li>
			<li>isSychron (Default: false)</li>
			<ul>
				<li>False: Non blocking asynchronous requests</li>
				<li>True: BLOCKING synchronous requests</li>
			</ul>
			<li>preventCache (Default: false)</li>
			<ul>
				<li>False: Nothing happens</li>
				<li>True: A parameter will be added to the request to advice the server to NOT send cached values</li>
			</ul>
			<li>handleAs: (Default: text)</li>
			<ul>
				<li>Standard handlers are: text, json, javascript and xml</li>
				<li>More info and how to create your own handlers are found here: "dojo/request/handlers"</li>
			</ul>
		</ul>
		<li>@return {object : deferred} deferred - A dojo object which allows easier asynchronous handling.</li>
	</ul>
	<p>
	<b>How to use deferreds:</b><br>
	x.getRequest(service, requestParams, requestHeader).then(function(success){<br>
	}, function(error){ <br>
	}); <br>
	</p>
</p>

