# zx-talkman
DIY Speech Interface for ZX Spectrum &amp; ZX81 published in Ny Elektronik 1984 issue 10 page 36. Recreated om KiCad as close as possible to original design.

# Original construction
This is the construction as published in the magazine in 1984.

<table>
  <tr>
    <td colspan="3" align="center"><img width="1200" alt="image" src="https://github.com/user-attachments/assets/bd449ac4-e4a5-4f37-ac2f-c7ed05c4f2f5"></td>
  </tr>
  <tr>
    <td align="center"><img width="400" alt="image" src="https://github.com/user-attachments/assets/f90aa2a6-9852-4418-a54d-f48472902ff3"></td>
    <td align="center"><img width="400" alt="image" src="https://github.com/user-attachments/assets/3287fc7b-85ad-4191-aec7-b3648284333a"></td>
    <td align="center"><img width="400" alt="image" src="https://github.com/user-attachments/assets/450c13ef-1f4f-4094-b04c-9d7a47cfbf96"> </td>
  </tr>
  <tr>
    <td align="center">Schema</td>
    <td align="center">PCB</td>
    <td align="center">Components layout</td>
  </tr>
</table>

# Recreated construction
The main goal was to get the schema redrawn in KiCad and a first try at a PCB, in order to build a version to check if everything works.

## Programming the ZX-TALKMAN
The interface is controled by outputting to port 31 (dec). On ZX Spectrum this can be done using the BASIC command out. On ZX81 you will need to write a short M/C program to send data to the interface. (May come later).

### Hello world on ZX Spectrum
```BASIC
10 READ data
20 IF data > 63 THEN OUT 31,0: STOP
30 OUT 31, data
40 GO TO 10
1000 DATA 27,51,45,53,46,52,45,21,0, 64
```

## version 1.0
From Magazine over KiCad to PCB.

| Schema | KiCad | PCB |
| ------ | ----- | --- |
|<img width="400" alt="KiCad Schema" src="https://github.com/user-attachments/assets/9f0afff5-8c62-48ed-bc11-0291c6217ed9" />|<img width="400" alt="KiCad PCB" src="https://github.com/user-attachments/assets/bf280df6-b22f-4035-b35d-1ca69cda4078" />|<img width="400" alt="PCB" src="https://github.com/user-attachments/assets/bd5bb86d-add7-45f2-a152-6e5ff2a53a8d" />

### produced version of v1.0
| Building | Final | In use |
| ------ | ----- | --- |
|<img width="400" alt="image" src="https://github.com/user-attachments/assets/a4144122-c74f-43fb-b8f0-23b1f707624c" />|<img width="400" alt="image" src="https://github.com/user-attachments/assets/f99abc93-4a34-4d34-9e4d-f826c333ce60" />|<img width="400" alt="image" src="https://github.com/user-attachments/assets/afd13a5f-6391-40ff-a90e-12ce152e4354" />

# BOM v1.0
You will need the following components:
- SP0256-AL2 (watch out for fakes!)
- LM386
- 74LS00
- 74LS32
