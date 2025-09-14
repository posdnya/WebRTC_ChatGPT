1. Start signaling server
cd D:\development\WebRTC_ChatGpt5
node signaling-server.js

2. Start cloudflare
cloudflared tunnel --url http://localhost:8787
cloudflared will output something like:
 https://cam-enforcement-appendix-forward.trycloudflare.com

created elecard-signal.com domain name at cloudeflare
set ws tunneling via ws.elecard-signal.com
NOT FINISHED YET
cloudflared tunnel run webrtc-signal

3. fast check if it working
in powershell
npx wscat -c wss://cam-enforcement-appendix-forward.trycloudflare.com
 
4. Open index.html
in WS URL type ws://cam-enforcement-appendix-forward.trycloudflare.com
in room name type "posdnya"

5. On viewer open 
https://andreyposdnyakov.github.io/webrtc/?role=viewer&ws=wss%253A%252F%252Fandreyposdnyakov.github.io%253A8787&room=posdnya&autoconnect=1
in WS URL type ws://cam-enforcement-appendix-forward.trycloudflare.com
check room name - must be "posdnya"
push Connect button

6. On sender push Connect button
7. Press Share Window button, choose the window to share
8. Press Create offer

check the viewer - it must start to show the shared window.