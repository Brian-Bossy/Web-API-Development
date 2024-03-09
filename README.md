
#Day one of learning api development
<p>Get JSON with the JavaScript XMLHttpRequest Method</p>

 ```javascript
const req = new XMLHttpRequest();
req.open("GET", '/json/cats.json', true);
req.send();
req.onload = function() {
  const json = JSON.parse(req.responseText);
  document.getElementsByClassName('message')[0].innerHTML = JSON.stringify(json);
};

```
1. First, an instance of the XMLHttpRequest object is created and saved in the req variable.
2. the open method initializes a request - this example is requesting data from an API, therefore is a GET request.
3. The second argument for open is the URL of the API you are requesting data from.
4. The third argument is a Boolean value where true makes it an asynchronous request.
5. The send method sends the request.
6. Finally, the onload event handler parses the returned data and applies the JSON.stringify method to convert the JavaScript object into a string. This string is then inserted as the message text.</p>
