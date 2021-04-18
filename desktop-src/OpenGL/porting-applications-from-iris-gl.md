---
title: Portieren von Anwendungen von IRIS GL
description: Portieren von Anwendungen von IRIS GL
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- OpenGL unter Windows, IRIS GL portieren
- Portieren auf OpenGL, IRIS GL
- OpenGL-Portierung, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9e739b40f63bb2fd00bb62b4e5ec5566df3c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339236"
---
# <a name="porting-applications-from-iris-gl"></a>Portieren von Anwendungen von IRIS GL

In diesem Abschnitt werden wichtige Unterschiede zwischen Iris GL und OpenGL aufgeführt und die grundlegenden Schritte zum Portieren von Code von IRIS GL zu OpenGL beschrieben. Eine umfassende Liste der Unterschiede zwischen Iris GL und Open GL finden Sie [unter IRIS GL-und OpenGL-Unterschiede](iris-gl-and-opengl-differences.md).

Das Portieren von IRIS GL-Programmen auf OpenGL für Windows erfordert erheblich mehr Arbeit als die Umstellung von OpenGL-Programmen aus dem X-Fenster System. Obwohl IRIS GL-Programme für die Verwendung mit spezifischer Hardware und Software entworfen wurden, wurde OpenGL für die Portabilität verschiedener Systeme entwickelt.

In der folgenden Tabelle sind einige der wichtigsten Unterschiede zwischen den Programmen OpenGL und IRIS GL aufgeführt.



| OpenGL-Code                                                                                                                                              | IRIS GL-Code                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Betriebssystemunabhängig; enthält keine Funktionen für Fenster, Ereignis Behandlung, Puffer Zuordnung/-Verwaltung usw.                              | Abhängig vom Betriebssystem; windowingsystemfunktionen werden mit Renderingfunktionen gemischt. Es gibt keinen Windows-Manager in IRIS GL. |
| Verwendet eine gängige standardmäßige Benennungs Konvention. OpenGL-Funktionen und definierte Typen beginnen mit einem "GL"-Präfix, um Konflikte mit anderen Bibliotheken zu vermeiden.        | Verwendet keine gängige Benennungs Konvention für Funktionen und definierte Typen.                                                              |
| Verwaltet Zustandsvariablen (z. b. Farbe, Nebel, Textur, Beleuchtung usw.) direkt und konsistent. Verwendet keine Tabellen zum Laden von Zustandsvariablen Werten. | Verwendet Tabellen zur Verwaltung von Zustandsvariablen und muss Variablen an Tabellenwerte binden.                                                        |
| Anzeigelisten können nicht bearbeitet werden.                                                                                                                          | Anzeigelisten können bearbeitet werden.                                                                                                          |
| Stellt kein Dateiformat für Schriftarten bereit.                                                                                                                | Stellt Funktionen zum Verarbeiten von Schriftarten und Text Zeichenfolgen sowie ein Dateiformat für Schriftarten bereit.                                                      |
| Beinhaltet eine "GL"-Hilfsprogrammbibliothek, die zusätzliche Funktionen und Routinen (z. b. nursb und quadratische renderingroutinen) enthält.                    | Die glu-Bibliothek wird von nicht unterstützt.                                                                                                     |



 

**Verwenden Sie das folgende allgemeine Verfahren, um Ihre IRIS GL-Programme auf OpenGL zu portieren.**

1.  Schreiben Sie jeglichen Code um, der einen Fenster-Manager, eine Fenster Konfiguration, ein Gerät oder ein Ereignis aufruft, oder wenn Sie eine Farbzuordnung zu einem entsprechenden Windows-Code laden. Das Umschreiben einer Anwendung von einem Betriebssystem in ein anderes kann komplex und schwierig sein. Dieses Thema geht über den Rahmen dieses Abschnitts hinaus.
2.  Suchen Sie nach Code, der Iris GL-Funktionen und-Routinen verwendet. Übersetzen Sie diese Funktionen in die entsprechenden OpenGL-Funktionen. Eine umfassende Liste der Iris GL-Funktionen und-Routinen und der entsprechenden OpenGL-Entsprechungen finden Sie unter [OpenGL-Funktionen und ihre IRIS GL-Entsprechungen](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Ändern Sie den Iris GL-Code, wie unter [besondere IRIS GL-Porting-Probleme](special-iris-gl-porting-issues.md)beschrieben.

<!-- -->

1.  Schreiben Sie jeglichen Code um, der einen Fenster-Manager, eine Fenster Konfiguration, ein Gerät oder ein Ereignis aufruft, oder wenn Sie eine Farbzuordnung zu einem entsprechenden Windows-Code laden. Das Umschreiben einer Anwendung von einem Betriebssystem in ein anderes kann komplex und schwierig sein. Dieses Thema geht über den Rahmen dieses Abschnitts hinaus.
2.  Suchen Sie nach Code, der Iris GL-Funktionen und-Routinen verwendet. Übersetzen Sie diese Funktionen in die entsprechenden OpenGL-Funktionen. Eine umfassende Liste der Iris GL-Funktionen und-Routinen und der entsprechenden OpenGL-Entsprechungen finden Sie unter [OpenGL-Funktionen und ihre IRIS GL-Entsprechungen](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Ändern Sie den Iris GL-Code, wie unter [besondere IRIS GL-Porting-Probleme](special-iris-gl-porting-issues.md)beschrieben.

 

 




