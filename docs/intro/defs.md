# Definitions #

| Term                            | Definition                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Callsign                        | The unique identifier that a client is logged in as; e.g. `AAL123`, `EGLL_TWR`, `XX_SUP`, etc. |
| Client                          | A pilot or ATC station. For the purposes of FSD, observers are considered to be ATC stations. |
| Client string                   | A string identifying the client software. This is the FSD equivalent of user agent strings for browsers. Examples include `Euroscope 3.2`, `vPilot`, etc. |
| Frequency (freq)                | The network analogue to VHF frequencies used for aircraft radio communication. For the purposes of FSD, observers are always tuned to **199.998 MHz**. |
| Latitude (lat), longitude (lon) | Latitude and longitude. They have a precision of 5 decimal places. |
| Network ID                      | A unique ID used by the network. For VATSIM, it is the CID; for IVAO, the VID. |
| Protocol version                | The version of FSD being used by the client. As of the time of writing, <br />VATSIM uses `100`, while IVAO uses `B` (all clients except IVAC 2) or `C` (IVAC 2). |
| Rating                          | The ATC or pilot rating, as assigned by the network. This is stored as an integer; the lowest rating is `1`. Examples: S1/C2/C3, AS3/ADC, FS3/SPP, etc. |
| Server                          | A FSD server.                                                |
| Packet                          | A formatted unit of data sent over an FSD network.           |

Placeholders are indicated using brackets; e.g. `(client string)`.



# Ratings #

Each user has a pilot and ATC rating. 

This is stored as an integer inside `cert.txt` on the server, but is advertised by IVAO and VATSIM under the following names:

## ATC ratings ##

| `cert.txt` value | VATSIM rating | IVAO rating |
| ---------------- | ------------- | ----------- |
| 1                | OBS           |             |
| 2                | S1            | AS1         |
| 3                | S2            | AS2         |
| 4                | S3            | AS3         |
| 5                | C1            | ADC         |
| 6                | C2            |             |
| 7                | C3            | ACC         |
| 8                | I1            |             |
| 9                | I2            |             |
| 10               | I3            |             |
| 11               | SUP           |             |
| 12               | ADM           |             |


## Pilot ratings ##

| `cert.txt` value | VATSIM rating | IVAO rating |
| ---------------- | ------------- | ----------- |
| 1                | No rating     |             |
| 2                |               | FS1         |
| 3                |               | FS2         |
| 4                |               | FS3         |
| 5                |               | PP          |
| 6                |               | SPP         |
| 7                |               | CP          |
| 8                |               | ATP         |
| 9                |               | SFI         |
| 10               |               |             |
| 11               | P1            |             |