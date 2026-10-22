# TVHeadend-InBrowser-Player-for-Samsung-TV
Lightweight (&lt;40K), TV Guide and player Web App for TVHeadend and Samsung TV.

<img width="2660" height="1365" alt="Screenshot 2026-10-21 220234" src="https://github.com/user-attachments/assets/b5d955d2-4fca-4625-aa7b-f2d5e7853247" />


This app was coded to my preferences with objectives of avoiding any additional apps or hardware to play TV streams from my personal TVHeadend server on my Samsung TVs. Apparently Samsung TVs with browser based on older WebKit are able to play default HTTP streams from TVHeadend beautifully. I am yet to find codecs these TVs cannot play. All broadcasts with MP2, H.264, AVC and HEVC, playing just fine. Provided code just wraps this capability into convenient guide grid.

I rarely do recordings, so this functionality is not implemented here, but feel free to grab this code and develop further.

## Using with other hardware:
While page can be opened in any browser, but HTTP stream playback is not supported by most browsers for PC, Mac or other devices that I have. Does not mean it cannot work on some other platforms, TVs or device, but I am not aware of it. You try and report. For me - this is intended and tested only with my Samsung TVs.

Installation: My TVHeadend running on RPi3. Depending on exact flavor of your hardware and Linux, you may have to adjust these instructions.

- Create new directory "/samsung-guide" in "/usr/share/tvheadend/src/webui/static".
- Copy "index.html" from this repository to newly created directory on your TVHeadend server. Can be done with single line terminal command: "sudo wget -O /usr/share/tvheadend/src/webui/static/samsung-guide/index.html http://...." You must enter HTTP location and the name of HTML file, obviously.
- Depending on your security settings you may need to set file and new directory permissions. I did not need to do that, SUDO did it as root and everything apparently working.
- Open Web browser on Samsung TV:  "http://[TVHeadend IP address]:9981/static/samsung-guide/index.html"
- Page has default credentials settings "user" for user and "password" for password. Adjust these under "settings" button on the page to match your server.
- The rest I believe is self explanatory.

Let me know how it works for you.
