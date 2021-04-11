---
description: Microsoft Windows-Netzwerkkomponenten wurden für Leistung und Skalierbarkeit entwickelt.
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: Hochleistungsfähige Windows Sockets-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0496198ef3a8f11e6a840fd75d0083899d23d5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041730"
---
# <a name="high-performance-windows-sockets-applications"></a>Hochleistungsfähige Windows Sockets-Anwendungen

Microsoft Windows-Netzwerkkomponenten wurden für Leistung und Skalierbarkeit entwickelt. Dadurch können Anwendungen die verfügbare Netzwerkbandbreite maximieren. Windows Sockets und der Windows-TCP/IP-Protokollstapel wurden optimiert und optimiert. Daher können ordnungsgemäß geschriebene Windows-Anwendungen einen außergewöhnlichen Durchsatz und eine höhere Leistung erzielen, wie in den folgenden Fakten veranschaulicht:

-   Windows kann über 200.000 gleichzeitige TCP-Verbindungen verarbeiten.
-   Bei einem Test, der von SPECWeb96 durchgeführt wird, bedient Internet Information Server unter Windows über 25.000 HTTP-Anforderungen pro Sekunde.
-   Windows legt einen Übertragungsdaten Satz von über 750 Mbit/s in einem transkontinentalen Gigabit-Netzwerk fest, das aus 10 Hops besteht.

Diese Errungenschaften veranschaulichen, dass Daten von Windows TCP/IP sehr schnell verarbeitet werden. Viele Anwendungen nutzen jedoch nicht die Leistungsfähigkeit Windows, TCP/IP und Windows-Sockets, da Sie unwissentlich Techniken zur Leistungs Beeinträchtigung implementieren.

In dieser Anleitung erfahren Sie, wie Sie häufige Programmierfehler erkennen und vermeiden können. Anschließend erlernen Sie Techniken, mit denen Windows Sockets-Anwendungen optimal durchgeführt werden können. Dieses Handbuch wird in sechs Abschnitten vorgestellt. Die Reihenfolge der Abschnitte ist beabsichtigt. um dieses Handbuch optimal zu nutzen, lesen Sie es in der richtigen Reihenfolge. In der folgenden Tabelle finden Sie Links zu den einzelnen Abschnitten sowie eine kurze Beschreibung der einzelnen Themen.



| Thema                                                                                            | BESCHREIBUNG                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Netzwerkterminologie](network-terminology-2.md)                                                 | Definiert die Netzwerkterminologie und Metriken, die zum Verständnis der Leistung einer Netzwerk Anwendung erforderlich sind.                                     |
| [Leistungsdimensionen](performance-dimensions-2.md)                                           | Erläutert Leistungsdimensionen, die sich auf die wahrgenommene und tatsächliche Netzwerkleistung einer Anwendung auswirken.                                        |
| [TCP/IP-Merkmale](tcp-ip-characteristics-2.md)                                           | Definiert TCP/IP-Protokoll Merkmale, die bei einer schlecht geschriebenen Anwendung zu Leistungsproblemen führen können.                                     |
| [Anwendungsverhalten](application-behavior-2.md)                                               | Erläutert, wie die Anzeichen einer Netzwerk Anwendung mit schlechter Leistung erkannt werden.                                                                     |
| [Verbessern einer langsamen Anwendung](improving-a-slow-application-2.md)                               | Bietet Beispiele für Anwendungs Entwurfs Probleme, die zu einer Anwendung mit schlechter Leistung beitragen und Änderungen am Code vornehmen, um die Leistung zu verbessern. |
| [Bewährte Methoden für interaktive Anwendungen](best-practices-for-interactive-applications-2.md) | Listet die bewährten Methoden für die Entwicklung optimaler interaktiver Netzwerkanwendungen auf.                                                         |



 

 

 



