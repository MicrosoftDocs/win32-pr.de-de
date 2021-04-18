---
title: Programmierhandbuch für 64-Bit-Windows
description: Microsoft hat 64-Bit-Versionen des Windows-Betriebssystems veröffentlicht.
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Startseite
- Programmier Handbuch für die 64-Bit-Windows 64-Bit-Windows-Programmierung siehe 64-Bit Windows-Programmier Handbuch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1fa906510d3d9909c5cf888b562deaccb3496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388406"
---
# <a name="programming-guide-for-64-bit-windows"></a>Programmierhandbuch für 64-Bit-Windows

Microsoft hat 64-Bit-Versionen des Windows-Betriebssystems veröffentlicht. 64-Bit-Windows wurde mit Kompatibilitätsgründen entworfen. Entwickler können sicherstellen, dass Ihre vorhandenen 32-Bit-Anwendungen unter 64-Bit-Windows gut ausgeführt werden können, oder Sie profitieren von den Vorteilen von 64-Bit-Fenstern durch Migrieren Ihrer Anwendungen.

## <a name="benefits-of-64-bit-windows"></a>Vorteile von 64-Bit-Windows

Ein 64-Bit-Betriebssystem unterstützt viel mehr physischen Speicher als ein 32-Bit-Betriebssystem. Beispielsweise unterstützen die meisten 32-Bit-Windows-Systeme maximal 4 Gigabyte an physischem Arbeitsspeicher, wobei für jeden Prozess bis zu 3 Gigabyte Adressraum verfügbar ist, während 64-Bit-Windows bis zu 2 Terabyte physischen Arbeitsspeicher mit 8 Terabyte Adressraum für jeden Prozess unterstützt. Der verstärkte physische Speicher umfasst die folgenden Vorteile für Anwendungen:

-   Jede Anwendung kann mehr Benutzer unterstützen. Alle oder Teile der einzelnen Anwendungen müssen für jeden Benutzer repliziert werden, was zusätzlichen Arbeitsspeicher erfordert.
-   Jede Anwendung verfügt über eine bessere Leistung. Erhöhter physischer Arbeitsspeicher ermöglicht es, dass mehr Anwendungen gleichzeitig ausgeführt werden und im Hauptspeicher des Systems vollständig verbleiben. Dadurch wird die Leistungseinbußen beim Austauschen von Seiten auf den und vom Datenträger reduziert oder eliminiert.
-   Jede Anwendung verfügt über mehr Arbeitsspeicher für die Speicherung und Bearbeitung von Daten. Datenbanken können mehr Daten in dem physischen Speicher des Systems speichern. Der Datenzugriff ist schneller, da keine Datenträger Lesevorgänge erforderlich sind.
-   Anwendungen können große Datenmengen mühelos und zuverlässiger bearbeiten. Die Video Komposition für Motion Picture work erfordert aus diesem Grund 64-Bit-Windows. Die Modellierung für wissenschaftliche und finanzielle Anwendungen profitiert stark von Speicher Residenten Datenstrukturen, die auf 32-Bit-Fenstern nicht möglich sind.

Es gibt auch wichtige Vorteile für Unternehmen:

-   Gesteigerte Produktivität: IT-Mitarbeiter können Ihre Zeit mit der Betrachtung und Produktion verbringen, anstatt darauf zu warten, dass die Software Ihre Tasks beendet.
-   Niedrigere Betriebskosten. Jeder Server kann eine größere Anzahl von Benutzern und Anwendungen unterstützen, sodass Ihr Unternehmen weniger Server benötigt. Dies führt direkt zu einem geringeren Verwaltungsaufwand – einer der höchsten Kosten in jeder Computerumgebung.
-   Neue Anwendungsmöglichkeiten. Neue Anwendungen können ohne die von 32-Bit-Windows vorgeschriebenen Barrieren entworfen werden. Neue Grafikanwendungen erleichtern das Arbeiten mit der Arbeit. Datenintensive Aufgaben, die heute nicht mehr möglich sind, können mit 64-Bit-Fenstern durchgeführt werden.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Vorbereitung auf 64-Bit-Windows](getting-ready-for-64-bit-windows.md)
-   [Entwerfen von 64-Bit-kompatiblen Schnittstellen](designing-64-bit-compatible-interfaces.md)
-   [Ausführen von 32-Bit-Anwendungen](running-32-bit-applications.md)
-   [Tipps zur Migration](migration-tips.md)

 

 




