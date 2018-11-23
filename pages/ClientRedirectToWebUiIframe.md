# Client redirect to WEB UI

If you wish to have an iFrame implementation – there is a slightly different approach. You will have to directly insert identification platform url with **authToken** query string parameter into your iframe tag:

<center>

|UI platform url                       |
|--------------------------------------|
|https://ui.idenfy.com/                 |

|Query string parameter name           |Example value               |
|--------------------------------------|----------------------------|
|`authToken`                           |`3FA5TFPA2ZE3LMPGGS1EGOJNJE`|

</center>

### Examples

An example redirect url looks like this:<br>https://ui.idenfy.com/?authToken=3FA5TFPA2ZE3LMPGGS1EGOJNJE

#### Example code

```html
<!DOCTYPE html>
<html>
  <body>
  
  <iframe 
    id='iframe' 
    style="width:80%; height:800px;" 
    src="https://ui.idenfy.com/?authToken=3FA5TFPA2ZE3LMPGGS1EGOJNJE">
  </iframe>
  
  <p id='display'></p>
  
  <script>
  window.addEventListener("message", receiveMessage, false);
    function receiveMessage(event) {
    console.log(event);
    // ...
  }
  </script>
  
  </body>
</html>
```
