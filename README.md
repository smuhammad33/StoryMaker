<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Story Form</title>
  <style>
    /* General Page Styling */
    body {
      font-family: "Georgia", serif; /* Beautiful serif font for elegance */
      background-color: #fdf6e3; /* A soft, creamy background */
      margin: 20px;
      color: #333;
    }
    h1 {
      font-size: 2.5em;
      color: #2a6478; /* Calm blue-green for the main title */
      text-align: center;
      margin-bottom: 20px;
    }
    /* Form Styling */
    .form-group {
      margin-bottom: 15px;
    }
    label {
      font-size: 1.2em;
      font-weight: bold;
      display: block;
      margin-bottom: 5px;
    }
    input, select, textarea {
      width: 100%;
      padding: 10px;
      font-size: 1em;
      border: 1px solid #bbb;
      border-radius: 5px;
      background-color: #fff;
      margin-bottom: 10px;
    }
    textarea {
      resize: none;
      height: 80px;
    }
    button {
      background-color: #6c5ce7; /* Vibrant purple for buttons */
      color: #fff;
      font-size: 1.1em;
      border: none;
      border-radius: 8px;
      padding: 10px 20px;
      cursor: pointer;
    }
    button:hover {
      background-color: #482b8e; /* Slightly darker shade on hover */
    }
    .button-group {
      display: flex;
      justify-content: space-between;
      margin-top: 20px;
    }
    /* Decorative Text for the Footer */
    .footer-text {
      text-align: center;
      font-size: 1em;
      color: #555;
      margin-top: 30px;
    }
  </style>
</head>
<body>
  <h1>Your Story Begins Here</h1>
  <form id="storyForm">
    <div class="form-group">
      <label for="name">What is your name?</label>
      <input type="text" id="name">
    </div>
    <div class="form-group">
      <label for="age">How old are you?</label>
      <input type="number" id="age">
    </div>
    <div class="form-group">
      <label for="favoriteColor">What is your favorite color?</label>
      <input type="text" id="favoriteColor">
    </div>
    <div class="form-group">
      <label for="hobby">What's your favorite hobby?</label>
      <input type="text" id="hobby">
    </div>
    <div class="form-group">
      <label for="dream">Share your biggest dream:</label>
      <textarea id="dream"></textarea>
    </div>
    <div class="form-group">
      <label for="country">Where do you live?</label>
      <input type="text" id="country">
    </div>
    <div class="form-group">
      <label for="pet">Do you have a pet?</label>
      <select id="pet">
        <option value="">Select</option>
        <option value="Yes">Yes</option>
        <option value="No">No</option>
      </select>
    </div>
    <div class="button-group">
      <button type="button" onclick="validateForm()">Tell My Story</button>
      <button type="button" onclick="resetForm()">Reset All</button>
    </div>
  </form>
  <p class="footer-text">✨ Let your imagination run wild. Every story is worth telling! ✨</p>
  <script>
    function validateForm() {
      const inputs = document.querySelectorAll('#storyForm input, #storyForm textarea, #storyForm select');
      for (const input of inputs) {
        if (!input.value.trim()) {
          alert('Oops! Please complete all fields before generating your story.');
          return;
        }
      }
      alert('Hooray! All fields are filled. Your story is coming to life.');
    }
    function resetForm() {
      document.getElementById('storyForm').reset();
    }
  </script>
</body>
</html>
