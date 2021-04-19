---
description: Bestimmte Programmiertechniken stoßen auf Leistungsprobleme, die mit der Implementierung von TCP/IP verknüpft sind.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: TCP/IP-spezifische Probleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363522"
---
# <a name="tcpip-specific-issues"></a>TCP/IP-spezifische Probleme

Bestimmte Programmiertechniken stoßen auf Leistungsprobleme, die mit der Implementierung von TCP/IP verknüpft sind. Diese Leistungsprobleme deuten nicht darauf hin, dass TCP/IP ineffizient ist oder einen Leistungsengpass verursacht. Diese Probleme werden vielmehr erkannt, wenn TCP/IP-Vorgänge nicht verstanden werden.

Die folgenden Probleme identifizieren häufige Szenarien, in denen die Kombination von TCP/IP-Betriebs-und Netzwerk Anwendungs Entwicklungsoptionen zu schlechter Leistung führt.

-   Verbinden Sie große Anwendungen.

    Einige Anwendungen instanziieren eine neue TCP-Verbindung für jede Transaktion. Das Einrichten der TCP-Verbindung nimmt Zeit in Betrieb, leistet zusätzliche RTTS und unterliegt einem langsamen Start. Außerdem unterliegen die geschlossenen Verbindungen der Wartezeit, die Systemressourcen beansprucht.

    Verbindungs intensive Anwendungen sind größtenteils üblich, weil Sie einfach zu erstellen sind. die Test-und Fehlerbehandlung ist sehr einfach. Das Erkennen von Fehlern bei einer permanenten Verbindung kann viel Code und Aufwand in Anspruch nehmen und ist daher manchmal nicht abgeschlossen.

    Beheben Sie diese Situation, indem Sie die TCP-Verbindung wieder verwenden. Dies kann die Serialisierung über die TCP-Verbindung bewirken, es sei denn, die Transaktionen werden über mehrere Verbindungen multiplext. Wenn dieser Ansatz verwendet wird, sollte die Anzahl der Verbindungen auf zwei begrenzt werden, und es sind die Rahmen-und erweiterte Fehlerbehandlung auf Anwendungsebene erforderlich.

-   Sendepuffer der Länge 0 (null) und blockierende Sende Vorgänge.

    Das Deaktivieren der Pufferung mithilfe der Funktion [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) zum Festlegen des Sendepuffers ( \_ sndbuf) auf 0 (null) ähnelt dem Ausschalten der Datenträger Zwischenspeicherung. Wenn der Sendepuffer auf NULL festgelegt und blockierende Sende Vorgänge ausgegeben werden, hat eine Anwendung eine Wahrscheinlichkeit von 50 Prozent, dass eine verzögerte Bestätigung von 200 Millisekunden auftritt.

    Deaktivieren Sie Send buffereing nicht, es sei denn, Sie haben die Auswirkungen in allen Netzwerkumgebungen in Betracht gezogen. Eine Ausnahme: beim Streamen von Daten mithilfe von überlappenden e/a-Vorgängen sollte der Sendepuffer auf NULL festgelegt werden.

-   Send-Send-Receive-Programmiermodell.

    Die Strukturierung einer Anwendung für die Durchführung von Send-Send-Receive erhöht die Wahrscheinlichkeit, dass Sie den Nagle-Algorithmus findet, was eine Verzögerung von RTT + 200 MS verursacht. Der Nagle-Algorithmus kann auftreten, wenn der letzte Sendevorgang kleiner ist als die maximale TCP-Segment Größe (MSS, die maximale Datenmenge in einem einzelnen Datagramm). MSS kann ein sehr großer Wert (64K in IPv4 und noch größer in IPv6) sein. Achten Sie daher nicht auf einen normalerweise kleinen MSS. Eine bessere Option besteht darin, die beiden Sendungen mithilfe der [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) -oder **memcpy** -Funktion in einem einzelnen Sendevorgang zu kombinieren.

-   Eine große Anzahl gleichzeitiger Verbindungen.

    Gleichzeitige Verbindungen sollten höchstens zwei überschreiten, außer in speziellen Anwendungen. Wenn zwei gleichzeitige Verbindungen überschritten werden, werden Ressourcen verschwendet. Eine gute Regel besteht darin, bis zu vier kurzlebige Verbindungen oder zwei persistente Verbindungen pro Ziel zu haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsverhalten](application-behavior-2.md)
</dt> <dt>

[Hochleistungsfähige Windows Sockets-Anwendungen](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Nagle-Algorithmus](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



