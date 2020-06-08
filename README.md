# IoT_Demo
<br>

<img src="https://github.com/bennettChen/IoT_Demo/blob/master/iot-demo.gif">



說明：<br>
這是研發中的無線AP的實驗板。<br>
AP可收發藍芽裝置的訊號以控制與AP相連的IoT裝置。<br>
研發目標為在另一地點用Alexa人工智慧音箱，語音控制與此AP相連的IoT裝置，或讀取此IoT裝置的狀態。<br>
(僅限英文發音)<br>
1. Lab AP上有兩支程式。<br>
   1支用來與Thunderboard連線與收發訊息，是支常駐的Daemon.<br>
   另一支是用來與雲端的AWS IoT service 作連結，並一直上傳IoT的狀態資訊。如 溫度，溼度，壓力，音量....等。<br>
   (AWS IoT 需作其它設定)<br>
2. 在樹莓派3上先安裝了Alexa客戶端程式，以模擬Alexa智慧音箱。並於Alexa cloud service 上新增自己的Skill。<br>
   此Skill將送出解譯語音指令的結果給AWS Lambda。以作進一步的處理。<br>
3. AWS Lambda可從AWS IoT 得到IoT裝置的狀態資訊。或設定(寫入操作)此IoT裝置(透過AP上的Daemon)。<br>
(demo video中即為Thunderboard的led閃光)<br>

<br>
Thunderboard™ Sense 2 : IoT device<br>
https://www.digikey.tw/zh/product-highlight/s/silicon-laboratories/thunderboard-sense-2-next-generation-iot-development-kit<br>

My  Alexa  Skill: <br>
lab  sensor: <br>
https://www.amazon.com/Bennett-Chen-lab-sensor/dp/B07D35GWRB<br>
house  sensor:<br>
https://www.amazon.com/Bennett-Chen-house-sensor/dp/B079YPDHLJ<br>
GuestNetwork:<br>
https://www.amazon.com/Bennett-Chen-GuestNetwork/dp/B078X5YZJH<br>


