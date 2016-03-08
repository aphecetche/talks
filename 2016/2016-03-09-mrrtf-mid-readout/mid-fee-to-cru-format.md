| Coding of HEARTBEAT event in LOCAL | Number of bits |
|:----------------------------------:|---------------:|
|START BIT (always '1') | 1 |
|BUSY ('0'=OK; '1'=FIFO full) | 1 |
|DECISION (tracklet) | 1 |
|CARD TYPE (always '1'=LOCAL) | 1 |
|HEARTBEAT (always '1') | 1 |
|ACQUISITION ('0'=OFF; '1'=ON) | 1 |
|('11'=RST; '10'=EOR; '01'=SOR; '00'=OTHER) | 2 |
|Bunch Counter | 16 |
|Board Position in crate (0-15) | 4 |
|Status: '0xF'|4|
|Status: Masks on inputs [(X4,Y4),(X3,Y3),(X2,Y2),(X1,Y1)]| 32*4 |
|Total number of bits | 32*5 |
|Bunches needed to send | 20 |

| Coding of PHYSICS event in LOCAL | Number of bits |
|:----------------------------------:|---------------:|
|START BIT (always '1') | 1 |
|BUSY ('0'=OK; '1'=FIFO full) | 1 |
|DECISION (tracklet) | 1 |
|CARD TYPE (always '1'=LOCAL) | 1 |
|HEARTBEAT (always '0') | 1 |
|ACQUISITION (always '1'=ON) | 1 |
|Free bits (always '0') | 2 |
|Bunch Counter | 16 |
|Board Position in crate (0-15) | 4 |
|Data: Non zero detector plane(s) (1 bit/word)|4|
|Data: Non zero strip pattern(s) [(X4,Y4),(X3,Y3),(X2,Y2),(X1,Y1)]| 32*i (i=0 to 4) |
|Total number of bits | 32*i (i=2 to 5) |
|Bunches needed to send | 8 to 20 |

| Coding of HEARTBEAT event in REGIONAL | Number of bits |
|:----------------------------------:|---------------:|
|START BIT (always '1') | 1 |
|BUSY ('0'=OK; '1'=FIFO full) | 1 |
|DECISION (tracklet) | 1 |
|CARD TYPE (always '0'=REGIONAL) | 1 |
|HEARTBEAT (always '1') | 1 |
|ACQUISITION ('0'=OFF; '1'=ON) | 1 |
|('11'=RST; '10'=EOR; '01'=SOR; '00'=OTHER) | 2 |
|Bunch Counter | 16 |
|Crate number (0-15) | 4 |
|Status: Masks on tracklet inputs|4|
|N/A| 0 |
|Total number of bits | 32 |
|Bunches needed to send | 4 |

| Coding of PHYSICS event in REGIONAL | Number of bits |
|:----------------------------------:|---------------:|
|START BIT (always '1') | 1 |
|BUSY ('0'=OK; '1'=FIFO full) | 1 |
|DECISION (tracklet) | 1 |
|CARD TYPE (always '0'=REGIONAL) | 1 |
|HEARTBEAT (always '0') | 1 |
|ACQUISITION (always '1') | 1 |
|Free bits (always '0') | 2 |
|Bunch Counter | 16 |
|Crate number (0-15) | 4 |
|Data: Non zero tracklet inputs|4|
|N/A| 0 |
|Total number of bits | 32 |
|Bunches needed to send | 4 |
