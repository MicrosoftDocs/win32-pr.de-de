---
description: Microsoft Windows-Netzwerkkomponenten wurden für Leistung und Skalierbarkeit entwickelt.
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: Hochleistungsanwendungen Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df2b050ac45bf0bf7788a356f4fdba98197d481dd99180f99f7dbf8cdfb5b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927869"
---
# <a name="high-performance-windows-sockets-applications"></a>Hochleistungsanwendungen Windows Sockets

Microsoft Windows-Netzwerkkomponenten wurden für Leistung und Skalierbarkeit entwickelt. Dadurch können Anwendungen die verfügbare Netzwerkbandbreite maximieren. Windows Sockets und der Windows TCP/IP-Protokollstapel wurden optimiert und optimiert. Daher können ordnungsgemäß geschriebene Windows-Anwendungen einen ungewöhnlichen Durchsatz und eine hervorragende Leistung erzielen, wie die folgenden Fakten veranschaulichen:

-   Windows kann mehr als 200.000 gleichzeitige TCP-Verbindungen bedienen.
-   In einem von SPECWeb96 durchgeführten Test hat internet information server on Windows mehr als 25.000 HTTP-Anforderungen pro Sekunde ausgeführt.
-   Windows einen Übertragungsdatensatz von über 750 MBit/s in einem transkontinentalen Gigabit-Netzwerk mit 10 Hops festlegen.

Diese Erfolge veranschaulichen, Windows TCP/IP Daten sehr schnell verarbeitet. Viele Anwendungen nutzen jedoch nicht die Leistungsfunktionen Windows, TCP/IP und Windows Sockets, da sie nicht wissentlich leistungsverwendende Techniken implementieren.

In diesem Leitfaden erfahren Sie, wie Sie häufige Programmierfehler identifizieren und wie Sie diese vermeiden. Anschließend lernen Sie Techniken kennen, die es Windows Sockets-Anwendungen ermöglichen, eine optimale Leistung zu bieten. Dieser Leitfaden wird in sechs Abschnitten vorgestellt. Die Reihenfolge der Abschnitte ist beabsichtigt. Lesen Sie diesen Leitfaden in der reihenfolgenweise, um das Beste aus diesem Leitfaden heraus zu erhalten. Die folgende Tabelle enthält Links zu den einzelnen Abschnitten sowie eine kurze Beschreibung der einzelnen Themen.



| Thema                                                                                            | BESCHREIBUNG                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Netzwerkterminologie](network-terminology-2.md)                                                 | Definiert Netzwerkterminologie und Metriken, die zum Verstehen der Leistung einer Netzwerkanwendung erforderlich sind.                                     |
| [Leistungsdimensionen](performance-dimensions-2.md)                                           | Erläutert Leistungsdimensionen, die sich auf die wahrgenommene und tatsächliche Netzwerkleistung einer Anwendung auswirken.                                        |
| [TCP/IP-Merkmale](tcp-ip-characteristics-2.md)                                           | Definiert TCP/IP-Protokollmerkmale, die zu Leistungsproblemen für eine schlecht geschriebene Anwendung führen können.                                     |
| [Anwendungsverhalten](application-behavior-2.md)                                               | Erläutert, wie die Anzeichen einer Netzwerkanwendung mit schlechter Leistung erkannt werden.                                                                     |
| [Verbessern einer langsamen Anwendung](improving-a-slow-application-2.md)                               | Enthält Beispiele für Anwendungsentwurfsprobleme, die zu einer Anwendung mit schlechter Leistung beitragen, und änderungen am Code vornehmen, um die Leistung zu verbessern. |
| [Bewährte Methoden für interaktive Anwendungen](best-practices-for-interactive-applications-2.md) | Listet die bewährten Methoden für die Entwicklung optimaler interaktiver Netzwerkanwendungen auf.                                                         |



 

 

 



