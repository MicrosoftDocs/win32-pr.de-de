---
title: Portieren von Linien
description: Das Portieren von IRIS GL-Code, der Linien zeichnet, ist recht einfach. Beachten Sie jedoch die Unterschiede in der Art und Weise, wie OpenGL-Ausschnitte verwendet werden. In der folgenden Tabelle sind IRIS GL-Funktionen zum Zeichnen von Linien und die entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- IRIS GL-Portierung, Zeilen
- Portieren von IRIS GL,Lines
- Portieren von IRIS GL,Lines zu OpenGL
- OpenGL-Portierung von IRIS GL,Lines
- Zeichnungsfunktionen, Linien
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b0dd0e254380e65171acef1a536038532a370da85ffaa361e8555f77457424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776960"
---
# <a name="porting-lines"></a>Portieren von Linien

Das Portieren von IRIS GL-Code, der Linien zeichnet, ist recht einfach. Beachten Sie jedoch die Unterschiede in der Art und Weise, wie OpenGL-Ausschnitte verwendet werden. In der folgenden Tabelle sind IRIS GL-Funktionen zum Zeichnen von Linien und die entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                               | OpenGL-Funktion                                                                                         | Bedeutung                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **bgnclosedline**,**endclosedline**<br/> | [**glBegin**](glbegin.md) ( GL \_ LINE LOOP ) \_ [**glEnd**](glend.md)<br/>                          | Zeichnet eine geschlossene Linie.                                                                                                                         |
| **bgnline**                                    | [**glBegin**](glbegin.md) ( GL \_ LINE \_ STRIP )                                                          | Zeichnet Liniensegmente.                                                                                                                         |
| **linewidth**                                  | [**glLineWidth**](gllinewidth.md)                                                                      | Legt die Linienbreite fest.                                                                                                                             |
| **getlwidth**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ WIDTH )            | Gibt die aktuelle Linienbreite zurück.                                                                                                                  |
| **deflinestyle**,**setlinestyle**<br/>   | [**glLineStipple**](gllinestipple.md)                                                                  | Gibt ein Zeilenausschnittmuster an.                                                                                                            |
| **lsrepeat**                                   | factor-Argument **von glLineStipple**                                                                    | Legt einen Wiederholungsfaktor für den Linienstil fest.                                                                                                     |
| **getlstyle**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ STIPPLE \_ PATTERN ) | Gibt das Zeilenausschnittmuster zurück.                                                                                                                |
| **getlsrepeat**                                | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ LINE \_ STIPPLE \_ REPEAT )  | Gibt den Wiederholungsfaktor zurück.                                                                                                                       |
| **linesmooth,** **smoothline**                 | [**glEnable**](glenable.md) ( GL \_ LINE \_ SMOOTH )                                                       | Aktiviert das Line-Antialiasing (Weitere Informationen zum Antialiasing finden Sie unter [Portieren von Antialiasingfunktionen](porting-antialiasing-functions.md).) |



 

OpenGL verwendet keine Tabellen für Zeilenausschnitte. es verwaltet nur ein Zeilenausschnittmuster. Sie können [**glPushAttrib und**](glpushattrib.md) [**glPopAttrib**](glpopattrib.md) verwenden, um zwischen verschiedenen Ausschnittmustern zu wechseln.

Ältere Iris GL-Linienstilfunktionen (z. B. **zeichnen,** **lsbackup,** **getlsbackup** und so weiter) werden von OpenGL nicht unterstützt.

Informationen zum Zeichnen von Antialiasinglinien finden Sie unter [Portieren von Antialiasingfunktionen.](porting-antialiasing-functions.md)

??

 

 





