---
title: Rasterungs
description: Die rasterierung ist der Prozess, durch den ein primitiver in ein zweidimensionales Bild konvertiert wird.
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- OpenGL-Verarbeitungs Pipeline, rasterisierungspipeline
- rasterisierung von OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0d8e7ece3bead408b8d056356593879edc638c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515644"
---
# <a name="rasterizing"></a>Rasterungs

Die *rasterierung* ist der Prozess, durch den ein primitiver in ein zweidimensionales Bild konvertiert wird. Jeder Punkt dieses Bilds enthält Informationen wie Farbe, Tiefe und Textur Daten. Ein Punkt und die zugehörigen Informationen werden als *Fragment* bezeichnet. Die aktuelle Raster Position, wie in [**glRasterPos \***](glrasterpos-functions.md)angegeben, wird in dieser Phase auf verschiedene Weise für das Zeichnen von Pixeln und Bitmaps verwendet. Beim Rasterisieren von Punkten, Liniensegmenten und Polygonen treten verschiedene Probleme auf. Außerdem müssen Pixel Rechtecke und Bitmaps rasterisiert werden.

Mit OpenGL steuern Sie die rasterisierung mithilfe der folgenden Funktionen:

-   Primitives. Steuern der Art und Weise, wie primitive mithilfe von Funktionen, die Dimensionen und Stippel Muster bestimmen, gerengt werden: [**glPointSize**](glpointsize.md), [**glLineWidth**](gllinewidth.md), [**glLineStipple**](gllinestipple.md)und [**glpolygonstippel**](glpolygonstipple.md). Steuern Sie, wie die Vorder-und Hintergrund Gesichter von Polygonen mit [**glcullface**](glcullface.md), [**glfrontface**](glfrontface.md)und [**glpolygonmode**](glpolygonmode.md)gerengt werden.
-   Pixel. Mehrere Funktionen steuern Pixel Speicher und Übertragungsmodi. Die Funktion " [**glpixelstore \***](glpixelstore-functions.md) " steuert die Codierung von Pixeln im Client Speicher, und [**glpixeltransfer \***](glpixeltransfer.md) und [**glpixelmap \***](glpixelmap.md) steuern, wie Pixel verarbeitet werden, bevor Sie im Framebuffer abgelegt werden. Angeben eines Pixel Rechtecks mit " [**gldrawpixels**](gldrawpixels.md);" Steuern Sie die rasterisierung mit [**glpixelzoom**](glpixelzoom.md).
-   Bitmaps. Bitmaps sind Rechtecke von Nullen und eine, die ein bestimmtes Muster von Fragmenten angeben, die erstellt werden sollen. Jedes dieser Fragmente verfügt über dieselben zugeordneten Daten. Die Funktion " [**glbitmap**](glbitmap.md) " gibt eine Bitmap an.
-   Texturspeicher. Wenn die Texturierung aktiviert ist, ordnet Texturing einem primitiven einen Teil eines angegebenen Textur Bilds zu. Diese Zuordnung wird erreicht, indem die Farbe des Textur Bilds an der Position verwendet wird, die durch die Texturkoordinaten eines Fragments angegeben wird, um die RGBA-Farbe des Fragments zu ändern. Geben Sie ein Textur Bild mit [**glTexImage2D**](glteximage2d.md) oder [**glTexImage1D**](glteximage1d.md)an. Die Funktionen [**gltexparameter \***](gltexparameter-functions.md) und [**gltexenv \***](gltexenv-functions.md) steuern, wie Textur Werte interpretiert und auf ein Fragment angewendet werden.
-   Neben. Verwenden Sie einen Mischungs Faktor, der von der Entfernung zwischen dem-und dem-Fragment abhängig ist, um eine Nebelfarbe mit der Post-texturierungsfarbe eines rasterisierten Fragments zu kombinieren. Verwenden Sie [**glnebel \***](glfog.md) , um die Nebelfarbe und den Mischungs Faktor anzugeben.

 

 




