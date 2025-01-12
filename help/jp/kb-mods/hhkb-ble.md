# HHKB BLE Mod

<table_w30x70>

|PCB | YANG |
|:--- |:--- |
|Firmware | YANG |
|Keymap Editor | YANG |
|Solder | YANG / 兰某人 |
|Test | YANG / 兰某人 |
|Seller | YANG / KBDFans |

</table_w30x70>

For sale：https://item.taobao.com/item.htm?id=590221409485  

<!-- For installation, please refer to the product introduction on Taobao above. -->
インストール方法については、Taobaoの製品説明を参照してください。
  
<!-- If you knew about Hasu's HHKB Mod, it is easy to understand this one. Simple to say, it is an  power-saving optimized version. The power saving of hardware comes from two ways. One is that the Bluetooth uses a ble module, and the other is that the working voltage needs only 3.3v no 5v. The power saving of software comes from the power saving strategy formulated according to the characteristics of the hardware. Taken together, the battery life may be 6 to 10 times improve from Hasu version. But the biggest hero is still him (the entire HHKB keyboard part of the scanning works), I just stand on the achievements of predecessors and improve the product. -->
hasuコントローラに詳しい人にとって、あんまり紹介いらないと思います。簡単的に言えば、電力消費を抑えたバージョンになります、抑えられた原因として二つあり、一つ目はbluetoothモジュールはbleになり、もう一つは電源供給は5vを必要としてなくなり、3.5vから5vへのコンバーター必要なくなりました。バッテリーのソフトウェア管理部分も、ハードウェアの特性から設計されており。ソフトウェアとハードウェアの組み合わせにより、使用可能の時間が6から10倍増えます。しかし、最も大きな英雄は、やはりhasuコントローラのキーボード部分のスキャン構造である、自身はhasuコントローラのデザインを基づいて、製品を改善したものです。

<!-- Most information, please refer to the BLE Series Part. Here we mainly talk about some special features of HHKB BLE Mod. -->
BLEモジュールについて、前helpページののBLE Seriesを参照してください、ここではHHKB BLE Modについて一部特徴を話します。

<!-- Note: This section is for the latest firmware of ydkb.io. -->
メモ：このページ内容の対象は最新版ファームウェアになります。

<!-- The firmware changelog can be found at: [HHKB BLE firmware changelog ](changelog/hhkb_ble) -->
ファームウェアの変更履歴はこちらを参照してください。[HHKB BLE firmware changelog ](changelog/hhkb_ble)


## Bluetooth ペアリング方法 (Bluetooth Pairing)

<!-- In short, there is no need to enable pairing mode. When Bluetooth is unconnected and discoverable, you can pair it. Mainly refer to this section: [BLE Series](/en/ble-series) -->

端的に言いますと、ペアリングモードを有効化にする必要はありません。Bluetoothが接続されていない状態で、可視状態になっているときにペアリングすることができます。このセクションを参照してください。[BLE Series](/en/ble-series)

<!-- If you have any problem, use ・ instruction to do troubleshooting: [BLE troubleshooting](/en/ble-series/troubleshooting) -->
もし接続に問題がある場合、この文章を参照し、トラブルシューティングしてください[BLE troubleshooting](/en/ble-series/troubleshooting)


## HHKB BLE用物理スイッチ (Hardware Switch of HHKB BLE)

<!-- There is a physical switch behind the dip switch cover. This is the only switch on the controller.  -->
純正のdipスイッチ部分のところに、ON/OFFスイッチに変更しました、これは、このコントローラにある唯一の物理スイッチです。

<html><div class="attention"> 
<subtitle>注意(ATTENTION):</subtitle>
<!-- <ul><li>This switch's function is to turn on/off the battery power supply, not Bluetooth.</li> -->
<ul><li>このスイッチはバッテリーへの電源供給を切り替えるだけのものになります、bluetoothモジュールへの給電はスイッチングしません。</li>
<!-- <li>Thus when this switch is turned off, if you plug in the USB cable, Bluetooth can still work as in this case USB is the power source.</li> -->
</ul><li>このため、USB接続中でスイッチoffであっても、bluetoothモジュールへの給電は続いてるため、bluetootの使用は可能になります。</li></ul>
</div></html>

<!-- The switch can be easily dialed by using the cover directly, close to the USB port (left in the figure below) is open, and away from the USB port (right in the figure below) is closed. When the keyboard is working abnormally, it is also necessary to turn off the switch and then turn it on again to restart the keyboard. -->
このスイッチは元のdipスイッチのフタで棒などを利用しなくても切り替えることができます、USBポート(左側)に近いときはオンて、USBポート(右側)に遠いときはオフになります。キーボードが異常動作している場合、スイッチをオフにしてからオンにすることで再起動になります。

<div style="width: 600px">

![](/assets/hhkb_ble_sw.jpg?600)
</div>

<!-- If you want to turn off Bluetooth, refer to [Bluetooth switch & connection status](/en/ble-series/connection-status) -->
bluetoothを有効化したい場合は、[Bluetooth switch & connection status](/en/ble-series/connection-status)を参照してください。

<html><div class="hint">
<subtitle>HINT</subtitle>
<!-- <ul><li>this software switch is designed to turn off **Bluetooth FUNCTION** completely for people who only or temporarily only use USB. It is recommended to turn off the physical power switch While this switch is off.</li> -->
<ul><li>上記ページのソフトウェアのbluetothスイッチは、一時的・もしくはUSBだけ使用する人向けのものになります。そうであればハードウェアスイッチもオフにしてください。</li>
<!-- <li>It is not designed for turning off Bluetooth daily to save energy as HHKB BLE consumes much more power when standby by using this function than Lock Mode.</li></ul> -->
<li>ソフトウェアのbluetootスイッチは、日常使用でバッテリー節約のためのものではありません、HHKB BLEでは、これらを使用しオフにした場合、エコモードレベル2よりもバッテリーを消費します。</li></ul>
</div></html>


## バッテリ充電 (Battery Charging)

<!-- The charging port and data port are both the small USB port on HHKB, not two large USB female ports. -->
充電と通信可能のポートは小さい方の1ポートだけになります(mini USB or USB-C)、大きい方のUSB2.0 Type-Aではありません。

<html><div class="attention">
<!-- <subtitle>It is recommended to use the PC's USB port or 5v charger to charge.</subtitle> -->
<subtitle>PCからのUSBポートもしくは5vのUSB充電器を推奨されています。</subtitle>
<br>Improper charging(like more than 6v) may broke the charging IC. Using a high-power charger will not increase the charging speed as the default charging current is limited to about 450mA.<br>高電力の充電器を使用しても、充電速度が上がりません。充電速度はデフォルトで450mAに制限されています。USBから電力供給はクリアの状態で,2500mAHの電池はおよそ6時間で満充電できます。高速充電器やサポートしない充電器を使用する場合、高電圧によって内臓充電ICを壊す可能性があります。
</div></html>

<!-- The charging indicator is a red led below the left USB HUB port(if hardware version is more than v2.5, it is a blue led). You can see it from the back. It has three states: -->
充電のインジケーターランプは左側のUSB HUBポートの下にあります。（基板がv2.5以上の場合は、青色と赤色のLEDになります。）ポートから覗くことで見ることができます。3つの状態があります:

<table_w30x70>

<!-- | Charging LED status | Meaning |
| ---- | ---- |
| Low brightness or flicker | abnormal(no battery or battery problem) |
| High brightness | charging |
| Off or extremely low brightness | the battery is fully charged | -->

|  LED状態 | 意味 |
| ---- | ---- |
| 低輝度 もしく 点滅 | 異常 (バッテリー切れか電池異常) |
| 高輝度 | 充電中 |
| 光らない もしく 極めて低輝度 | 満充電 |

</table_w30x70>

<!-- Generally it is no need to pay too much attention to this indicator light. You can know how long it takes to charge after one charge. -->
一般的にこれらのインジケーターを気にする必要がありません、基本的に一回の充電をやればだいたいいつ終わるかの時間を知ることができます。

<!-- In win10 1809 or later, the battery percentage display is supported. It is not accurate and is for reference only (especially the error displayed during charging will be greater). Every 10% is a level and the highest is 90%. In addition, the percentage is displayed as x1% during charging which is 1% more than when not charging as the following pic shows. -->
Win10 1809 もしくは以降では、バッテリー残量の表示はOSでサポートされています。（正確な数値ではありません、充電中に表示されるものはより誤差が大きくなります。）10%ごとに一区間となり、最高は90%です。充電中の時はx1%として表示されます（バッテリーではx0%）。

<div style="width: 450px">

![](/assets/hhkb-ble-charge.png?450)
</div>  

<!-- When fully charged, the charging indicator will go off or the brightness will be extremely low. -->
満充電時には、インジケーターが消えるか、輝度が極めて低い状態になります。

<!-- Mac has blocked the battery service of third-party Bluetooth devices. Thus we can use **Output Battery Percetage as Text** function (default hotkey for HHKB BLE is Fn+E) if we want to know the battery level:__[[ble-series: blebattery | Charge & Battery Information]]__ -->
Macでは、サードパティBluetoothデバイスのバッテリーサービスをブロックしています。そのため、バッテリー残量を知りたい場合は、**バッテリー状態をテキスト出力** を使用します（HHKB BLEのデフォルトのホットキーはFn+E）:__[[ble-series: blebattery | Charge & Battery Information]]__


## キーマップの変更やファームウェアの更新 (Edit Keymap and Reflash Firmware)

<!-- Open the website https://ydkb.io, select the keyboard **HHKB BLE**, and then there is its flashing method on the page [Mass Storage Device Bootloader (U Disk Mode)] (bootloader/msd-bootloader). Refer to other parts of this document for the description of the key editor. -->
https://ydkb.io/ を開き、左のメニュから **HHKB BLE もしく (HHKB BLE S)** を選択し、そのページでは、[Mass Storage Device Bootloader (U Disk Mode)] (bootloader/msd-bootloader) にあるフラッシュ方法を参照してください。このドキュメントの他の部分については、key editorセクションを参照してください。


<!-- In addition to pressing the upper left key (usually ESC) to insert the cable to enter the flashing mode, you can also use the <kbd>Reset</kbd> in **LEDs and Functions**, in order to prevent accidental pressing, you need to hold down the < kbd>LCtrl</kbd>, and then press this <kbd>Reset</kbd>, you can jump directly to the flashing mode without unplugging and replugging. -->
一番左上のキー（ESC）を押したまま、ケーブルを挿入することでフラッシュモードに入ります。また、LEDs and Functionsの<kbd>Reset</kbd>を使用することで、誤作動を防ぐために、<kbd>LCtrl</kbd>を押している間にこの<kbd>Reset</kbd>を押すことで、フラッシュモードに移行することができます。


<html><div class="attention">
<subtitle>注意(ATTENTION)</subtitle>
<!-- <ul><li>In addition to the choice of <b>HHKB BLE</b> for the keyboard, you can also use <b>HHKB BLE S</b>. </li> -->
<ul><li>キーマップの選択は <b>HHKB BLE</b> か,  <b>HHKB BLE S</b> でも使用可能です。 </li>

<!-- <li>This firmware with S has a faster response speed, and it is temporarily unable to guarantee compatibility with all HHKBs. Most of them should be fine. </li> -->
<li>Sバージョンでの応答速度はより高速になっていますが、現在では全HHKBモデルへの互換性を確認できてないですが、基本的に問題にはなりません</li>
<!-- <li>If your keyboard has no compatibility issues, it is strongly recommended to choose the firmware of <b>HHKB BLE S</b>. </li><ul> -->
<li>お持ちのHHKBで互換性の問題がなければ、 <b>HHKB BLE S</b>への利用をお勧めします。 </li><ul>
</div></html>


## lEDインジケーターと省エネルギー(Indicators and Power Saving)

<!-- Common functions for indicators can be defined by [LEDMAP](en/features/ledmap) . The indicator lights only when the keyboard is working, not power saving. It is recommended not to set any indicators to a function that may keep it constantly on as that may increase the power consumption and significantly reduce the battery life. -->
一般的な機能は、[LEDMAP](en/features/ledmap) によって定義できます。インジケーターは、キーボードが動作中のみ点灯します。省エネルギーのためには、常に点灯する設定を推奨しません。これは、電池消費量を大幅に増加させ、電池残量を大幅に減らす可能性があります。

<html><div class="hint">
<subtitle>ヒント(HINT)</subtitle>
<!-- <br>As mentioned above, the red light under the USB port on the left is the charging indicator. In addition, the green light below the USB on the right is equivalent to LED3. -->
<br>USBポートの下にある赤いライトは、充電中のインジケーターです。また、右側のUSBの下にある緑色のライトは、LED3と同義です。
</div></html>

<!-- Default LEDMAP Setting is LED1 for CapsLock，LED2 for Layer1(fn)，LED3 for Layer2. -->
デフォルトにLEDMAPに設定されているものは、LED1:Capslock LED2:FNレイヤー LED3:レイヤー2になります。 
<!-- The default LEDMAP settings is as below. If you want to modify it yourself, please see [LEDMAP](en/features/ledmap). -->
LEDMAPを変更したい場合は、[LEDMAP](en/features/ledmap) を参照してください。

<table_w30x70>

<!-- | Indicator | Default setting |
|:--- |:--- |
| LED1(default red) | CapsLock |
| LED2(default yellow or white) | Layer1(It will light up when you press Fn/L1.) |
| LED3(default green) | Layer2 | -->
| インジケーター | デフォルト値 |
|:--- |:--- |
| LED1(デフォルト 赤) | CapsLock |
| LED2(デフォルト 黄色 もしくは しろ) | Layer1(FNキー押し込みでレイヤー1に切り替わる時に点灯)) |
| LED3(デフォルト 緑) | レイヤー2 | 

</table_w30x70>

<div class="attention">
<subtitle>bluetoothモードでの注意事項(ATTENTION when in bluetooth mode)</subtitle>

  <!-- - In bluetooth mode，The Num, Caps, and Scroll Lock indicators are not synchronous with the OS status in Bluetooth mode. 
  - In bluetooth mode, They just toggle on or off when pressed. They are synchronous in USB mode.
  - If one indicator is out of sync, you can use Shift + KEY, such as Shift + Capslock. In this way CapsLock will take effect but its indicator won't change.
  - Reasonable use of this in bluetooth mode to reverse the indicator light, such as turning off the numlock light when numlock is on and light on when it is off, which can save power. -->

  - bluetoothモードでは、Num, Caps, と Scroll Lock インジケーターはOSと同期しません。
  - bluetoothモードでは、押したときに点灯するだけです。USBモードでは同期します。
  - インジケーターが同期していない場合は、Shift + キー を使用して、Shift + CapsLockなどを押したとき、CapsLockを有効にします。このように CapsLockが有効になりますが、HHKB上のインジケーターは変化しません。
  - これらの特性を利用し、インジケーターを反転させることができます。例えば、NumLockがオンの時にNumLockをオフにしたいとき、それをNumLockをオン(Numlockインジケーターがオフ)にした状態で押すことができます。これは電池消費量を少なくすることができます。
</div>

<!-- Besides LEDMAP setting, they have some other special functions. -->
LEDMAP設定以外にも、他に特殊な機能があります。

<table_w30x70>

| State or operation | LED indication method |
|:--- |:--- |
| Flash mode (idle) | The three indicator lights flash together or flash alternately, always on |
| Flash mode (writing) | Based on the above, LED3 flashes quickly |
| Bluetooth disconnection status indication when starting | LED3 flashes, if it has not been connected, it will stop flashing in about 15 seconds |
| Bluetooth connected status indicator at startup | LED2 and LED3 flash slowly at the same time. Each time the light is on is significantly longer than the off time. |
| Press <key>LShift+RShift+s</key> | Indicate Bluetooth connection status as above |
| Manually enter the Lock Mode | Three lights light up at the same time, and then turn off in the order of LED3 LED2 LED1 |
| Wake from Level 2 Energy Saving or Lock Mode | Three lights light up at the same time, and then start to indicate Bluetooth connection status |
| Low battery reminder | When using the keyboard, the three lights flash at the same time; when saving energy, do not flash. It can still be used for two or three days. |
| Very low battery reminder | When using the keyboard, the three lights flash rapidly at the same time; no flash when saving energy. At this time, it is recommended to charge as soon as possible. |

| 状態もしくは操作 | LEDインジケーター表示 |
|:--- |:--- |
| フラッシュモード (待機) | 三つインジケーターは同時に点灯もしくは交互に点滅、停止することはない |
| フラッシュモード (書き込み中) | 待機モードをもとに、LED3は高速に点滅します |
| 起動時にbluetoothは未接続の状態時 | LED3 が点滅, 接続がずっとない状態では 、15秒後に点滅が停止|
| 起動時にbluetoothは接続の状態時 | LED2 と LED3 は同時に遅く点滅し、点滅の速度は非接続時より明らかに遅い |
| <key>LShift+RShift+s</key> | Bluetooth接続状態は上記と同じく表示します |
| 手動でLock Mode | 全LEDが点灯し、LED3 LED2 LED1順に消灯します |
| レベル2のエコモードもしくはLock Modeから解除時 | 全LEDが同時に点灯し、それからbluetoothの接続状態表示に切り替わります |
| Low battery reminder | When using the keyboard, the three lights flash at the same time; when saving energy, do not flash. It can still be used for two or three days. |
| Very low battery reminder | When using the keyboard, the three lights flash rapidly at the same time; no flash when saving energy. At this time, it is recommended to charge as soon as possible. |

</table_w30x70>


Then about the power saving mode:
  1. After the keyboard is idle for 3 seconds without pressing any key, it enters the general power saving mode. At this mode, the matrix is scanned every 30ms. If there is any key pressed, it exits the general power saving mode.
  2. If the keyboard's bluetooth is not connected for 90 seconds, or it is idle for more than 2.5 hours, it will turn off bluetooth and enter the deep power saving mode. Press and hold any key for 3 to 5 seconds to wake it up.
  3. Using Lock Mode will directly make the keyboard enter deep power saving mode. The difference from 2 is that by this way, you can press and hold only F and J together for 3 to 5 seconds to wake it up.


The black hhkb can't use leds in the front. But with another LED3 below the right USB port, it can show most status.

The power consumption of the deep power saving mode is very low. For daily use you don't need to turn the power switch off, just leave the keybaord to let itselt enter power saving mode. If you want take it away in a bag, it is recommended to make it enter Lock Mode to prevent unexpectedly wake up.


## USB HUB

The built-in interface is a miniUSB, so the USB HUB here supports USB 2.0 high speed at the highest.

In addition to the two USB ports on the HHKB case, there is an extra USB Port on the controller inside the keyboard. It is forbidden to connect high-current devices to these USB ports. The  power supply of the internal USB port is controllable. The control function can be selected in **LEDs & Functions**. <html><button style="text-align: center; line-height: 19px; width: 46px; height : 42px; font-size: 12px">Inner<br>USB</button></html>. You can put an USB Disk in it or just leave it with nothing.


## Use Karabiner-Elements in MacOS

Karabiner-Elements regards the same keyboard Bluetooth mode and wired mode as different keyboards.

Refer to the instructions provided by the user. To use Karabiner-Elements in Bluetooth mode, please use the latest version of the software, as shown in the figure below, and check **[ HHKB BLE(Adafruit Industries)]**.

![](/assets/hhkb_karabiner-elements.jpg)


## Exception Handling

If there is a key press error trigger or random trigger. Please confirm whether the battery is insulated from the hhkb upper keyboard circuit board according to the installation instructions provided by taobao link.

If something goes wrong during work, the quickest way is to re-plug the USB cable or switch the keyboard power switch off and on again to check if it works well again.

And please refer to [BLE Troubleshooting](/en/ble-series/troubleshooting).
 
If any other bugs, email me.


