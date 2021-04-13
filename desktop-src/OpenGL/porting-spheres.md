---
title: Portieren von Bereichen
description: 'Beachten Sie bei der Portierung von Bereichen zu OpenGL die folgenden Punkte:'
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- IRIS GL portieren, Bereiche
- Portieren von IRIS GL, Sphären
- Portieren auf OpenGL von IRIS GL, Sphären
- OpenGL-Portierung von IRIS GL, Sphären
- Zeichnungsfunktionen, Bereiche
- Mikro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388480"
---
# <a name="porting-spheres"></a>Portieren von Bereichen

Beachten Sie beim Portieren von Bereichen zu OpenGL die folgenden Punkte:

-   Der Typ der zum Zeichnen der Kugel verwendeten primitiven kann nicht gesteuert werden. Sie können die zeichengenauigkeit auf eine andere Weise steuern: Verwenden Sie die Slices und Stapel Parameter. Slices sind länglicher. Stapel sind "latitudini".
-   Bereiche werden am Ursprung zentriert gezeichnet. Anstatt den Speicherort anzugeben, führen Sie wie bei der Iris GL **sphdraw** -Funktion einen aufzurufenden Befehl an die Funktion "glu [**glusphere**](glusphere.md) " mit einer Übersetzung aus.
-   Die Sphere-Bibliothek ist für OpenGL noch nicht verfügbar.

In der folgenden Tabelle sind die Iris GL-Funktionen für Zeichnungs Sphären und ihre entsprechenden glu-Funktionen aufgeführt, sofern verfügbar.



| IRIS GL-Funktion | Glu-Funktion                                 | Bedeutung                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| **sphobj**       | [**glunewquadric**](glunewquadric.md)       | Erstellt ein neues Sphere-Objekt.                  |
| **sphfree**      | [**gludeletequadric**](gludeletequadric.md) | Löscht das kugelobjekt und den verwendeten freien Arbeitsspeicher.   |
| **sphdraw**      | [**glusphere**](glusphere.md)               | Zeichnet eine Kugel.                               |
| **sphmode**      |                                              | Legt Sphere-Attribute fest.                       |
| **sphrotmatrix** |                                              | Steuert die Kugel Ausrichtung.                  |
| **sphgnpolys**   |                                              | Gibt die Anzahl von Polygonen in der aktuellen Kugel zurück. |



 

??

 

 




