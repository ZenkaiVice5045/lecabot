# LeCabot by phospho🧪

phospho is introducing **LeCabot.** A mobile manipulator mod for the SO-100 robot arm and the Go2 robot dog, controlled with a Meta Quest thanks to [phosphobot.](https://github.com/phospho-app/phosphobot)

An open source and low cost alternative to Spot by Boston Dynamics. Star this repo and start building!

# Bill of Materials

| Part                                                                | Amount |                                Unit Cost (US)                                 | Buy (US)                                                                                                                                                                      | Unit Cost (EU) |                                                                                                  Buy (EU) | Unit Cost (CN) | Buy (CN)                                                           |
| :------------------------------------------------------------------ | :----: | :---------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------: | --------------------------------------------------------------------------------------------------------: | :------------: | ------------------------------------------------------------------ |
| Raspberry Pi 5 (4GB)                                                |   1    |                                    \$60.00                                    | [Adafruit](https://www.adafruit.com/product/5812)                                                                                                                             |     €57.00     |         [Mouser](https://eu.mouser.com/ProductDetail/Raspberry-Pi/SC1111?qs=HoCaDK9Nz5fnLhlMNnKTiQ%3D%3D) |     ￥ 410     | [Taobao](https://e.tb.cn/h.64IIvlisvAL15g8?tk=fdOVexkHECW)         |
| 12v 5a Battery                                                      |   1    |                                    \$32.99                                    | [Amazon](https://www.amazon.com/KBT-Rechargeable-Connector-Replacement-Security/dp/B0C242DYT1/ref=sr_1_2_sspa?)                                                               |     €45.79     |                                                             [Amazon](https://www.amazon.fr/dp/B0D5QSMW21) |     ￥ 70      | [Taobao](https://e.tb.cn/h.64IJNTnXwhn44BS?tk=PQQ8exkJEtR)         |
| Lever Wire Connector                                                |   1    |                                    \$6.70                                     | [Amazon](https://www.amazon.com/Wago-221-413-LEVER-NUTS-Conductor-Connectors/dp/B06XGYXVXR/ref=sr_1_4)                                                                        |     €7.18      |     [Amazon](https://www.amazon.fr/221-413-fil-%C3%A9lectrique-connecteur-220-240-Terminal/dp/B01AKF3I58) |    ￥ 3.50     | [Taobao](https://e.tb.cn/h.64r0Z6Y5jZczq5q?tk=XEaSex908q0)         |
| 12v 5a DC plug connector                                            |   1    |                                    \$9.49                                     | [Amazon](https://www.amazon.com/43x2pcs-Connectors-Security-Lighting-MILAPEAK/dp/B072BXB2Y8/ref=sr_1_11)                                                                      |     €8.99      | [Amazon](https://www.amazon.fr/RUNCCI-YUN-Alimentation-dalimentation-Connecteur-Surveiller/dp/B0CX44HTKZ) |    ￥ 3.10     | [Taobao](https://e.tb.cn/h.64IFOvrMdUVoQQX?tk=nahtexkvokE)         |
| 12v to 5v 5a USB-C converter                                        |   1    |                                    \$9.99                                     | [Amazon](https://www.amazon.com/Klnuoxj-Converter-Interface-Waterproof-Compatible/dp/B0CRVW7N2J?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&smid=A1QRG6NHEUKUZO&gQT=0&th=1) |     €9.99      |   [Amazon](https://www.amazon.fr/Greluma-convertisseur-Adaptateur-dalimentation-Compatible/dp/B0D7VDL2X6) |     ￥ 20      | [1688](https://qr.1688.com/s/Eb6ykv4y)                             |
| M5 x 30mm Screw Kit                                                 |   1    |                                    \$8.99                                     | [Amazon](https://www.amazon.com/Mywish-50Sets-Stainless-Washers-Spanner/dp/B0DJP888H2)                                                                                        |     €15.83     |       [Amazon](https://www.amazon.fr/hexagonale-inoxydable-Entièrement-Fileté-Boulons/dp/B08RN8QY5J?th=1) |     ￥ 24      | [Taobao](https://za.meest-shop.com/en/taobao/product/717340363892) |
| Unitree Go2 (Air, Edu, or Pro)                                      |   1    | [Official Unitree Store](https://shop.unitree.com/en-fr/products/unitree-go2) |
| [12V SO-100 or SO-101](https://github.com/TheRobotStudio/SO-ARM100) |   1    |      Get your dev kit on [robots.phospho.ai](https://robots.phospho.ai)       |
| **Total**                                                           |        |                                 **\$128.16**                                  |                                                                                                                                                                               |  **€144.78**   |                                                                                                           | **￥ 530.60**  |                                                                    |

> [!NOTE]
> Prices and items may vary depending on geographic location and time of purchase.

# 3D Printing

1. Print the [SO-100 mount for the Go2](./3DPrintMeshes/SO-100_Go2_Mount.stl), made by [the golden-robot-retriever team](https://github.com/DominiquePaul/golden-robot-retriever) and Philipp from Mimic.
2. Drill holes with a 5 mm drill through the SO-100 mount for the Go2.
3. Print the [Raspberry Pi 5 case](./3DPrintMeshes/RPi-5_case_slim_port.stl).

# Assembly

# Setup

1. Install phosphobot on your raspberry pi 5, with the username `phosphobot`

```bash
curl -fsSL https://raw.githubusercontent.com/phospho-app/phosphobot/main/install.sh | sudo bash
```

[See the full tutorial here.](https://docs.phospho.ai/installation#setup-your-raspberry-pi)

2. Install the [Meta Quest app phospho teleoperation.](https://www.meta.com/en-gb/experiences/phospho-teleoperation/8873978782723478/) It's compatible with Meta Quest 2, Pro, 3, and 3s.

3. Plug everything together. Start your raspberry pi 5. The phosphobot dashboard is accessible on `<YOUR LOCAL RPI IP>:80` in your browser. The SO-100 robot arm should be automatically detected.

4. Turn on the Unitree Go2 by pressing the button, and wait for it to stand up.

5. In the phosphobot dashboard, click in the top right on the robot head, then click on "Connect to another robot".

   ![Connect](./images/connect_1.png)

   Select Unitree Go2, then select or enter the IP address of the Unitree.

   ![Connect](./images/connect_2.png)

   _Tip: The MAC address of the Unitree often starts with `78:22:88`. You can also use the Unitree mobile app to discover the IP and MAC address of your Go2. Make sure the Unitree remote controler and Unitree mobile app are disconnected._

6. Start the Meta Quest app and select your phosphobot server in the list. [See here for a full tutorial](https://docs.phospho.ai/examples/teleop).

7. Press A to start the teleoperation. Move the robot dog with the right joystick. Move the SO-100 by moving your arm around. Have fun!

---

Share your demos and tag [our twitter account](https://x.com/phospho_ai) so we can repost you!

Join our [Discord server](https://discord.gg/cbkggY6NSK) to keep the conversation going.

Made with 💚 by the Phospho community
