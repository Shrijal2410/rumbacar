# Day 001: Feature List
 
- N25 12V 75RPM Metal Gear Encoded Motor With D-Shaft - 494
- TB6612FNG 15V(max) 1.2 A/3.2 A (peak) 
- MPU6050 IMU with I2C
- GoPro Hero Camera with gimbal
- 4x ToF Sensor VLXXLXX
- Indoor nav stack hardware
- 26 Wh Lithium Ion (14.4V nominal) Rechargable
 0.31 m/s (safe mode), 0.46 m/s (cliff sensors disabled)
- RPLIDAR-A1
- OAK-D-PRO 0.15-12m range; 8kHz sampling rate;
- 4x IR cliff sensors, 6x IR obstacle sensors, 1x downward optical flow, 1x battery level monitor
- Status LEDs, 128x64 OLED Display
- 2x Wheel R36 W15 - Space D80 W30

# Day 002-004: Mech Design start
- Circular Design just like rumba
    options: hexagonal design (got idea while writing this )
- finallized design: ⌀220mm
- caster selection: using grabcad design for ⌀47.45 wheel, H37.2
- intial base assembly done in Fusion
    can be printed on mini printer with 180x180x180
    nut slots are there for strong structure
    need design change on motor mount

# Day 005-Present: Elec Design
- search of a versatile power source
    found pd power bank with PD3.0 providing upto 100W power
    its cheap but there is a output current limitation upto 3-5A
    - cheap option: at 2500 (waiting for price near 2000)
        - Stufcool Major Ultra 65W PD 20000mAh: 2500
            3700mAh for 20V (1.12 hour runtime at full 65W)
            PPS : 3.3-13V/5A (Max 65W)​
    - Expensive but not much: at 4000-5000 many options for 100w
        - Ambrane 100W 25000mAh: 4799
        - Boat 160W (80+80W) 27000mAh: 4499
        - Zebronics EnergiPOD 27R31 100W 27000mAh: 3999
    - power adapter: 100W GaN Charger
        - USB C1/C2: 5V⎓3A / 9V⎓3A / 12V⎓3A / 15V⎓3A / 20V⎓5A (100W Max)
        - PPS: 5V-20V⎓5A (25-100W Max)
        - USB A: 5V⎓3A / 9V⎓3A / 12V⎓3A

- Now going to need a reliable buck boost converter with reference design
    - LTC3780 Vin: 5-32V Vout: 1-30V Imax: 10A Buck-Boost Converter 
    - LM51772: Vin: 3.5-55V Vout: 3.3V to 55
    - LM251772: Vin: 2.5-36 Vout: 3.3-60V
    - LM5176

more research required..   