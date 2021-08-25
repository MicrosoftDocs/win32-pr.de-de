---
title: Rasterung
description: Rasterung ist der Prozess, mit dem ein Primitiver in ein zweidimensionales Bild konvertiert wird.
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- OpenGL-Verarbeitungspipeline, Rasterung
- Rastern von OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192f8fdd919c14be4bd47688abf911b363e13f2e8ca9606f1943eb2956378ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776880"
---
# <a name="rasterizing"></a>Rasterung

*Rasterung* ist der Prozess, mit dem ein Primitiver in ein zweidimensionales Bild konvertiert wird. Jeder Punkt dieses Bilds enthält Informationen wie Farb-, Tiefen- und Texturdaten. Ein Punkt und die zugehörigen Informationen werden als *Fragment* bezeichnet. Die aktuelle Rasterposition, wie mit [**glRasterPos \***](glrasterpos-functions.md)angegeben, wird während dieser Phase auf verschiedene Weise zum Zeichnen von Pixeln und Bitmaps verwendet. Beim Rastern von Punkten, Liniensegmenten und Polygonen treten unterschiedliche Probleme auf. Darüber hinaus müssen Pixelrechtecke und Bitmaps gerastert werden.

Mit OpenGL steuern Sie die Rasterung mithilfe der folgenden Funktionen:

-   Primitive. Steuern Sie die Rasterung von Primitiven mithilfe von Funktionen, die Dimensionen und Stipplemuster bestimmen: [**glPointSize**](glpointsize.md), [**glLineWidth**](gllinewidth.md), [**glLineStipple**](gllinestipple.md)und [**glPolygonStipple**](glpolygonstipple.md). Steuern Sie, wie die vorderen und hinteren Gesichter von Polygonen mit [**glCullFace,**](glcullface.md) [**glFrontFace**](glfrontface.md)und [**glPolygonMode**](glpolygonmode.md)gerastert werden.
-   Pixel. Mehrere Funktionen steuern den Speicher- und Übertragungsmodus von Pixeln. Die Funktion [ * *glPixelStore \** _](glpixelstore-functions.md) steuert die Codierung von Pixeln im Clientspeicher, und [_*glPixelTransfer \**_](glpixeltransfer.md) und [_*glPixelMap \**_](glpixelmap.md) steuern, wie Pixel verarbeitet werden, bevor sie im Framepuffer platziert werden. Geben Sie ein Pixelrechteck mit [_ *glDrawPixels an.* *](gldrawpixels.md)Steuern Sie dessen Rasterung mit [**glPixelZoom.**](glpixelzoom.md)
-   Bitmaps. Bitmaps sind Rechtecke mit Nullen und solche, die ein bestimmtes Muster von Fragmenten angeben, die erstellt werden sollen. Jedem dieser Fragmente sind die gleichen Daten zugeordnet. Die [**glBitmap-Funktion**](glbitmap.md) gibt eine Bitmap an.
-   Texturspeicher. Wenn die Texturierung aktiviert ist, ordnet die Texturierung jedem Primitiven einen Teil eines angegebenen Texturbilds zu. Diese Zuordnung erfolgt mithilfe der Farbe des Texturbilds an der Position, die durch die Texturkoordinaten eines Fragments angegeben wird, um die RGBA-Farbe des Fragments zu ändern. Geben Sie ein Texturbild mit [**glTexImage2D**](glteximage2d.md) oder [**glTexImage1D an.**](glteximage1d.md) Die Funktionen [ * *glTexParameter \** _](gltexparameter-functions.md) und _ [*glTexEnv \** *](gltexenv-functions.md) steuern, wie Texturwerte interpretiert und auf ein Fragment angewendet werden.
-   Nebel. Verwenden Sie einen Mischungsfaktor, der vom Abstand zwischen dem Augenpunkt und dem Fragment abhängt, um eine Farbtonfarbe mit der Farbe nach der Texturierung eines gerasterten Fragments zu kombinieren. Verwenden Sie [**glFog, \***](glfog.md) um die Farbfarbe und den Mischungsfaktor anzugeben.

 

 




