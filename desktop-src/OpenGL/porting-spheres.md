---
title: Portieren von Kugeln
description: 'Beachten Sie beim Portieren von Kugeln zu OpenGL die folgenden Punkte:'
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- IRIS GL-Portierung, Kugeln
- Portieren von IRIS GL,Spheres
- Portieren von IRIS GL,Spheres zu OpenGL
- OpenGL-Portierung von IRIS GL,Spheres
- Zeichnungsfunktionen,Kugeln
- Bereichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1e0666393e923767d342d215622e0ed58bfa7b1b620e045a0054b31918a7a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358309"
---
# <a name="porting-spheres"></a>Portieren von Kugeln

Beachten Sie beim Portieren von Kugeln zu OpenGL die folgenden Punkte:

-   Sie können nicht den Typ der Primitive steuern, die zum Zeichnen der Kugel verwendet werden. Sie können die Zeichnungsgenauigkeit auf andere Weise steuern: Verwenden Sie die Parameter slices und stacks. Slices sind Ungen; -Stapel sind latitudinal.
-   Kugeln werden am Ursprung zentriert gezeichnet. Anstatt den Speicherort wie bei der IRIS **GL-Sphdraw-Funktion** anzugeben, gehen Sie einem Aufruf der [**GLU-gluSphere-Funktion**](glusphere.md) mit einer Übersetzung voraus.
-   Die Sphere-Bibliothek ist für OpenGL noch nicht verfügbar.

In der folgenden Tabelle sind die IRIS GL-Funktionen zum Zeichnen von Kugeln und die entsprechenden GLU-Funktionen aufgeführt, sofern verfügbar.



| IRIS GL-Funktion | GLU-Funktion                                 | Bedeutung                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**gluNewQuadric**](glunewquadric.md)       | Erstellt ein neues Kugelobjekt.                  |
| **sphfree**      | [**gluDeleteQuadric**](gludeletequadric.md) | Löscht das Sphere-Objekt und den verwendeten freien Arbeitsspeicher.   |
| **sphdraw**      | [**gluSphere**](glusphere.md)               | Zeichnet eine Kugel.                               |
| **sphmode**      |                                              | Legt Kugelattribute fest.                       |
| **sphrotmatrix** |                                              | Steuert die Ausrichtung der Kugel.                  |
| **splknpolys**   |                                              | Gibt die Anzahl von Polygonen in der aktuellen Kugel zurück. |



 

??

 

 




