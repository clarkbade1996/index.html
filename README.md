
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Ticket Demo</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>

<style>
* { box-sizing: border-box; }

body {
  margin: 0;
  background: #111;
  font-family: -apple-system, BlinkMacSystemFont, Arial;
  display: flex;
  justify-content: center;
  min-height: 100vh;
}

.phone {
  background: #f5f3f1;
  width: 100%;
  max-width: 430px;
  min-height: 100vh;
  padding: 25px 18px;
}

.status {
  display: flex;
  justify-content: space-between;
  font-weight: 600;
  padding: 5px 8px 30px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 5px 10px 35px;
  font-size: 19px;
}

.header button {
  border: 0;
  background: transparent;
  font-size: 17px;
  color: #555;
}

.ticket {
  background: #fff;
  border-radius: 24px;
  overflow: hidden;
}

.details {
  padding: 27px 25px 35px;
}

.label {
  color: #888;
  font-size: 17px;
  margin-bottom: 10px;
}

.zone {
  font-size: 43px;
  margin: 0 0 12px;
  font-weight: 400;
}

.traveller {
  font-size: 31px;
  margin: 0;
  font-weight: 400;
}

.demo {
  color: #a15c32;
  font-size: 10px;
  letter-spacing: 2px;
  font-weight: bold;
  margin-top: 22px;
}

.separator {
  border-top: 1px solid #e4e4e4;
}

.qr-area {
  padding: 35px 15px 30px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

#qrcode {
  padding: 8px;
  background: white;
}

#qrcode canvas,
#qrcode img {
  display: block;
  max-width: 100%;
}

.owl {
  width: 235px;
  height: 235px;
  object-fit: cover;
  margin-top: 20px;
}

.footer {
  text-align: center;
  color: #a15c32;
  font-size: 11px;
  letter-spacing: 1px;
  padding: 0 10px 22px;
}
</style>
</head>

<body>
<div class="phone">

  <div class="status">
    <span>10:42</span>
    <span>▮ ▮ ▰</span>
  </div>

  <div class="header">
    <span></span>
    <strong>Your ticket</strong>
    <button>Done</button>
  </div>

  <div class="ticket">

    <div class="details">
      <div class="label">Zone</div>
      <h1 class="zone">4N</h1>

      <div class="label">Traveller</div>
      <h2 class="traveller">1 student</h2>

      <div class="demo">DEMO TICKET</div>
    </div>

    <div class="separator"></div>

    <div class="qr-area">
      <div id="qrcode"></div>

      <img class="owl"
           src="owl.jpg"
           alt="Owl">
    </div>

    <div class="footer">
      NOT VALID FOR TRAVEL
    </div>

  </div>
</div>

<script>
new QRCode(document.getElementById("qrcode"), {
  text: "DEMO ONLY - NOT A VALID RUTER TICKET",
  width: 260,
  height: 260,
  correctLevel: QRCode.CorrectLevel.H
});
</script>

</body>
</html>
