---
title: Portieren von Kürzungs Kurven
description: OpenGL-Kürzungs Kurven sind sehr ähnlich wie IRIS GL-Kürzungs Kurven. In der folgenden Tabelle sind die Iris GL-Funktionen zum Definieren von Kürzungs Kurven und ihre entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- IRIS GL portieren, Kürzungs Kurven
- Portieren von IRIS GL, kürzen von Kurven
- Portieren auf OpenGL von IRIS GL, kürzen von Kurven
- OpenGL-Portierung von IRIS GL, kürzen von Kurven
- Kürzen von Kurven
- Kurven
- IRIS GL portieren, Kurven
- Portieren von IRIS GL, Kurven
- Portieren auf OpenGL von IRIS GL, Kurven
- OpenGL-Portierung von IRIS GL, Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207148"
---
# <a name="porting-trimming-curves"></a>Portieren von Kürzungs Kurven

OpenGL-Kürzungs Kurven sind sehr ähnlich wie IRIS GL-Kürzungs Kurven. In der folgenden Tabelle sind die Iris GL-Funktionen zum Definieren von Kürzungs Kurven und ihre entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion | OpenGL-Funktion                        | Bedeutung                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**glubegintrim**](glubegintrim.md)   | Beginnt die Definition der Kürzungs Kurve.    |
| **pwlcurve**     | [**glupwlcurve**](glupwlcurve.md)     | Definiert eine schrittweise lineare Kurve.    |
| **nurbscurve**   | [**glunurbscurve**](glunurbscurve.md) | Gibt Attribute der Kürzungs Kurve an. |
| **endtrim**      | [**gluendtrim**](gluendtrim.md)       | Beendet die Definition der Kürzung der Kurve.      |



 

??

 

 




