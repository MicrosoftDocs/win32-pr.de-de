---
title: Portieren von Matrix-und Transformations Funktionen
description: IRIS GL und OpenGL behandeln Matrizen und Transformationen auf ähnliche Weise.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- IRIS GL portieren, Matrizen
- Portieren von IRIS GL, Matrizen
- Portieren auf OpenGL von IRIS GL, Matrizen
- OpenGL-Portierung von IRIS GL, Matrizen
- Matrizen
- IRIS GL portieren, Transformationen
- Portieren von IRIS GL, Transformationen
- Portieren auf OpenGL von IRIS GL, Transformationen
- OpenGL-Portierung von IRIS GL, Transformationen
- Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310548"
---
# <a name="porting-matrix-and-transformation-functions"></a>Portieren von Matrix-und Transformations Funktionen

IRIS GL und OpenGL behandeln Matrizen und Transformationen auf ähnliche Weise. Beim Portieren von Code von IRIS GL sind jedoch mehrere Unterschiede zu beachten:

-   In OpenGL befinden Sie sich immer im Double-Matrix-Modus. Es gibt keinen Einzel Matrix Modus.
-   Winkel werden in Grad gemessen, anstelle von Zehntel Graden.
-   Projektions Matrix Aufrufe, wie z. b. [**glfrustum**](glfrustum.md) und [**glortho**](glortho.md), werden jetzt auf der aktuellen Matrix multipliziert, anstatt auf die aktuelle Matrix geladen zu werden.
-   Die OpenGL-Funktion " [**glrotation**](glrotate.md)" unterscheidet sich sehr von der **Drehung**. Sie können sich um jede beliebige Achse drehen, anstatt Sie auf die x-, y-und z-Achsen zu beschränken. Beispielsweise können Sie Folgendes übersetzen:

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    in:

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    Bei der Übersetzung von " **drehen** " in " **glrotation** " wechseln Sie zu Grad von Zehntel Graden, und ersetzen Sie "z" durch einen Vektor für die z-Achse.

-   OpenGL hat keine Entsprechung zur **Polar View** -Funktion. Sie können es problemlos durch eine Übersetzung und drei Umdrehungen ersetzen. Beispielsweise können Sie Folgendes übersetzen:

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

    

In der folgenden Tabelle werden die OpenGL-Matrix Funktionen und ihre entsprechenden IRIS GL-Funktionen aufgelistet.



| IRIS GL-Funktion              | OpenGL-Funktion                                                                        | Bedeutung                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MMode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | Legt den aktuellen Matrix Modus fest.                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | Ersetzt die aktuelle Matrix durch die Identitätsmatrix.                                                                                                                              |
| **loadmatrix**                | [**glloadmatrixf**](glloadmatrix.md),[**glloadmatrixd**](glloadmatrix.md)<br/> | Ersetzt die aktuelle Matrix durch die angegebene Matrix.                                                                                                                             |
| **multmatrix**                | [**glmultmatrixf**](glmultmatrix.md),[**glmultmatrixd**](glmultmatrix.md)<br/> | Nach dem Multiplizieren der aktuellen Matrix mit der angegebenen Matrix (Beachten Sie, dass **multmatrix** vorab multipliziert ist).                                                                            |
| **mapw**, **mapw2**           | [**"gluunproject"**](gluunproject.md)                                                   | Projiziert Raumkoordinaten in den Objekt Raum (siehe auch [**gluproject**](gluproject.md)).                                                                                  |
| **Ortho**                     | [**glortho**](glortho.md)                                                             | Multipliziert die aktuelle Matrix mit einer orthografischen Projektions Matrix.                                                                                                                |
| **ortho2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | Definiert eine zweidimensionale orthografische Projektions Matrix.                                                                                                                      |
| **Schau**               | [**gluperspective**](gluperspective.md)                                               | Definiert eine perspektivische Projektions Matrix.                                                                                                                                       |
| **picksize**                  | [**glupickmatrix**](glupickmatrix.md)                                                 | Definiert einen Auswahlbereich.                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | Holt den aktuellen Matrix Stapel und ersetzt dabei die aktuelle Matrix durch die darunter liegenden Matrix.                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | Überträgt den aktuellen Matrix Stapel um eins und duplizieren die aktuelle Matrix.                                                                                                       |
| **drehen**,**rot**<br/> | [**glrotgedreht**](glrotate.md),[**glrotatef**](glrotate.md)<br/>                 | Rotiert das aktuelle Koordinatensystem um den angegebenen Winkel um den Vektor vom Ursprung bis zum angegebenen Punkt. Beachten Sie, dass **Drehung** nur um die x-, y-und z-Achsen gedreht wurde. |
| **scale**                     | [](glscale.md)[**glScalef**](glscale.md)<br/>                     | Multipliziert die aktuelle Matrix mit einer Skalierungs Matrix.                                                                                                                                 |
| **Übersetzen**                 | [**glTranslatef**](gltranslate.md),[**glTranslatef**](gltranslate.md)<br/>     | Verschiebt den Ursprung des Koordinatensystems auf den angegebenen Punkt, indem die aktuelle Matrix mit einer Übersetzungs Matrix multipliziert wird.                                                              |
| **ster**                    | [**glfrustum**](glfrustum.md)                                                         | Bei angegebenen Koordinaten für das Abschneiden von Ebenen multipliziert die aktuelle Matrix mit einer Perspektiven Matrix.                                                                                  |



 

OpenGL verfügt über drei Matrix Modi, die mit [**glMatrixMode**](glmatrixmode.md)festgelegt werden. In der folgenden Tabelle werden die Modi aufgelistet, die als Parameter für **glMatrixMode** verfügbar sind.



| IRIS GL-Matrix Modus | OpenGL-Modus    | Bedeutung                                  | Minimale Stapel Tiefe |
|---------------------|----------------|------------------------------------------|-----------------|
| **Mtexture**        | GL- \_ Textur    | Arbeitet auf dem Textur Matrix Stapel.    | 2               |
| **MVIEW**        | GL \_ Modelview  | Wird im Modell Ansicht-Matrix Stapel betrieben. | 32              |
| **Mprojektion**     | GL- \_ Projektion | Arbeitet auf dem Projektions Matrix Stapel. | 2               |



 

 

 





