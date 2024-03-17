# File-sharing-website-<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>File Sharing Website</title>
    <style>
        /* Add your CSS styles here */
        body {
            font-family: Arial, sans-serif;
        }
        #file-input {
            display: none;
        }
        #upload-button {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            cursor: pointer;
        }
        #file-list {
            margin-top: 20px;
        }
        .file-item {
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <h1>File Sharing Website</h1>
    <input type="file" id="file-input" multiple>
    <button id="upload-button">Upload Files</button>
    <div id="file-list"></div>

    <script>
        // JavaScript code to handle file uploading and listing
        document.getElementById('upload-button').addEventListener('click', function() {
            document.getElementById('file-input').click();
        });

        document.getElementById('file-input').addEventListener('change', function(event) {
            var fileList = event.target.files;
            var fileListContainer = document.getElementById('file-list');
            fileListContainer.innerHTML = ''; // Clear previous file list

            for (var i = 0; i < fileList.length; i++) {
                var fileItem = document.createElement('div');
                fileItem.classList.add('file-item');
                fileItem.textContent = fileList[i].name;
                fileListContainer.appendChild(fileItem);
            }
        });
    </script>
</body>
</html>
<script>
    // JavaScript code to handle file uploading and listing
    document.getElementById('upload-button').addEventListener('click', function() {
        document.getElementById('file-input').click();
    });

    document.getElementById('file-input').addEventListener('change', function(event) {
        var fileList = event.target.files;
        var fileListContainer = document.getElementById('file-list');
        fileListContainer.innerHTML = ''; // Clear previous file list

        for (var i = 0; i < fileList.length; i++) {
            var fileItem = document.createElement('div');
            fileItem.classList.add('file-item');
            fileItem.textContent = fileList[i].name;
            fileListContainer.appendChild(fileItem);
        }
    });
</script>
