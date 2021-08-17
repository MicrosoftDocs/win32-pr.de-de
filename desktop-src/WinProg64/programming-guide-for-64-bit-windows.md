---
title: Programmierhandbuch für 64-Bit-Windows
description: Microsoft hat 64-Bit-Versionen des Windows veröffentlicht.
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- 64-Bit-Windows 64-Bit-Programmierhandbuch Windows Programmieren
- 64-Bit-Windows 64-Bit-Programmierhandbuch Windows Programmierung , Startseite
- Programmierhandbuch für 64-Bit-Windows 64-Bit-Windows 64-Bit-Programmierhandbuch siehe 64-Bit-Windows-Programmierhandbuch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8af8c2cb6340bd7617dd7e712f89cb5d9485c65d3d56258850c1a885df1f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743467"
---
# <a name="programming-guide-for-64-bit-windows"></a>Programmierhandbuch für 64-Bit-Windows

Microsoft hat 64-Bit-Versionen des Windows veröffentlicht. 64-Bit-Windows wurde unter Berücksichtigen der Kompatibilität entworfen. Entwickler können sicherstellen, dass ihre vorhandenen 32-Bit-Anwendungen gut unter 64-Bit-Windows ausgeführt werden, oder die Vorteile von 64-Bit-Windows nutzen, indem sie ihre Anwendungen migrieren.

## <a name="benefits-of-64-bit-windows"></a>Vorteile von 64-Bit-Windows

Ein 64-Bit-Betriebssystem unterstützt deutlich mehr physischen Arbeitsspeicher als ein 32-Bit-Betriebssystem. Die meisten 32-Bit-Windows-Systeme unterstützen beispielsweise maximal 4 GB physischen Arbeitsspeicher mit bis zu 3 GIGABYTE Adressraum für jeden Prozess, während 64-Bit-Windows bis zu 2 Terabyte physischen Arbeitsspeicher mit 8 Terabyte Adressraum für jeden Prozess unterstützt. Der erhöhte physische Speicher bietet die folgenden Vorteile für Anwendungen:

-   Jede Anwendung kann mehr Benutzer unterstützen. Jede Anwendung muss ganz oder teilweise für jeden Benutzer repliziert werden, was zusätzlichen Arbeitsspeicher erfordert.
-   Jede Anwendung bietet eine bessere Leistung. Durch die Erhöhung des physischen Speichers können mehr Anwendungen gleichzeitig ausgeführt werden und verbleiben vollständig im Hauptspeicher des Systems. Dies reduziert oder beseitigt leistungssentspricht, wenn Seiten auf und vom Datenträger ausgetauscht werden.
-   Jede Anwendung verfügt über mehr Arbeitsspeicher für die Datenspeicherung und -bearbeitung. Datenbanken können mehr ihrer Daten im physischen Speicher des Systems speichern. Der Datenzugriff ist schneller, da keine Datenträgerleseberechtigungen erforderlich sind.
-   Anwendungen können große Datenmengen einfach und zuverlässiger bearbeiten. Die Videokomposition für die Arbeit mit Bewegungsaufnahmen erfordert aus Windows 64-Bit-Verschlüsselung. Die Modellierung für wissenschaftliche und Finanzanwendungen profitiert stark von speicheridenten Datenstrukturen, die auf 32-Bit-Anwendungen nicht Windows.

Es gibt auch wichtige Vorteile für Unternehmen:

-   Gesteigerte Produktivität: Wissensarbeiter können ihre Zeit damit verbringen, zu denken und zu erzeugen, anstatt darauf zu warten, dass die Software ihre Aufgaben abgeschlossen hat.
-   Niedrigere Besitzkosten. Jeder Server kann eine größere Anzahl von Benutzern und Anwendungen unterstützen, sodass Ihr Unternehmen weniger Server benötigt. Dies führt direkt zu weniger Verwaltungsaufwand – einer der höchsten Kosten in jeder Computingumgebung.
-   Neue Anwendungsmöglichkeiten. Neue Anwendungen können ohne die Barrieren entworfen werden, die durch 32-Bit-Windows. Neue Grafikanwendungen erleichtern die Arbeit und erleichtern die Arbeit. Datenintensive Aufgaben, die heute unmöglich sind, können mit 64-Bit-Windows.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md)
-   [Entwerfen von 64-Bit-kompatiblen Schnittstellen](designing-64-bit-compatible-interfaces.md)
-   [Ausführen von 32-Bit-Anwendungen](running-32-bit-applications.md)
-   [Tipps zur Migration](migration-tips.md)

 

 




