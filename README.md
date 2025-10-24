# esphome-a2dp2eth
## WIP: THIS IS A WORK IN PROGRESS!!!
Open Source ESPHome firmware for ESP32 BT A2DP steaming to a TCP server [over Ethernet] (ex: LilyGo T-Internet-POE)

As I was building out my fully open smarthome, I finally got around to replacing my GHome speakers with open speakers from FutureProofHomes. While I love Snapcast paired with Music Assistant/Home Assistant, there's no way for myself or guests in my home to "cast" their own music to my speakers on the fly. That lack of on-demand casting kinda bugged me. One of the main limitations of ESP32 devices is the inability to [reliably] co-exist BT and WiFi on the same controller; there simply is no way to enable BT A2DP support on a device such as the Satellite1 while maintaining WiFi connectivity. 

So, I purchased a LilyGo T-Internet-POE with a mission in mind: To deploy one in each main area of my home, connected to PoE ethernet, waiting and ready to accept BT media connections and send them to a TCP stream server such as Snapcast as a Source for casting to as many speakers as I desire. While I did find a wonderful ESP32 project for A2DP support, which I will be heavily borrowing from, it was intended to send that received audio and output to a DAC/Speaker. 

I will be borrowing code from all over the place, as ESPHome/ESP-IDF is not my forte (but I have a strong Arduino/C background), and the goal is to provide a universal ESP32 BT A2DP sink to TCP Stream package that can be utilized with nearly any ESPHome compatible board, but focusing on Ethernet boards like those from LilyGo, M5Stack, Olimex, etc.
