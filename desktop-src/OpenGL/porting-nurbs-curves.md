---
title: Portieren von nursb-Kurven
description: Die OpenGL-Funktionen zum Zeichnen von nursb-Kurven sind den Iris GL-Funktionen sehr ähnlich. Sie geben die-und-Steuerungs Punkte mithilfe einer glunurbscurve-Funktion an, die in einem "glubegincurve/gluendcurve"-paar enthalten sein muss.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- IRIS GL portieren, nursb-Kurven
- Portieren von IRIS GL, nursb-Kurven
- Portieren auf OpenGL von IRIS GL, nursb-Kurven
- OpenGL-Portierung von IRIS GL, nursb-Kurven
- Nursb-Kurven
- Kurven
- IRIS GL portieren, Kurven
- Portieren von IRIS GL, Kurven
- Portieren auf OpenGL von IRIS GL, Kurven
- OpenGL-Portierung von IRIS GL, Kurven
- NURBS (Non-Uniform Rational B-Spline)
- Nicht einheitlicher rationaler B-Spline (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388485"
---
# <a name="porting-nurbs-curves"></a>Portieren von nursb-Kurven

Die OpenGL-Funktionen zum Zeichnen von nursb-Kurven sind den Iris GL-Funktionen sehr ähnlich. Sie geben die-und-Steuerungs Punkte mithilfe der Funktion " [**glunurbscurve**](glunurbscurve.md) " an, die in einem " [**glubegincurve**](glubegincurve.md)"-paar "  /  [**gluendcurve**](gluendcurve.md) " enthalten sein muss.

In der folgenden Tabelle sind die Iris GL-Funktionen zum Zeichnen von nursb-Kurven und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion | OpenGL-Funktion                        | Bedeutung                     |
|------------------|----------------------------------------|-----------------------------|
| **bgncurve**     | [**glubegincurve**](glubegincurve.md) | Beginnt eine Kurven Definition.  |
| **nurbscurve**   | [**glunurbscurve**](glunurbscurve.md) | Gibt Kurven Attribute an. |
| **endcurve**     | [**gluendcurve**](gluendcurve.md)     | Beendet eine Kurven Definition.    |



 

Ordnen Sie Positionen, Textur und Farbkoordinaten zu, indem Sie diese als separate **glunurbscurve** innerhalb des Begin/End-Paars darstellen. Sie können für jedes Farb-, Positions-und Textur Datenelement innerhalb eines einzelnen " **glubegincurve/gluendcurve"-** Paars nicht mehr als einen Aufrufen von " **glunurbscurve** " durchführen. Sie müssen genau einen-Befehl erstellen, um die Position der Kurve zu beschreiben (a GL \_ zuordnung1 \_ Vertex \_ 3 oder GL \_ zuordnung1 \_ Vertex \_ 4 Description). Wenn Sie " **gluendcurve**" aufgerufen haben, wird die Kurve in Liniensegmente und dann gerendert.

In der folgenden Tabelle sind die Kurven Typen IRIS GL und OpenGL nursb aufgeführt.



| IRIS GL-Typ | OpenGL-Typ                  | Bedeutung                                 |
|--------------|------------------------------|-----------------------------------------|
| N \_ v3d       | GL \_ zuordnung1 \_ Scheitelpunkt \_ 3          | Polynomial-Kurve.                       |
| N \_ V3DR      | GL \_ zuordnung1 \_ Scheitelpunkt \_ 4          | Rationelle Kurve.                         |
|              | GL \_ zuordnung1 \_ Textur \_ Koord\_\* | Kontrollpunkte sind Texturkoordinaten. |
|              | GL \_ zuordnung1 \_ Normal             | Kontrollpunkte sind normale.             |



 

Weitere Informationen zu verfügbaren evaluatortypen finden Sie unter [**glMap1**](glmap1.md).

??

 

 




