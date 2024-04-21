<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Video Page</title>
</head>
<body>
    <div id="player"></div>

    <script src="https://www.youtube.com/iframe_api"></script>
    <script>
        let player;

        function onYouTubeIframeAPIReady() {
            player = new YT.Player('player', {
                videoId: 'IDQYlsDqpAU', // Replace with your video ID
                events: {
                    'onReady': onPlayerReady
                }
            });
        }

        function onPlayerReady(event) {
            event.target.playVideo();
            event.target.mute();
            event.target.setPlaybackQuality('hd720');
            event.target.setVolume(100);
            event.target.setSize(window.innerWidth, window.innerHeight);
            document.addEventListener("fullscreenchange", function () {
                event.target.setSize(window.innerWidth, window.innerHeight);
            }, false);
        }
    </script>
</body>
</html>
