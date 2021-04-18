---
title: Eingabedaten
description: Die OpenGL-Pipeline erfordert, dass Sie mehrere Datentypen eingeben.
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- OpenGL-Verarbeitungs Pipeline, Eingabedaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337569"
---
# <a name="input-data"></a>Eingabedaten

Die OpenGL-Pipeline erfordert, dass Sie mehrere Datentypen eingeben:

-   **Vertices**. Vertices beschreiben die Form des gewünschten geometrischen Objekts. Um Vertices anzugeben, verwenden Sie die [**glVertex \***](glvertex-functions.md) -Funktionen in Verbindung mit [**glBegin**](glbegin.md) und [**glEnd**](glend.md) , um einen Punkt, eine Linie oder ein Polygon zu erstellen. Sie können auch [**glrect**](glrect-functions.md) verwenden, um ein gesamtes Rechteck gleichzeitig zu beschreiben.
-   **Edge-Flag**. Standardmäßig sind alle Ränder von Polygonen Begrenzungs Kanten. Verwenden Sie [**gledgeflag \***](gledgeflag-functions.md) , um das Edge-Flag explizit festzulegen.
-   **Aktuelle Raster Position**. Mit [**glRasterPos \***](glrasterpos-functions.md)angegeben, wird die aktuelle Raster Position verwendet, um Raster Koordinaten für Pixel-und Bitmap-Zeichnungsvorgänge zu bestimmen.
-   **Aktuelle normal**. Ein normaler Vektor, der einem bestimmten Scheitelpunkt zugeordnet ist, bestimmt, wie eine Oberfläche an diesem Scheitelpunkt im dreidimensionalen Raum ausgerichtet wird. Dies wirkt sich wiederum darauf aus, wie viel Licht der jeweilige Scheitelpunkt empfängt. Verwenden Sie [**glnormal \***](glnormal-functions.md) , um einen normalen Vektor anzugeben.
-   **Aktuelle Farbe**. Die Farbe eines Scheitel Punkts und die Beleuchtungsbedingungen bestimmen die endgültige, Leuchtende Farbe. Die Farbe wird mit " [**glcolor \***](glcolor-functions.md) " angegeben, wenn im RGBA-Modus angegeben ist, oder mit " [**glindex \***](glindex-functions.md) ", wenn im Farb Index Modus
-   **Aktuelle Texturkoordinaten**. Mit " [**gltexcoord \***](gltexcoord-functions.md)" angegeben, bestimmen Texturkoordinaten die Position in einer Textur Zuordnung, die einem Scheitelpunkt eines Objekts zugeordnet werden soll.

> [!Note]  
> Wenn " **glVertex \*** " aufgerufen wird, erbt der resultierende Scheitelpunkt die aktuellen Edge-Flag-, normal-, Farb-und Texturkoordinaten. Daher muss " **gledgeflag \***", " **glnormal \***", " **glcolor \***" und " **gltexcoord \*** " vor " **glVertex \***" aufgerufen werden, wenn Sie sich auf den resultierenden Scheitelpunkt auswirken.

 

 

 




