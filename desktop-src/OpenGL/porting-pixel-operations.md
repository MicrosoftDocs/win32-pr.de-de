---
title: Portieren von Pixelvorgängen
description: Portieren von Pixelvorgängen
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- IRIS GL-Portierung, Pixel
- Portieren von IRIS GL,Pixel
- Portieren zu OpenGL von IRIS GL,Pixel
- OpenGL-Portierung von IRIS GL,Pixel
- Pixel, Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc67a4c9224dbe6544c60cb205f8a192517af7f3ab16ba64134b4d55d1c8676f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132379"
---
# <a name="porting-pixel-operations"></a>Portieren von Pixelvorgängen

Beachten Sie beim Portieren von Code, der Pixelvorgänge umfasst, die folgenden Punkte:

-   Logische Pixelvorgänge werden nicht auf RGBA-Farbpuffer angewendet. Weitere Informationen finden Sie unter [**glLogicOp**](gllogicop.md).
-   Im Allgemeinen verwendet IRIS GL das Format ABGR für Pixel, während OpenGL RGBA verwendet. Sie können das Format mit [**glPixelStore**](glpixelstore-functions.md)ändern.
-   Achten Sie beim Portieren von **lrectwrite-Funktionen** darauf, dass Sie beachten, wo **lrectwrite** schreibt (z. B. in den Tiefenpuffer schreiben).

OpenGL bietet Ihnen zusätzliche Flexibilität bei Pixelvorgängen. In der folgenden Tabelle sind die IRIS GL-Funktionen für Pixelvorgänge und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                                   | OpenGL-Funktion                                                                           | Bedeutung                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **lrectread**, **rectread**,**readRGB**<br/> | [**glReadPixels**](glreadpixels.md)                                                      | Liest einen Pixelblock aus dem Framepuffer.                           |
| **lrectwrite**, **rectwrite**                      | [**glDrawPixels**](gldrawpixels.md)                                                      | Schreibt einen Block von Pixeln in den Framepuffer.                            |
| **rectcopy**                                       | [**glCopyPixels**](glcopypixels.md)                                                      | Kopiert Pixel in den Framepuffer.                                       |
| **rectzoom**                                       | [**glPixelZoom**](glpixelzoom.md)                                                        | Gibt Pixelzoomfaktoren für **glDrawPixels** und **glCopyPixels an.** |
| **cmov**                                           | [glRasterPos](glrasterpos-functions.md)                                                  | Gibt die Rasterposition für Pixelvorgänge an.                         |
| **readsource**                                     | [**glReadBuffer**](glreadbuffer.md)                                                      | Wählt eine Farbpufferquelle für Pixel aus.                               |
| **pixmode**                                        | [**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md) | Legt die Pixelspeichermodi fest. Legen Sie die Pixelübertragungsmodi fest.                      |
| **logicop**                                        | [**glLogicOp**](gllogicop.md)                                                            | Gibt einen logischen Vorgang für Pixel-Schreibvorgänge an.                         |
|                                                    | [**glEnable**](glenable.md) ( GL \_ LOGIC \_ OP )                                            | Aktiviert Pixellogikvorgänge.                                        |



 

Eine vollständige Liste der möglichen logischen Vorgänge finden Sie unter [**glLogicOp**](gllogicop.md).

Dieses IRIS GL-Codebeispiel zeigt einen typischen Pixelschreibvorgang:

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

 

 





