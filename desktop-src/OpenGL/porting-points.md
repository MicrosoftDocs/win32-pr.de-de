---
title: Portieren von Punkten
description: OpenGL hat keinen Befehl zum Zeichnen eines einzelnen Punkts. Andernfalls ist das Portieren von Punkt Funktionen einfach. In der folgenden Tabelle sind die Funktionen von IRIS GL für Zeichnungs Punkte und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- IRIS GL portieren, Punkte
- Portieren von IRIS GL, Points
- Portieren auf OpenGL von IRIS GL, Points
- OpenGL-Portierung von IRIS GL, Points
- Zeichnungsfunktionen, Punkte
- Punkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338602"
---
# <a name="porting-points"></a>Portieren von Punkten

OpenGL hat keinen Befehl zum Zeichnen eines einzelnen Punkts. Andernfalls ist das Portieren von Punkt Funktionen einfach. In der folgenden Tabelle sind die Funktionen von IRIS GL für Zeichnungs Punkte und ihre entsprechenden OpenGL-Funktionen aufgelistet.



| IRIS GL-Funktion           | OpenGL-Funktion                                                   | Bedeutung                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pnt**                    |                                                                   | Zeichnet einen einzelnen Punkt.                                                                                                                                |
| **bgnpoint**, **Endpunkt** | [**glBegin**](glbegin.md) (GL- \_ Punkte), [ **glEnd**](glend.md) | Interpretiert Scheitel Punkte als Punkte.                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | Legt die Punktgröße in Pixel fest.                                                                                                                           |
| **PNP**              | [**glEnable**](glenable.md) (GL- \_ Punkt \_ glatt)                | Schaltet das Antialiasing von Punkten um. (Weitere Informationen zum Punkt-Antialiasing finden Sie unter [Portieren von Antialiasing-Funktionen](porting-antialiasing-functions.md).) |



 

Weitere Informationen zu verwandten Get-Funktionen finden Sie unter [**glPointSize**](glpointsize.md).

??

 

 




