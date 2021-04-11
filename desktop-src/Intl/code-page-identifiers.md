---
description: In der folgenden Tabelle sind die verfügbaren Code Page Bezeichner definiert.
ms.assetid: 5d6fc86a-f205-4d14-bb7c-ecd71682e0fe
title: Code Page Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb0482247313e8d61d61d7d3178906536ab9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128933"
---
# <a name="code-page-identifiers"></a>Code Page Bezeichner

In der folgenden Tabelle sind die verfügbaren Code Page Bezeichner definiert.

> [!Note]  
> ANSI-Codepages können sich auf verschiedenen Computern unterscheiden, oder Sie können für einen einzelnen Computer geändert werden, was zu Daten Beschädigungen führt. Um möglichst konsistente Ergebnisse zu erzielen, sollten Anwendungen anstelle einer bestimmten Codepage Unicode verwenden, z. b. UTF-8 oder UTF-16.

 



| Bezeichner | .Net-Name               | Zusätzliche Informationen                                                                              |
|------------|-------------------------|-----------------------------------------------------------------------------------------------------|
| 037        | IBM037                  | IBM EBCDIC-US-Canada                                                                                |
| 437        | IBM437                  | OEM-USA                                                                                   |
| 500        | IBM500                  | IBM EBCDIC International                                                                            |
| 708        | ASMO-708                | Arabisch (ASMO 708)                                                                                   |
| 709        |                         | Arabisch (ASMO-449 und höher, bcon v4)                                                                         |
| 710        |                         | Arabisch-transparent Arabisch                                                                         |
| 720        | DOS-720                 | Arabisch (transparente ASMO); Arabisch (DOS)                                                             |
| 737        | ibm737                  | OEM Greek (früher 437g); Griechisch (DOS)                                                              |
| 775        | ibm775                  | OEM-Baltisch; Baltisch (DOS)                                                                            |
| 850        | ibm850                  | OEM-mehrsprachige lateinische 1; Westeuropäisch (DOS)                                                    |
| 852        | ibm852                  | OEM Latin 2; Mitteleuropäisch (DOS)                                                                 |
| 855        | IBM855                  | OEM Cyrillic (primär Russisch)                                                                    |
| 857        | ibm857                  | OEM Türkisch; Türkisch (DOS)                                                                          |
| 858        | IBM00858                | OEM-mehrsprachige lateinische 1 + Euro-Symbol                                                              |
| 860        | IBM860                  | OEM Portugiesisch; Portugiesisch (DOS)                                                                    |
| 861        | ibm861                  | OEM-Isländisch Isländisch (DOS)                                                                      |
| 862        | DOS-862                 | OEM Hebräisch; Hebräisch (DOS)                                                                            |
| 863        | IBM863                  | OEM Französisch, Kanada; Französisch (Kanada)                                                          |
| 864        | IBM864                  | OEM-Arabisch; Arabisch (864)                                                                            |
| 865        | IBM865                  | OEM-Nordisch; Nordisch (DOS)                                                                            |
| 866        | cp866                   | OEM Russisch; Kyrillisch (DOS)                                                                         |
| 869        | ibm869                  | OEM modern Greek; Griechisch, modern (DOS)                                                               |
| 870        | IBM870                  | IBM EBCDIC mehrsprachig/roece (lateinisch 2); IBM EBCDIC, mehrsprachig, lateinisch 2                            |
| 874        | Windows-874             | Thailändisch (Windows)                                                         |
| 875        | cp875                   | IBM EBCDIC Greek modern                                                                             |
| 932        | Shift \_ JIS              | ANSI/OEM Japanisch; Japanisch (Shift-JIS)                                                             |
| 936        | GB2312                  | ANSI/OEM Simplified Chinesisch (PRC, Singapur); Vereinfachtes Chinesisch (GB2312)                           |
| 949        | \_k c \_ 5601-1987        | ANSI/OEM Koreanisch (einheitlicher Hangul-Code)                                                               |
| 950        | Big5                    | ANSI/OEM-Chinesisch (traditionell) (Taiwan; Hongkong SAR, PRC); Chinesisch (traditionell) (Big5)               |
| 1026       | IBM1026                 | IBM EBCDIC Türkisch (lateinisch 5)                                                                        |
| 1047       | IBM01047                | IBM EBCDIC Latin 1/offenes System                                                                      |
| 1140       | IBM01140                | IBM EBCDIC US-Canada (037 + Euro-Symbol); IBM EBCDIC (USA-Kanada-Euro)                               |
| 1.141       | IBM01141                | IBM EBCDIC Deutschland (20273 + Euro-Symbol); IBM EBCDIC (Deutschland-Euro)                                 |
| 1142       | IBM01142                | IBM EBCDIC Denmark-Norway (20277 + Euro-Symbol); IBM EBCDIC (Dänemark-Norwegen-Euro)                   |
| 1143       | IBM01143                | IBM EBCDIC Finland-Sweden (20278 + Euro-Symbol); IBM EBCDIC (Finnland-Schweden-Euro)                   |
| 1144       | IBM01144                | IBM EBCDIC Italien (20280 + Euro-Symbol); IBM EBCDIC (Italien-Euro)                                     |
| 1145       | IBM01145                | IBM EBCDIC Latin America-Spain (20284 + Euro-Symbol); IBM EBCDIC (Spanien-Euro)                       |
| 1146       | IBM01146                | IBM EBCDIC Vereinigtes Königreich (20285 + Euro-Symbol); IBM EBCDIC (UK-Euro)                               |
| 1147       | IBM01147                | IBM EBCDIC Frankreich (20297 + Euro-Symbol); IBM EBCDIC (Frankreich-Euro)                                   |
| 1148       | IBM01148                | IBM EBCDIC International (500 + Euro-Symbol); IBM EBCDIC (International-Euro)                       |
| 1149       | IBM01149                | IBM EBCDIC Isländisch (20871 + Euro-Symbol); IBM EBCDIC (Isländisch-Euro)                             |
| 1200       | UTF-16                  | Unicode UTF-16, Little-Endian-Byte Reihenfolge (BMP von ISO 10646); nur für verwaltete Anwendungen verfügbar |
| 1201       | unicodeFFFE             | Unicode UTF-16, Big Endian-Byte Reihenfolge; nur für verwaltete Anwendungen verfügbar                       |
| 1250       | Windows-1250            | ANSI-zentral europäisch; Mitteleuropäisch (Windows)                                                   |
| 1251       | Windows-1251            | ANSI Cyrillic; Kyrillisch (Windows)                                                                   |
| 1252       | Windows-1252            | ANSI Latin 1; Westeuropäisch (Windows)                                                            |
| 1253       | Windows-1253            | ANSI Griechisch; Griechisch (Windows)                                                                         |
| 1254       | Windows-1254            | ANSI Türkisch; Türkisch (Windows)                                                                     |
| 1255       | Windows-1255            | ANSI Hebräisch; Hebräisch (Windows)                                                                       |
| 1256       | Windows-1256            | ANSI Arabisch; Arabisch (Windows)                                                                       |
| 1257       | Windows-1257            | ANSI-Ostsee; Baltisch (Windows)                                                                       |
| 1258       | Windows-1258            | ANSI/OEM Vietnamese; Vietnamesisch (Windows)                                                           |
| 1361       | Johab                   | Koreanisch (Johab)                                                                                      |
| 10000      | Macintosh               | Mac Roman; Westeuropäisch (Mac)                                                                   |
| 10001      | x-Mac-Japanisch          | Japanisch (Mac)                                                                                      |
| 10002      | x-Mac-chinesetrad       | Mac traditionell Chinesisch (Big5); Chinesisch (traditionell) (Mac)                                           |
| 10003      | x-Mac-Koreanisch            | Koreanisch (Mac)                                                                                        |
| 10004      | x-Mac-Arabisch            | Arabisch (Mac)                                                                                        |
| 10005      | x-Mac-Hebräisch            | Hebräisch (Mac)                                                                                        |
| 10006      | x-Mac-Griechisch             | Griechisch (Mac)                                                                                         |
| 10007      | x-Mac-Kyrillisch          | Kyrillisch (Mac)                                                                                      |
| 10008      | x-Mac-chinesesimp       | Chinesisch (vereinfacht) Chinesisch (GB 2312); Chinesisch vereinfacht (Mac)                                          |
| 10010      | x-Mac-Rumänisch          | Rumänisch (Mac)                                                                                      |
| 10017      | x-Mac-Ukrainisch         | Ukrainisch (Mac)                                                                                     |
| 10021      | x-Mac-Thai              | Thailändisch (Mac)                                                                                          |
| 10029      | x-Mac-CE                | Mac Latin 2; Mitteleuropäisch (Mac)                                                                 |
| 10079      | x-Mac-Isländisch         | Isländisch (Mac)                                                                                     |
| 10081      | x-Mac-Türkisch           | Türkisch (Mac)                                                                                       |
| 10082      | x-Mac-Kroatisch          | Kroatisch (Mac)                                                                                      |
| 12000      | UTF-32                  | Unicode UTF-32, Little-Endian-Byte Reihenfolge; nur für verwaltete Anwendungen verfügbar                    |
| 12001      | UTF-32be                | Unicode UTF-32, Big Endian-Byte Reihenfolge; nur für verwaltete Anwendungen verfügbar                       |
| 20000      | x-Chinesisch ( \_ CNS)          | CNS (Taiwan); Chinesisch (traditionell) (CNS)                                                               |
| 20001      | x-cp20001               | TCA-Taiwan                                                                                          |
| 20002      | x \_ Chinesisch-eTEN         | ETEN Taiwan; Chinesisch (traditionell) (eTEN)                                                             |
| 20003      | x-cp20003               | IBM5550 Taiwan                                                                                      |
| 20004      | x-cp20004               | Teletext-Taiwan                                                                                     |
| 20005      | x-cp20005               | Wang Taiwan                                                                                         |
| 20105      | x-IA5                   | IA5 (UNV International Alphabet No. 5, 7 Bit); Westeuropäisch (IA5)                               |
| 20106      | x-IA5-Deutsch            | IA5 Deutsch (7-Bit)                                                                                  |
| 20107      | x-IA5-Schwedisch           | IA5 Swedish (7-Bit)                                                                                 |
| 20108      | x-IA5-Norwegisch         | IA5 Norwegisch (7-Bit)                                                                               |
| 20127      | US-ASCII                | US-ASCII (7-Bit)                                                                                    |
| 20261      | x-cp20261               | T. 61                                                                                                |
| 20269      | x-cp20269               | ISO 6937 Non-Spacing Accent                                                                         |
| 20273      | IBM273                  | IBM EBCDIC Deutschland                                                                                  |
| 20277      | IBM277                  | IBM EBCDIC-Denmark-Norway                                                                           |
| 20278      | IBM278                  | IBM EBCDIC-Finland-Sweden                                                                           |
| 20280      | IBM280                  | IBM EBCDIC Italien                                                                                    |
| 20284      | IBM284                  | IBM EBCDIC Latin America-Spain                                                                      |
| 20285      | IBM285                  | IBM EBCDIC Vereinigtes Königreich                                                                           |
| 20290      | IBM290                  | IBM EBCDIC Japanisch, Katakana erweitert                                                               |
| 20297      | IBM297                  | IBM EBCDIC Frankreich                                                                                   |
| 20420      | IBM420                  | IBM EBCDIC Arabisch                                                                                   |
| 20423      | IBM423                  | IBM EBCDIC Griechisch                                                                                    |
| 20424      | IBM424                  | IBM EBCDIC Hebräisch                                                                                   |
| 20833      | x-EBCDIC-koreanextended | IBM EBCDIC Koreanisch erweitert                                                                          |
| 20838      | IBM-Thai                | IBM EBCDIC Thai                                                                                     |
| 20866      | koi8-r                  | Russisch (KOI8-R); Kyrillisch (KOI8-R)                                                                 |
| 20871      | IBM871                  | IBM EBCDIC-Isländisch                                                                                |
| 20880      | IBM880                  | IBM EBCDIC Cyrillic Russisch                                                                         |
| 20905      | IBM905                  | IBM EBCDIC Türkisch                                                                                  |
| 20924      | IBM00924                | IBM EBCDIC Latin 1/Open System (1047 + Euro-Symbol)                                                 |
| 20932      | EUC-JP                  | Japanisch (JIS 0208-1990 und 0212-1990)                                                              |
| 20936      | x-cp20936               | Vereinfachtes Chinesisch (GB2312); Chinesisch (vereinfacht) (GB2312-80)                                         |
| 20949      | x-cp20949               | Koreanisch Wansung                                                                                      |
| 21025      | cp1025                  | IBM EBCDIC Cyrillic-Serbian-Bulgarian                                                               |
| 21027      |                         | veraltet                                                                                        |
| 21866      | KOI8-u                  | Ukrainisch (KOI8-U); Kyrillisch (KOI8-U)                                                               |
| 28591      | ISO-8859-1              | ISO 8859-1 Lateinisch 1; Westeuropäisch (ISO)                                                          |
| 28592      | ISO-8859-2              | ISO 8859-2 zentral europäisch; Mitteleuropäisch (ISO)                                                 |
| 28593      | ISO-8859-3              | ISO 8859-3 Lateinisch 3                                                                                  |
| 28594      | ISO-8859-4              | ISO 8859-4-Ostsee                                                                                   |
| 28595      | ISO-8859-5              | ISO 8859-5 Cyrillic                                                                                 |
| 28596      | ISO-8859-6              | ISO 8859-6 Arabic                                                                                   |
| 28597      | ISO-8859-7              | ISO 8859-7 Greek                                                                                    |
| 28598      | ISO-8859-8              | ISO 8859-8 Hebräisch; Hebräisch (ISO-Visual)                                                              |
| 28599      | ISO-8859-9              | ISO 8859-9 Turkish                                                                                  |
| 28603      | ISO-8859-13             | ISO 8859-13 Estonian                                                                                |
| 28605      | ISO-8859-15             | ISO 8859-15 lateinisch 9                                                                                 |
| 29001      | x-Europa                | Europa 3                                                                                            |
| 38598      | ISO-8859-8-i            | ISO 8859-8 Hebräisch; Hebräisch (ISO-logisch)                                                             |
| 50220      | ISO-2022-JP             | ISO 2022 Japanisch ohne Halfwidth Katakana; Japanisch (JIS)                                        |
| 50221      | csISO2022JP             | ISO 2022 Japanisch mit Halfwidth Katakana; Japanisch (JIS-1-Byte-Kana zulassen)                         |
| 50222      | ISO-2022-JP             | ISO 2022 Japanisch JIS X 0201-1989; Japanisch (JIS-1 Byte Kana-so/SI)                         |
| 50225      | ISO-2022-KR             | ISO 2022 Koreanisch                                                                                     |
| 50227      | x-cp50227               | ISO 2022 vereinfachtes Chinesisch; Vereinfachtes Chinesisch (ISO 2022)                                          |
| 50229      |                         | ISO 2022 Chinesisch (traditionell)                                                                        |
| 50930      |                         | EBCDIC Japanisch (Katakana) erweitert                                                                 |
| 50931      |                         | EBCDIC US-Canada und Japanisch                                                                       |
| 50933      |                         | EBCDIC Koreanisch erweitert und Koreanisch                                                                   |
| 50935      |                         | EBCDIC vereinfachtes Chinesisch (erweitert) und Chinesisch (vereinfacht)                                           |
| 50936      |                         | EBCDIC-Chinesisch (vereinfacht)                                                                           |
| 50937      |                         | EBCDIC US-Canada und Chinesisch (traditionell)                                                            |
| 50939      |                         | EBCDIC Japanisch (lateinisch) erweitert und Japanisch                                                       |
| 51932      | EUC-JP                  | EUC Japanisch                                                                                        |
| 51936      | EUC-CN                  | EUC vereinfachtes Chinesisch; Chinesisch (vereinfacht) (EUC)                                                    |
| 51949      | EUC-KR                  | EUC Koreanisch                                                                                          |
| 51950      |                         | EUC Chinesisch (traditionell)                                                                             |
| 52936      | Hz-GB-2312              | Hz GB2312 vereinfachtes Chinesisch; Chinesisch (vereinfacht) (Hz)                                               |
| 54936      | GB18030                 | **Windows XP und höher:** GB18030 vereinfachtes Chinesisch (4 Byte); Vereinfachtes Chinesisch (GB18030)         |
| 57002      | x-ISCII-de              | ISCII-Geräte Abteilung                                                                                    |
| 57003      | x-ISCII-be              | ISCII Bangla                                                                                        |
| 57004      | x-ISCII-Ta              | ISCII Tamil                                                                                         |
| 57005      | x-ISCII-te              | ISCII Telugu                                                                                        |
| 57006      | x-ISCII-as              | ISCII-Assamese                                                                                      |
| 57007      | x-ISCII-or              | ISCII-odia                                                                                          |
| 57008      | x-ISCII-Ka              | ISCII Kannada                                                                                       |
| 57009      | x-ISCII-MA              | ISCII Malayalam                                                                                     |
| 57010      | x-ISCII-gu              | ISCII Gujarati                                                                                      |
| 57011      | x-ISCII-PA              | ISCII Punjabi                                                                                       |
| 65000      | UTF-7                   | Unicode (UTF-7)                                                                                     |
| 65001      | UTF-8                   | Unicode (UTF-8)                                                                                     |



 

 

 



