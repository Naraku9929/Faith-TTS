FAITH TTS setup instructions

You need these 4 files:
- HTML.txt
- CSS.txt
- JS.txt
- fields.txt

Follow the steps in this order.


Set up the StreamElements overlay
1. Open StreamElements in your browser.
2. Go to:
   Streaming Tools > My Overlays

3. Create a new overlay, or open the overlay you want to use.
4. Add a Custom Widget.
5. Open the widget editor.
6. Paste the files into the matching tabs:

   HTML tab:
   paste the HTML file Content

   CSS tab:
   paste the CSS file Content

   JS tab:
   paste the JS file Content

   Fields tab:
   paste the JSON / fields file Content

7. Save the widget.
8. Open the widget settings/fields and check these values:

   Twitch reward title:
   Faith TTS

   Twitch reward ID:
   Use the real Twitch reward ID if you have it.
   Example format:
   xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

   UNSAFE fallback: accept any channel point redemption if no reward name/ID is visible:
   OFF / unchecked

   Leave this OFF unless you are only testing. If this is ON, other channel point redeems may also trigger the TTS.

   Debug mode:
   ON while testing
   OFF later if everything works

   Volume:
   1

   Caption seconds:
   7 to 20

9. Save the overlay.
10. Copy the StreamElements overlay URL. You will need it for OBS.

Set up the Twitch channel point redeem
1. Open Twitch Creator Dashboard.
2. Go to:
   Viewer Rewards > Channel Points > Manage Rewards & Challenges

3. Create a new Custom Reward, or edit an existing one.
4. Set the reward name to exactly:
   Faith TTS

   The spelling must match.

   Correct:
   Faith TTS

   Wrong:
   Faith-TTS

5. Turn ON:
   Require Viewer to Enter Text

   This is important. The viewer's typed message is what the TTS will speak.

6. Set the cost to whatever you want.

   For testing, use a low cost like:
   1 or 100

7. Add a simple prompt, for example:
   What should the FAITH voice say?

8. Make sure the reward is enabled and not paused.
9. Save the reward.
10. Test it from Twitch by redeeming the reward and typing a short message.


Add the overlay to OBS
1. Open OBS.
2. Go to the scene where you want the TTS to appear.
3. Click the + button in Sources.
4. Choose:
   Browser

5. Name it something clear, for example:
   Faith TTS

6. Paste the StreamElements overlay URL into the URL box.
7. Set the size to:
   Width: 1920
   Height: 1080

8. Turn ON:
   Control audio via OBS

9. Click OK.
10. In the OBS Audio Mixer, make sure the Faith TTS source is not muted.
11. If you want to hear it yourself, open Advanced Audio Properties and set Faith TTS to:
   Monitor and Output

   If you only want the stream to hear it, use:
   Output only

12. Put the Faith TTS source above your game/capture sources so the text appears on top.
13. Right-click the Faith TTS source and choose:
   Properties

14. Click:
   Refresh cache of current page

15. Click OK.

If it does not work

Check these first:

1. The Twitch reward name must be exactly:
   Faith TTS

2. Require Viewer to Enter Text must be ON.
3. The StreamElements overlay must be saved.
4. The OBS browser source must use the StreamElements overlay URL.
5. The OBS browser source must be visible and above the main capture source.
6. The OBS browser source must not be muted.
7. In OBS, right-click the Faith TTS source, open Properties, and click:
   Refresh cache of current page

8. If it only works when the unsafe fallback is ON, update to the latest JS. The newer JS reads StreamElements' channel-points-latest redemption name and should not need the unsafe fallback.
