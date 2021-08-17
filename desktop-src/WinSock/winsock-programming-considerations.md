---
description: Windows Sockets 2 erweitert die Funktionalität von Windows Sockets 1.1 in einer Reihe von Bereichen. In der folgenden Tabelle sind einige der wichtigsten Funktionsänderungen zusammengefasst.
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Überlegungen zur Winsock-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8451601f92f0fbf7b85532fc5a63479fe2bec26adc1984c74fc1cd7d750a04aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739859"
---
# <a name="winsock-programming-considerations"></a>Überlegungen zur Winsock-Programmierung

Windows Sockets 2 erweitert die Funktionalität von Windows Sockets 1.1 in einer Reihe von Bereichen. In der folgenden Tabelle sind einige der wichtigsten Funktionsänderungen zusammengefasst.



| Features                                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Sockets 2-Architektur](windows-sockets-2-architecture-2.md)                                             | Eine Beschreibung der Windows Sockets 2-Architektur.                                                                                                                                                                                                                                           |
| [Sockethandles](socket-handles-2.md)                                                                             | Ein Sockethandle kann optional ein Dateihandle in Windows Sockets 2 sein. Es ist möglich, Sockethandles mit standardmäßigen Windows Datei-E/A-Funktionen zu verwenden.                                                                                                                                           |
| [Gleichzeitiger Zugriff auf mehrere Transportprotokolle](simultaneous-access-to-multiple-transport-protocols-2.md)   | Ermöglicht einer Anwendung die Verwendung der vertrauten Socketschnittstelle, um gleichzeitigen Zugriff auf eine Reihe installierter Transportprotokolle zu erhalten.                                                                                                                                                        |
| [Protokollunabhängige Namensauflösung](protocol-independent-name-resolution-2.md)                                 | Enthält einen standardisierten Satz von Funktionen zum Abfragen und Arbeiten mit den unzähligen Namensauflösungsdomänen, die heute vorhanden sind (z. B. DNS, SAP und X.500).                                                                                                                                  |
| [Protokollunabhängige Multicasts und Multipoints](protocol-independent-multicast-and-multipoint-2.md)               | Anwendungen ermitteln, welche Multipoint- oder Multicastfunktionen ein Transport bereitstellt, und verwenden diese Funktionen auf generische Weise.                                                                                                                                                     |
| [Überlappende E/A](overlapped-i-o-and-event-objects-2.md)                                                           | Integriert das überlappende Paradigma für Socket-E/A, das dem in Windows Umgebungen eingerichteten Modell folgt.                                                                                                                                                                                   |
| [Punkt-/Erfassungs-E/A](scatter-gather-i-o-2.md)                                                                     | Integriert Punkt-/Erfassungsfunktionen mit dem überlappenden Paradigma für Socket-E/A und folgt dem in Windows Umgebungen eingerichteten Modell.                                                                                                                                                 |
| [Quality of Service](flow-specification-quality-of-service-2.md) (QoS)                                            | Legt Konventionen fest, mit denen Anwendungen erforderliche Servicelevel für Parameter wie Bandbreite und Latenz aushandeln. Weitere QoS-bezogene Verbesserungen umfassen Mechanismen für netzwerkspezifische Quality of Service Erweiterungen.                                                         |
| [Anbieterspezifischer Erweiterungsmechanismus](provider-specific-extension-mechanism-2.md)                               | Mit [**der WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) können Dienstanbieter anbieterspezifische Featureerweiterungen anbieten.                                                                                                                                                                           |
| [Freigegebene Sockets](shared-sockets-2.md)                                                                             | Die [**WSADuplicateSocket-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) wurde eingeführt, um die Freigabe von Sockets über Prozesse hinweg zu ermöglichen.                                                                                                                                                                       |
| [Verbindungseinrichtung und -abschaltung](connection-setup-and-teardown-2.md)                                               | Eine Anwendung kann Aufruferinformationen wie Aufruferbezeichner und Quality of Service abrufen, bevor sie entscheidet, ob eine eingehende Verbindungsanforderung akzeptiert werden soll. Es ist auch möglich (für Protokolle, die dies unterstützen), Benutzerdaten zwischen den Endpunkten zum Zeitpunkt der Verbindungsentsperrung auszutauschen. |
| [Ordnungsgemäßes Herunterfahren, Lingeroptionen und Socketabschluss](graceful-shutdown-linger-options-and-socket-closure-2.md) | Eine Anwendung verfügt über mehrere Optionen zum Herunterfahren einer Socketverbindung (Abschaltungssequenz).                                                                                                                                                                                                  |
| [Protokollunabhängige Out-of-Band-Daten](protocol-independent-out-of-band-data-2.md)                               | Die Streamsocketabstraktion umfasst das Konzept von Out-of-Band-Daten (OOB).                                                                                                                                                                                                                   |
| [Debug- und Ablaufverfolgungs-Funktionen](debug-and-trace-facilities-2.md)                                                     | Windows Sockets 2 unterstützt eine speziell entwickelte Version der \_ Ws2-32.dll und eine separate Debug-/Ablaufverfolgungs-DLL.                                                                                                                                                                                      |
| [Windows Kompatibilitätsprobleme bei Sockets](windows-sockets-compatibility-issues-2.md)                                 | Windows Sockets 2 unterstützt weiterhin alle Windows Sockets 1.1-Semantik und Funktionsaufrufe, mit Ausnahme derjenigen, die pseudoblockiert werden.                                                                                                                                              |
| [Behandeln von Winsock-Fehlern](handling-winsock-errors.md)                                                             | Wie Winsock-Fehler von einer Anwendung abgerufen und behandelt werden können.                                                                                                                                                                                                                             |



 

 

 



