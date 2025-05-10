<!DOCTYPE html>
<html lang="ku">
<head>
  <meta charset="UTF-8">
  <title>ناردنی ئیمێلی مێژوو</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Roboto', sans-serif;
    }

    body {
      background: linear-gradient(145deg, #d3cce3, #e9e4f0);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      perspective: 1000px;
    }

    .form-box {
      background: white;
      padding: 2rem;
      border-radius: 20px;
      width: 400px;
      box-shadow: 0 25px 50px rgba(0, 0, 0, 0.2);
      transform: rotateY(10deg) rotateX(5deg);
      transition: transform 0.5s ease;
      position: relative;
    }

    .form-box:hover {
      transform: rotateY(0deg) rotateX(0deg);
    }

    .form-box h2 {
      text-align: center;
      color: #6a1b9a;
      margin-bottom: 1rem;
    }

    .form-group {
      margin-bottom: 1.5rem;
    }

    label {
      display: block;
      margin-bottom: 0.5rem;
      color: #333;
    }

    input, textarea {
      width: 100%;
      padding: 0.75rem;
      border-radius: 10px;
      border: 1px solid #ccc;
      transition: border 0.3s ease;
    }

    input:focus, textarea:focus {
      border-color: #6a1b9a;
      outline: none;
    }

    button {
      width: 100%;
      padding: 0.75rem;
      background: #6a1b9a;
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 1rem;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    button:hover {
      background: #4a148c;
    }

    .icon {
      position: absolute;
      top: -25px;
      left: -25px;
      background: white;
      padding: 15px;
      border-radius: 50%;
      font-size: 1.5rem;
      color: #6a1b9a;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
    }

    .history-icon {
      font-size: 1.8rem;
      animation: spin 5s linear infinite;
    }

    @keyframes spin {
      0% {transform: rotate(0deg);}
      100% {transform: rotate(360deg);}
    }

  </style>
</head>
<body>

  <div class="form-box">
    <div class="icon">
      <i class="fas fa-landmark history-icon"></i>
    </div>
    <h2>ناردنی ئیمێلی مێژوو</h2>
    <form id="historyEmailForm">
      <div class="form-group">
        <label for="email">ئیمێڵی وەرگر</label>
        <input type="email" id="email" placeholder="namayak@example.com" required>
      </div>
      <div class="form-group">
        <label for="subject">ناونیشانی مێژوویی</label>
        <input type="text" id="subject" placeholder="ئەو ڕووداوەی مێژوویی" required>
      </div>
      <div class="form-group">
        <label for="message">پەیامەکەت</label>
        <textarea id="message" rows="5" placeholder="پەیامێکی گەرمی مێژوویی..." required></textarea>
      </div>
      <button type="submit">بنێرە</button>
    </form>
  </div>

  <script>
    document.getElementById('historyEmailForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const email = document.getElementById('email').value;
      const subject = document.getElementById('subject').value;
      const message = document.getElementById('message').value;

      alert(`ئیمێل نێردرا بۆ: ${email}\n\nبابەت: ${subject}\n\nپەیام: ${message}`);
      
      // لەڕاستیدا ئەمە ناردنی ڕاستەقینە ناکات، بۆ ناردن بەڕاستی پێویستە بە بێکەند و PHP یان API کاربکەیت.
    });
  </script>

</body>
</html>
