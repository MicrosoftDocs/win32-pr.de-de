---
description: In diesem Abschnitt werden die ternären Rastervorgangcodes aufgeführt, die von den Funktionen BitBlt, PatBlt und StretchBlt verwendet werden. Ternäre Rasteroperationscodes definieren, wie GDI die Bits in einer Quellbitmap mit den Bits in der Zielbitmap kombiniert.
ms.assetid: 538f3580-d6a7-4dae-8185-802eb9c96735
title: Ternäre Rastervorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a6dd0009a9be4a1fe062dbb2ab40766a7b01a565b80a7b866c0ce1af40ca48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889010"
---
# <a name="ternary-raster-operations"></a>Ternäre Rastervorgänge

In diesem Abschnitt werden die ternären Rasteroperationscodes aufgeführt, die von den [**Funktionen BitBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)und [**StretchBlt verwendet**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) werden. Ternäre Rasteroperationscodes definieren, wie GDI die Bits in einer Quellbitmap mit den Bits in der Zielbitmap kombiniert.

Jeder Rastervorgang-Code stellt einen booleschen Vorgang dar, bei dem die Werte der Pixel in der Quelle, des ausgewählten Pinsels und des Ziels kombiniert werden. Im Folgenden finden Sie die drei Operanden, die in diesen Vorgängen verwendet werden.



| Operand | Bedeutung                              |
|---------|--------------------------------------|
| D       | Zielbitmap                   |
| P       | Ausgewählter Pinsel (auch als Muster bezeichnet) |
| E       | Quellbitmap                        |



 

In diesen Vorgängen verwendete boolesche Operatoren folgen.



| Operator | Bedeutung                    |
|----------|----------------------------|
| a        | Bitweises AND                |
| n        | Bitweises NOT (umgekehrt)      |
| o        | Bitweises OR                 |
| x        | Bitweises exklusives OR (XOR) |



 

Alle booleschen Vorgänge werden in umgekehrter polnischer Notation dargestellt. Der folgende Vorgang ersetzt beispielsweise die Werte der Pixel in der Zielbitmap durch eine Kombination aus den Pixelwerten der Quelle und des Pinsels:


```C++
PSo 
```



Der folgende Vorgang kombiniert die Werte der Pixel in der Quelle und im Pinsel mit den Pixelwerten der Zielbitmap (es gibt alternative Schreibweisen derselben Funktion, obwohl eine bestimmte Rechtschreibung möglicherweise nicht in der Liste enthalten ist, wäre eine entsprechende Form):


```C++
DPSoo 
```



Jeder Rasteroperationscode ist eine 32-Bit-Ganzzahl, deren hochwertiges Wort ein boolescher Vorgangsindex ist und dessen niedrigwertiges Wort der Vorgangscode ist. Der 16-Bit-Vorgangsindex ist ein null-erweiterter 8-Bit-Wert, der das Ergebnis des booleschen Vorgangs für vordefinierte Pinsel-, Quell- und Zielwerte darstellt. Beispielsweise werden die Vorgangsindizes für die PSo- und DPSoo-Vorgänge in der folgenden Liste angezeigt.



| P                | E   | D   | Pso   | DPSoo |
|------------------|-----|-----|-------|-------|
| 0                | 0   | 0   | 0     | 0     |
| 0                | 0   | 1   | 0     | 1     |
| 0                | 1   | 0   | 1     | 1     |
| 0                | 1   | 1   | 1     | 1     |
| 1                | 0   | 0   | 1     | 1     |
| 1                | 0   | 1   | 1     | 1     |
| 1                | 1   | 0   | 1     | 1     |
| 1                | 1   | 1   | 1     | 1     |
| Vorgangsindex: |     |     | 00FCh | 00FEh |



 

In diesem Fall hat PSo den Vorgangsindex 00FC (von unten nach oben gelesen). DPSoo hat den Vorgangsindex 00FE. Diese Werte definieren die Position der entsprechenden Rastervorgangcodes, wie in Tabelle A.1, "Raster-Vorgangscodes" gezeigt. Der PSo-Vorgang befindet sich in Zeile 252 (00FCh) der Tabelle. DPSoo befindet sich in Zeile 254 (00FEh).

Den am häufigsten verwendeten Rastervorgängen wurden spezielle Namen in der SDK-Headerdatei WINDOWS.H. zugewiesen. Sie sollten diese Namen nach Möglichkeit in Ihren Anwendungen verwenden.

Wenn die Quell- und Zielbitmaps monofarbig sind, stellt der Bitwert 0 ein schwarzes Pixel und der Bitwert 1 ein weißes Pixel dar. Wenn die Quell- und Zielbitmaps Farben sind, werden diese Farben mit RGB-Werten dargestellt. Weitere Informationen zu RGB-Werten finden Sie unter [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb).

**Rasteroperationscodes**



| Boolesche Funktion (hexadezimal) | Rastervorgang (hexadezimal) | Boolesche Funktion in umgekehrter Sprache | Allgemeiner Name    |
|--------------------------------|--------------------------------|------------------------------------|----------------|
| 00                             | 00000042                       | 0                                  | Schwärze      |
| 01                             | 00010289                       | DPSoon                             |                |
| 02                             | 00020C89                       | DPSona                             |                |
| 03                             | 000300AA                       | PSon                               |                |
| 04                             | 00040C88                       | SDPona                             |                |
| 05                             | 000500A9                       | DPon                               |                |
| 06                             | 00060865                       | PDSxnon                            |                |
| 07                             | 000702C5                       | PDSaon                             |                |
| 08                             | 00080F08                       | SDPnaa                             |                |
| 09                             | 00090245                       | PDSxon                             |                |
| 0A                             | 000A0329                       | DPna                               |                |
| 0 B                             | 000B0B2A                       | PSDnaon                            |                |
| 0C                             | 000C0324                       | SPna                               |                |
| 0D                             | 000D0B25                       | PDSnaon                            |                |
| 0e                             | 000E08A5                       | PDSonon                            |                |
| 0F                             | 000F0001                       | Pn                                 |                |
| 10                             | 00100C85                       | PDSona                             |                |
| 11                             | 001100A6                       | DSon                               | NOTSRCERASE    |
| 12                             | 00120868                       | SDPxnon                            |                |
| 13                             | 001302C8                       | SDPaon                             |                |
| 14                             | 00140869                       | DPSxnon                            |                |
| 15                             | 001502C9                       | DPSaon                             |                |
| 16                             | 00165CCA                       | PSDPSanaxx                         |                |
| 17                             | 00171D54                       | SSPxDSxaxn                         |                |
| 18                             | 00180D59                       | SPxPDxa                            |                |
| 19                             | 00191CC8                       | SDPSanaxn                          |                |
| 1A                             | 001A06C5                       | PDSPaox                            |                |
| 1B                             | 001B0768                       | SDPSxaxn                           |                |
| 1C                             | 001C06CA                       | PSDPaox                            |                |
| 1D                             | 001D0766                       | DSPDxaxn                           |                |
| 1E                             | 001E01A5                       | PDSox                              |                |
| 1F                             | 001F0385                       | PDSoan                             |                |
| 20                             | 00200F09                       | DPSnaa                             |                |
| 21                             | 00210248                       | SDPxon                             |                |
| 22                             | 00220326                       | DSna                               |                |
| 23                             | 00230B24                       | SPDnaon                            |                |
| 24                             | 00240D55                       | SPxDSxa                            |                |
| 25                             | 00251CC5                       | PDSPanaxn                          |                |
| 26                             | 002606C8                       | SDPSaox                            |                |
| 27                             | 00271868                       | SDPSxnox                           |                |
| 28                             | 00280369                       | DPSxa                              |                |
| 29                             | 002916CA                       | PSDPSaoxxn                         |                |
| 2A                             | 002A0CC9                       | DPSana                             |                |
| 2B                             | 002B1D58                       | SSPxPDxaxn                         |                |
| 2C                             | 002C0784                       | BESENSOAX                            |                |
| 2D                             | 002D060A                       | PSDnox                             |                |
| 2E                             | 002E064A                       | PSDPxox                            |                |
| 2F                             | 002F0E2A                       | PSDnoan                            |                |
| 30                             | 0030032A                       | PSna                               |                |
| 31                             | 00310B28                       | SDPnaon                            |                |
| 32                             | 00320688                       | SDPSoox                            |                |
| 33                             | 00330008                       | Sn                                 | NOTSRCCOPY     |
| 34                             | 003406C4                       | besensaox                            |                |
| 35                             | 00351864                       | FLOWSxnox                           |                |
| 36                             | 003601A8                       | SDPox                              |                |
| 37                             | 00370388                       | SDPoan                             |                |
| 38                             | 0038078A                       | PSDPoax                            |                |
| 39                             | 00390604                       | SPDnox                             |                |
| 3A                             | 003A0644                       | BESxox                            |                |
| 3B                             | 003B0E24                       | SPDnoan                            |                |
| 3C                             | 003C004A                       | Psx                                |                |
| 3D                             | 003D18A4                       | BESENSONOX                           |                |
| 3E                             | 003E1B24                       | FLOWSnaox                           |                |
| 3F                             | 003F00EA                       | PSan                               |                |
| 40                             | 00400F0A                       | PSDnaa                             |                |
| 41                             | 00410249                       | DPSxon                             |                |
| 42                             | 00420D5D                       | SDxPDxa                            |                |
| 43                             | 00431CC4                       | DASSSanaxn                          |                |
| 44                             | 00440328                       | SDna                               | SRCERASE       |
| 45                             | 00450B29                       | DPSnaon                            |                |
| 46                             | 004606C6                       | DSPDaox                            |                |
| 47                             | 0047076A                       | PSDPxaxn                           |                |
| 48                             | 00480368                       | SDPxa                              |                |
| 49                             | 004916C5                       | PDSPDaoxxn                         |                |
| 4A                             | 004A0789                       | DPSDoax                            |                |
| 4B                             | 004B0605                       | PDSnox                             |                |
| 4C                             | 004C0CC8                       | SDPana                             |                |
| 4D                             | 004D1954                       | SSPxDSxoxn                         |                |
| 4E                             | 004E0645                       | PDSPxox                            |                |
| 4F                             | 004F0E25                       | PDSnoan                            |                |
| 50                             | 00500325                       | PDna                               |                |
| 51                             | 00510B26                       | DSPnaon                            |                |
| 52                             | 005206C9                       | DPSDaox                            |                |
| 53                             | 00530764                       | DASSSxaxn                           |                |
| 54                             | 005408A9                       | DPSonon                            |                |
| 55                             | 00550009                       | Dn                                 | DSTINVERT      |
| 56                             | 005601A9                       | DPSox                              |                |
| 57                             | 00570389                       | DPSoan                             |                |
| 58                             | 00580785                       | PDSPoax                            |                |
| 59                             | 00590609                       | DPSnox                             |                |
| 5A                             | 005A0049                       | Dpx                                | PATINVERT      |
| 5B                             | 005B18A9                       | DPSDonox                           |                |
| 5C                             | 005C0649                       | DPSDxox                            |                |
| 5d                             | 005D0E29                       | DPSnoan                            |                |
| 5E                             | 005E1B29                       | DPSDnaox                           |                |
| 5F                             | 005F00E9                       | DPan                               |                |
| 60                             | 00600365                       | PDSxa                              |                |
| 61                             | 006116C6                       | DSPDSaoxxn                         |                |
| 62                             | 00620786                       | DSPDoax                            |                |
| 63                             | 00630608                       | SDPnox                             |                |
| 64                             | 00640788                       | SDPSoax                            |                |
| 65                             | 00650606                       | DSPnox                             |                |
| 66                             | 00660046                       | Dsx                                | SRCINVERT      |
| 67                             | 006718A8                       | SDPSonox                           |                |
| 68                             | 006858A6                       | DSPDSonoxxn                        |                |
| 69                             | 00690145                       | PDSxxn                             |                |
| 6A                             | 006A01E9                       | DPSax                              |                |
| 6B                             | 006B178A                       | PSDPSoaxxn                         |                |
| 6C                             | 006C01E8                       | SDPax                              |                |
| 6D                             | 006D1785                       | PDSPDoaxxn                         |                |
| 6E                             | 006E1E28                       | SDPSnoax                           |                |
| 6F                             | 006F0C65                       | PDSxnan                            |                |
| 70                             | 00700CC5                       | PDSana                             |                |
| 71                             | 00711D5C                       | SSDxPDxaxn                         |                |
| 72                             | 00720648                       | SDPSxox                            |                |
| 73                             | 00730E28                       | SDPnoan                            |                |
| 74                             | 00740646                       | DSPDxox                            |                |
| 75                             | 00750E26                       | DSPnoan                            |                |
| 76                             | 00761B28                       | SDPSnaox                           |                |
| 77                             | 007700E6                       | DSan                               |                |
| 78                             | 007801E5                       | PDSax                              |                |
| 79                             | 00791786                       | DSPDSoaxxn                         |                |
| 7a                             | 007A1E29                       | DPSDnoax                           |                |
| 7B                             | 007B0C68                       | SDPxnan                            |                |
| 7C                             | 007C1E24                       | BESneinax                           |                |
| 7d                             | 007D0C69                       | DPSxnan                            |                |
| 7e                             | 007E0955                       | SPxDSxo                            |                |
| 7f                             | 007F03C9                       | DPSaan                             |                |
| 80                             | 008003E9                       | DPSaa                              |                |
| 81                             | 00810975                       | SPxDSxon                           |                |
| 82                             | 00820C49                       | DPSxna                             |                |
| 83                             | 00831E04                       | CHEFSnoaxn                          |                |
| 84                             | 00840C48                       | SDPxna                             |                |
| 85                             | 00851E05                       | PDSPnoaxn                          |                |
| 86                             | 008617A6                       | DSPDSoaxx                          |                |
| 87                             | 008701C5                       | PDSaxn                             |                |
| 88                             | 008800C6                       | Dsa                                | SRCAND         |
| 89                             | 00891B08                       | SDPSnaoxn                          |                |
| 8A                             | 008A0E06                       | DSPnoa                             |                |
| 8B                             | 008B0666                       | DSPDxoxn                           |                |
| 8C                             | 008C0E08                       | SDPnoa                             |                |
| 8D                             | 008D0668                       | SDPSxoxn                           |                |
| 8E                             | 008E1D7C                       | SSDxPDxax                          |                |
| 8F                             | 008F0CE5                       | PDSanan                            |                |
| 90                             | 00900C45                       | PDSxna                             |                |
| 91                             | 00911E08                       | SDPSnoaxn                          |                |
| 92                             | 009217A9                       | DPSDPoaxx                          |                |
| 93                             | 009301C4                       | SPDaxn                             |                |
| 94                             | 009417AA                       | PSDPSoaxx                          |                |
| 95                             | 009501C9                       | DPSaxn                             |                |
| 96                             | 00960169                       | DPSxx                              |                |
| 97                             | 0097588A                       | PSDPSonoxx                         |                |
| 98                             | 00981888                       | SDPSonoxn                          |                |
| 99                             | 00990066                       | DSxn                               |                |
| 9a                             | 009A0709                       | DPSnax                             |                |
| 9B                             | 009B07A8                       | SDPSoaxn                           |                |
| 9C                             | 009C0704                       | SPDnax                             |                |
| 9D                             | 009D07A6                       | DSPDoaxn                           |                |
| 9E                             | 009E16E6                       | DSPDSaoxx                          |                |
| 9F                             | 009F0345                       | PDSxan                             |                |
| A0                             | 00A000C9                       | Dpa                                |                |
| A1                             | 00A11B05                       | PDSPnaoxn                          |                |
| A2                             | 00A20E09                       | DPSnoa                             |                |
| A3                             | 00A30669                       | DPSDxoxn                           |                |
| A4                             | 00A41885                       | PDSPonoxn                          |                |
| A5                             | 00A50065                       | PDxn                               |                |
| A6                             | 00A60706                       | DSPnax                             |                |
| A7                             | 00A707A5                       | PDSPoaxn                           |                |
| A8                             | 00A803A9                       | DPSoa                              |                |
| A9                             | 00A90189                       | DPSoxn                             |                |
| AA                             | 00AA0029                       | D                                  |                |
| AB                             | 00AB0889                       | DPSono                             |                |
| Netzbetrieb                             | 00AC0744                       | PROXYSxax                            |                |
| AD                             | 00AD06E9                       | DPSDaoxn                           |                |
| AE                             | 00AE0B06                       | DSPnao                             |                |
| AF                             | 00AF0229                       | DPno                               |                |
| B0                             | 00B00E05                       | PDSnoa                             |                |
| B1                             | 00B10665                       | PDSPxoxn                           |                |
| B2                             | 00B21974                       | SSPxDSxox                          |                |
| B3                             | 00B30CE8                       | SDPanan                            |                |
| B4                             | 00B4070A                       | PSDnax                             |                |
| B5                             | 00B507A9                       | DPSDoaxn                           |                |
| B6                             | 00B616E9                       | DPSDPaoxx                          |                |
| B7                             | 00B70348                       | SDPxan                             |                |
| B8                             | 00B8074A                       | PSDPxax                            |                |
| B9                             | 00B906E6                       | DSPDaoxn                           |                |
| BA                             | 00BA0B09                       | DPSnao                             |                |
| BB                             | 00BB0226                       | DSno                               | MERGEPAINT     |
| BC                             | 00BC1CE4                       | BESENSANAX                           |                |
| BD                             | 00BD0D7D                       | SDxPDxan                           |                |
| BE                             | 00BE0269                       | DPSxo                              |                |
| BF                             | 00BF08C9                       | DPSano                             |                |
| C0                             | 00C000CA                       | Psa                                | MERGECOPY      |
| C1                             | 00C11B04                       | NATSnaoxn                          |                |
| C2                             | 00C21884                       | ANZSonoxn                          |                |
| C3                             | 00C3006A                       | PSxn                               |                |
| C4                             | 00C40E04                       | SPDnoa                             |                |
| C5                             | 00C50664                       | FLOWSxoxn                           |                |
| C6                             | 00C60708                       | SDPnax                             |                |
| C7                             | 00C707AA                       | PSDPoaxn                           |                |
| C8                             | 00C803A8                       | SDPoa                              |                |
| C9                             | 00C90184                       | SPDoxn                             |                |
| CA                             | 00CA0749                       | DPSDxax                            |                |
| CB                             | 00CB06E4                       | BESENSAOXN                           |                |
| CC                             | 00CC0020                       | E                                  | SRCCOPY        |
| CD                             | 00CD0888                       | SDPono                             |                |
| CE                             | 00CE0B08                       | SDPnao                             |                |
| CF                             | 00CF0224                       | SPno                               |                |
| D0                             | 00D00E0A                       | PSDnoa                             |                |
| D1                             | 00D1066A                       | PSDPxoxn                           |                |
| D2                             | 00D20705                       | PDSnax                             |                |
| D3                             | 00D307A4                       | BESENSOAXN                           |                |
| D4                             | 00D41D78                       | SSPxPDxax                          |                |
| D5                             | 00D50CE9                       | DPSanan                            |                |
| D6                             | 00D616EA                       | PSDPSaoxx                          |                |
| D7                             | 00D70349                       | DPSxan                             |                |
| D8                             | 00D80745                       | PDSPxax                            |                |
| D9                             | 00D906E8                       | SDPSaoxn                           |                |
| DA                             | 00DA1CE9                       | DPSDanax                           |                |
| DB                             | 00DB0D75                       | SPxDSxan                           |                |
| DC                             | 00DC0B04                       | SPDnao                             |                |
| DD                             | 00DD0228                       | SDno                               |                |
| DE                             | 00DE0268                       | SDPxo                              |                |
| DF                             | 00DF08C8                       | SDPano                             |                |
| E0                             | 00E003A5                       | PDSoa                              |                |
| E1                             | 00E10185                       | PDSoxn                             |                |
| E2                             | 00E20746                       | DSPDxax                            |                |
| E3                             | 00E306EA                       | PSDPaoxn                           |                |
| E4                             | 00E40748                       | SDPSxax                            |                |
| E5                             | 00E506E5                       | PDSPaoxn                           |                |
| E6                             | 00E61CE8                       | SDPSanax                           |                |
| E7                             | 00E70D79                       | SPxPDxan                           |                |
| E8                             | 00E81D74                       | SSPxDSxax                          |                |
| E9                             | 00E95CE6                       | DSPDSanaxxn                        |                |
| EA                             | 00EA02E9                       | DPSao                              |                |
| EB                             | 00EB0849                       | DPSxno                             |                |
| EC                             | 00EC02E8                       | SDPao                              |                |
| ED                             | 00ED0848                       | SDPxno                             |                |
| EE                             | 00EE0086                       | Dso                                | SRCPAINT       |
| EF                             | 00EF0A08                       | SDPnoo                             |                |
| F0                             | 00F00021                       | P                                  | PATCOPY        |
| F1                             | 00F10885                       | PDSono                             |                |
| F2                             | 00F20B05                       | PDSnao                             |                |
| F3                             | 00F3022A                       | PSno                               |                |
| F4                             | 00F40B0A                       | PSDnao                             |                |
| F5                             | 00F50225                       | PDno                               |                |
| F6                             | 00F60265                       | PDSxo                              |                |
| F7                             | 00F708C5                       | PDSano                             |                |
| F8                             | 00F802E5                       | PDSao                              |                |
| F9                             | 00F90845                       | PDSxno                             |                |
| FA                             | 00FA0089                       | Dsb                                |                |
| FB                             | 00FB0A09                       | DPSnoo                             | PATPAINT       |
| FC                             | 00FC008A                       | Pso                                |                |
| FD                             | 00FD0A0A                       | PSDnoo                             |                |
| FE                             | 00FE02A9                       | DPSoo                              |                |
| FF                             | 00FF0062                       | 1                                  | Weiße      |
| 8.000                           | 80000000                       |                                    | NOMIRRORBITMAP |



 

 

 



