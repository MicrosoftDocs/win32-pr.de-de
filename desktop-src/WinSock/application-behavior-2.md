---
description: Ein weiterer Aspekt der zu berücksichtigenden Anwendungsentwicklung ist der Unterschied im Verhalten zwischen lokalen Computern oder betriebsinternen Vorgängen sowie das Verhalten, wenn Vorgänge zwischen zwei vernetzten Computern stattfinden.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Anwendungsverhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526213"
---
# <a name="application-behavior"></a>Anwendungsverhalten

Ein weiterer Aspekt der zu berücksichtigenden Anwendungsentwicklung ist der Unterschied im Verhalten zwischen lokalen Computern oder betriebsinternen Vorgängen sowie das Verhalten, wenn Vorgänge zwischen zwei vernetzten Computern stattfinden. Es gibt Anwendungs Verhaltensweisen, die auf einem lokalen Computer möglicherweise akzeptabel sind, aber wenn Sie in einem Netzwerk ausgeführt werden, führen Sie zu erheblichen Leistungseinbußen und Ressourcenverbrauch. Die folgenden Anwendungs Verhaltensweisen sollten bei der Entwicklung von Windows Sockets-Anwendungen vermieden werden.

## <a name="behaviors-to-avoid"></a>Zu vermeide Verhalten

-   Chatty-Anwendungen.

    Einige Anwendungen führen viele kleine Transaktionen aus. In Kombination mit dem Netzwerk Aufwand, der den einzelnen Transaktionen zugeordnet ist, wird der Effekt multipliziert. In Netzwerken können kleine Transaktionen so viele Ressourcen und so viel Zeit wie große Transaktionen verbrauchen. Ein besserer Ansatz ist die Kombination vieler kleiner Transaktionen zu einer einzelnen großen Transaktion.

-   Serialisierte Transaktionen.

    Unnötige Serialisierung von Transaktionen kann zu schlechter Leistung führen und die Skalierbarkeit beeinträchtigen. Beispielsweise nehmen 1000 serialisierte Transaktionen mindestens 1000 \* RTT zum Abschluss. Ein besserer Ansatz besteht darin, nicht verbundene Transaktionen parallel auszuführen. Bei der Kombination von serialisierten Anwendungen mit ' geschwätzige '-Anwendungen kann die Reaktionsfähigkeit erheblich beeinträchtigt werden.

    > [!Note]  
    > Eine ordnungsgemäße Deserialisierung einer Anwendung kann schwierig sein. Wenn die Änderung von serialisiert in parallel zu schwierig ist, sollten Sie mehrere Transaktionen in weniger großen Transaktionen kombinieren.

     

-   FAT-Transaktionen.

    Anwendungen, die unnötige Bytes im Netzwerk senden, werden als FAT-Anwendungen angesehen. Anwendungen, die unnötige Bytes im Netzwerk senden, erhöhen den Netzwerk Mehraufwand, und die Leistung wird beeinträchtigt. Diese Situation tritt häufig von ineffizienten Datenstrukturen oder ineffizienten Datenstreaming auf. Um dieses Problem zu beheben, optimieren Sie die Datenstrukturen, oder verwenden Sie die Komprimierung.

In den folgenden Abschnitten werden Aspekte der zu berücksichtigenden Anwendungsentwicklung behandelt.

-   [TCP/IP-spezifische Probleme](tcp-ip-specific-issues-2.md)
-   [Erkennen langsamer Anwendungen](recognizing-slow-applications-2.md)
-   [Berechnen des Aufwands mit netstat](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hochleistungsfähige Windows Sockets-Anwendungen](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



