In this section, we will go over how to connect to the Soft Power Switch Mk2 - JST 2mm.



### Connecting via PTH

For temporary connections to the PTHs, you could use IC hooks to test out the pins. However, you'll need to solder headers or wires of your choice to the board for a secure connection. You can choose between a combination of [header pins and jumper wires](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all), or [stripping wire and soldering the wire](https://learn.sparkfun.com/tutorials/working-with-wire/all) directly to the board.

<div class="grid cards col-2" markdown>

-   <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/5/Soldering_Action-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Solder: Through Hole Soldering">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering/all">
      <b>How to Solder: Through Hole Soldering</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->

-   <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/0/5/0/0/f/5138de3cce395fbb1b000002.JPG" style="width:264px; height:148px; object-fit:contain;" alt="Working with Wire">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/working-with-wire/all">
      <b>Working with Wire</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>



### Input Power

The board was designed to be used with single cell LiPo batteries with the built-in 2-pin JST connector. Simply insert the LiPo Battery into the JST connector labeled as IN.


<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/ width="600px" height="600px" alt="LiPo Battery inserted into JST Connector"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>LiPo Battery inserted into JST Connector</i></td>
    </tr>
  </table>
</div>

Of course, power can also be soldered directly to the PTH as well.

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Power Supply
            </th>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Soft Power Switch Mk2
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">1.8V to 5.5V<br /> Typically 3.7V <br />if using a LiPo Battery (Red Wire)</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">VIN</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND (Black Wire)</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
        </tr>
    </table>
</div>

Remember, the Soft Power Switch Mk2 also supports battery charging. If the target device has onboard LiPo charging, current can be passed back through the switch circuit and charge the battery. For more information about LiPo battery charging and care, make sure to check the tutorial on [Single Cell LiPo Battery Care](https://learn.sparkfun.com/tutorials/single-cell-lipo-battery-care).

<div class="grid cards" style="width:500px; margin: 0 auto;" markdown>

-   <a href="https://learn.sparkfun.com/tutorials/single-cell-lipo-battery-care">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/3/0/4/5/Remove_2-pin_JST-PH_Connector_LiPo_Battery_Needle_Nose_Pliers_Wiggling-3.jpg" style="width:264px; height:148px; object-fit:contain;" alt="Single Cell LiPo Battery Care">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/single-cell-lipo-battery-care">
      <b>Single Cell LiPo Battery Care</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>



### Output Power

For boards that have a built-in 2-pin JST connector for LiPo batteries, you can [splice two](https://learn.sparkfun.com/tutorials/working-with-wire/all#how-to-splice-wires) JST cables together. Then you can insert it between the Soft Power Switch's JST connector labeled OUT and the other end will be inserted into the JST connector of the target board being powered (in this case, the SparkFun IoT RedBoard - ESP32 Development Board).

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/ width="600px" height="600px" alt="JST Cable between the Soft Power Switch Mk2 and IoT RedBoard - ESP32"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>JST Cable between the Soft Power Switch Mk2 and IoT RedBoard - ESP32</i></td>
    </tr>
  </table>
</div>

Of course, power can also be soldered directly to the PTH as well. Since we are powering the output with a single cell LiPo battery, you will need to connect it to your system's battery input. In this case, VBATT net was labeled as + on the board. Depending on your system, it may be labeled as VBAT, RAW, or VCC. Make sure to check the board's hardware design before deciding to connect VOUT to your system.

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Soft Power Switch Mk2
            </th>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">SparkFun IoT RedBoard -<br />ESP32 Development Board
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">VOUT</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#f2dede"><font color="#000000">+</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">-</font>
            </td>
        </tr>
    </table>
</div>

!!! note
    The voltage range of the Soft Power Switch Mk2 is between 1.8V to 5.5V. Users can also connect a different power source and connect the output to VIN or 5V of their system. Just make that the voltage is within the operating range of the target device.



### External Button

For users that need to connect an external button, you will simply need to connect one terminal of the button to BTN and the other terminal to GND.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/ width="600px" height="600px" alt="External Button Connected"></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>External Button Connected</i></td>
    </tr>
  </table>
</div>

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Soft Power Switch Mk2
            </th>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Button
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">BTN</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">Normally Open Pin</font>
            </td>
        </tr>
        <tr>
        <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">GND</font>
        </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#DDDDDD"><font color="#000000">Common Pin</font>
            </td>
        </tr>
    </table>
</div>



### Off and Push

To connect to the OFF and PUSH pins with a microcontroller, you will need two GPIO pins with code to control or read the pins.

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><a href="../assets/img/"><img src="../assets/img/ width="600px" height="600px" alt="OFF and PUSH Pins Connected to IoT RedBoard "></a></td>
    </tr>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;"><i>External Button Connected</i></td>
    </tr>
  </table>
</div>

<div style="text-align: center;">
    <table>
        <tr>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">Soft Power Switch Mk2
            </th>
            <th style="text-align: center; vertical-align: middle; border: solid 1px #cccccc;">SparkFun IoT RedBoard -<br />ESP32 Development Board
            </th>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000">OFF</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#cce5ff"><font color="#000000"><code>32</code> (or <code>A4</code>)</font>
            </td>
        </tr>
        <tr>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000">PUSH</font>
            </td>
            <td style="text-align: center; border: solid 1px #cccccc;" bgcolor="#d4edda"><font color="#000000"><code>14</code></font>
            </td>
        </tr>
    </table>
</div>

!!! tip
    Remember, the PUSH pin requires a pull-up resistor when connecting it to a microcontroller's GPIO pin. You can use the [internal pull-up resistor](https://learn.sparkfun.com/tutorials/pull-up-resistors/all) on the microcontroller so that the pin is not floating.
