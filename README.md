<!DOCTYPE html>
<html>
<head>
    <title>Random Funny Videos</title>
</head>
<body>
    <h1>Welcome to the Random Funny Videos Page</h1>
    <p>Click the button below to watch a random funny video:</p>
    <button id="generateVideo">Generate Random Video</button>
    <div id="videoContainer">
        <!-- This is where the video link will be displayed -->
    </div>
    <script>
        // Array of funny video links
        var videoLinks = [
            "https://www.youtube.com/watch?v=VIDEO_ID_1",
            "https://www.youtube.com/watch?v=VIDEO_ID_2",
            "https://www.youtube.com/watch?v=VIDEO_ID_3",
            // Add more video links here
        ];

        // Function to generate a random video link
        function generateRandomVideo() {
            var randomIndex = Math.floor(Math.random() * videoLinks.length);
            var randomVideoLink = videoLinks[randomIndex];
            var videoContainer = document.getElementById("videoContainer");
            videoContainer.innerHTML = '<a href="' + randomVideoLink + '" target="_blank">Watch Random Funny Video</a>';
        }

        // Add an event listener to the button
        var generateButton = document.getElementById("generateVideo");
        generateButton.addEventListener("click", generateRandomVideo);
    </script>
</body>
</html>

