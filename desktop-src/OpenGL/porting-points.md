---
title: Portieren von Punkten
description: OpenGL verfügt über keinen Befehl zum Zeichnen eines einzelnen Punkts. Andernfalls ist das Portieren von Punktfunktionen einfach. In der folgenden Tabelle sind IRIS GL-Funktionen für Zeichnungspunkte und die entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- IRIS GL-Portierung, Punkte
- Portieren von IRIS GL,Points
- Portieren von IRIS GL zu OpenGL,Punkte
- OpenGL-Portierung von IRIS GL,Points
- Zeichnungsfunktionen,Punkte
- Punkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ef24ad81942681b3d70a303a22e89e9573aa609d3f08f52a92583ae88e0e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012068"
---
# <a name="porting-points"></a>Portieren von Punkten

OpenGL verfügt über keinen Befehl zum Zeichnen eines einzelnen Punkts. Andernfalls ist das Portieren von Punktfunktionen einfach. In der folgenden Tabelle sind IRIS GL-Funktionen für Zeichnungspunkte und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion           | OpenGL-Funktion                                                   | Bedeutung                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pnt**                    |                                                                   | Zeichnet einen einzelnen Punkt.                                                                                                                                |
| **bgnpoint,** **endpoint** | [**glBegin**](glbegin.md) ( GL \_ POINTS ), [ **glEnd**](glend.md) | Interpretiert Scheitelpunkte als Punkte.                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | Legt die Punktgröße in Pixel fest.                                                                                                                           |
| **pntsmooth**              | [**glEnable**](glenable.md) ( GL \_ POINT \_ SMOOTH )                | Aktiviert Punkt-Antialiasing. (Weitere Informationen zum Antialiasing von Punkt finden Sie unter [Portieren von Antialiasingfunktionen](porting-antialiasing-functions.md).) |



 

Informationen zu verwandten get-Funktionen finden Sie [**unter glPointSize**](glpointsize.md).

??

 

 




