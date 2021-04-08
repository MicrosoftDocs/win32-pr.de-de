---
title: Portieren von Farb aufrufen
description: In der folgenden Tabelle sind die Funktionen von IRIS GL und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- IRIS GL portieren, Farbe
- Portieren von IRIS GL, Color
- Portieren auf OpenGL von IRIS GL, Color
- OpenGL-Portierung von IRIS GL, Color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708465"
---
# <a name="porting-color-calls"></a>Portieren von Farb aufrufen

In der folgenden Tabelle sind die Funktionen von IRIS GL und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion                  | OpenGL-Funktion                                                                                                                               | Bedeutung                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glcolor](glcolor-functions.md)                                                                                                              | Legt RGB-Farbe fest.                                      |
| **color**                         | [glindex](glindex-functions.md)                                                                                                              | Legt den Farbindex fest.                                |
| **GetColor**                      | [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ Aktueller Index von GL \_ )                                               | Gibt den aktuellen Farbindex zurück.                     |
| **getmcolor**                     |                                                                                                                                               | Ruft eine Kopie der RGB-Werte für einen Farb Zuordnungs Eintrag ab. |
| **grgbcolor**                     | **glget**(aktuelle GL- \_ \_ Farbe)                                                                                                               | Ruft die aktuellen RGB-Farbwerte ab.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **RGBColor**                      | **glcolor**                                                                                                                                   | Legt RGB-Farbe fest.                                      |
| **Schreibzugriff**                     | [**glindexmask**](glindexmask.md)                                                                                                            | Legt die Farb Maske für den Farb Index Modus fest.                |
| **wmpackrgbschreitefrage**<br/> | [**glcolormask**](glcolormask.md)                                                                                                            | Legt die RGB-farbmodusmaske fest.                        |
| **getschreitefrage**                  | [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ - \_ farbschreibfrage)**glget**(GL- \_ Index \_ schreibfrage)<br/> | Ruft die Farb Maske ab.                                 |
| **grgbmask**                      | **glget**(GL- \_ Farb \_ schreibfrage)                                                                                                             | Ruft die Farb Maske ab.                                 |
| **zschreitemask**                    | [**gldepthmask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Seien Sie vorsichtig, wenn Sie **zschreitemask** durch " [**gldepthmask**](gldepthmask.md)" ersetzen. **gldepthmask** nimmt ein boolesches Argument an, während **zwrite temask** ein Bitfeld annimmt.

 

Wenn Sie mehrere Farb Zuordnungen verwenden möchten, müssen Sie die entsprechenden Windows Color Map-Funktionen verwenden. Daher verfügen **multimap**, **onemap**, **getcmmode**, **setmap** und **getMap** über keine OpenGL-Entsprechungen.

 

 





