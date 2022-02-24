![cover](https://github.com/y4aniv/MailTo/blob/main/cover.png?raw=true)
<br>
## Description
MailTo is a JavaScript library that allows you to easily prepare the sending of an email using the mailto

## Installation
To install MailTo you can :
<br>
&nbsp;&nbsp;&nbsp;&nbsp;• use JsDelivr
```js
<script src="https://cdn.jsdelivr.net/gh/y4aniv/MailTo/MailTo.min.js"></script>
```
&nbsp;&nbsp;&nbsp;&nbsp;• download and import the library
```js
<script src="./MailTo.min.js"></script>
```
## Usage
### Demo
```js
<script src="https://cdn.jsdelivr.net/gh/y4aniv/MailTo/MailTo.min.js"></script>
// <script src="./MailTo.min.js"></script>

<script>
const element = "email_send"; // The id of the element to click
var opt = {
  subject: "Partnership request",
  body: "Hello, I want to become rich!",
  cc: "harry.potter@poudlard.com",
  bcc: ["dior@chanel.com", "coca@pepsi.com"],
};
MailTo.launch(element, () => {
  MailTo.open(["steve.jobs@apple.com", "helloworld@europe.fr"], opt);
  console.log("link open:" + MailTo.link(["steve.jobs@apple.com", "helloworld@europe.fr"], opt));
});
</script>
```
### Api
```MailTo.launch(element_id, callback)``` Allows you to launch a function when you click on the element
<br>
```MailTo.open(recipient, options)``` Opens a mailto link containing the recipient and the options
<br>
```MailTo.link(recipient, options)``` Return a mailto link containing the recipient and the options
<br><br>
```options.subject``` The subject of the mail
<br>
```options.body``` The content of the email
<br>
```options.cc``` Recipient in copy
<br>
```options.bcc``` Hidden copy recipient
<br><br>
If there are several recipients for the fields ```options.subject```, ```options.cc``` and ```options.bcc``` put their email in an array
## Todo
- Adding the name of the recipient
## License
[MIT](https://github.com/y4aniv/MailTo/blob/main/LICENSE)
