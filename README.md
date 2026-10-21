# Moonboard

Moonboard is a Tamagotchi-style game played on a custom PCB.
The idea is simple: look after your moon every day and help it move through its
eight phases. I wanted it to feel like a small object you could keep on your desk,
pick up, and play with for a minute.

![Moonboard PCB render](https://github.com/user-attachments/assets/283441fb-68b5-4b4a-a15b-dfe1263070b3)

I made this project for [Hack Club Half Life](https://halflife.hackclub.com/?ref=3159).

## Try it without the board

I currently don't have the physical board, so no demos. I do have a firmware simulator. To get there,
open [`Firmware/simulator/index.html`](Firmware/simulator/index.html) and you can try out most features of my console!

Use `Q` / `W` / `E` for the top row and `A` / `S` / `D` for the bottom row, or just
click the buttons. The simulator is intentionally simple, but it makes it much
easier to try ideas without constantly flashing the board.

## What it can do

- Show all eight moon phases on the OLED
- Let you move around with a six-key matrix
- Use the rotary potentiometer for game input
- React to tilting and shaking through the MPU6050
- Read temperature and humidity from the DHT11
- Run on a XIAO ESP32-C3, with fallbacks for testing without every sensor connected

## The parts

| Part | Role |
| --- | --- |
| Part | What I’m using it for |
| --- | --- |
| XIAO ESP32-C3 | Running the game |
| 128x64 SSD1306 OLED | Showing the moon and menus over I2C |
| 6 mechanical keys | The 2x3 game controls |
| EC11 rotary encoder | Navigation and extra game input |
| MPU6050 | Tilt and shake interactions |
| DHT11 | Temperature and humidity experiments |

See [`BOM.md`](BOM.md) for the complete parts list and [`KiCAD/`](KiCAD/) for
the schematic, PCB, and manufacturing exports.

## Images

| Schematic | PCB |
| :---: | :---: |
| <img width="799" height="630" alt="Moonboard schematic" src="https://github.com/user-attachments/assets/db80967f-126a-46b7-9c74-430f674b4f7a" /> | <img width="682" height="477" alt="Moonboard PCB" src="https://github.com/user-attachments/assets/a3f6f4f4-35fc-418b-8d75-e43086d94258" /> |

## Renders

<p align="center">
	<img width="48%" alt="Moonboard render front" src="https://github.com/user-attachments/assets/283441fb-68b5-4b4a-a15b-dfe1263070b3" />
	<img width="48%" alt="Moonboard render angle" src="https://github.com/user-attachments/assets/5a7f2f54-12fe-4fb6-be68-b19ff605ef1f" />
</p>

<p align="center">
	<img width="48%" alt="Moonboard render detail" src="https://github.com/user-attachments/assets/1bdb53be-c6fb-44c3-a15d-62a934df26f5" />
	<img width="48%" alt="Moonboard render back" src="https://github.com/user-attachments/assets/cb7b2251-f977-4ed6-9f43-96102e7548b7" />
</p>
