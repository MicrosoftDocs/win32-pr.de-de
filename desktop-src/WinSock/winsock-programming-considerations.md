---
description: Windows Sockets 2 erweitert die Funktionen von Windows Sockets 1,1 in verschiedenen Bereichen. In der folgenden Tabelle werden einige der wichtigsten Funktionsänderungen zusammengefasst.
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Überlegungen zur Winsock-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaee2cd04f03afe050ca539190b51e66c0abff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130401"
---
# <a name="winsock-programming-considerations"></a>Überlegungen zur Winsock-Programmierung

Windows Sockets 2 erweitert die Funktionen von Windows Sockets 1,1 in verschiedenen Bereichen. In der folgenden Tabelle werden einige der wichtigsten Funktionsänderungen zusammengefasst.



| Features                                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Architektur von Windows Sockets 2](windows-sockets-2-architecture-2.md)                                             | Eine Beschreibung der Architektur von Windows Sockets 2.                                                                                                                                                                                                                                           |
| [Sockethandles](socket-handles-2.md)                                                                             | Ein Sockethandle kann optional ein Datei Handle in Windows Sockets 2 sein. Es ist möglich, Sockethandles mit standardmäßigen Windows-Datei-e/a-Funktionen zu verwenden.                                                                                                                                           |
| [Gleichzeitiger Zugriff auf mehrere Transportprotokolle](simultaneous-access-to-multiple-transport-protocols-2.md)   | Ermöglicht einer Anwendung die Verwendung der vertrauten Socketschnittstelle, um gleichzeitigen Zugriff auf eine Reihe installierter Transportprotokolle zu erzielen.                                                                                                                                                        |
| [Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)                                 | Umfasst einen standardisierten Satz von Funktionen zum Abfragen und arbeiten mit den unzähligen namens Auflösungs Domänen, die heute vorhanden sind (z. b. DNS, SAP und X. 500).                                                                                                                                  |
| [Protokoll unabhängige Multicast-und Multipoint-Funktion](protocol-independent-multicast-and-multipoint-2.md)               | Anwendungen ermitteln, welche Art von Multipoint-oder Multicast Funktionen ein Transport bereitstellt, und verwenden diese Funktionen auf generische Weise.                                                                                                                                                     |
| [Überlappende e/a](overlapped-i-o-and-event-objects-2.md)                                                           | Umfasst das überlappende Paradigma für die Socket-e/a-Vorgänge nach dem in Windows-Umgebungen eingerichteten Modell.                                                                                                                                                                                   |
| [Scatter/Gather-e/a](scatter-gather-i-o-2.md)                                                                     | Umfasst Punkt-/sammlungsereignis mit dem überlappenden Paradigma für Socket-e/a-Vorgänge, die dem in Windows-Umgebungen eingerichteten Modell folgen.                                                                                                                                                 |
| [Quality of Service](flow-specification-quality-of-service-2.md) (QoS)                                            | Richtet Konventionen ein, die von Anwendungen verwendet werden, um erforderliche Service Levels für Parameter wie Bandbreite und Latenz auszuhandeln. Weitere QoS-bezogene Erweiterungen umfassen Mechanismen für Netzwerk spezifische Quality of Service Erweiterungen.                                                         |
| [Anbieter spezifischer Erweiterungsmechanismus](provider-specific-extension-mechanism-2.md)                               | Mit der [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion können Dienstanbieter anbieterspezifische Featureerweiterungen anbieten.                                                                                                                                                                           |
| [Freigegebene Sockets](shared-sockets-2.md)                                                                             | Die [**wsadupliingesocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) -Funktion wird eingeführt, um die prozessübergreifende socketfreigabe zu aktivieren.                                                                                                                                                                       |
| [Einrichten und Löschen der Verbindung](connection-setup-and-teardown-2.md)                                               | Eine Anwendung kann Aufruferinformationen abrufen, z. b. die Aufruferkennung und die Quality of Service, bevor Sie entscheiden, ob eine eingehende Es ist auch möglich (bei Protokollen, die dies unterstützen), Benutzerdaten zwischen den Endpunkten zum Zeitpunkt der Verbindungs Löschung auszutauschen. |
| [Ordnungsgemäßes Herunterfahren, Linger Optionen und Socket-Schließung](graceful-shutdown-linger-options-and-socket-closure-2.md) | Eine Anwendung verfügt über mehrere Optionen zum Herunterfahren einer Socketverbindung (Sequenz für das Herunterfahren).                                                                                                                                                                                                  |
| [Protokoll unabhängige out-of-Band-Daten](protocol-independent-out-of-band-data-2.md)                               | Die Stream-Socket-Abstraktion enthält das Konzept von OOB-Daten (Out-of-Band).                                                                                                                                                                                                                   |
| [Debug-und Ablauf Verfolgungs Funktionen](debug-and-trace-facilities-2.md)                                                     | Windows Sockets 2 unterstützt eine speziell entwickelte Version des Ws2 \_ -32.dll und eine separate Debug/Trace-dll.                                                                                                                                                                                      |
| [Windows Sockets-Kompatibilitätsprobleme](windows-sockets-compatibility-issues-2.md)                                 | Windows Sockets 2 unterstützt weiterhin alle Semantik-und Funktionsaufrufe von Windows Sockets 1,1, mit Ausnahme derjenigen, die mit der Pseudo Blockierung arbeiten.                                                                                                                                              |
| [Behandeln von Winsock-Fehlern](handling-winsock-errors.md)                                                             | Wie Winsock-Fehler von einer Anwendung abgerufen und verarbeitet werden können.                                                                                                                                                                                                                             |



 

 

 



