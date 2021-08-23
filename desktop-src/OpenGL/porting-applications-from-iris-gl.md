---
title: Portieren von Anwendungen von IRIS GL
description: Portieren von Anwendungen von IRIS GL
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- OpenGL auf Windows,IRIS GL-Portierung
- Portieren zu OpenGL, IRIS GL
- OpenGL-Portierung, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68e218e5b6f57039e364ab4e6ebc29fb1f2b2fad2e8a679b35c1368367f5f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777230"
---
# <a name="porting-applications-from-iris-gl"></a>Portieren von Anwendungen von IRIS GL

In diesem Abschnitt werden wichtige Unterschiede zwischen IRIS GL und OpenGL sowie die grundlegenden Schritte zum Portieren von Code von IRIS GL zu OpenGL beschrieben. Eine vollständige Liste der Unterschiede zwischen IRIS GL und Open GL finden Sie unter [IRIS GL and OpenGL Differences](iris-gl-and-opengl-differences.md).

Das Portieren von IRIS GL-Programmen zu OpenGL für Windows erfordert deutlich mehr Arbeit als das Konvertieren von OpenGL-Programmen aus dem X-Fenstersystem. Während IRIS GL-Programme für die Ausführung mit bestimmter Hardware und Software konzipiert sind, wurde OpenGL für Portabilität zwischen verschiedenen Systemen entwickelt.

In der folgenden Tabelle sind einige der wichtigsten Unterschiede zwischen OpenGL- und IRIS GL-Programmen aufgeführt.



| OpenGL-Code                                                                                                                                              | IRIS GL-Code                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Betriebssystemunabhängig; enthält keine Funktionen für Windowing, Ereignisbehandlung, Pufferzuordnung/Verwaltung usw.                              | Abhängig vom Betriebssystem; Windowing-Systemfunktionen werden mit Renderingfunktionen kombiniert. Es gibt keinen Windows-Manager in IRIS GL. |
| Verwendet eine allgemeine Standardbenennungskonvention. OpenGL-Funktionen und definierte Typen beginnen mit einem "gl"-Präfix, um Konflikte mit anderen Bibliotheken zu vermeiden.        | Verwendet keine allgemeine Benennungskonvention für Funktionen und definierte Typen.                                                              |
| Verwaltet Zustandsvariablen (z. B. Farbe, Oberfläche, Textur, Beleuchtung usw.) direkt und konsistent. Verwendet keine Tabellen, um Zustandsvariablenwerte zu laden. | Verwendet Tabellen zum Verwalten von Zustandsvariablen und muss Variablen an Tabellenwerte binden.                                                        |
| Anzeigelisten können nicht bearbeitet werden.                                                                                                                          | Anzeigelisten können bearbeitet werden.                                                                                                          |
| Stellt kein Dateiformat für Schriftarten bereit.                                                                                                                | Stellt Funktionen zum Verarbeiten von Schriftarten und Textzeichenfolgen sowie ein Dateiformat für Schriftarten bereit.                                                      |
| Enthält eine GL-Hilfsprogrammbibliothek (GLU), die zusätzliche Funktionen und Routinen enthält (z. B. NURBS und quadratische Renderingroutinen).                    | Unterstützt die GLU-Bibliothek nicht.                                                                                                     |



 

**Verwenden Sie das folgende allgemeine Verfahren, um Ihre IRIS GL-Programme auf OpenGL zu portieren.**

1.  Schreiben Sie code, der Aufrufe an einen Fenster-Manager, eine Fensterkonfiguration, ein Gerät oder ein Ereignis vornimmt oder bei dem Sie eine Farbzuordnung zu einem entsprechenden Windows Code laden. Das Umschreiben einer Anwendung von einem Betriebssystem in ein anderes kann komplex und schwierig sein. Dieses Thema geht über den Rahmen dieses Abschnitts hinaus.
2.  Suchen Sie nach Code, der IRIS GL-Funktionen und -Routinen verwendet. Übersetzen Sie diese Funktionen in die entsprechenden OpenGL-Funktionen. Eine vollständige Liste der IRIS GL-Funktionen und -Routinen und ihrer entsprechenden OpenGL-Entsprechungen finden Sie unter [OpenGL Functions and Their IRIS GL Equivalents (OpenGL-Funktionen und ihre IRIS GL-Entsprechungen).](opengl-functions-and-their-iris-gl-equivalents.md)
3.  Ändern Sie den IRIS GL-Code wie unter [Spezielle IRIS GL-Portierungsprobleme](special-iris-gl-porting-issues.md)beschrieben.

<!-- -->

1.  Schreiben Sie code, der Aufrufe an einen Fenster-Manager, eine Fensterkonfiguration, ein Gerät oder ein Ereignis vornimmt oder bei dem Sie eine Farbzuordnung zu einem entsprechenden Windows Code laden. Das Umschreiben einer Anwendung von einem Betriebssystem in ein anderes kann komplex und schwierig sein. Dieses Thema geht über den Rahmen dieses Abschnitts hinaus.
2.  Suchen Sie nach Code, der IRIS GL-Funktionen und -Routinen verwendet. Übersetzen Sie diese Funktionen in die entsprechenden OpenGL-Funktionen. Eine vollständige Liste der IRIS GL-Funktionen und -Routinen und ihrer entsprechenden OpenGL-Entsprechungen finden Sie unter [OpenGL Functions and Their IRIS GL Equivalents (OpenGL-Funktionen und ihre IRIS GL-Entsprechungen).](opengl-functions-and-their-iris-gl-equivalents.md)
3.  Ändern Sie den IRIS GL-Code wie unter [Spezielle IRIS GL-Portierungsprobleme](special-iris-gl-porting-issues.md)beschrieben.

 

 




