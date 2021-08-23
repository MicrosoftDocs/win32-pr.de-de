---
title: Portieren von Kürzungskurven
description: OpenGL-Trimmkurven ähneln den IRIS GL-Kürzungskurven sehr. In der folgenden Tabelle sind die IRIS GL-Funktionen zum Definieren von Kürzungskurven und deren äquivalente OpenGL-Funktionen aufgeführt.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- IRIS GL-Portierung, Kürzen von Kurven
- Portieren von IRIS GL,Kürzen von Kurven
- Portieren von IRIS GL zu OpenGL, Kürzen von Kurven
- OpenGL-Portierung von IRIS GL,Kürzen von Kurven
- Kürzen von Kurven
- Kurven
- IRIS GL-Portierung, Kurven
- Portieren von IRIS GL,Curves
- Portieren von IRIS GL,Curves zu OpenGL
- OpenGL-Portierung von IRIS GL,Curves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad544431adaa7f0b049341ec7314e3e53ae60752d633a48c760ca09334f79d33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553860"
---
# <a name="porting-trimming-curves"></a>Portieren von Kürzungskurven

OpenGL-Trimmkurven ähneln den IRIS GL-Kürzungskurven sehr. In der folgenden Tabelle sind die IRIS GL-Funktionen zum Definieren von Kürzungskurven und deren äquivalente OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion | OpenGL-Funktion                        | Bedeutung                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**gluBeginTrim**](glubegintrim.md)   | Beginnt die Trimmingkurvendefinition.    |
| **pwlcurve**     | [**gluPwlCurve**](glupwlcurve.md)     | Definiert eine stückweise lineare Kurve.    |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Gibt Trimmingkurvenattribute an. |
| **endtrim**      | [**gluEndTrim**](gluendtrim.md)       | Beendet die Trimmingkurvendefinition.      |



 

??

 

 




