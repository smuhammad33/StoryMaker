<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Adventure Story Teller</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 20px; }
    label { display: block; margin-top: 10px; }
    button { margin-top: 20px; }
  </style>
</head>
<body>
  <h1>Your Own Adventure Story</h1>
  <form id="storyForm">
    <label>Hero's Name: <input type="text" id="heroName"></label>
    <label>Companion's Name: <input type="text" id="companionName"></label>
    <label>Adventure Location: <input type="text" id="location"></label>
    <label>Villain's Name: <input type="text" id="villainName"></label>
    <label>Magical Object: <input type="text" id="magicObject"></label
    <label>Vehicle: <input type="text" id="vehicle"></label>
    <label>Climactic Battle Location: <input type="text" id="battleLocation"></label>
    <button type="button" onclick="generateStory()">Tell me the Story</button>
    <button type="reset">Reset</button>
  </form>
  <p id="storyOutput"></p
