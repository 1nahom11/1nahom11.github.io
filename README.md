# 1nahom11.github.io
<!DOCTYPE html>
<html>
	<head>
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<link rel="stylesheet" href="/css/iframe.css">
		<link rel="stylesheet" href="/css/index.css">
		<link rel="icon" type="image/png" href="/img/cornicon.png">
		<title>Corn Pr0xy</title>
	</head>
	<body>
		<div class="center">
			<div class="center-block">
				<a class="button inline" href="/index.html">Back</a>
				<a class="button inline" href="/license.txt">License</a>
			</div>
			<div class="center-block">
				<input type="text" id="text" />
				<button class="button inline" onclick="enter()">Enter</button>
			</div>
		</div>
		<iframe allow="fullscreen" id="iframe" src="/other/select.html"></iframe>
		<script>
			var gamelist = { "proxy": "https://pr0xy.vaughanm.tk/loader.html" };
		</script>
		<script src="/scripts/gameinfo.js"></script>
		<script>
			let proxy = getGameUrl("proxy");
			function setUrlForIframe(e) {
                let input = document.getElementById("text");
                let iframe = document.getElementById("iframe");
                iframe.contentWindow.postMessage("input:" + input.value, "*");
				iframe.removeEventListener("load", setUrlForIframe);
			}
			function enter() {
                let iframe = document.getElementById("iframe");
				iframe.addEventListener("load", setUrlForIframe);
				iframe.src = proxy;
			}
			document.getElementById("text").addEventListener("keydown", function (e) { if (e.code === "Enter") { enter(); } });
		</script>
		<script src="/scripts/themeloader.js"></script>
	</body>
</html>
