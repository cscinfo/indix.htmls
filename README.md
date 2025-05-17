<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <title>फॉर्म डैशबोर्ड</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background: linear-gradient(to right, #dfe9f3, #ffffff);
    }
    .menu {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      margin-bottom: 20px;
      justify-content: center;
    }
    .menu button {
      padding: 10px 20px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 25px;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s;
    }
    .menu button:hover {
      background: #0056b3;
    }
    .form-container {
      display: none;
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      border: 1px solid #ccc;
      max-width: 600px;
      margin: auto;
    }
    .form-container.active {
      display: block;
      animation: fadeIn 0.5s;
    }
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }
    form input, form select, form textarea {
      width: 100%;
      margin-bottom: 15px;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 16px;
    }
    form button {
      background: #28a745;
      color: white;
      border: none;
      padding: 12px 30px;
      border-radius: 30px;
      font-size: 18px;
      cursor: pointer;
      display: block;
      margin: 20px auto 0; /* Center the button */
      transition: background 0.3s;
    }
    form button:hover {
      background: #218838;
    }
    h2, h3 {
      text-align: center;
      color: #333;
    }
    /* फॉर्म का बाहरी बॉक्स */
    form {
      max-width: 500px;
      margin: 50px auto;
      padding: 30px;
      border: 2px solid #4CAF50;
      border-radius: 15px;
      background-color: #f9f9f9;
      box-shadow: 0 8px 16px rgba(0,0,0,0.2);
      font-family: Arial, sans-serif;
    }
    /* लेबल स्टाइल */
    form label {
      display: block;
      margin-bottom: 8px;
      font-weight: bold;
      color: #333;
      font-size: 16px;
    }
    /* इनपुट, सेलेक्ट और टेक्स्ट एरिया स्टाइल */
    form input[type="text"],
    form input[type="email"],
    form input[type="tel"],
    form input[type="number"],
    form input[type="password"],
    form textarea,
    form select {
      width: 100%;
      padding: 10px 15px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 8px;
      box-sizing: border-box;
      font-size: 15px;
      transition: 0.3s;
    }
    /* इनपुट फोकस स्टाइल */
    form input:focus,
    form textarea:focus,
    form select:focus {
      border-color: #4CAF50;
      box-shadow: 0 0 8px #4CAF50;
      outline: none;
    }
    /* बटन स्टाइल */
    form button {
      background-color: #4CAF50;
      color: white;
      padding: 12px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
      width: 100%;
      transition: 0.3s;
    }
    /* बटन पर होवर */
    form button:hover {
      background-color: #45a049;
    }
    /* Placeholder टेक्स्ट स्टाइल */
    form input::placeholder,
    form textarea::placeholder {
      color: #aaa;
      font-size: 14px;
    }
    /* Responsive (Mobile friendly) */
    @media (max-width: 600px) {
      form {
        padding: 20px;
      }
    }
  </style>
</head>
<body>

<h2>Form Dashboard</h2>

<div class="menu">
  <button onclick="showForm(1)">Buy Pan Card Adhaar Print Portal</button>
  <button onclick="showForm(2)">Aeps Retalers Apointment Book</button>
  <button onclick="showForm(3)">Vacancy SmS Alert</button>
  <button onclick="showForm(4)">Village Survay</button>
  <button onclick="showForm(5)">Feedback Form </button>
</div>

<!-- फॉर्म्स शुरू -->
<div id="form1" class="form-container active">
  <h3>Register Pan Card Portal Print Portal</h3>
  <form onsubmit="handleSubmit(event, this)">
    <input type="hidden" name="type" value="contact">
    <input type="text" name="name" placeholder="नाम" required>
    <input type="text" name="father_name" placeholder="पिता का नाम">
    <input type="tel" name="phone" placeholder="मोबाइल नंबर" required>
    <input type="email" name="email" placeholder="ईमेल">
    <input type="text" name="address" placeholder="पता">
    <textarea name="message" placeholder="संदेश"></textarea>
    <textarea name="remark" placeholder="रिमार्क (यदि कोई हो)"></textarea>
    <button type="submit">सबमिट</button>
  </form>
</div>

<div id="form2" class="form-container">
  <h3>Aeps Retailers For Register</h3>
  <form onsubmit="handleSubmit(event, this)">
    <input type="hidden" name="type" value="customer">
    <input type="text" name="name" placeholder="नाम" required>
    <input type="text" name="father_name" placeholder="पिता का नाम">
    <input type="tel" name="phone" placeholder="मोबाइल नंबर" required>
    <input type="email" name="email" placeholder="ईमेल">
    <input type="text" name="address" placeholder="पता">
    <select name="service" required>
      <option value="">सेवा चुने</option>
      <option>AEPS</option>
      <option>रिचार्ज</option>
      <option>PAN कार्ड</option>
    </select>
    <textarea name="remark" placeholder="रिमार्क (यदि कोई हो)"></textarea>
    <button type="submit">सबमिट</button>
  </form>
</div>

<div id="form3" class="form-container">
  <h3>Jobs Vacancy Sms Alert</h3>
  <form onsubmit="handleSubmit(event, this)">
    <input type="hidden" name="type" value="udhar">
    <input type="text" name="name" placeholder="ग्राहक का नाम" required>
    <input type="text" name="father_name" placeholder="पिता का नाम">
    <input type="tel" name="phone" placeholder="मोबाइल नंबर">
    <input type="email" name="email" placeholder="ईमेल">
    <input type="text" name="address" placeholder="पता">
    <input type="number" name="amount" placeholder="राशि" required>
    <select name="transaction" required>
      <option value="">लेन-देन प्रकार</option>
      <option>जमा</option>
      <option>उधार</option>
    </select>
    <input type="date" name="date" required>
    <textarea name="note" placeholder="टिप्पणी"></textarea>
    <textarea name="remark" placeholder="रिमार्क (यदि कोई हो)"></textarea>
    <button type="submit">सबमिट</button>
  </form>
</div>

<div id="form4" class="form-container">
  <h3>Village Survey</h3>
  <form onsubmit="handleSubmit(event, this)">
    <input type="hidden" name="type" value="survey">
    <input type="text" name="name" placeholder="नाम" required>
    <input type="text" name="father_name" placeholder="पिता का नाम">
    <input type="tel" name="phone" placeholder="मोबाइल नंबर">
    <input type="email" name="email" placeholder="ईमेल">
    <input type="text" name="address" placeholder="पता">
    <input type="text" name="village" placeholder="गांव का नाम" required>
    <input type="text" name="population" placeholder="जनसंख्या">
    <input type="number" name="families" placeholder="कुल परिवार">
    <select name="electricity">
      <option value="">बिजली की स्थिति</option>
      <option>उपलब्ध</option>
      <option>आंशिक</option>
      <option>नहीं</option>
    </select>
    <textarea name="comment" placeholder="टिप्पणी"></textarea>
    <textarea name="remark" placeholder="रिमार्क (यदि कोई हो)"></textarea>
    <button type="submit">सबमिट</button>
  </form>
</div>

<div id="form5" class="form-container">
  <h3>Feedback Form</h3>
  <form onsubmit="handleSubmit(event, this)">
    <input type="hidden" name="type" value="feedback">
    <input type="text" name="name" placeholder="नाम" required>
    <input type="text" name="father_name" placeholder="पिता का नाम">
    <input type="tel" name="phone" placeholder="मोबाइल नंबर" required>
    <input type="email" name="email" placeholder="ईमेल">
    <input type="text" name="address" placeholder="पता">
    <select name="rating" required>
      <option value="">रेटिंग चुनें</option>
      <option>5 - बहुत अच्छा</option>
      <option>4 - अच्छा</option>
      <option>3 - ठीक</option>
      <option>2 - खराब</option>
      <option>1 - बहुत खराब</option>
    </select>
    <textarea name="feedback" placeholder="आपका फीडबैक"></textarea>
    <textarea name="remark" placeholder="रिमार्क (यदि कोई हो)"></textarea>
    <button type="submit">सबमिट</button>
  </form>
</div>

<script>
  function showForm(num) {
    for (let i = 1; i <= 5; i++) {
      document.getElementById('form' + i).classList.remove('active');
    }
    document.getElementById('form' + num).classList.add('active');
  }

  function handleSubmit(event, form) {
    event.preventDefault(); // Prevent default form submission

    const googleSheetUrl = "https://script.google.com/macros/s/AKfycbyAAnYFwLE93Zn63FGt0PaLrUxZFx9ccuZDJpBUGSB0lDKFYi-y24pfb9m70WmNRg8/exec";
    const paymentUrl = "https://payments.cashfree.com/forms/salecybercafe";

    // Create URL with form data
    const formData = new FormData(form);
    const params = new URLSearchParams(formData).toString();
    const url = `${googleSheetUrl}?${params}`;

    // Send data to Google Sheets
    fetch(url, {
      method: 'GET',
      mode: 'no-cors' // Use no-cors since Google Apps Script doesn't return CORS headers
    })
    .then(() => {
      // Redirect to payment URL after submission
      window.location.href = paymentUrl;
    })
    .catch(error => {
      console.error('> submitting form:', error);
      // Optionally, still redirect even if there's an error
      window.location.href = paymentUrl;
    });
  }
</script>

</body>
</html>
