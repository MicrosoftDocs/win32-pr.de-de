---
description: Das Internetprotokollhilfs-Hilf hilft bei der Netzwerkverwaltung des lokalen Computers, indem Es Anwendungen ermöglicht wird, Informationen zur Netzwerkkonfiguration des lokalen Computers abzurufen und diese Konfiguration zu ändern.
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: Informationen zum IP-Hilf hilft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77445eb999b08bda038fbffc4de5d440b7a3e79c3fa921d50f6da4ccc1f42237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014188"
---
# <a name="about-ip-helper"></a>Informationen zum IP-Hilf hilft

Das Internetprotokollhilfs-Hilf hilft bei der Netzwerkverwaltung des lokalen Computers, indem Es Anwendungen ermöglicht wird, Informationen zur Netzwerkkonfiguration des lokalen Computers abzurufen und diese Konfiguration zu ändern. Das IP-Hilfssystem stellt auch Benachrichtigungsmechanismen bereit, um sicherzustellen, dass eine Anwendung benachrichtigt wird, wenn bestimmte Aspekte der Netzwerkkonfiguration des lokalen Computers geändert werden.

Viele der IP-Hilfsfunktionen übergeben Strukturparameter, die Datentypen darstellen, die der [Management Information Base-Technologie](/previous-versions/windows/desktop/mib/about-management-information-base) zugeordnet sind. Die IP-Hilfsfunktionen verwenden diese Strukturen, um verschiedene Netzwerkinformationen darzustellen, z. B. ARP-Cacheeinträge. Da diese Strukturen auch von der MIB-API verwendet werden, werden sie in der Referenz zur [Verwaltungsinformationsbasis](/previous-versions/windows/desktop/mib/management-information-base-reference)beschrieben. Obwohl die IP-Hilfs-API diese Strukturen verwendet, unterscheidet sich die IP-Hilfe von der Verwaltungsinformationsbasis (MIB) und dem Simple Network Management Protocol (SNMP).

In der Dokumentation des IP-Hilfers werden die Begriffe "Adapter" und "Schnittstelle" ausführlich verwendet. Ein "Adapter" ist ein veralteter Begriff, der eine abgekürzte Form des Netzwerkadapters ist, der ursprünglich auf eine Form von Netzwerkhardware verwiesen wurde. Ein Adapter ist eine Abstraktion auf Datenverknüpfungsebene.

Eine "Schnittstelle" ist ein neuerer Begriff, der in den IETF RFC-Dokumenten verwendet wird. Die RFCs definieren eine Schnittstelle als abstraktes Konzept, das die Verknüpfung eines Knotens darstellt. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene.

Die Begriffe "Adapter" und "Schnittstelle" werden in der IP-Hilfedokumentation etwas austauschbar verwendet. In der Dokumentation des IP-Hilfsprogrammes kann eine Liste von Adaptern eine Software-WAN-Schnittstelle sowie die Loopbackschnittstelle enthalten (keiner davon bezieht sich auf ein Hardwaregerät). In den IP-Hilfs-APIs gibt es eine 1:1-Zuordnung von Adaptern zu Schnittstellen.

Das IP-Hilfsfunktionen bietet Funktionen in den folgenden Bereichen:

-   [Abrufen von Informationen zur Netzwerkkonfiguration](retrieving-information-about-network-configuration.md)
-   [Verwalten von Netzwerkadaptern](managing-network-adapters.md)
-   [Verwalten von Schnittstellen](managing-interfaces.md)
-   [Verwalten von IP-Adressen](managing-ip-addresses.md)
-   [Verwenden des Address Resolution-Protokolls](using-the-address-resolution-protocol.md)
-   [Abrufen von Informationen über das Internetprotokoll und das Internet Control Message Protocol](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [Verwalten des Routings](managing-routing.md)
-   [Empfangen von Benachrichtigungen über Netzwerkereignisse](receiving-notification-of-network-events.md)
-   [Abrufen von Informationen über das Transmission Control-Protokoll und das User Datagram-Protokoll](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 
