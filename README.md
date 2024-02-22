<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Button to Text Areas</title>
<style>
    /* Optional: Some basic styling */
    .container {
        display: flex;
        justify-content: space-around;
        margin-top: 50px;
    }
    textarea {
        width: 300px;
        height: 150px;
        resize: none;
    }
</style>
</head>
<body>
<div class="container">
    <button onclick="showTextArea('textArea1')">Show Text Area 1</button>
    <button onclick="showTextArea('textArea2')">Show Text Area 2</button>
    <button onclick="showTextArea('textArea3')">Show Text Area 3</button>
</div>

<div class="container">
    <textarea id="textArea1" style="display:none;">This is Text Area 1</textarea>
    <textarea id="textArea2" style="display:none;">This is Text Area 2</textarea>
    <textarea id="textArea3" style="display:none;">This is Text Area 3</textarea>
</div>

<script>
    function showTextArea(textAreaId) {
        // Hide all text areas
        var textAreas = document.querySelectorAll('textarea');
        textAreas.forEach(function(textArea) {
            textArea.style.display = 'none';
        });

        // Show the selected text area
        var selectedTextArea = document.getElementById(textAreaId);
        if (selectedTextArea) {
            selectedTextArea.style.display = 'block';
        }
    }
</script>
</body>
</html>

