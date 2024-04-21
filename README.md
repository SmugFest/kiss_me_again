<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Auto-play MP4</title>
</head>
<body>
    <video id="myVideo" autoplay controls>
        <source src="https://github.com/SmugFest/kiss_me_again/assets/167689974/d3e735e7-e0ea-4ec0-93bf-f7f5994a385c" type="video/mp4">
        Your browser does not support the video tag.
    </video>

    <script>
        // Get the video element
        var video = document.getElementById("myVideo");

        // Set the volume to max
        video.volume = 1.0; // 1.0 is the maximum volume

        // Add event listener to handle errors and play the video
        video.addEventListener('error', function() {
            console.error('Failed to load the video');
        });

        video.play();
    </script>
</body>
</html>
