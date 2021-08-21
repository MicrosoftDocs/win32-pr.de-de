---
title: Portieren von NURBS-Kurven
description: Die OpenGL-Funktionen zum Zeichnen von NURBS-Kurven sind den IRIS GL-Funktionen sehr ähnlich. Sie geben Sequenzen und Kontrollpunkte mithilfe einer gluNurbsCurve-Funktion an, die in einem gluBeginCurve-/gluEndCurve-Paar enthalten sein muss.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- IRIS GL-Portierung, NURBS-Kurven
- Portieren von IRIS GL,NURBS-Kurven
- Portieren von IRIS GL,NURBS-Kurven zu OpenGL
- OpenGL-Portierung von IRIS GL,NURBS-Kurven
- NURBS-Kurven
- Kurven
- IRIS GL-Portierung, Kurven
- Portieren von IRIS GL,Kurven
- Portieren von IRIS GL,Curves zu OpenGL
- OpenGL-Portierung von IRIS GL,Curves
- NURBS (Non-Uniform Rational B-Spline)
- Non-Uniform Rational B-Spline (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9aa43bcc40c2b6a93eb5690abe4265f792a58a2520e579d536a08520ca4f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132399"
---
# <a name="porting-nurbs-curves"></a>Portieren von NURBS-Kurven

Die OpenGL-Funktionen zum Zeichnen von NURBS-Kurven sind den IRIS GL-Funktionen sehr ähnlich. Sie geben Mithilfe einer [**gluNurbsCurve-Funktion**](glunurbscurve.md) Sequenzen und Kontrollpunkte an, die in einem gluBeginCurve-gluEndCurve-Paar [](glubegincurve.md)  /  [**enthalten sein**](gluendcurve.md) müssen.

In der folgenden Tabelle sind die IRIS GL-Funktionen zum Zeichnen von NURBS-Kurven und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion | OpenGL-Funktion                        | Bedeutung                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**gluBeginCurve**](glubegincurve.md) | Beginnt eine Kurvendefinition.  |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Gibt Kurvenattribute an. |
| **endcurve**     | [**gluEndCurve**](gluendcurve.md)     | Beendet eine Kurvendefinition.    |



 

Ordnen Sie Positions-, Textur- und Farbkoordinaten zu, indem Sie sie als separate **gluNurbsCurve** innerhalb des Begin/End-Paars präsentieren. Sie können nicht mehr als einen Aufruf von **gluNurbsCurve** für jedes Farb-, Positions- und Texturdaten innerhalb eines einzelnen **gluBeginCurve/gluEndCurve-Paars** machen. Sie müssen genau einen Aufruf machen, um die Position der Kurve zu beschreiben (eine GL \_ MAP1 \_ VERTEX \_ 3- oder GL \_ MAP1 \_ VERTEX \_ 4-Beschreibung). Wenn Sie **gluEndCurve aufrufen,** wird die Kurve in Liniensegmente geesselt und dann gerendert.

In der folgenden Tabelle sind die IRIS GL- und OpenGL NURBS-Kurventypen aufgeführt.



| IRIS GL-Typ | OpenGL-Typ                  | Bedeutung                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ V3D       | GL \_ MAP1 \_ VERTEX \_ 3          | Polynomiale Kurve.                       |
| N \_ V3DR      | GL \_ MAP1 \_ VERTEX \_ 4          | Rationale Kurve.                         |
|              | GL \_ MAP1 \_ TEXTURE \_ COORD\_\* | Kontrollpunkte sind Texturkoordinaten. |
|              | GL \_ MAP1 \_ NORMAL             | Kontrollpunkte sind Normals.             |



 

Weitere Informationen zu verfügbaren Auswertungstypen finden Sie unter [**glMap1**](glmap1.md).

??

 

 




