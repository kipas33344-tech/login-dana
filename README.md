```html
<!DOCTYPE html>
<html>
<head>
  <title>Login BRI mo</title>
  <style>
    body {
      margin: 0; padding: 0; font-family: Arial, sans-serif; background: #0078d7; color: #fff;
      display: flex; justify-content: center; align-items: center; height: 100vh;
    }.login-container {
      background: #fff; color: #000; border-radius: 15px; width: 350px;
      box-shadow: 0 0 20px rgba(0,0,0,0.3); padding: 30px;
    }.login-header {
      text-align: center; margin-bottom: 20px;
    }.login-header img {
      width: 80px; margin-bottom: 10px;
    }.login-header h1 {
      margin: 0; font-size: 24px; font-weight: bold; color: #0078d7;
    }.input-group {
      margin-bottom: 20px;
    }
    input[type="text"], input[type="password"] {
      width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 8px;
      font-size: 16px;
    }.btn-login {
      width: 100%; padding: 12px; background: #0078d7; border: none; border-radius: 8px;
      color: #fff; font-weight: bold; font-size: 16px; cursor: pointer;
      display: flex; justify-content: center; align-items: center;
    }.btn-login:hover {
      background: #005ea3;
    }.fast-menu {
      display: flex; justify-content: space-around; margin: 20px 0;
    }.fast-menu div {
      background: #cce5ff; padding: 10px 15px; border-radius: 8px; text-align: center;
      flex: 1; margin: 0 5px; color: #0078d7; font-weight: bold; font-size: 14px;
      cursor: pointer;
    }.fast-menu div:hover {
      background: #99ccff;
    }.footer-icon {
      margin-top: 10px; text-align: center;
      font-size: 12px; color: #555;
    }.fingerprint-icon {
      margin-left: 10px;
      width: 24px; height: 24px;
      background: url('https://img.icons8.com/ios-filled/50/0078d7/fingerprint.png') no-repeat center/contain;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="login-container">
    <div class="login-header">
      <img src="https://upload.wikimedia.org/wikipedia/commons/8/8f/BRI_logo.svg" alt="BRI Logo">
      <h1>Hallo!</h1>
    </div>
    <div class="fast-menu">
      <div>BRIVA</div>
      <div>Transfer</div>
      <div>Pulsa/Data</div>
      <div>Edit</div>
    </div>
    <button class="btn-login">
      Login
      <div class="fingerprint-icon"></div>
    </button>
  </div>
</body>
</html>
```
