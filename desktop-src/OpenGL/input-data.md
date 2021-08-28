---
title: Eingabedaten
description: Für die OpenGL-Pipeline müssen Sie verschiedene Arten von Daten eingeben.
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- OpenGL-Verarbeitungspipeline, Eingabedaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a588e60991ad068653890659e236f8a7a96e62cad524b13ea72bfd38fb5bba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937427"
---
# <a name="input-data"></a>Eingabedaten

Für die OpenGL-Pipeline müssen Sie verschiedene Arten von Daten eingeben:

-   **Vertices**. Scheitelpunkte beschreiben die Form des gewünschten geometrischen Objekts. Verwenden Sie zum Angeben von Scheitelpunkten [ * *glVertex \** _-Funktionen](glvertex-functions.md) in Verbindung mit [_ *glBegin* *](glbegin.md) und [**glEnd,**](glend.md) um einen Punkt, eine Linie oder ein Polygon zu erstellen. Sie können [**glRect**](glrect-functions.md) auch verwenden, um ein gesamtes Rechteck gleichzeitig zu beschreiben.
-   **Edgeflag**. Standardmäßig sind alle Kanten von Polygonen Begrenzungsränder. Verwenden Sie [**glEdgeFlag, \***](gledgeflag-functions.md) um das Edgeflag explizit festzulegen.
-   **Aktuelle Rasterposition.** Mit [**glRasterPos \***](glrasterpos-functions.md)angegeben, wird die aktuelle Rasterposition verwendet, um Rasterkoordinaten für Pixel- und Bitmapzeichnungsvorgänge zu bestimmen.
-   **Der aktuelle normale**. Ein normaler Vektor, der einem bestimmten Scheitelpunkt zugeordnet ist, bestimmt, wie eine Oberfläche an diesem Scheitelpunkt im dreidimensionalen Raum ausgerichtet ist. dies wiederum wirkt sich darauf aus, wie viel Licht ein bestimmter Scheitelpunkt empfängt. Verwenden Sie [**glNormal, \***](glnormal-functions.md) um einen normalen Vektor anzugeben.
-   **Aktuelle Farbe**. Die Farbe eines Scheitelpunkts sowie die Beleuchtungsbedingungen bestimmen die endgültige, helle Farbe. Die Farbe wird mit [ * *glColor \** _](glcolor-functions.md) im RGBA-Modus oder mit _ [*glIndex \** *](glindex-functions.md) im Farbindexmodus angegeben.
-   **Aktuelle Texturkoordinaten.** Mit [**glTexCoord \***](gltexcoord-functions.md)angegeben, bestimmen Texturkoordinaten die Position in einer Texturkarte, die einem Scheitelpunkt eines Objekts zugeordnet werden soll.

> [!Note]  
> Wenn **glVertex \* *_ aufgerufen wird, erbt der resultierende Scheitelpunkt das aktuelle Randflag, die normale, die Farbe und die Texturkoordinaten. Daher* müssen _ glEdgeFlag \* *_, _* glNormal \* *_, _* glColor \* *_, und _* glTexCoord _ vor _ \* glVertex \* *aufgerufen werden,*** wenn sie sich auf den resultierenden Scheitelpunkt auswirken sollen.

 

 

 




