# AJAX

_Asynchronous JavaScript and XML_

AJAX is a set of technologies to send and receive data between client and server asynchronously.
AJAX uses the XmlHTTPRequest (XHR) Object, which is an API in the form of an object - it has methods and properties that allow data transfer between client and server. You can work with the HTTP methods to interact with the server

**You make a XHR request using JavaScript, which will asynchronously collect data from the server, and when the data is available, you can update a part of your HTML to display the information on the page.**

---

### Make an AJAX Request

1. create the XHR object
1. define the type of request, url/file, if is async or not
1. define function to handle response from xhr
1. send request for data

```javascript
// 1
let xhr = new XmlHTTPRequest();

// 2
xhr.open(method, url, async);
// xhr.open('GET', file.txt, true);

// 3
xhr.onload = function () {
	// this = xhr
	// use http codes to check status of the response
	if (this.status == 200) {
		// display data
	} else if (this.status == 404) {
		// error handle
	}
};

// 4
xhr.send();
```
