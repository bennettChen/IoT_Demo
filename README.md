# IoT_Demo


|-----------------------|         |-----------------------|        |----------------|
| Alexa Server          |         | AWS Lambda            |        | AWS IoT        |
| (Amazon cloud service)|<------->| (Amazon cloud service)|<------>| (cloud service)|
|-----------------------|         |-----------------------|        |----------------|
       ^                                                                ^
       |                                                                |
       |                                                                |
       v                                                                v
|----------------|                                 |--------------------------------|
| Alexa Client   |                                 |             | AWS IoT client SW|             
|----------------|                                 |             |------------------|       |-------------|
| Raspberry Pi 3 |                                 |             |   BLE cmd Daemon |<----->|Thunderboard™|
|----------------|                                 |             |------------------|       |(IoT device) |
                                                   |                                |       |-------------|           
										                        		   |  Lab AP in development         |
                                                   |--------------------------------|
說明：
這是研發中的無線AP的實驗板。
AP可收發藍芽裝置的訊號以控制與AP相連的IoT裝置。
研發目標為在另一地點用Alexa人工智慧音箱，語音控制與此AP相連的IoT裝置，或讀取此IoT裝置的狀態。
(僅限英文發音)
1. Lab AP上有兩支程式。
   1支用來與Thunderboard連線與收發訊息，是支常駐的Daemon.
   另一支是用來與雲端的AWS IoT service 作連結，並一直上傳IoT的狀態資訊。如 溫度，溼度，壓力，音量....等。
   (AWS IoT 需作其它設定)
2. 在樹莓派3上先安裝了Alexa客戶端程式，以模擬Alexa智慧音箱。並於Alexa cloud service 上新增自己的Skill。
   此Skill將送出解譯語音指令的結果給AWS Lambda。以作進一步的處理。
3. AWS Lambda可從AWS IoT 得到IoT裝置的狀態資訊。或設定(寫入操作)此IoT裝置(透過AP上的Daemon)。
(demo video中即為Thunderboard的led閃光)


Thunderboard™ Sense 2 : IoT device
https://www.digikey.tw/zh/product-highlight/s/silicon-laboratories/thunderboard-sense-2-next-generation-iot-development-kit

My  Alexa  Skill: 
lab  sensor: 
https://www.amazon.com/Bennett-Chen-lab-sensor/dp/B07D35GWRB
house  sensor:
https://www.amazon.com/Bennett-Chen-house-sensor/dp/B079YPDHLJ
GuestNetwork:
https://www.amazon.com/Bennett-Chen-GuestNetwork/dp/B078X5YZJH


