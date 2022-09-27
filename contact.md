# Contact Me

Subject:  <input id="subject" style="width: 200px" required>
<br>
<br>
Message: 
<br>
<textarea id="body" rows="15" cols="60"></textarea>
<br>
<br>
<button id="notARobotElement" onclick="imNotARobot()">I'm Not A Robot ❌</button>
<br>
<br>
<button onclick="sendEmail()">Send</button>
<br>
<br>
<div id="message"></div>
<script>
  let notARobot = false;
  function sendEmail () {
    let messageElement = document.getElementById("message");
    let subject = document.getElementById("subject").value;
    let body = document.getElementById("body").value;
    let a1 = 'mai'; 
    let a3 = 'lto:'; 
    let a2 = 'zac'; 
    let a6 = 'h@aggelous.';
    let a10 = 'com&subject='; 
    let a4 = '&body=';
    if (notARobot) {
      window.open(a1 + a3 + a2 + a6 + a10 + subject + a4 + body);
      messageElement.innerHTML = "Sent Message!";
    }
    else {
      messageElement.innerHTML = "BOT DETECTED; SEND FAILED";
    }
  }
  function imNotARobot() {
    let notARobotElement = document.getElementById("notARobotElement");
    if (!notARobot) {
      notARobot = true;
      notARobotElement.innerText = "I'm Not A Robot ✅";
    }
    else {
      notARobot = false;
      notARobotElement.innerText = "I'm Not A Robot ❌"
    }
  }
</script>
