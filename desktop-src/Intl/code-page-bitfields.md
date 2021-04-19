---
description: Die Codepage-Bitfelder werden in der fontSignature-und der LOCALESIGNATURE-Struktur verwendet. Hinweis Alle Gebiets Schemas unterstützen keine Codepages.
ms.assetid: 830b1a88-cb0c-4719-b857-4cc2cd67dd5d
title: Codepage-Bitfields
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f9df44ac14d935a026a10ab1e71eb7378840de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355478"
---
# <a name="code-page-bitfields"></a>Codepage-Bitfields

Die Codepage-Bitfelder werden in der [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) -und der [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) -Struktur verwendet.

> [!Note]  
> Alle Gebiets Schemas unterstützen keine Codepages. Die in diesem Thema beschriebenen Bitfelder gelten nicht für Unicode-Gebiets Schemas. Zum Ermitteln unterstützter Skripts für ein Gebiets Schema kann die Anwendung das Gebiets Schema-bezeichnerkonstante-Gebiets Schema [ \_ sscripts](locale-sscripts.md) mit [**getlocaleingefoex**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)verwenden.

 

> [!Note]  
> Wenn ein Bit in einem Codepage-Bitfeld vorhanden ist, bedeutet dies nicht unbedingt, dass alle Zeichen folgen für ein Gebiets Schema ohne Verlust in dieser Codepage codiert werden können. Um Daten ohne Verlust beizubehalten, empfiehlt sich die Verwendung von Unicode UTF-8 oder UTF-16.

 



| bit          | Codepage | BESCHREIBUNG                                           |
|--------------|-----------|-------------------------------------------------------|
| ANSI         |           |                                                       |
| 0            | 1252      | Lateinisch 1                                               |
| 1            | 1250      | Lateinisch 2: Mitteleuropa                               |
| 2            | 1251      | Kyrillisch                                              |
| 3            | 1253      | Griechisch                                                 |
| 4            | 1254      | Türkisch                                               |
| 5            | 1255      | Hebräisch                                                |
| 6            | 1256      | Arabisch                                                |
| 7            | 1257      | Baltisch                                                |
| 8            | 1258      | Vietnamesisch                                            |
| 9 - 15       |           | Reserviert für ANSI                                     |
| ANSI und OEM |           |                                                       |
| 16           | 874       | Thailändisch                                                  |
| 17           | 932       | Japanisch (Shift_JIS)                                   |
| 18           | 936       | Vereinfachtes Chinesisch (PRC, Singapur)                   |
| 19           | 949       | Koreanischer einheitlicher Hangul-Code (Hangul tonghabhyung-Code) |
| 20           | 950       | Chinesisch (traditionell) (Taiwan; Hongkong SAR, PRC      |
| 21           | 1361      | Koreanisch (Johab)                                        |
| 22 - 29      |           | Reserviert für alternative ANSI und OEM                   |
| 30 - 31      |           | Vom System reserviert.                                   |
| OEM          |           |                                                       |
| 32-46      |           | Reserviert für OEM                                      |
| 47           | 1258      | Vietnamesisch                                            |
| 48           | 869       | Modernes Griechisch                                          |
| 49           | 866       | Russisch                                               |
| 50           | 865       | Nordischen                                                |
| 51           | 864       | Arabisch                                                |
| 52           | 863       | Französisch (Kanada)                                       |
| 53           | 862       |                                                       |
| 54           | 861       | Isländisch                                             |
| 55           | 860       | Portugiesisch                                            |
| 56           | 857       | Türkisch                                               |
| 57           | 855       | Cyrillic primär Russisch                           |
| 58           | 852       | Lateinisch 2                                               |
| 59           | 775       | Baltisch                                                |
| 60           | 737       | Greek früher 437g                                  |
| 61           | 708; 720  | Sprache ASMO 708                                      |
| 62           | 850       | Mehrsprachige lateinische 1                                  |
| 63           | 437       | US                                                    |



 

 

 



