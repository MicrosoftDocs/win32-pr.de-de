---
description: In diesem Abschnitt werden bewährte Methoden zum Portieren einer IPv6-Broadcast Anwendung auf die mit Windows Sockets verfügbaren Multicast Funktionen beschrieben.
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: Portieren von Broadcast Anwendungen auf IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7dce09db6822a6f9b0a61873ca6bbff5a256b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484918"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>Portieren von Broadcast Anwendungen auf IPv6

In diesem Abschnitt werden bewährte Methoden zum Portieren einer IPv6-Broadcast Anwendung auf die mit Windows Sockets verfügbaren Multicast Funktionen beschrieben.

## <a name="comparing-ipv4-to-ipv6"></a>Vergleichen von IPv4 mit IPv6

Der wichtigste Aspekt beim Vorbereiten der Portierung einer IPv4-Broadcast Anwendung auf IPv6 ist: IPv6 hat kein implementiertes Übertragungs Konzept. Stattdessen verwendet IPv6 Multicast.

Multicast für IPv6 kann herkömmliche Broadcast Funktionen emulieren, die in IPv4 gefunden werden. Das Festlegen der IPv6-Option zum [ \_ Hinzufügen von \_ Mitgliedschafts](ipproto-ipv6-socket-options.md) Sockets (IPv6) mit der IPv6-Adresse, die auf die Adresse des Link-Local-Bereichs alle Knoten (FF02:: 1) festgelegt ist, entspricht dem Senden von IPv4-Broadcast Adressen [mithilfe der \_ ](socket-options.md) Diese Adresse wird manchmal als " *alle Knoten"-Multicast Gruppe* bezeichnet. Bei Anwendungen, die einfach Broadcast Emulation für IPv6 wünschen, ist dieser Ansatz operationale Äquivalent. Ein wichtiger Unterschied zu IPv6 besteht jedoch darin, dass mit auf der Multicast Gruppen Adresse aller Knoten standardmäßig nicht empfangen werden (IPv4-Übertragungen werden standardmäßig empfangen). Anwendungsprogrammierer müssen die IPv6- \_ Option zum Hinzufügen \_ von Mitgliedschaften in IPv6 verwenden, um den Multicast Empfang aus beliebigen Quellen, einschließlich der Multicast Gruppen Adresse für alle Knoten, zu aktivieren.

> [!Note]  
> In IPv6 wird die Schnittstellen Auswahl in der Argument Struktur angegeben, die an die Multicast-Socketoption oder ioctl übermittelt wurde.

 

Für umfangreichere, robustere, selektivere und besser verwaltbare Übertragungen zu mehreren Hosts sollten Anwendungsentwickler jedoch erwägen, zu einem Multicast Modell zu wechseln.

## <a name="moving-to-multicast"></a>Verschieben zu Multicast

Mit Multicast können Anwendungsprogrammierer selektiv ein bestimmtes Quell-/gruppenpaar auswählen und so ein selektives Empfangs Modell aktivieren. Die Multicast-listenerermittlung (MLD) in IPv6 und Version 3 des Internet Group Management-Protokolls (IGMPv3) unterstützen die Multicasting-Programmierung. Darüber hinaus ermöglicht Multicast Anwendungen, Absender innerhalb einer Gruppe explizit zu blockieren (oder zu entsperren) und damit Anwendungen vor nicht autorisierten Sendern zu schützen. Diese Funktion ist für IPv4 (erfordert IGMPv3) und IPv6 (erfordert MLDv2) verfügbar.

Es gibt zwei primäre Szenarien für Anwendungsprogrammierer, die Multicast verwenden: solche, die von IPv4-Broadcast Anwendungen (oder Multicast Anwendungen) zu IPv6 portieren, und solche, die neue IPv6-Multicast Anwendungen erstellen.

Zum Portieren vorhandener Anwendungen gibt es zwei Optionen für den Wechsel zu IPv6-Multicast: die Verwendung von Socketoptionen und die Verwendung von IOCTLs.

-   Die Verwendung von Socketoptionen ist ein Änderungs basierter Ansatz, mit dem Entwickler die socketeigenschaften nach Bedarf ändern können (z. b. das Blockieren oder Entsperren eines Absenders, das Hinzufügen einer neuen Quelle usw.). Diese Vorgehensweise ist intuitiver und wird empfohlen. Weitere Informationen zum Änderungs basierten Ansatz bei der Multicast Programmierung finden [Sie unter MLD und IGMP mithilfe von Windows Sockets](igmp-and-windows-sockets.md).
-   Die Verwendung von IOCTLs ist ein auf Endzuständen basierender Ansatz, da Entwickler mit einem-Befehl einen vollständig konfigurierten socketzustand bereitstellen können, einschließlich der Einschluss-und Ausschluss Listen. Weitere Informationen zum endgültigen Zustands basierten Ansatz finden Sie unter [Final-State-based Multicast Programming](final-state-based-multicast-programming.md).

Wenn Sie neue IPv6-Multicast Anwendungen erstellen, empfiehlt es sich, die Socketoptionen anstelle von IOCTLs zu verwenden.

Es gibt einen anderen Ansatz für das Erstellen von Multicast Anwendungen mit IPv6 und erfordert die Verwendung der [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) -Funktion. Die Verwendung der **wsajoinleaf** -Funktion ist nicht die empfohlene Vorgehensweise, es gibt jedoch Situationen, in denen die Verwendung möglicherweise vorgegeben ist. Ein Nachteil bei der Verwendung von Socketoptionen unter Windows Server 2003 und früher besteht beispielsweise darin, dass Sie für die IP-Version spezifisch sind. Bei diesen älteren Versionen von Windows müssen verschiedene Sockets-Optionen für IPv6 und IPv4 gelten. Unter Windows Vista und höher werden neue Socketoptionen unterstützt, die sowohl für IPv4 als auch für IPv6 verwendet werden können. Die **wsajoinleaf** -Funktion ist dagegen IP-Version und Protokoll agnostisch und kann daher ein nützlicher Ansatz zum Entwickeln einer Anwendung sein, die unter Windows Server 2003 und früher mit mehreren IP-Versionen funktionieren muss. Die Verwendung der **wsajoinleaf** -Funktion kann in bestimmten Situationen, in denen Protokoll-und IP-Versions Agnostizismus erforderlich sind, besser geeignet sein.

 

 



