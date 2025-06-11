# ICU-PORTAL-EXAMS
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ICU Student Portal</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f0f4f8; margin:0; padding:0; }
    .container { max-width:700px; margin:50px auto; background:#fff; border-radius:10px; box-shadow:0 0 15px rgba(0,0,0,0.1); padding:30px; }
    .logo { display:block; margin:0 auto 20px; width:120px; }
    h1,h2,h3 { text-align:center; color:#004080; margin-bottom:20px; }
    form { max-width:400px; margin:0 auto; display:flex; flex-direction:column; gap:15px; }
    input,button { padding:12px; font-size:1rem; border-radius:6px; }
    input { border:1px solid #ccc; }
    button { background:#004080; color:#fff; border:none; cursor:pointer; transition:0.3s; }
    button:hover { background:#002d5c; }
    .error { color:red; text-align:center; margin:10px 0; display:none; }
    table { width:100%; border-collapse:collapse; margin-top:20px; }
    th,td { padding:10px; border:1px solid #ccc; text-align:center; }
    th { background:#004080; color:#fff; }
    .fail { background:#ffd6d6; }
    .pass { background:#d6f5d6; }
    .payment-link { text-align:center; margin-top:20px; }
  </style>
</head>
<body>

<div class="container" id="login-container">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Information_and_Communications_University_Logo.svg/120px-Information_and_Communications_University_Logo.svg.png" alt="ICU Logo" class="logo" />
  <h1>Information and Communications University</h1>
  <h2>Student Portal Login</h2>
  <form id="login-form">
    <input type="text" id="username" placeholder="Username (Exam Number)" required />
    <input type="password" id="password" placeholder="Password" required />
    <button type="submit">Login</button>
    <p class="error" id="error-msg">Incorrect username or password.</p>
  </form>
</div>

<div class="container" id="results-container" style="display:none;">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Information_and_Communications_University_Logo.svg/120px-Information_and_Communications_University_Logo.svg.png" alt="ICU Logo" class="logo" />
  <h1>Information and Communications University</h1>
  <h2>Electrical &amp; Electronics Engineering BSc</h2>
  <h3>Second Semester Exam, June 2025</h3>
  <p><strong>Name:</strong> MWEWA SANGISTA MUSONDA</p>
  <p><strong>Exam Number:</strong> 2210332800</p>

  <table>
    <thead>
      <tr><th>Course</th><th>CA</th><th>Attendance</th><th>Result</th><th>Grade</th></tr>
    </thead>
    <tbody>
      <tr class="fail"><td>HM2</td><td>24</td><td>24%</td><td>37%</td><td>D (Fail)</td></tr>
      <tr class="fail"><td>Web Dev</td><td>22</td><td>16%</td><td>32%</td><td>D (Fail)</td></tr>
      <tr class="fail"><td>EC1</td><td>28</td><td>24%</td><td>35%</td><td>D (Fail)</td></tr>
      <tr class="fail"><td>EC2</td><td>19</td><td>7%</td><td>29%</td><td>D (Fail)</td></tr>
      <tr class="pass"><td>TEE</td><td>20</td><td>10%</td><td>60%</td><td>C+</td></tr>
      <tr class="pass"><td>ED1</td><td>12</td><td>15%</td><td>41%</td><td>C</td></tr>
      <tr class="fail"><td>BE1</td><td>29</td><td>5%</td><td>39%</td><td>D (Fail)</td></tr>
    </tbody>
  </table>

  <div class="payment-link">
    <button onclick="showPayments()">View Payments</button>
  </div>

  <div id="payments" style="display:none; margin-top:40px;">
    <h3>Payment History</h3>
    <table>
      <thead>
        <tr><th>Date</th><th>Payment Type</th><th>Amount</th><th>Status</th></tr>
      </thead>
      <tbody>
        <tr><td>2025-05-22</td><td>Exam Fees</td><td>K1200</td><td>Paid</td></tr>
        <tr><td>2025-01-10</td><td>Tuition Fees</td><td>K2500</td><td>Paid</td></tr>
        <tr><td>2025-03-05</td><td>Library Fees</td><td>K100</td><td>Paid</td></tr>
        <tr><td>2025-05-22</td><td>Exam Fees</td><td>K1200</td><td>Pending</td></tr>
      </tbody>
    </table>
  </div>
</div>

<script>
  document.getElementById('login-form').addEventListener('submit', e => {
    e.preventDefault();
    const u = document.getElementById('username').value.trim();
    const p = document.getElementById('password').value.trim();
    if(u === '2210332800' && p === '2210332800') {
      document.getElementById('login-container').style.display = 'none';
      document.getElementById('results-container').style.display = 'block';
    } else {
      document.getElementById('error-msg').style.display = 'block';
    }
  });

  function showPayments() {
    document.getElementById('payments').style.display = 'block';
  }
</script>

</body>
</html>
