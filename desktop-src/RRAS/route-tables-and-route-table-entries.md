---
title: Routentabellen und Routentabelleneinträge
description: Der Routingtabellen-Manager verwaltet für jede Protokollfamilie unterschiedliche Routingtabellen.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31fea4ac965fe397d5bb7eba2b65479358a1e192f1583b1e7e73c2532dbd3a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788055"
---
# <a name="route-tables-and-route-table-entries"></a>Routentabellen und Routentabelleneinträge

**Windows Server 2003:** Diese API wurde durch die [RoutingTabellen-Manager-API Version 2](about-routing-table-manager-version-2.md) ersetzt und ist über Windows Server 2003 hinaus nicht mehr verfügbar. Neue Anwendungen sollten die Routingtabellen-Manager-API Version 2 verwenden.

Der Routingtabellen-Manager verwaltet für jede Protokollfamilie unterschiedliche Routingtabellen. Derzeit wird explizite Unterstützung für die Routingprotokollfamilien Internet protocol (IP) und Internet Packet Exchange (IPX) bereitgestellt. Unabhängig von der Protokollfamilie enthält jeder Routeneintrag die folgenden Informationen:

-   Zielnetzwerk.
-   Bezeichner des Protokolls, das die Route hinzugefügt hat.
-   Index der Schnittstelle, über die die Route erhalten wurde. Dieser Indexwert ist der numerische Wert, der einer (hardwarebasierten oder virtuellen) Netzwerkschnittstelle zugewiesen ist, die die Daten in das Netzwerk überträgt. (Beispielsweise eine Ethernet-NIC oder eine 802.1b-Drahtloskarte.)
-   Adresse des Routers des nächsten Hops. RRAS verwendet diesen Router, um Pakete an das Zielnetzwerk weiter zu senden, wenn das Netzwerk nicht direkt verbunden ist.
-   Der Zeitpunkt, zu dem die Route erstellt oder zuletzt aktualisiert wurde.
-   Die Zeit, die diese Route in der Routingtabelle beibehalten wird. Wenn diese Zeitspanne verstreicht und die Route nicht aktualisiert wurde, entfernt der Routingtabellen-Manager die Route aus der Tabelle. In diesem Fall wird für die Route ein Alter *von bezeichnet.*
-   Daten, die für die Protokollfamilie spezifisch sind. Diese Daten sind für RTMv1 transparent. Wenn sich diese Daten jedoch für eine Route ändern, die als "beste Route" festgelegt ist, sendet der Routingtabellen-Manager eine Benachrichtigung zur Routenänderung.
-   Spezifische Daten für das Routingprotokoll. Diese Daten sind für den Routingtabellen-Manager vollständig transparent, da Änderungen an diesen Daten keine Routenänderungsbenachrichtigung verursachen.

Die folgenden Werte identifizieren eine Route in der Routingtabelle eindeutig:

-   Zielnetzwerk
-   Protokollbezeichner
-   Schnittstellenindex
-   Adresse des Routers des nächsten Hops

Im Allgemeinen erstellt der Routingtabellen-Manager separate Einträge für Routen, die sich in einem dieser Parameterwerte unterscheiden. Es wird jedoch eine Ausnahme für Routingprotokolle gemacht, die nicht mehr als einen Eintrag für jedes Zielnetzwerk behalten. Für diese Protokolle ignoriert der Routingtabellen-Manager Unterschiede im Schnittstellenindex oder in der Adresse des nächsten Hops. Ein Beispiel für ein solches Protokoll ist die RRAS-Implementierung von Open Shortest Path First (OSPF).

 

 




