---
title: Portieren von Textur Funktionen
description: Portieren von Textur Funktionen
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- IRIS GL portieren, Textur
- Portieren von IRIS GL, Textur
- Portieren auf OpenGL von IRIS GL, Texture
- OpenGL-Portierung von IRIS GL, Textur
- Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037188"
---
# <a name="porting-texture-functions"></a>Portieren von Textur Funktionen

Beachten Sie beim Portieren von IRIS GL-Textur Funktionen in OpenGL die folgenden Punkte:

-   OpenGL verwaltet keine Tabellen mit Texturen. Sie verwendet entweder eine 1-d-Textur und eine 2D-Textur. Um die Texturen aus dem IRIS GL-Code wiederzuverwenden, platzieren Sie Sie in einer Anzeigeliste.
-   OpenGL generiert nicht automatisch Mipmaps. Wenn Sie Mipmaps verwenden, müssen Sie zuerst die [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) -Funktion aufzurufen.
-   In OpenGL verwenden Sie [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md) , um die Funktionen für die Texturierung zu aktivieren und zu deaktivieren.
-   In OpenGL ist die Textur Größe strenger geregelt als in IRIS GL. Die Größe einer OpenGL-Textur muss wie folgt lauten:

    2 *n* + 2 *b*

    Dabei ist *n* eine ganze Zahl, und *b* ist:

    -   0, wenn die Textur keinen Rahmen hat.
    -   1, wenn die Textur einen Rahmen Pixel aufweist (OpenGL-Texturen können 1-Pixel-Rahmen aufweisen).

In der folgenden Tabelle werden die Textur Funktionen von IRIS GL und ihre allgemeinen OpenGL-Entsprechungen aufgelistet.



| IRIS GL-Funktion | OpenGL-Funktion                                                                                                                                                                                                                                                       | Bedeutung                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [**glTexImage2D**](glteximage2d.md)[**gltexparameter**](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | Gibt ein 2D-Textur Bild an.                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | Wählt eine Textur Funktion aus.                                                                 |
| **tevdef**       | [**gltexd**](gltexenv-functions.md)                                                                                                                                                                                                                                | Definiert eine Textur Mapping-Umgebung.                                                      |
| **tevbind**      | **gltexd**[**glTexImage1D**](glteximage1d.md)<br/>                                                                                                                                                                                                           | Wählt eine Textur Umgebung aus.                                                              |
| **T2**           | [**gltexcoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | Legt die aktuellen Texturkoordinaten fest.                                                       |
| **TEXGEN**       | [**gltexgen**](gltexgen-functions.md)[**glgettexparameter**](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluscaleimage**](gluscaleimage.md)<br/> | Steuert die Generierung von Texturkoordinaten. Skaliert ein Bild auf eine beliebige Größe.<br/> |



 

Weitere Informationen zum Texturierung finden Sie im *OpenGL-Programmier Handbuch*.

Dieses Thema enthält Informationen zu den folgenden Themen.

-   [Übersetzen von tevdef](translating-tevdef.md)
-   [Übersetzen von texdef](translating-texdef.md)
-   [Übersetzen von TEXGEN](translating-texgen.md)

 

 





