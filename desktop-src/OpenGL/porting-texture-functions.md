---
title: Portieren von Texturfunktionen
description: Portieren von Texturfunktionen
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- IRIS GL-Portierung, Textur
- Portieren von IRIS GL, Textur
- Portieren von IRIS GL zu OpenGL, Textur
- OpenGL-Portierung aus IRIS GL,Textur
- Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17cd79aaf8e7e5b90d0f171ddcec4b49b6d15b3615ccc1f5e44a04b3e16fae9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339240"
---
# <a name="porting-texture-functions"></a>Portieren von Texturfunktionen

Beachten Sie beim Portieren von IRIS GL-Texturfunktionen zu OpenGL die folgenden Punkte:

-   OpenGL verwaltet keine Tabellen mit Texturen. Sie verwendet entweder eine 1D-Textur und nur eine 2D-Textur. Um die Texturen aus Ihrem IRIS GL-Code wiederzuverwenden, legen Sie sie in einer Anzeigeliste ab.
-   OpenGL generiert nicht automatisch Mipmaps. Wenn Sie mipmaps verwenden, müssen Sie zuerst die [**Funktion gluBuild2DMipmaps**](glubuild2dmipmaps.md) aufrufen.
-   In OpenGL verwenden Sie [**glEnable**](glenable.md) und [**glDisable,**](gldisable.md) um Texturfunktionen zu aktivieren und zu deaktivieren.
-   In OpenGL ist die Texturgröße strikter reguliert als in IRIS GL. Die Größe einer OpenGL-Textur muss wie die folgenden sein:

    2 *n* + 2 *b*

    Wobei *n* eine ganze Zahl und *b* ist:

    -   0, wenn die Textur keinen Rahmen hat
    -   1, wenn die Textur über ein Rahmenpixel verfügt (OpenGL-Texturen können 1-Pixel-Rahmen aufweisen.)

In der folgenden Tabelle sind die IRIS GL-Texturfunktionen und ihre allgemeinen OpenGL-Entsprechungen aufgeführt.



| IRIS GL-Funktion | OpenGL-Funktion                                                                                                                                                                                                                                                       | Bedeutung                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | Gibt ein 2D-Texturbild an.                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | Wählt eine Texturfunktion aus.                                                                 |
| **tevdef**       | [**glTexEnv**](gltexenv-functions.md)                                                                                                                                                                                                                                | Definiert eine Texturzuordnungsumgebung.                                                      |
| **tevbind**      | **glTexEnv**[**glTexImage1D**](glteximage1d.md)<br/>                                                                                                                                                                                                           | Wählt eine Texturumgebung aus.                                                              |
| **t2**           | [**glTexCoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | Legt die aktuellen Texturkoordinaten fest.                                                       |
| **texgen**       | [**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluScaleImage**](gluscaleimage.md)<br/> | Steuert die Generierung von Texturkoordinaten. Skaliert ein Bild auf eine beliebige Größe.<br/> |



 

Weitere Informationen zur Texturierung finden Sie im *OpenGL-Programmierhandbuch.*

Dieses Thema enthält Informationen zu folgenden Themen.

-   [Übersetzen von tevdef](translating-tevdef.md)
-   [Übersetzen von texdef](translating-texdef.md)
-   [Übersetzen von Texgen](translating-texgen.md)

 

 





