### PCB változások 2026.05.25 (terv még nincs tesztelve)

- Az IR LED átkerült a GPIO 2-re, mert a távirányítóval való ébresztéshez az RTC szükséges.
- A PCM5102A DAC VIN +5V bemenetét egy A03401A MOSFET kapcsolja a GPIO 38 állapotának megfelelően.Így a DAC sem kap áramot az ESP alatatásakor.
- Lett egy 3.3V-os kimenet a bekapcsoló gomb LED világításának meghajtásához mely egy BC817 tranzisztorral van kapcsolva a GPIO 38-hoz. Így a bekapcsológomb világítása is kikapcsol az ESP alvó állapotában.
- A rotary használta az ESP32 alaplap RGB LED GPIO 48 -at. Ez GPIO 42 -re lett változtatva.
- Az I2C touch kivezetés hozzá lett adva.
    - INT GPIO 17
    - SDA GPIO 8
    - RST GPIO 1
    - SCL GPIO 7

- A furatok és a kűlső méretek nem változtak.   
<br><br>


![PCB front](2D_pcb_top_98x100mm.jpg)<br><br>
![PCB back](2D_pcb_bottom_98x100mm.jpg)<br><br>

## Alkatrészek:
| Alkatrész neve    | Érték | Típus    |
|-------------------|-------|----------|     
| R1 - R4           | 4,7k  | SMD 1206 |    
| R5 - R6           | 1k    | SMD 1206 |
| R7 - R13          | 10k   | SMD 1206 |
| R14 - R15         | 4,7k  | SMD 1206 |
| R16               | 330   | SMD 1206 |
| R17               | 47k   | SMD 1206 |
| R18               | 680   | SMD 1206 |
| R19               | 47k   | SMD 1206 |
| C1                | 220uF/10V | |
| C2                | Kondenzátor 100nF 100V 10% Polipropilén RM-5
| C3                | 10uF/10V | |
| C4                | Kondenzátor 100nF 100V 10% Polipropilén RM-5 |
| LD1117AS33TR POS.V-REG. | 3.3V 1.2A Low-Drop.(1.15V) | SOT-223       | 
| AO3401A | P-MOSFET SMD 30V (3.8A) | SOT-23 |
| BC817-40.215 NPN SMD 45V/50V 0.5A 0.25W 100MHz | | SOT-23 |
| LTV817STA1 | Optocsatoló 5kV tranzisztor kimenet 35V 50mA 80KHz 4p. SMD 
| Csatlakozók| JST-XH | 2,54 |
### Ha támogatni szeretnéd a munkámat itt meghívhatsz egy kávéra!!!     
https://buymeacoffee.com/vtom