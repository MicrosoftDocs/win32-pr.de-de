---
description: Bei bestimmten Programmiertechniken treten Leistungsprobleme auf, die mit der Implementierung von TCP/IP verknüpft sind.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: TCP/IP-spezifische Probleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10e63bf20f545106d6b94ad4628c3fe4fe779136bacd5c8bd1a88ec32da1f233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993259"
---
# <a name="tcpip-specific-issues"></a>TCP/IP-spezifische Probleme

Bei bestimmten Programmiertechniken treten Leistungsprobleme auf, die mit der Implementierung von TCP/IP verknüpft sind. Solche Leistungsprobleme deuten nicht darauf hin, dass TCP/IP ineffizient oder ein Leistungsengpass ist. Stattdessen treten diese Probleme auf, wenn TCP/IP-Vorgänge nicht verstanden werden.

Die folgenden Probleme identifizieren häufige Szenarien, in denen die Kombination aus TCP/IP-Vorgang und Auswahl der Entwicklung von Netzwerkanwendungen zu einer schlechten Leistung führt.

-   Verbinden anwendungen.

    Einige Anwendungen instanziieren eine neue TCP-Verbindung für jede Transaktion. Die Einrichtung der TCP-Verbindung nimmt Zeit in Anspruch, trägt zu zusätzlichen RTTs bei und unterliegt einem langsamen Start. Darüber hinaus unterliegen die geschlossenen Verbindungen TIME-WAIT, wodurch Systemressourcen verbraucht werden.

    Verbinden anwendungen sind größtenteils üblich, da sie einfach zu erstellen sind. Tests und Fehlerbehandlung sind sehr einfach. Das Erkennen von Fehlern bei einer persistenten Verbindung kann erheblichen Code und Aufwand in Anspruch nehmen und ist daher manchmal nicht abgeschlossen.

    Beheben Sie diese Situation, indem Sie die TCP-Verbindung wiederverwenden. Dies kann zu einer Serialisierung über die TCP-Verbindung führen, es sei denn, die Transaktionen werden über mehrere Verbindungen mehrfach ausgeführt. Wenn dieser Ansatz verfolgt wird, sollte die Anzahl der Verbindungen auf zwei beschränkt werden, und ein Rahmen auf Anwendungsebene und eine erweiterte Fehlerbehandlung sind erforderlich.

-   Sendepuffer der Länge 0 (null) und blockierende Sendedaten.

    Das Deaktivieren der Pufferung mithilfe der [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) zum Festlegen des Sendepuffers (SO \_ SNDBUF) auf 0 (null) ähnelt dem Deaktivieren der Datenträgerzwischenspeicherung. Beim Festlegen des Sendepuffers auf 0 (null) und ausgebenden blockierenden Sendedaten hat eine Anwendung eine 50-prozentige Wahrscheinlichkeit, dass eine verzögerte Bestätigung von 200 Millisekunden erreicht wird.

    Deaktivieren Sie die Sendepufferung nur, wenn Sie die Auswirkungen in allen Netzwerkumgebungen berücksichtigt haben. Eine Ausnahme: Beim Streamen von Daten mit überlappender E/A sollte der Sendepuffer auf 0 (null) festgelegt werden.

-   Send-Send-Receive-Programmiermodell.

    Das Strukturieren einer Anwendung zum Ausführen von Send-Send-Receive-Benachrichtigungen erhöht die Wahrscheinlichkeit, dass der Nagle-Algorithmus auftritt, was zu einer Verzögerung von RTT+200 ms führt. Der Nagle-Algorithmus kann auftreten, wenn der letzte Sendewert kleiner als die maximale TCP-Segmentgröße (MSS, die maximale Datenmenge in einem einzelnen Datagramm) ist. MSS kann ein sehr großer Wert sein (64.000 in IPv4 und sogar noch größer in IPv6). Zählen Sie daher nicht auf ein in der Regel kleines MSS. Eine bessere Option besteht darin, die beiden Sende senden mithilfe der [**WSASend-**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) oder **memcpy-Funktion** in einem einzelnen Sendesenden zu kombinieren.

-   Große Anzahl gleichzeitiger Verbindungen.

    Gleichzeitige Verbindungen dürfen nicht größer als zwei sein, außer in Speziellen Anwendungen. Das Überschreiten von zwei gleichzeitigen Verbindungen führt zu ressourcenverschwendungen Verbindungen. Eine gute Regel besteht darin, bis zu vier kurzlebige Verbindungen oder zwei persistente Verbindungen pro Ziel zu haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsverhalten](application-behavior-2.md)
</dt> <dt>

[Hochleistungsanwendungen für Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Nagle-Algorithmus](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



