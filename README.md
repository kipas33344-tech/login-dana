```html
<!DOCTYPE html>
<html>
<head>
  <title>Login DANA Simulasi</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 350px;
      margin: 30px auto;
      padding: 20px;
      border: 2px solid #007bff;
      border-radius: 8px;
      background: #f0f8ff;
    }
    h2 {
      text-align: center;
      color: #007bff;
    }
    input[type="text"], input[type="password"] {
      width: 100%;
      padding: 8px 6px;
      margin: 6px 0 12px;
      border: 1px solid #007bff;
      border-radius: 4px;
      box-sizing: border-box;
    }
    button {
      width: 100%;
      background-color: #007bff;
      color: white;
      padding: 10px 0;
      border: none;
      border-radius: 4px;
      font-weight: bold;
      cursor: pointer;
    }
    button:hover {
      background-color: #0056b3;
    }
    #message {
      margin-top: 15px;
      font-weight: bold;
      text-align: center;
    }
  </style>
</head>
<body>
  <h2>Login DANA Simulasi</h2>
  <label>Nomor HP:</label><br>
  <input type="text" id="nomorHp" placeholder="Masukkan nomor HP"><br><br>
  <button onclick="kirimOtp()">Kirim OTP</button>

  <div id="otpSection" style="display:none; margin-top:20px;">
    <label>Masukkan OTP:</label><br>
    <input type="text" id="otp" placeholder="Kode OTP"><br><br>
    <button onclick="cekOtp()">Verifikasi OTP</button>
  </div>

  <div id="pinSection" style="display:none; margin-top:20px;">
    <label>Masukkan PIN:</label><br>
    <input type="password" id="pin" placeholder="PIN DANA"><br><br>
    <button onclick="cekPin()">Login</button>
  </div>

  <p id="message" style="color:red;"></p>

  <script>
    function kirimOtp() {
      const nomorHp = document.getElementById('nomorHp').value;
      if (!nomorHp) {
        document.getElementById('message').textContent = 'Masukkan nomor HP dulu ya.';
        document.getElementById('message').style.color = 'red';
        return;
      }
      document.getElementById('message').textContent = `Kode OTP sudah dikirim ke ${nomorHp} (simulasi).`;
      document.getElementById('message').style.color = 'green';
      document.getElementById('otpSection').style.display = 'block';
    }

    function cekOtp() {
      const otp = document.getElementById('otp').value;
      if (otp === '123456') {
        document.getElementById('message').textContent = 'OTP benar! Masukkan PIN untuk login.';
        document.getElementById('message').style.color = 'green';
        document.getElementById('pinSection').style.display = 'block';
      } else {
        document.getElementById('message').textContent = 'OTP salah, coba lagi.';
        document.getElementById('message').style.color = 'red';
      }
    }

    function cekPin() {
      const pin = document.getElementById('pin').value;
      if (pin === '0000') {
        document.getElementById('message').style.color = 'green';
        document.getElementById('message').textContent = 'Login berhasil! Selamat datang di DANA.';
      } else {
        document.getElementById('message').style.color = 'red';
        document.getElementById('message').textContent = 'PIN salah, coba lagi.';
      }
    }
  </script>
</body>
</html>
