---
title: Portieren von Clippingebenen
description: OpenGL implementiert clippingplane ähnlich wie IRIS GL. Außerdem können Sie in OpenGL Clippingebenen Abfragen. In der folgenden Tabelle sind die Funktionen von IRIS GL Clipping Plane und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- IRIS GL portieren, Clipping-Ebenen
- Portieren von IRIS GL, Clipping-Ebenen
- Portieren auf OpenGL von IRIS GL, Clipping-Ebenen
- OpenGL-Portierung von IRIS GL, Clipping-Ebenen
- Clipping-Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713583"
---
# <a name="porting-clipping-planes"></a>Portieren von Clippingebenen

OpenGL implementiert clippingplane ähnlich wie IRIS GL. Außerdem können Sie in OpenGL Clippingebenen Abfragen. In der folgenden Tabelle sind die Funktionen von IRIS GL Clipping Plane und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion                          | OpenGL-Funktion                                                                               | Bedeutung                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| **clipplane** (i, **CP \_ on**, Parametern)     | [**glEnable**](glenable.md) (GL- \_ Clip \_ planei)                                             | Aktiviert Clipping auf Ebene i.             |
| **clipplane**(i, **CP \_ define**, Plane) | [**glclipplane**](glclipplane.md) (GL- \_ Clip \_ planei, Plane)                                | Definiert die Clippingebene.                  |
|                                           | [**glgetclipplane**](glgetclipplane.md)                                                      | Gibt die Gleichung der Clipping-Ebene zurück.         |
|                                           | [**glisenabled**](glisenabled.md) (GL- \_ Clip \_ planei)                                       | Gibt true zurück, wenn Clip Plane i aktiviert ist. |
| **scrmask**                               | [**glscissor**](glscissor.md)                                                                | Definiert das Feld "Scheren".                 |
| **getscrmask**                            | [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (Feld "GL \_ Scissor" \_ ) | Gibt das aktuelle Scheren Feld zurück.         |



 

Um den Scheren Test zu aktivieren, nennen Sie " **glEnable** " mithilfe von "GL \_ Scheren \_ Box" als Parameter.

??

 

 




