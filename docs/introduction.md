


The [SparkFun Soft Power Switch Mk2](https://www.sparkfun.com/products/26993) is a passive, hard on/off switch with software feedback and control. In other words, it's like the on/off switch on a laptop. A simple press will turn the system on. Another press can (with MCU intervention) turn off the system. And if things go really wrong, pressing and holding the button for ~10 seconds will force a power-down. If you're building something with an enclosed battery and need a good power button, this is the board you need. This version has JST 2mm battery connectors.

<div class="grid cards" style="width:500px; margin: 0 auto;" markdown>

-   <a href="https://www.sparkfun.com/products/26993">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/8/0/9/9/PRT-26993-Soft_Power_Switch-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Soft Power Switch Mk2">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/26993">
      <b>SparkFun Soft Power Switch Mk2</b>
      <br />
      PRT-26993
      <br />
      <center>[Purchase from SparkFun :fontawesome-solid-cart-plus:](https://www.sparkfun.com/products/26993){ .md-button .md-button--primary }</center>
    </a>
</div>

In this tutorial, we'll go over the hardware and how to hookup the SparkFun Soft Power Switch Mk2 to an Arduino. We will also go over an Arduino example to get started.



### Required Materials

To follow along with this tutorial, you will need the following materials. You may not need everything though depending on what you have. Add it to your cart, read through the guide, and adjust the cart as necessary.

<div class="grid cards col-4" markdown>

<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/15424">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/3/9/8/3/15424-Reversible_USB_A_to_C_Cable_-_2m-02.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Reversible USB A to C Cable - 2m">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/15424">
      <b>Reversible USB A to C Cable - 2m</b>
      <br />
      CAB-15424
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/19177">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/8/8/0/0/ESP32_03.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun IoT RedBoard - ESP32 Development Board">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/19177">
      <b>SparkFun IoT RedBoard - ESP32 Development Board</b>
      <br />
      WRL-19177
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/26993">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/8/0/9/9/PRT-26993-Soft_Power_Switch-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Soft Power Switch Mk2">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/26993">
      <b>SparkFun Soft Power Switch Mk2</b>
      <br />
      PRT-26993
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/18286">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/7/6/0/6/17748-Lithium_Ion_Battery_-_1250_mAh__IEC62133_certified_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Lithium Ion Battery - 1250mAh (IEC62133 Certified)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/18286">
      <b>Lithium Ion Battery - 1250mAh (IEC62133 Certified)</b>
      <br />
      PRT-18286
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9914">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/4/0/2/0/09914-02b.jpg" style="width:140px; height:140px; object-fit:contain;" alt="JST Jumper 2 Wire Assembly">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9914">
      <b>JST Jumper 2 Wire Assembly</b>
      <br>
      PRT-09914
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/115">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/0/5/00115-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Female Headers">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/115">
      <b>Female Headers</b>
      <br />
      PRT-00115
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/8431">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/1/8/1/JumperWire-Male-01-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wires Premium 6" M/M Pack of 10">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/8431">
      <b>Jumper Wires Premium 6" M/M Pack of 10</b>
      <br />
      PRT-08431
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14460">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/2/2/1/8/14460-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Multicolor Buttons - 4-pack">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14460">
      <b>Multicolor Buttons - 4-pack</b>
      <br />
      PRT-14460
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/15096">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/3/4/5/2/15096-SparkFun_Serial_Basic_Breakout_-_CH340C_and_USB-C-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun Serial Basic Breakout - CH340C and USB-C">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/15096">
      <b>SparkFun Serial Basic Breakout - CH340C and USB-C</b>
      <br />
      DEV-15096
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/12045">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/6/2/8/12045-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Breadboard - Mini Modular (Blue)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12045">
      <b>Breadboard - Mini Modular (Blue)</b>
      <br />
      PRT-12045
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### 2-Pin JST Cables

For those that want to take advantage of the 2-pin JST-style connector with 2mm pitch, you can grab the following cables from the catalog. Two jumper 2 wire assemblies were spliced together with heat shrink to easily connect the Soft Power Switch Mk2 to the IoT RedBoard's 2-pin JST-style connector.

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/8670">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/8/2/6/08670-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wire - JST Black Red">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/8670">
      <b>Jumper Wire - JST Black Red</b>
      <br />
      PRT-08670
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9914">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/4/0/2/0/09914-02b.jpg" style="width:140px; height:140px; object-fit:contain;" alt="JST Jumper 2 Wire Assembly">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9914">
      <b>JST Jumper 2 Wire Assembly</b>
      <br>
      PRT-09914
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/8671">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/8/2/7/08671-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wire - JST Black Blue">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/8671">
      <b>Jumper Wire - JST Black Blue</b>
      <br>
      PRT-08671
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->

</div>



### Tools

For users connecting to the plated through holes, you will need a soldering iron, solder, and [general soldering accessories](https://www.sparkfun.com/categories/49).

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/24063">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/2/4/3/8/5/KIT-24063-PINECIL-Soldering-Iron-Kit-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="PINECIL Soldering Iron Kit">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/24063">
      <b>PINECIL Soldering Iron Kit</b>
      <br />
      TOL-24063
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9163">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/5/8/7/09162-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Solder Lead Free - 15-gram Tube">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9163">
      <b>Solder Lead Free - 15-gram Tube</b>
      <br>
      TOL-09163
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11375">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/7/1/2/0/11375-Hook-Up_Wire_-_Assortment__Solid_Core__22_AWG_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Hook-Up Wire - Assortment (Stranded, 22 AWG)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11375">
      <b>Hook-Up Wire - Assortment (Stranded, 22 AWG)</b>
      <br />
      PRT-11375
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/12630">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/9/3/1/2/12630-Hakko-Wire-Strippers-30AWG-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Wire Strippers - 30AWG (Hakko)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12630">
      <b>Wire Strippers - 30AWG (Hakko)</b>
      <br />
      TOL-12630
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11952">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/4/2/2/11952-Hakko-Flush-Cutters-feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Flush Cutters - Hakko">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11952">
      <b>Flush Cutters - Hakko</b>
      <br />
      TOL-11952
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->

-   <a href="https://www.sparkfun.com/products/9353">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/455-455/assets/parts/2/9/2/3/09353-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Heat Shrink Kit">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9353">
      <b>Heat Shrink Kit</b>
      <br />
      PRT-09353
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Prototyping Accessories

Depending on your setup, you may want to use IC hooks for a temporary connection. However, you will want to solder header pins to connect devices to the plated through holes for a secure connection.

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/12002">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/5/0/3/12002-Breadboard_-_Self-Adhesive__White_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Breadboard - Self-Adhesive (White)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12002">
      <b>Breadboard - Self-Adhesive (White)</b>
      <br />
      PRT-12002
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9741">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/6/9/6/09741-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="IC Hook with Pigtail">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9741">
      <b>IC Hook with Pigtail</b>
      <br>
      CAB-09741
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/553">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/7/8/00553-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Break Away Male Headers - Right Angle">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/553">
      <b>Break Away Male Headers - Right Angle</b>
      <br />
      PRT-00553
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9140">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/2/5/5/7/09140-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wires Premium 6" M/F Pack of 10">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9140">
      <b>Jumper Wires Premium 6" M/F Pack of 10</b>
      <br />
      PRT-09140
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Suggested Reading

If you aren’t familiar with the following concepts, we also recommend checking out a few of these tutorials before continuing.

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/5/Soldering_Action-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Solder: Through-Hole Soldering">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering">
      <b>How to Solder: Through-Hole Soldering</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/working-with-wire">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/0/5/0/0/f/5138de3cce395fbb1b000002.JPG"style="width:264px; height:148px; object-fit:contain;" alt="Working with Wire">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/working-with-wire">
      <b>Working with Wire</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/6/1/arduinoThumb.jpg" style="width:264px; height:148px; object-fit:contain;" alt="Installing Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <b>Installing Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/redboard-turbo-hookup-guide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/2/2/5/7/285808434_548438690244031_7008413248633042033_n.jpg" style="width:264px; height:148px; object-fit:contain;" alt="IoT RedBoard ESP32 Development Board Hookup Guide">
      </figure>
    </a>

    ---

    <a href="hhttps://learn.sparkfun.com/tutorials/iot-redboard-esp32-development-board-hookup-guide">
      <b>IoT RedBoard ESP32 Development Board Hookup Guide</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG" style="width:264px; height:148px; object-fit:contain;" alt="Installing Board Definitions in the Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <b>Installing Board Definitions in the Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/logic-levels">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png" style="width:264px; height:148px; object-fit:contain;" alt="Logic Levels">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/logic-levels">
      <b>Logic Levels</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->

-   <a href="https://learn.sparkfun.com/tutorials/how-to-power-a-project/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/3/6/Bench_Power_Supply.jpg" style="width:264px; height:148px; object-fit:contain;" alt="How to Power a Project">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-power-a-project/all">
      <b>How to Power a Project</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>
