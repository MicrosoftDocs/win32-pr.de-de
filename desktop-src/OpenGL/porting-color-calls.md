---
title: Portieren von Farbaufrufen
description: In der folgenden Tabelle sind die IRIS GL-Farbfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- IRIS GL-Portierung, Farbe
- Portieren von IRIS GL, Farbe
- Portieren von IRIS GL,Color zu OpenGL
- OpenGL-Portierung von IRIS GL,Color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e15774f66964c11527955b57651e69db26f6f3d3704d114fdfa4de9a0d5b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777050"
---
# <a name="porting-color-calls"></a>Portieren von Farbaufrufen

In der folgenden Tabelle sind die IRIS GL-Farbfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                  | OpenGL-Funktion                                                                                                                               | Bedeutung                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | Legt die RGB-Farbe fest.                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | Legt den Farbindex fest.                                |
| **getcolor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ CURRENT \_ INDEX )                                               | Gibt den aktuellen Farbindex zurück.                     |
| **getmcolor**                     |                                                                                                                                               | Ruft eine Kopie der RGB-Werte für einen Farbzuordnungseintrag ab. |
| **gRGBcolor**                     | **glGet**( GL \_ CURRENT \_ COLOR )                                                                                                               | Ruft die aktuellen RGB-Farbwerte ab.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **RGBcolor**                      | **glColor**                                                                                                                                   | Legt die RGB-Farbe fest.                                      |
| **Writemask**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | Legt die Farbmaske für den Farbindexmodus fest.                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | Legt die RGB-Farbmodusmaske fest.                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ COLOR \_ WRITEMASK )**glGet**( GL \_ INDEX \_ WRITEMASK )<br/> | Ruft die Farbmaske ab.                                 |
| **gRGBmask**                      | **glGet**( GL \_ COLOR \_ WRITEMASK )                                                                                                             | Ruft die Farbmaske ab.                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Seien Sie vorsichtig, wenn **Sie zwritemask** durch [**glDepthMask ersetzen.**](gldepthmask.md) **glDepthMask verwendet** ein boolesches Argument, während **zwritemask** ein Bitfeld verwendet.

 

Wenn Sie mehrere Farbzuordnungen verwenden möchten, müssen Sie die entsprechenden Windows Farbzuordnungsfunktionen verwenden. Daher verfügen **multimap**, **onemap**, **getcmmode,** **setmap** und **getmap** über keine OpenGL-Entsprechungen.

 

 





