---
title: Portieren von Pixel Vorgängen
description: Portieren von Pixel Vorgängen
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- IRIS GL Porting, Pixel
- Portieren von IRIS GL, Pixel
- Portieren auf OpenGL von IRIS GL, Pixel
- OpenGL-Portierung von IRIS GL, Pixel
- Pixel, Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712509"
---
# <a name="porting-pixel-operations"></a>Portieren von Pixel Vorgängen

Beachten Sie beim Portieren von Code, der Pixel Vorgänge umfasst, die folgenden Punkte:

-   Logische Pixel Vorgänge werden nicht auf RGBA-Farb Puffer angewendet. Weitere Informationen finden Sie unter [**gllogicop**](gllogicop.md).
-   Im Allgemeinen verwendet IRIS GL das Format ABGR für Pixel, während OpenGL RGBA verwendet. Sie können das Format mit [**glpixelstore**](glpixelstore-functions.md)ändern.
-   Beachten Sie bei der Portierung von **lrectwrite** -Funktionen, dass **lrectwrite** schreibt (z. b. könnte es in den tiefen Puffer schreiben).

OpenGL bietet Ihnen zusätzliche Flexibilität bei Pixel Vorgängen. In der folgenden Tabelle werden die Iris GL-Funktionen für Pixel Vorgänge und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion                                   | OpenGL-Funktion                                                                           | Bedeutung                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **lrectread**, **rectread**, Read **RGB**<br/> | [**glread Pixels**](glreadpixels.md)                                                      | Liest einen Pixel Block aus dem Framebuffer.                           |
| **lrectwrite**, **rectwrite**                      | [**gldrawpixels**](gldrawpixels.md)                                                      | Schreibt einen Pixel Block in den Framebuffer.                            |
| **neu kopieren**                                       | [**glcopypixels**](glcopypixels.md)                                                      | Kopiert Pixel im Framebuffer.                                       |
| **rectzoom**                                       | [**glpixelzoom**](glpixelzoom.md)                                                        | Gibt die Pixel Zoomfaktoren für **gldrawpixels** und **glcopypixels** an. |
| **cmov**                                           | [glRasterPos](glrasterpos-functions.md)                                                  | Gibt die Raster Position für Pixel Vorgänge an.                         |
| **"lesen"**                                     | [**glread Buffer**](glreadbuffer.md)                                                      | Wählt eine Farb Puffer Quelle für Pixel aus.                               |
| **pixmode**                                        | [**glpixelstore**](glpixelstore-functions.md),[**glpixeltransfer**](glpixeltransfer.md) | Legt die Pixel Speicher Modi fest. Legen Sie Pixel Übertragungsmodi fest.                      |
| **logicop**                                        | [**gllogicop**](gllogicop.md)                                                            | Gibt eine logische Operation für Pixel Schreibvorgänge an.                         |
|                                                    | [**glEnable**](glenable.md) (GL \_ Logic \_ OP)                                            | Schaltet Pixel Logik Vorgänge ein.                                        |



 

Eine umfassende Liste der möglichen logischen Vorgänge finden Sie unter [**gllogicop**](gllogicop.md).

Dieses IRIS GL-Codebeispiel zeigt einen typischen Pixel Schreibvorgang:

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

Der vorangehende Code sieht wie folgt aus, wenn er in OpenGL übersetzt wird:

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





