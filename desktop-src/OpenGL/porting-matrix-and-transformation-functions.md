---
title: Portieren von Matrix- und Transformationsfunktionen
description: IRIS GL und OpenGL behandeln Matrizen und Transformationen auf ähnliche Weise.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- IRIS GL-Portierung, Matrizen
- Portieren von IRIS GL,Matrizen
- Portieren von IRIS GL,Matrizen zu OpenGL
- OpenGL-Portierung von IRIS GL,Matrizen
- Matrizen
- IRIS GL-Portierung, Transformationen
- Portieren von IRIS GL,Transformationen
- Portieren von IRIS GL,Transformationen zu OpenGL
- OpenGL-Portierung von IRIS GL,Transformationen
- Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e2dc0ed6b53f3a2ee5ef5310369b734a58cba27481b8b478eef63fdfe5722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132602"
---
# <a name="porting-matrix-and-transformation-functions"></a>Portieren von Matrix- und Transformationsfunktionen

IRIS GL und OpenGL behandeln Matrizen und Transformationen auf ähnliche Weise. Es gibt jedoch mehrere Unterschiede, die beim Portieren von Code aus IRIS GL zu beachten sind:

-   In OpenGL befinden Sie sich immer im Doppelmatrixmodus. es gibt keinen Einzelmatrixmodus.
-   Winkel werden in Grad statt zehn Grad gemessen.
-   Projektionsmatrixaufrufe wie [**glFrustum**](glfrustum.md) und [**glOrtho**](glortho.md)multiplizieren sich jetzt auf die aktuelle Matrix, anstatt in die aktuelle Matrix geladen zu werden.
-   Die OpenGL-Funktion [**glRotate**](glrotate.md)ist sehr anders als **die Rotieren von**. Sie können um jede beliebige Achse drehen, anstatt auf die x-, y- und z-Achse beschränkt zu sein. Beispielsweise können Sie Folgendes übersetzen:

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    in:

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    Wenn Sie von **"rotate"** in **"glRotate"** übersetzen, wechseln Sie von Zehntel grad zu Grad und ersetzen "z" durch einen Vektor für die Z-Achse.

-   OpenGL hat kein Äquivalent zur **Polarview-Funktion.** Sie können ihn problemlos durch eine Übersetzung und drei Drehungen ersetzen. Beispielsweise können Sie Folgendes übersetzen:

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    in:

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

In der folgenden Tabelle sind die OpenGL-Matrixfunktionen und die entsprechenden IRIS GL-Funktionen aufgeführt.



| IRIS GL-Funktion              | OpenGL-Funktion                                                                        | Bedeutung                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **mmode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | Legt den aktuellen Matrixmodus fest.                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | Ersetzt die aktuelle Matrix durch die Identitätsmatrix.                                                                                                                              |
| **loadmatrix**                | [**glLoadMatrixf,**](glloadmatrix.md)[**glLoadMatrixd**](glloadmatrix.md)<br/> | Ersetzt die aktuelle Matrix durch die angegebene Matrix.                                                                                                                             |
| **multmatrix**                | [**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)<br/> | Post-multipliziert die aktuelle Matrix mit der angegebenen Matrix (beachten Sie, **dass multmatrix** vorab multipliziert ist).                                                                            |
| **mapw,** **mapw2**           | [**gluUnProject**](gluunproject.md)                                                   | Projiziert Weltraumkoordinaten in den Objektraum (siehe auch [**gluProject**](gluproject.md)).                                                                                  |
| **Ortho**                     | [**glOrtho**](glortho.md)                                                             | Multipliziert die aktuelle Matrix mit einer orthografischen Projektionsmatrix.                                                                                                                |
| **ortho2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | Definiert eine zweidimensionale orthografische Projektionsmatrix.                                                                                                                      |
| **Perspektive**               | [**gluPerspective**](gluperspective.md)                                               | Definiert eine Perspektivische Projektionsmatrix.                                                                                                                                       |
| **picksize**                  | [**gluPickMatrix**](glupickmatrix.md)                                                 | Definiert einen Auswahlbereich.                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | Popt den aktuellen Matrixstapel und ersetzt die aktuelle Matrix durch die darunter.                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | Pusht den aktuellen Matrixstapel um eins nach unten und dupliziert die aktuelle Matrix.                                                                                                       |
| **rotieren,****rotieren**<br/> | [**glRotated,**](glrotate.md)[**glRotatef**](glrotate.md)<br/>                 | Dreht das aktuelle Koordinatensystem um den angegebenen Winkel um den Vektor vom Ursprung bis zum angegebenen Punkt. Beachten **Sie, dass die Drehung** nur um die x-, y- und z-Achse gedreht wurde. |
| **scale**                     | [**glScaled,**](glscale.md)[**glScalef**](glscale.md)<br/>                     | Multipliziert die aktuelle Matrix mit einer Skalierungsmatrix.                                                                                                                                 |
| **Übersetzen**                 | [**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)<br/>     | Verschiebt den Ursprung des Koordinatensystems an den angegebenen Punkt, indem die aktuelle Matrix mit einer Übersetzungsmatrix multipliziert wird.                                                              |
| **Fenster**                    | [**glFrustum**](glfrustum.md)                                                         | Bei angegebenen Koordinaten für Clippingebenen multipliziert die aktuelle Matrix mit einer Perspektivmatrix.                                                                                  |



 

OpenGL verfügt über drei Matrixmodi, die mit [**glMatrixMode festgelegt werden.**](glmatrixmode.md) In der folgenden Tabelle sind die Modi aufgeführt, die als Parameter für **glMatrixMode verfügbar sind.**



| IRIS GL-Matrixmodus | OpenGL-Modus    | Bedeutung                                  | Mindeststapeltiefe |
|---------------------|----------------|------------------------------------------|-----------------|
| **MTEXTURE**        | GL \_ TEXTURE    | Wird auf dem Texturmatrixstapel verwendet.    | 2               |
| **MVIEWING**        | GL \_ MODELVIEW  | Wird auf dem Matrixstapel der Modellansicht verwendet. | 32              |
| **MPROJECTION**     | \_GL-PROJEKTION | Wird auf dem Projektionsmatrixstapel verwendet. | 2               |



 

 

 





