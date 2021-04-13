---
title: Portieren von Arcs und Kreisen
description: Bei OpenGL werden gefüllte Bögen und Kreise mit denselben aufrufen wie nicht gefüllte Bögen und Kreise gezeichnet. In der folgenden Tabelle werden die Funktionen "IRIS GL Arc" und "Circle" und ihre entsprechenden OpenGL (GLU)-Funktionen aufgelistet.
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- IRIS GL portieren, Arcs
- Portieren von IRIS GL, Arcs
- Portieren auf OpenGL von IRIS GL, Arcs
- OpenGL-Portierung von IRIS GL, Arcs
- Zeichnungsfunktionen, Arcs
- IRIS GL portieren, Kreise
- Portieren von IRIS GL, Kreisen
- Portieren auf OpenGL von IRIS GL, Kreisen
- OpenGL-Portierung von IRIS GL, Kreisen
- Zeichnungsfunktionen, Kreise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388734"
---
# <a name="porting-arcs-and-circles"></a>Portieren von Arcs und Kreisen

Bei OpenGL werden gefüllte Bögen und Kreise mit denselben aufrufen wie nicht gefüllte Bögen und Kreise gezeichnet. In der folgenden Tabelle werden die Funktionen "IRIS GL Arc" und "Circle" und ihre entsprechenden OpenGL (GLU)-Funktionen aufgelistet.



| IRIS GL-Funktion | OpenGL-Funktion                          | Bedeutung                 |
|------------------|------------------------------------------|-------------------------|
| **arcarcf**      | [**glupartialdisk**](glupartialdisk.md) | Zeichnet einen Bogen.           |
| **circcircf**    | [**gludisk**](gludisk.md)               | Zeichnet einen Kreis oder einen Datenträger. |



 

Sie können einige Dinge mit OpenGL-Bögen und-Kreisen erledigen, die Sie mit Iris GL nicht tun können. OpenGL ruft Bögen und Kreise, Datenträger und partielle Datenträger auf.

Beachten Sie bei der Portierung von Bögen und Kreisen die folgenden Punkte über OpenGL:

-   Winkel werden in Grad und nicht in Zehntel Grad gemessen.
-   Der Start Winkel wird von der positiven y-Achse und nicht von der x-Achse gemessen.
-   Der Mittelpunktswinkel ist nun im Uhrzeigersinn statt gegen den Uhrzeigersinn.

??

 

 




