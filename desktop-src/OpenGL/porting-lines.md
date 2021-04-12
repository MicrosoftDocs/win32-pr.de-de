---
title: Portieren von Linien
description: Das Portieren von IRIS GL-Code, der Linien zeichnet, ist recht unkompliziert. Beachten Sie jedoch die Unterschiede in der Art und Weise, wie OpenGL Stipeln. In der folgenden Tabelle sind IRIS GL-Funktionen für Zeichnungslinien und ihre entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- IRIS GL Porting, Lines
- Portieren von IRIS GL, Lines
- Portieren auf OpenGL von IRIS GL, Lines
- OpenGL-Portierung von IRIS GL, Zeilen
- Zeichnungsfunktionen, Zeilen
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207150"
---
# <a name="porting-lines"></a>Portieren von Linien

Das Portieren von IRIS GL-Code, der Linien zeichnet, ist recht unkompliziert. Beachten Sie jedoch die Unterschiede in der Art und Weise, wie OpenGL Stipeln. In der folgenden Tabelle sind IRIS GL-Funktionen für Zeichnungslinien und ihre entsprechenden OpenGL-Funktionen aufgeführt.



| IRIS GL-Funktion                               | OpenGL-Funktion                                                                                         | Bedeutung                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **bgnclosedline**,**endclosedline**<br/> | [**glBegin**](glbegin.md) (GL- \_ Zeilen \_ Schleife)[**glEnd**](glend.md)<br/>                          | Zeichnet eine geschlossene Zeile.                                                                                                                         |
| **bgnline**                                    | [**glBegin**](glbegin.md) (GL- \_ Zeilen \_ Streifen)                                                          | Zeichnet Liniensegmente.                                                                                                                         |
| **LineWidth**                                  | [**glLineWidth**](gllinewidth.md)                                                                      | Legt die Linienbreite fest.                                                                                                                             |
| **getlwidth**                                  | [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL- \_ Linienstärke \_ )            | Gibt die aktuelle Linienbreite zurück.                                                                                                                  |
| **deflinestyle**,**SetLineStyle**<br/>   | [**gllinestippel**](gllinestipple.md)                                                                  | Gibt ein Zeilen stippingmuster an.                                                                                                            |
| **lsrepeat**                                   | Faktor Argument von **gllinestippel**                                                                    | Legt einen Wiederholungs Faktor für den Linienstil fest.                                                                                                     |
| **getlstyle**                                  | [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL- \_ Zeilen \_ stippingmuster \_ ) | Gibt ein Zeilen stippingmuster zurück.                                                                                                                |
| **getlsrepeat**                                | [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL- \_ Zeilen- \_ Stippel \_ wiederholen)  | Gibt den Wiederholungs Faktor zurück.                                                                                                                       |
| **linesmuoth**, **glä-Linie**                 | [**glEnable**](glenable.md) (GL- \_ Linie \_ glatt)                                                       | Schaltet ein Zeilen-Antialiasing (Weitere Informationen zum Antialiasing finden Sie unter [Portieren von Antialiasing-Funktionen](porting-antialiasing-functions.md).) |



 

OpenGL verwendet keine Tabellen für Zeilen Stipeln; Es wird nur ein Zeilen stippingmuster verwaltet. Sie können mit [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) zwischen verschiedenen Stippel Mustern wechseln.

Ältere Zeilen Stil Funktionen von IRIS gl (z. b. **Draw**, **lsbackup**, **getlsbackup** usw.) werden von OpenGL nicht unterstützt.

Weitere Informationen zum Zeichnen von Zeilen mit Antialiasing finden Sie unter [Portieren von Antialiasing-Funktionen](porting-antialiasing-functions.md).

??

 

 





