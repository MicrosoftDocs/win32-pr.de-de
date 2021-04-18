---
title: Die Iris GL Sphere-Bibliothek
description: OpenGL unterstützt die Iris GL Sphere-Bibliothek nicht. Sie können Ihre Sphere-Bibliotheks Aufrufe durch viercs-Routinen aus der glu-Bibliothek ersetzen. Weitere Informationen zur glu-Bibliothek finden Sie im Open GL-Programmier Handbuch und im OpenGL Utility Library.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- IRIS GL Porting, Sphere Library
- Portieren von IRIS GL, Sphere Library
- Portieren auf OpenGL von IRIS GL, Sphere Library
- OpenGL-Portierung von IRIS GL, Sphere Library
- Zeichnungsfunktionen, Sphere-Bibliothek
- Sphere-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310360"
---
# <a name="the-iris-gl-sphere-library"></a>Die Iris GL Sphere-Bibliothek

OpenGL unterstützt die Iris GL Sphere-Bibliothek nicht. Sie können Ihre Sphere-Bibliotheks Aufrufe durch viercs-Routinen aus der glu-Bibliothek ersetzen. Weitere Informationen zur glu-Bibliothek finden Sie im *Open GL-Programmier Handbuch* und im [OpenGL Utility Library](opengl-utility-library.md).

In der folgenden Tabelle sind die OpenGL viercs-Funktionen aufgelistet.



| OpenGL-Funktion                                        | Bedeutung                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [**glunewquadric**](glunewquadric.md)                 | Erstellt ein neues Quadric-Objekt.                                    |
| [**gludeletequadric**](gludeletequadric.md)           | Löscht ein Quadric-Objekt.                                        |
| [*gluvierccallback*](gluquadric.md)                 | Ordnet einen Rückruf einem quadrischen Objekt zu, um die Fehlerbehandlung zu beheben. |
| [**gluquadricnormals**](gluquadricnormals.md)         | Gibt normale an: keine normale, eine pro Gesicht oder eine pro Scheitelpunkt.  |
| [**gluquadricorientation**](gluquadricorientation.md) | Gibt die Richtung von normalen an: nach außen oder nach innen.               |
| [**gluquadrictexture**](gluquadrictexture.md)         | Wandelt die Generierung der Textur Koordinate ein bzw. aus.                   |
| [**gluquadricdrawstyle**](gluquadricdrawstyle.md)     | Gibt die Zeichnungsart an: Polygone, Linien, Punkte usw.     |
| [**glusphere**](glusphere.md)                         | Zeichnet eine Kugel.                                                  |
| [**gluzylinder**](glucylinder.md)                     | Zeichnet einen Zylinder oder Kegel.                                        |
| [**glupartialdisk**](glupartialdisk.md)               | Zeichnet einen Bogen.                                                    |
| [**gludisk**](gludisk.md)                             | Zeichnet einen Kreis oder einen Datenträger.                                          |



 

Sie können ein Quadric-Objekt für alle viercs verwenden, die Sie auf ähnliche Weise darstellen möchten. Im folgenden Codebeispiel werden zwei Quadric-Objekte zum Zeichnen von vier vierfachen verwendet, von denen zwei als texturiert wurden.


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




