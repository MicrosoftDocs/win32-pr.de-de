---
title: Routen Tabellen und Routen Tabelleneinträge
description: Der Routing Tabellen-Manager verwaltet unterschiedliche Routen Tabellen für jede Protokollfamilie.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f118ec1d0a6f8fe4ef301654e139f217257c3a0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341212"
---
# <a name="route-tables-and-route-table-entries"></a>Routen Tabellen und Routen Tabelleneinträge

**Windows Server 2003:** Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Neue Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.

Der Routing Tabellen-Manager verwaltet unterschiedliche Routen Tabellen für jede Protokollfamilie. Zurzeit wird die explizite Unterstützung für die Internet Protocol (IP)-und IPX-Routing Protokoll Familien (Internet Packet Exchange) bereitgestellt. Unabhängig von der Protokollfamilie enthält jeder Routen Eintrag die folgenden Informationen:

-   Zielnetzwerk.
-   Der Bezeichner des Protokolls, das die Route hinzugefügt hat.
-   Index der Schnittstelle, über die die Route abgerufen wurde. Dieser Indexwert ist der numerische Wert, der einer Netzwerkschnittstelle (Hardware basiert oder Virtual) zugewiesen ist, die die Daten an das Netzwerk überträgt. (Z. b. eine Ethernet-NIC oder eine 802.1 b-Drahtlos Karte.)
-   Adresse des Routers für den nächsten Hop. RRAS verwendet diesen Router, um Pakete an das Zielnetzwerk weiterzuleiten, wenn das Netzwerk nicht direkt verbunden ist.
-   Der Zeitpunkt, zu dem die Route erstellt oder zuletzt aktualisiert wurde.
-   Die Zeitspanne, in der diese Route in der Routing Tabelle aufbewahrt wird. Wenn diese Zeitspanne abläuft und die Route nicht aktualisiert wurde, entfernt der Routing Tabellen-Manager die Route aus der Tabelle. In diesem Fall wird die Route als veraltet *bezeichnet.*
-   Spezifische Daten für die Protokollfamilie. Diese Daten sind für RTMv1 transparent. Wenn sich diese Daten jedoch für eine Route ändern, die als "beste Route" festgelegt ist, sendet der Routing-Tabellen-Manager die Weiterleitungs Änderungs Benachrichtigung.
-   Spezifische Daten für das Routing Protokoll. Diese Daten sind vollständig für den Routing Tabellen-Manager transparent, da Änderungen an diesen Daten keine Benachrichtigung über die Routen Änderung verursachen.

Die folgenden Werte, die eine Route in der Routing Tabelle eindeutig identifizieren:

-   Zielnetzwerk
-   Protokoll Bezeichner
-   Schnittstellen Index
-   Adresse des Routers für den nächsten Hop

Im Allgemeinen erstellt der Routing Tabellen-Manager separate Einträge für Routen, die sich in diesen Parameterwerten unterscheiden. Es wird jedoch eine Ausnahme für Routing Protokolle ausgelöst, die nicht mehr als einen Eintrag für jedes Zielnetzwerk aufbewahren. Bei diesen Protokollen ignoriert der Routing Tabellen-Manager Unterschiede im Schnittstellen Index oder an der Adresse des nächsten Hops. Ein Beispiel für ein solches Protokoll ist die RRAS-Implementierung von Open kürzeste Path First (OSPF).

 

 




