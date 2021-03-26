---
description: In diesem Abschnitt werden die ternären Raster-Operation-Codes aufgelistet, die von den Funktionen BitBLT, patblt und StretchBlt verwendet werden. TERNÄRE Raster-Vorgangs Codes definieren, wie GDI die Bits in einer Quell Bitmap mit den Bits in der Ziel Bitmap kombiniert.
ms.assetid: 538f3580-d6a7-4dae-8185-802eb9c96735
title: TERNÄRE Raster Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c30411ff4e5a38f54b52baa086510cecb6168dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960719"
---
# <a name="ternary-raster-operations"></a>TERNÄRE Raster Vorgänge

In diesem Abschnitt werden die ternären Raster-Operation-Codes aufgelistet, die von den Funktionen [**BitBLT**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt), [**patblt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)und [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) verwendet werden. TERNÄRE Raster-Vorgangs Codes definieren, wie GDI die Bits in einer Quell Bitmap mit den Bits in der Ziel Bitmap kombiniert.

Jeder Raster Vorgangs Code stellt einen booleschen Vorgang dar, in dem die Werte der Pixel in der Quelle, der ausgewählte Pinsel und das Ziel kombiniert werden. Im folgenden finden Sie die drei in diesen Vorgängen verwendeten Operanden.



| Operand | Bedeutung                              |
|---------|--------------------------------------|
| D       | Ziel Bitmap                   |
| P       | Ausgewählter Pinsel (auch als Muster bezeichnet) |
| E       | Quell Bitmap                        |



 

Die in diesen Vorgängen verwendeten booleschen Operatoren folgen.



| Operator | Bedeutung                    |
|----------|----------------------------|
| a        | Bitweises AND                |
| n        | Bitweises NOT (inversen)      |
| o        | Bitweises OR                 |
| x        | Bitweises exklusives OR (XOR) |



 

Alle booleschen Vorgänge werden in umgekehrter polnischer Schreibweise dargestellt. Der folgende Vorgang ersetzt z. b. die Werte der Pixel in der Ziel Bitmap durch eine Kombination der Pixelwerte von Quelle und Pinsel:


```C++
PSo 
```



Der folgende Vorgang kombiniert die Werte der Pixel in der Quelle und dem Pinsel mit den Pixelwerten der Ziel Bitmap (es gibt alternative rechtschreibweisen der gleichen Funktion, sodass eine bestimmte Schreibweise nicht in der Liste enthalten sein kann):


```C++
DPSoo 
```



Jeder Raster Vorgangs Code ist eine 32-Bit-Ganzzahl, deren hohes Wort ein boolescher Vorgangs Index ist und dessen niedriges Wort der Vorgangs Code ist. Bei dem 16-Bit-Vorgangs Index handelt es sich um einen 8-Bit-Wert mit 0 (null), der das Ergebnis der booleschen Operation für vordefinierte Pinsel-, Quell-und Zielwerte darstellt. Beispielsweise werden die Vorgangs Indizes für den PSO-und den dpsoo-Vorgang in der folgenden Liste angezeigt.



| P                | E   | D   | PSo   | Dpsoo |
|------------------|-----|-----|-------|-------|
| 0                | 0   | 0   | 0     | 0     |
| 0                | 0   | 1   | 0     | 1     |
| 0                | 1   | 0   | 1     | 1     |
| 0                | 1   | 1   | 1     | 1     |
| 1                | 0   | 0   | 1     | 1     |
| 1                | 0   | 1   | 1     | 1     |
| 1                | 1   | 0   | 1     | 1     |
| 1                | 1   | 1   | 1     | 1     |
| Vorgangs Index: |     |     | 00F | 00feh |



 

In diesem Fall hat PSO den Vorgangs Index 00FC (von unten nach oben gelesen). Dpsoo weist den Vorgangs Index 00fe auf. Diese Werte definieren den Speicherort der entsprechenden Raster Vorgangs Codes, wie in Tabelle A. 1, "Raster-Vorgangs Codes" gezeigt. Der PSO-Vorgang befindet sich in Zeile 252 (00fch) der Tabelle. Dpsoo ist in Zeile 254 (00feh).

Den am häufigsten verwendeten Raster Vorgängen wurden in der SDK-Header Datei "Windows. H" besondere Namen zugewiesen. Sie sollten diese Namen möglichst in Ihren Anwendungen verwenden.

Wenn die Quell-und Ziel Bitmaps Monochrom sind, stellt ein Bitwert von 0 (null) ein schwarzes Pixel dar, und der Bitwert 1 stellt ein weißes Pixel dar. Wenn die Quell-und Ziel Bitmaps Farben sind, werden diese Farben mit RGB-Werten dargestellt. Weitere Informationen zu RGB-Werten finden Sie unter [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb).

**Raster Vorgangs Codes**



| Boolesche Funktion (hexadezimal) | Raster Vorgang (hexadezimal) | Boolesche Funktion in umgekehrter Polnisch | Allgemeiner Name    |
|--------------------------------|--------------------------------|------------------------------------|----------------|
| 00                             | 00000042                       | 0                                  | Blackness      |
| 01                             | 00010289                       | Dpbald                             |                |
| 02                             | 00020c89                       | Dpsona                             |                |
| 03                             | 000300aa                       | PSon                               |                |
| 04                             | 00040c88                       | Sdpona                             |                |
| 05                             | 000500a9                       | Dpon                               |                |
| 06                             | 00060865                       | Pdsxnon                            |                |
| 07                             | 000702c5                       | Pdsaon                             |                |
| 08                             | 00080                       | Sdpnaa                             |                |
| 09                             | 00090245                       | Pdsxon                             |                |
| 0a                             | 000a0329                       | DPNA                               |                |
| 0 B                             | 000b0b2a                       | Psdnaon                            |                |
| 0C                             | 000c0324                       | Spna                               |                |
| 0d                             | 000d0b25                       | Pdsnaon                            |                |
| 0E                             | 000e08a5                       | Pdsonon                            |                |
| 0F                             | 000f 0001                       | PN                                 |                |
| 10                             | 00100c85                       | Pdsona                             |                |
| 11                             | 001100a6                       | DSon                               | Nozrcerase    |
| 12                             | 00120868                       | Sdpxnon                            |                |
| 13                             | 001302c8                       | Sdpon                             |                |
| 14                             | 00140869                       | Dpsxnon                            |                |
| 15                             | 001502c9                       | Dpsaon                             |                |
| 16                             | 00165-CCA                       | Psdpsanaxx                         |                |
| 17                             | 00171-D54                       | Sspxdsxaxn                         |                |
| 18                             | 00180-D59                       | Spxpdxa                            |                |
| 19                             | 00191cc8                       | Sdpsanaxn                          |                |
| 1A                             | 001a06c5                       | Pdspaox                            |                |
| 1B                             | 001b0768                       | Sdpsxaxn                           |                |
| 1C                             | 001c06ca                       | Psdpaox                            |                |
| 1D                             | 001d0766                       | Dspdxaxn                           |                |
| 1E                             | 001e01a5                       | Pdsox                              |                |
| 1F                             | 001-0385                       | Pdsoan                             |                |
| 20                             | 00200                       | Dpsnaa                             |                |
| 21                             | 00210248                       | Sdpxon                             |                |
| 22                             | 00220326                       | Dsna                               |                |
| 23                             | 00230b24                       | Spdnaon                            |                |
| 24                             | 00240d55                       | Spxdsxa                            |                |
| 25                             | 00251cc5                       | Pdspanaxn                          |                |
| 26                             | 002606c8                       | Sdpsaox                            |                |
| 27                             | 00271868                       | Sdpsxnox                           |                |
| 28                             | 00280369                       | Dpsxa                              |                |
| 29                             | 002916-Zertifizierungsstelle                       | Psdpsaoxxn                         |                |
| 2a                             | 002a0cc9                       | Dpsana                             |                |
| 2B                             | 002b1d58                       | Sspxpdxaxn                         |                |
| 2C                             | 002c0784                       | Spdsoax                            |                |
| 2D                             | 002d060a                       | Psdnox                             |                |
| 2E                             | 002e064a                       | Psdpxox                            |                |
| 2F                             | 002-l0e2a                       | Psdnoan                            |                |
| 30                             | 0030032a                       | Psna                               |                |
| 31                             | 00310b28                       | Sdpnaon                            |                |
| 32                             | 00320688                       | Sdpsoox                            |                |
| 33                             | 00330008                       | SN                                 | Nozrccopy     |
| 34                             | 003406c4                       | Spdsaox                            |                |
| 35                             | 00351864                       | Spdsxnox                           |                |
| 36                             | 003601a8                       | Sdpox                              |                |
| 37                             | 00370388                       | Sdpoan                             |                |
| 38                             | 0038078a                       | Psdpoax                            |                |
| 39                             | 00390604                       | Spdnox                             |                |
| 3a                             | 003a0644                       | Spdsxox                            |                |
| 3B                             | 003b0e24                       | Spdnoan                            |                |
| 3C                             | 003c004a                       | PSx                                |                |
| 3D                             | 003d18a4                       | Spdsonox                           |                |
| 3e                             | 003e1b24                       | Spdsnaox                           |                |
| 3F                             | 003                       | PSAn                               |                |
| 40                             | 00400-"f"                       | Psdnaa                             |                |
| 41                             | 00410249                       | Dpsxon                             |                |
| 42                             | 00420d5d                       | Sdxpdxa                            |                |
| 43                             | 00431cc4                       | Spdsanaxn                          |                |
| 44                             | 00440328                       | Sdna                               | Srcerase       |
| 45                             | 00450b29                       | Dpsnaon                            |                |
| 46                             | 004606c6                       | Dspdaox                            |                |
| 47                             | 0047076a                       | Psdpxaxn                           |                |
| 48                             | 00480368                       | Sdpxa                              |                |
| 49                             | 004916c5                       | Pdspdaoxxn                         |                |
| 4a                             | 004a0789                       | Dpsdoax                            |                |
| 4B                             | 004b0605                       | Pdsnox                             |                |
| 4C                             | 004c0cc8                       | Sdpana                             |                |
| 4D                             | 004d1954                       | Sspxdsxoxn                         |                |
| 4E                             | 004e0645                       | Pdspxox                            |                |
| 4f                             | 004f-25                       | Pdsnoan                            |                |
| 50                             | 00500325                       | Pdna                               |                |
| 51                             | 00510b26                       | Dspnaon                            |                |
| 52                             | 005206c9                       | Dpsdaox                            |                |
| 53                             | 00530764                       | Spdsxaxn                           |                |
| 54                             | 005408a9                       | Dpsonon                            |                |
| 55                             | 00550009                       | Dn                                 | Dstinvert      |
| 56                             | 005601a9                       | Dpsox                              |                |
| 57                             | 00570389                       | Dpsoan                             |                |
| 58                             | 00580785                       | Pdspoax                            |                |
| 59                             | 00590609                       | Dpsnox                             |                |
| 5a                             | 005a0049                       | DPX                                | Patinvert      |
| 5B                             | 005b18a9                       | Dpsdonox                           |                |
| 5C                             | 005c0649                       | Dpsdxox                            |                |
| 5D                             | 005d0e29                       | Dpsnoan                            |                |
| 5e                             | 005e1b29                       | Dpsdnaox                           |                |
| 5F                             | 005                       | DPAN                               |                |
| 60                             | 00600365                       | Pdsxa                              |                |
| 61                             | 006116c6                       | Dspdsaoxxn                         |                |
| 62                             | 00620786                       | Dspdoax                            |                |
| 63                             | 00630608                       | Sdpnox                             |                |
| 64                             | 00640788                       | Sdpsoax                            |                |
| 65                             | 00650606                       | Dspnox                             |                |
| 66                             | 00660046                       | DSX                                | Srcinvert      |
| 67                             | 006718a8                       | Sdpsonox                           |                |
| 68                             | 006858a6                       | Dspdsonoxxn                        |                |
| 69                             | 00690145                       | Pdsxxn                             |                |
| 6a                             | 006a01e9                       | Dpsax                              |                |
| 6B                             | 006b178a                       | Psdpsoaxxn                         |                |
| 6C                             | 006c01e8                       | Sdpax                              |                |
| 6d                             | 006-d1785                       | Pdspdoaxxn                         |                |
| 6E                             | 006e1e28                       | Sdpsnoax                           |                |
| 6f                             | 006-Datei (0)                       | Pdsxnan                            |                |
| 70                             | 00700cc5                       | Pdsana                             |                |
| 71                             | 00711d5c                       | Ssdxpdxaxn                         |                |
| 72                             | 00720648                       | Sdpsxox                            |                |
| 73                             | 00730e28                       | Sdpnoan                            |                |
| 74                             | 00740646                       | Dspdxox                            |                |
| 75                             | 00750e26                       | Dspnoan                            |                |
| 76                             | 00761b28                       | Sdpsnaox                           |                |
| 77                             | 007700e6                       | DSAN                               |                |
| 78                             | 007801e5                       | Pdsax                              |                |
| 79                             | 00791786                       | Dspdsoaxxn                         |                |
| 7a                             | 007a1e29                       | Dpsdnoax                           |                |
| 7B                             | 007b0c68                       | Sdpxnan                            |                |
| 7C                             | 007c1e24                       | Spdsnoax                           |                |
| 7D                             | 007d0c69                       | Dpsxnan                            |                |
| 7e                             | 007e0955                       | Spxdsxo                            |                |
| 7F                             | 007, f. C9                       | Dpsaan                             |                |
| 80                             | 008003e9                       | Dpsaa                              |                |
| 81                             | 00810975                       | Spxdsxon                           |                |
| 82                             | 00820c49                       | Dpsxna                             |                |
| 83                             | 00831e04                       | Spdsnoaxn                          |                |
| 84                             | 00840c48                       | Sdpxna                             |                |
| 85                             | 00851e05                       | Pdspnoaxn                          |                |
| 86                             | 008617a6                       | Dspdsoaxx                          |                |
| 87                             | 008701c5                       | Pdsaxn                             |                |
| 88                             | 008800c6                       | DSa                                | Srcand         |
| 89                             | 00891b08                       | Sdpsnaoxn                          |                |
| 8A                             | 008a0e06                       | Dspnoa                             |                |
| 8B                             | 008b0666                       | Dspdxoxn                           |                |
| 8c                             | 008c0e08                       | Sdpnoa                             |                |
| 8D                             | 008d0668                       | Sdpsxoxn                           |                |
| 8E                             | 008e1d7c                       | Ssdxpdxax                          |                |
| 8f                             | 008-"f"                       | Pdsanan                            |                |
| 90                             | 00900c45                       | Pdsxna                             |                |
| 91                             | 00911e08                       | Sdpsnoaxn                          |                |
| 92                             | 009217a9                       | Dpsdpoaxx                          |                |
| 93                             | 009301c4                       | Spdaxn                             |                |
| 94                             | 009417aa                       | Psdpsoaxx                          |                |
| 95                             | 009501c9                       | Dpsaxn                             |                |
| 96                             | 00960169                       | Dpsxx                              |                |
| 97                             | 0097588a                       | Psdpsonoxx                         |                |
| 98                             | 00981888                       | Sdpsonoxn                          |                |
| 99                             | 00990066                       | Dsxn                               |                |
| 9a                             | 009a0709                       | Dpsnax                             |                |
| 9B                             | 009b07a8                       | Sdpsoaxn                           |                |
| 9C                             | 009c0704                       | Spdnax                             |                |
| 9d                             | 009d07a6                       | Dspdoaxn                           |                |
| 9E                             | 009e16e6                       | Dspdsaoxx                          |                |
| 9F                             | 009-0345                       | Pdsxan                             |                |
| A0                             | 00a000c9                       | DPa                                |                |
| A1                             | 00a11b05                       | Pdspnaoxn                          |                |
| A2                             | 00a20e09                       | Dpsnoa                             |                |
| A3                             | 00a30669                       | Dpsdxoxn                           |                |
| A4                             | 00a41885                       | Pdsponoxn                          |                |
| A5                             | 00a50065                       | Pdxn                               |                |
| A6                             | 00a60706                       | Dspnax                             |                |
| A7                             | 00a707a5                       | Pdspoaxn                           |                |
| A8                             | 00a803a9                       | Dpsoa                              |                |
| A9                             | 00a90189                       | Dpsoxn                             |                |
| AA                             | 00aa0000                       | D                                  |                |
| AB                             | 00ab0889                       | Dpsono                             |                |
| Netzbetrieb                             | 00ac0744                       | Spdsxax                            |                |
| AD                             | 00ad06e9                       | Dpsdaoxn                           |                |
| AE                             | 00ae0b06                       | Dspnao                             |                |
| AF                             | 00af0229                       | Dpno                               |                |
| B0                             | 00b00e05                       | Pdsnoa                             |                |
| B1                             | 00b10665                       | Pdspxoxn                           |                |
| B2                             | 00b21974                       | Sspxdsxox                          |                |
| B3                             | 00b30ce8                       | Sdpanan                            |                |
| B4                             | 00b4070a                       | Psdnax                             |                |
| B5                             | 00b507a9                       | Dpsdoaxn                           |                |
| B6                             | 00b616e9                       | Dpsdpoxx                          |                |
| B7                             | 00b70348                       | Sdpxan                             |                |
| B8                             | 00b8074a                       | Psdpxax                            |                |
| B9                             | 00b906e6                       | Dspdaoxn                           |                |
| BA                             | 00ba0b09                       | Dpsnao                             |                |
| BB                             | 00bb0226                       | Dsno                               | MergePaint     |
| BC                             | 00bc1ce4                       | Spdsanax                           |                |
| BD                             | 00bd0d7d                       | Sdxpdxan                           |                |
| BE                             | 00be0269                       | Dpsxo                              |                |
| BF                             | 00BF 08c9                       | Dpsano                             |                |
| C0                             | 00c000ca                       | PSa                                | Mergecopy      |
| C1                             | 00c11b04                       | Spdsnaoxn                          |                |
| C2                             | 00c21884                       | Spdsonoxn                          |                |
| C3                             | 00c3006a                       | Psxn                               |                |
| C4                             | 00c40e04                       | Spdnoa                             |                |
| C5                             | 00c50664                       | Spdsxoxn                           |                |
| C6                             | 00c60708                       | Sdpnax                             |                |
| C7                             | 00c707aa                       | Psdpoaxn                           |                |
| C8                             | 00c803a8                       | Sdpoa                              |                |
| C9                             | 00c90184                       | Spdoxn                             |                |
| CA                             | 00ca0749                       | Dpsdxax                            |                |
| CB                             | 00cb06e4                       | Spdsaoxn                           |                |
| CC                             | 00cc0020                       | E                                  | Srccopy        |
| CD                             | 00cd0888                       | Sdpono                             |                |
| CE                             | 00ce0b08                       | Sdpnao                             |                |
| CF                             | 00cf0224                       | Spno                               |                |
| D0                             | 00d00e0a                       | Psdnoa                             |                |
| D1                             | 00d1066a                       | Psdpxoxn                           |                |
| D2                             | 00d20705                       | Pdsnax                             |                |
| D3                             | 00d307a4                       | Spdsoaxn                           |                |
| D4                             | 00d41d78                       | Sspxpdxax                          |                |
| D5                             | 00d50ce9                       | Dpsanan                            |                |
| D6                             | 00d616ea                       | Psdpsaoxx                          |                |
| Handelte                             | 00d70349                       | Dpsxan                             |                |
| D8                             | 00d80745                       | Pdspxax                            |                |
| D9                             | 00d906e8                       | Sdpsaoxn                           |                |
| DA                             | 00da1ce9                       | Dpsdanax                           |                |
| DB                             | 00db0d75                       | Spxdsxan                           |                |
| DC                             | 00dc0b04                       | Spdnao                             |                |
| DD                             | 00dd0228                       | Sdno                               |                |
| DE                             | 00DE 0268                       | Sdpxo                              |                |
| DF                             | 00df08c8                       | Sdpano                             |                |
| E0                             | 00e003a5                       | Pdsoa                              |                |
| E1                             | 00e10185                       | Pdsoxn                             |                |
| E2                             | 00e20746                       | Dspdxax                            |                |
| E3                             | 00e306ea                       | Psdpaoxn                           |                |
| E4                             | 00e40748                       | Sdpsxax                            |                |
| E5                             | 00e506e5                       | Pdspaoxn                           |                |
| E6                             | 00e61ce8                       | Sdpsanax                           |                |
| E7                             | 00e70d79                       | Spxpdxan                           |                |
| Verstoßen                             | 00e81d74                       | Sspxdsxax                          |                |
| E9                             | 00e95ce6                       | Dspdsanaxxn                        |                |
| EA                             | 00ea02e9                       | Dpsao                              |                |
| EB                             | 00eb0849                       | Dpsxno                             |                |
| EC                             | 00ec02e8                       | Sdpaar                              |                |
| ED                             | 00ed0848                       | Sdpxno                             |                |
| EE                             | 00ee0086                       | DSo                                | Srcpaint       |
| EF                             | 00ef0a08                       | Sdpnoo                             |                |
| F0                             | 00F 00021                       | P                                  | Patcopy        |
| F1                             | 00F 10885                       | Pdsono                             |                |
| F2                             | 00b20b05                       | Pdsnao                             |                |
| F3                             | 00F 3022a                       | Psno                               |                |
| F4                             | 00F 40b0a                       | Psdnao                             |                |
| F5                             | 00F 50225                       | Pdno                               |                |
| F6                             | 00F 60265                       | Pdsxo                              |                |
| F7                             | 00F 708c5                       | Pdsano                             |                |
| F8                             | 00F 802e5                       | Pdsao                              |                |
| F9                             | 00F 90845                       | Pdsxno                             |                |
| FA                             | 00fa0089                       | DPO                                |                |
| FB                             | 00b0a09                       | Dpsnoo                             | Patpaint       |
| FC                             | 00fc008a                       | PSo                                |                |
| FD                             | 00gd0a0a                       | Psdnoo                             |                |
| FE                             | 00fe02a9                       | Dpsoo                              |                |
| FF                             | 00ff0062                       | 1                                  | Whitheit      |
| 8.000                           | 80 Millionen                       |                                    | Nomirrorbitmap |



 

 

 



