---
description: Beschreibt die Microsoft-Implementierung des SMB-Protokolls (Server Message Block).
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Übersicht über das Microsoft SMB-Protokoll und CIFS-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30326221694ce843733f6da7a6ad49c8dff336ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958891"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a>Übersicht über das Microsoft SMB-Protokoll und CIFS-Protokoll

Das SMB-Protokoll (Server Message Block) ist ein Netzwerkdatei Freigabe-Protokoll, das in Microsoft Windows implementiert ist, wird als Microsoft SMB-Protokoll bezeichnet. Der Satz von Nachrichten Paketen, der eine bestimmte Version des Protokolls definiert, wird als Dialekt bezeichnet. Das CIFS-Protokoll (Common Internet File System) ist ein Dialekt von SMB. Sowohl SMB als auch CIFS sind auch auf VMS, mehreren Versionen von UNIX und anderen Betriebssystemen verfügbar.

Die technische Referenz zu CIFS ist in der Microsoft Corporation unter [Common Internet File System (CIFS) File Access Protocol](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b)verfügbar.

Obwohl der Hauptzweck der Dateifreigabe ist, beinhaltet die zusätzliche Funktionalität von Microsoft SMB-Protokoll Folgendes:

-   [Dialekt Aushandlung](microsoft-smb-protocol-dialects.md)
-   Bestimmen anderer Microsoft SMB-Protokollserver im Netzwerk oder Durchsuchen des Netzwerks
-   Drucken über ein Netzwerk
-   [Datei-, Verzeichnis-und Freigabe Zugriffs Authentifizierung](microsoft-smb-protocol-authentication.md)
-   Datei-und Datensatzsperren
-   Datei-und Verzeichnis Änderungs Benachrichtigung
-   Erweiterte Datei Attribut Verarbeitung
-   Unicode-Unterstützung
-   [Opportunistische Sperren](opportunistic-locks.md)

Im OSI-Netzwerkmodell wird das Microsoft SMB-Protokoll am häufigsten als Anwendungsschicht oder Präsentationsschicht Protokoll verwendet, und es basiert auf Protokollen auf niedrigerer Ebene für den Transport. Das Transportschicht Protokoll, mit dem das Microsoft SMB-Protokoll am häufigsten verwendet wird, ist NetBIOS über TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))). Das Microsoft SMB-Protokoll kann jedoch auch ohne ein separates Transportprotokoll verwendet werden. die Kombination aus dem Microsoft SMB-Protokoll/NBT wird in der Regel aus Gründen der Abwärtskompatibilität verwendet.

Das Microsoft SMB-Protokoll ist eine Client/Server-Implementierung und besteht aus einem Satz von Datenpaketen, die jeweils eine vom Client gesendete Anforderung oder eine vom Server gesendete Antwort enthalten. Diese Pakete können wie folgt weitgehend klassifiziert werden:

-   Mit Sitzungs Steuerungs Paketen wird eine Verbindung mit freigegebenen Server Ressourcen festgelegt und getrennt.
-   Datei Zugriffs Pakete greifen auf Dateien und Verzeichnisse auf dem Remote Server zu und manipulieren Sie.
-   Allgemeine Nachrichten Pakete senden Daten an Druck Warteschlangen, Postfächer und Named Pipes und stellen Daten zum Status von Druck Warteschlangen bereit.

Einige Nachrichten Pakete können gruppiert und in einer Übertragung gesendet werden, um die Antwort Latenz zu verringern und die Netzwerkbandbreite zu erhöhen. Dies wird als "Batch Verarbeitung" bezeichnet. Im Abschnitt " [Microsoft SMB Protocol Packet Exchange Scenario](microsoft-smb-protocol-packet-exchange-scenario.md) " wird ein Beispiel für eine Microsoft SMB-Protokoll Sitzung beschrieben, die die Paket Batch Verarbeitung verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft SMB-Protokoll Dialekte](microsoft-smb-protocol-dialects.md)<br/>                                 | Zum Herstellen einer Verbindung zwischen einem Client und einem Server mithilfe des Microsoft SMB-Protokolls müssen Sie zunächst den Dialekt mit dem höchsten Grad an Funktionalität ermitteln, die sowohl vom Client als auch vom Server unterstützt werden.<br/>                                                      |
| [Microsoft SMB-Protokoll Authentifizierung](microsoft-smb-protocol-authentication.md)<br/>                     | Das Sicherheitsmodell, das im Microsoft SMB-Protokoll verwendet wird, ist identisch mit dem im Microsoft SMB-Protokoll verwendeten Sicherheitsmodell und besteht aus zwei Sicherheitsstufen: Benutzer und Freigabe. Bei einer Freigabe handelt es sich um eine Datei, ein Verzeichnis oder einen Drucker, auf die von Microsoft SMB-Protokoll Clients zugegriffen werden kann.<br/> |
| [Microsoft SMB Protocol-Paket Austausch Szenario](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | Beispiel für einen Microsoft SMB-Protokoll Paket Austausch zwischen einem Client und einem Server.<br/>                                                                                                                                                                               |



 

 

