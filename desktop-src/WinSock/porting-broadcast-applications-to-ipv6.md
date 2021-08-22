---
description: In diesem Abschnitt werden bewährte Methoden zum Portieren einer IPv6-Broadcastanwendung auf die Multicastfunktionen beschrieben, die mit Windows Sockets verfügbar sind.
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: Portieren von Broadcastanwendungen zu IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb54fec87be2aa6174de603d2c3e4d0e640156902002b1e87fab149a70e3d1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641700"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>Portieren von Broadcastanwendungen zu IPv6

In diesem Abschnitt werden bewährte Methoden zum Portieren einer IPv6-Broadcastanwendung auf die Multicastfunktionen beschrieben, die mit Windows Sockets verfügbar sind.

## <a name="comparing-ipv4-to-ipv6"></a>Vergleich zwischen IPv4 und IPv6

Der wichtigste Aspekt bei der Vorbereitung der Portierung einer IPv4-Broadcastanwendung zu IPv6 ist: IPv6 verfügt über kein implementiertes Broadcastkonzept. Stattdessen verwendet IPv6 Multicast.

Multicast für IPv6 kann herkömmliche Broadcastfunktionen in IPv4 emulieren. Das Festlegen der [IPV6 \_ ADD MEMBERSHIP-Socketoption, \_ ](ipproto-ipv6-socket-options.md) bei der die IPv6-Adresse auf den link-local-Bereich für alle Knotenadressen (FF02::1) festgelegt ist, entspricht der Übertragung auf IPv4-Broadcastadressen mithilfe der [SO BROADCAST-Socketoption. \_ ](socket-options.md) Diese Adresse wird manchmal als *Multicastgruppe mit allen Knoten bezeichnet.* Für Anwendungen, die einfach broadcast emulation für IPv6 wünschen, ist dieser Ansatz betriebsbereit gleichwertig. Ein beachtenswerter Unterschied zu IPv6 ist jedoch, dass Multicasts für die Multicastgruppenadresse aller Knoten standardmäßig nicht empfangen werden (IPv4-Broadcasts werden standardmäßig empfangen). Anwendungsprogrammierer müssen die IPV6-Socketoption ADD MEMBERSHIP verwenden, um den Multicastempfang von einer beliebigen Quelle zu aktivieren, einschließlich der Multicastgruppenadresse aller \_ \_ Knoten.

> [!Note]  
> In IPv6 wird die Schnittstellenauswahl in der Argumentstruktur angegeben, die an die Multicastsocketoption oder IOCTL übergeben wird.

 

Für umfangreiche, stabilere, selektivere und besser verwaltbare Übertragungen an mehrere Hosts sollten Anwendungsentwickler jedoch den Wechsel zu einem Multicastmodell in Erwägung ziehen.

## <a name="moving-to-multicast"></a>Wechsel zu Multicast

Mit Multicast können Anwendungsprogrammierer selektiv ein bestimmtes Quell-/Gruppenpaar auswählen, wodurch ein modellgesteuerter Empfang ermöglicht wird. Die Multicastlistenerermittlung (MLD) unter IPv6 und Version 3 des Internet Group Management Protocol (IGMPv3) unter IPv4 unterstützen die Multicastprogrammierung. Darüber hinaus ermöglicht Multicast Anwendungen das explizite Blockieren (oder Entsperren) von Absendern innerhalb einer Gruppe, um Anwendungen vor nicht autorisierten Sendern weiter zu schützen. Diese Funktion ist für IPv4 (erfordert IGMPv3) und IPv6 (erfordert MLDv2) verfügbar.

Es gibt zwei primäre Szenarien für Anwendungsprogrammierer, die Multicast verwenden: das Portieren von IPv4-Broadcastanwendungen (oder Multicastanwendungen) zu IPv6 und diejenigen, die neue IPv6-Multicastanwendungen erstellen.

Zum Portieren vorhandener Anwendungen gibt es zwei Optionen für den Wechsel zu IPv6-Multicast: die Verwendung von Socketoptionen und die Verwendung von IOCTLs.

-   Die Verwendung von Socketoptionen ist ein änderungsbasierter Ansatz, mit dem Entwickler die Socketeigenschaften nach Bedarf ändern können (z. B. das Blockieren oder Entsperren eines Absenders, das Hinzufügen einer neuen Quelle und so weiter). Dieser Ansatz ist intuitiver und der empfohlene Ansatz. Weitere Informationen zum änderungsbasierten Ansatz der Multicastprogrammierung finden Sie unter [MLD und IGMP mit Windows Sockets.](igmp-and-windows-sockets.md)
-   Die Verwendung von IOCTLs ist ein Aufschlusszustandsbasierter Ansatz, da Entwickler damit einen vollständig konfigurierten Socketzustand, einschließlich Einschluss- und Ausschlusslisten, mit einem Aufruf bereitstellen können. Weitere Informationen zum final-state-basierten Ansatz finden Sie unter [Final-State-Based Multicast Programming](final-state-based-multicast-programming.md).

Für Benutzer, die neue IPv6-Multicastanwendungen erstellen, wird empfohlen, Socketoptionen anstelle von IOCTLs zu verwenden.

Es gibt einen anderen Ansatz zum Erstellen von Multicastanwendungen mit IPv6, der die Verwendung der [**WSAJoinLeaf-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) umfasst. Die Verwendung der **WSAJoinLeaf-Funktion** ist zwar nicht die empfohlene Vorgehensweise, es gibt jedoch Situationen, die ihre Verwendung vorschreiben können. Ein Nachteil bei der Verwendung von Socketoptionen auf Windows Server 2003 und früher ist beispielsweise, dass sie ip-versionsspezifisch sind. In diesen älteren Versionen von Windows müssen verschiedene Socketsoptionen für IPv6 und IPv4 verfügbar sein. Unter Windows Vista und höher werden neue Socketoptionen unterstützt, die sowohl mit IPv4 als auch mit IPv6 verwendet werden können. Die **WSAJoinLeaf-Funktion** ist dagegen ip-versions- und protokollunabhängig und kann daher ein nützlicher Ansatz zum Erstellen einer Anwendung sein, die mit mehreren IP-Versionen auf Windows Server 2003 und früher arbeiten muss. Die **Verwendung der WSAJoinLeaf-Funktion** kann in bestimmten Situationen besser geeignet sein, in denen eine Agnostik zwischen Protokoll und IP-Version erforderlich ist.

 

 



