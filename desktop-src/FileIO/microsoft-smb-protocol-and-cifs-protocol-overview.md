---
description: Beschreibt die Microsoft-Implementierung des SMB-Protokolls (Server Message Block).
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Übersicht über das Microsoft SMB-Protokoll und das CIFS-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09702c719d4e4c5225b35691d7e23980c90c959b7096d7995f3d60b3ef0b204b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951149"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a>Übersicht über das Microsoft SMB-Protokoll und das CIFS-Protokoll

Das SMB-Protokoll (Server Message Block) ist ein Netzwerkdateifreigabeprotokoll, das in Microsoft Windows als Microsoft SMB-Protokoll bezeichnet wird. Der Satz von Nachrichtenpaketen, der eine bestimmte Version des Protokolls definiert, wird als Dialekt bezeichnet. Das CIFS-Protokoll (Common Internet File System) ist ein Dialekt von SMB. Sowohl SMB als auch CIFS sind auch auf VMS, mehreren Unix-Versionen und anderen Betriebssystemen verfügbar.

Die technische Referenz zu CIFS ist über Microsoft Corporation unter [Common Internet File System (CIFS) File Access Protocol](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b)verfügbar.

Obwohl der Hauptzweck der Dateifreigabe ist, umfasst die zusätzliche Funktionalität des Microsoft SMB-Protokolls Folgendes:

-   [Dialektaushandlung](microsoft-smb-protocol-dialects.md)
-   Bestimmen anderer Microsoft SMB-Protokollserver im Netzwerk oder Durchsuchen des Netzwerks
-   Drucken über ein Netzwerk
-   [Datei-, Verzeichnis- und Freigabezugriffsauthentifizierung](microsoft-smb-protocol-authentication.md)
-   Datei- und Datensatzsperren
-   Datei- und Verzeichnisänderungsbenachrichtigung
-   Behandlung erweiterter Dateiattribute
-   Unicode-Unterstützung
-   [Opportunistische Sperren](opportunistic-locks.md)

Im OSI-Netzwerkmodell wird das Microsoft SMB-Protokoll am häufigsten als Anwendungsebene oder Präsentationsebene verwendet und basiert für den Transport auf Protokollen auf niedrigerer Ebene. Das Transportschichtprotokoll, mit dem das Microsoft SMB-Protokoll am häufigsten verwendet wird, ist NetBIOS über TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))). Das Microsoft SMB-Protokoll kann jedoch auch ohne ein separates Transportprotokoll verwendet werden. Die Kombination aus Microsoft SMB-Protokoll und NBT wird im Allgemeinen aus Gründen der Abwärtskompatibilität verwendet.

Das Microsoft SMB-Protokoll ist eine Client-Server-Implementierung und besteht aus einem Satz von Datenpaketen, die jeweils eine vom Client gesendete Anforderung oder eine vom Server gesendete Antwort enthalten. Diese Pakete können im Großen und Ganzen wie folgt klassifiziert werden:

-   Sitzungssteuerungspakete Richten eine Verbindung mit freigegebenen Serverressourcen ein und stellen sie ein.
-   Dateizugriffspakete Greift auf Dateien und Verzeichnisse auf dem Remoteserver zu und bearbeitet sie.
-   Allgemeine Nachrichtenpakete Sendet Daten an Druckwarteschlangen, Mailslots und Named Pipes und stellt Daten zum Status von Druckwarteschlangen bereit.

Einige Nachrichtenpakete können gruppiert und in einer Übertragung gesendet werden, um die Antwortlatenz zu reduzieren und die Netzwerkbandbreite zu erhöhen. Dies wird als "Batchverarbeitung" bezeichnet. Im Abschnitt [Microsoft SMB Protocol Packet Exchange Scenario](microsoft-smb-protocol-packet-exchange-scenario.md) wird ein Beispiel für eine Microsoft SMB-Protokollsitzung beschrieben, die Paketbatchverarbeitung verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft SMB-Protokolldialekte](microsoft-smb-protocol-dialects.md)<br/>                                 | Um mithilfe des Microsoft SMB-Protokolls eine Verbindung zwischen einem Client und einem Server herzustellen, müssen Sie zunächst den Dialekt mit der höchsten Funktionalitätsstufe bestimmen, die sowohl vom Client als auch vom Server unterstützt wird.<br/>                                                      |
| [Microsoft SMB-Protokollauthentifizierung](microsoft-smb-protocol-authentication.md)<br/>                     | Das im Microsoft SMB-Protokoll verwendete Sicherheitsmodell ist mit dem von anderen Varianten von SMB verwendeten identisch und besteht aus zwei Sicherheitsbenutzer- und Freigabeebenen. Eine Freigabe ist eine Datei, ein Verzeichnis oder ein Drucker, auf die von Microsoft SMB-Protokollclients zugegriffen werden kann.<br/> |
| [Szenario mit Microsoft SMB-Protokollpaketaustausch](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | Beispiel für einen Paketaustausch des Microsoft SMB-Protokolls zwischen einem Client und einem Server.<br/>                                                                                                                                                                               |



 

 

