---
description: Ein weiterer aspekt der Anwendungsentwicklung ist der Unterschied im Verhalten zwischen lokalen oder computerinternen Vorgängen und dem Verhalten, wenn Vorgänge zwischen zwei Netzwerkcomputern stattfinden.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Anwendungsverhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb09441eda4f0d909652ac38a9ca0596a1b4bce456f58c0e1eae1a7af7dc53b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121460"
---
# <a name="application-behavior"></a>Anwendungsverhalten

Ein weiterer aspekt der Anwendungsentwicklung ist der Unterschied im Verhalten zwischen lokalen oder computerinternen Vorgängen und dem Verhalten, wenn Vorgänge zwischen zwei Netzwerkcomputern stattfinden. Es gibt Anwendungsverhalten, das auf einem lokalen Computer möglicherweise gut funktioniert, aber wenn es über ein Netzwerk ausgeführt wird, führt dies zu einer erheblichen Leistungsbeeinträchtigung und einem erheblichen Ressourcenverbrauch. Die folgenden Anwendungsverhalten sollten vermieden werden, wenn Sie Windows Sockets-Anwendungen entwickeln.

## <a name="behaviors-to-avoid"></a>Zu vermeidende Verhaltensweisen

-   Chatty-Anwendungen.

    Einige Anwendungen führen viele kleine Transaktionen aus. In Kombination mit dem Netzwerkmehraufwand, der jeder solchen Transaktion zugeordnet ist, wird der Effekt multipliziert. Im Netzwerk können kleine Transaktionen so viele Ressourcen und so viel Zeit wie große Transaktionen verbrauchen. Ein besserer Ansatz besteht in der Kombination vieler kleiner Transaktionen zu einer einzelnen großen Transaktion.

-   Serialisierte Transaktionen.

    Eine unnötige Serialisierung von Transaktionen kann zu einer schlechten Leistung führen und sich auf die Skalierbarkeit auswirken. Für 1.000 serialisierte Transaktionen wird beispielsweise mindestens 1.000 \* RTT verwendet. Ein besserer Ansatz ist die parallele Ausführung nicht verbundener Transaktionen. Wenn serialisierte Anwendungen mit chattenden Anwendungen kombiniert werden, kann die Reaktionsfähigkeit erheblich beeinträchtigt werden.

    > [!Note]  
    > Das ordnungsgemäße Deserialisieren einer Anwendung kann schwierig sein. Wenn sich der Wechsel von serialisiert zu parallel als zu schwierig erweist, sollten Sie erwägen, mehrere Transaktionen in weniger großen Transaktionen zu kombinieren.

     

-   Fat Transactions( Fat-Transaktionen).

    Anwendungen, die unnötige Bytes im Netzwerk senden, werden als fat-Anwendungen betrachtet. Anwendungen, die unnötige Bytes im Netzwerk senden, erhöhen den Netzwerkaufwand, und die Leistung wird beeinträchtigt. Diese Situation wird häufig durch ineffiziente Datenstrukturen oder ineffizientes Datenstreaming geschaffen. Um dieses Problem zu beheben, optimieren Sie Datenstrukturen, oder erwägen Sie die Verwendung der Komprimierung.

In den folgenden Abschnitten werden aspekte der Anwendungsentwicklung erläutert, die berücksichtigt werden sollten.

-   [TCP/IP-spezifische Probleme](tcp-ip-specific-issues-2.md)
-   [Erkennen langsamer Anwendungen](recognizing-slow-applications-2.md)
-   [Berechnen des Mehraufwands mit Netstat](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hochleistungsanwendungen Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



