---
description: Internet Protocol Helper (IP-Hilfsobjekt) unterstützt die Netzwerkverwaltung des lokalen Computers, indem es Anwendungen ermöglicht, Informationen zur Netzwerkkonfiguration des lokalen Computers abzurufen und diese Konfiguration zu ändern.
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50587b4abdcbad0cddd6d6ce3281c908fdebef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041756"
---
# <a name="about-ip-helper"></a>Info

Internet Protocol Helper (IP-Hilfsobjekt) unterstützt die Netzwerkverwaltung des lokalen Computers, indem es Anwendungen ermöglicht, Informationen zur Netzwerkkonfiguration des lokalen Computers abzurufen und diese Konfiguration zu ändern. IP-Hilfsprogramm stellt außerdem Benachrichtigungsmechanismen bereit, um sicherzustellen, dass eine Anwendung benachrichtigt wird, wenn bestimmte Aspekte der Netzwerkkonfiguration des lokalen Computers geändert werden.

Viele der IP-Hilfsfunktionen übergeben Struktur Parameter, die Datentypen darstellen, die der [Verwaltungs Informationsbasis](/previous-versions/windows/desktop/mib/about-management-information-base) Technologie zugeordnet sind. Die IP-Hilfsfunktionen verwenden diese Strukturen, um verschiedene Netzwerkinformationen darzustellen, wie z. b. ARP-Cache Einträge. Da diese Strukturen auch von der MIB-API verwendet werden, werden Sie in der [Referenz zur Basis der Verwaltungsinformationen](/previous-versions/windows/desktop/mib/management-information-base-reference)beschrieben. Obwohl die IP-hilfsprogrammapi diese Strukturen verwendet, unterscheidet sich das IP-Hilfsprogramm von der Management Information Base (MIB) und dem Simple Network Management-Protokoll (SNMP).

In der IP-Hilfsdokumentation werden die Begriffe "Adapter" und "Interface" ausführlich verwendet. Bei einem "Adapter" handelt es sich um einen veralteten Begriff, bei dem es sich um eine abgekürzte Form von Netzwerkadaptern handelt, die ursprünglich auf Netzwerkhardware verwiesen Ein Adapter ist eine Abstraktion auf DataLink-Ebene.

Eine "Schnittstelle" ist ein neuer Begriff, der in den IETF RFC-Dokumenten verwendet wird. Die RFCs definieren eine Schnittstelle als abstraktes Konzept, das die Anlage eines Knotens zu einem Link darstellt. Eine Schnittstelle ist eine Abstraktion auf IP-Ebene.

Die Adapter-und Schnittstellen Begriffe werden in der IP-Hilfsobjekt etwas austauschbar verwendet. In der IP-hilfsobjektive kann eine Liste von Adaptern eine Software-WAN-Schnittstelle und die Loopback Schnittstelle enthalten (keines dieser Verweise bezieht sich auf ein Hardware Gerät). In den IP-Hilfsobjekten gibt es eine eins-zu-Eins-Zuordnung von Adaptern zu Schnittstellen.

IP Helper bietet Funktionen in den folgenden Bereichen:

-   [Abrufen von Informationen zur Netzwerkkonfiguration](retrieving-information-about-network-configuration.md)
-   [Verwalten von Netzwerkadaptern](managing-network-adapters.md)
-   [Verwalten von Schnittstellen](managing-interfaces.md)
-   [Verwalten von IP-Adressen](managing-ip-addresses.md)
-   [Verwenden des adressauflösungsprotokolls](using-the-address-resolution-protocol.md)
-   [Abrufen von Informationen über das Internetprotokoll und das Internet Control Message-Protokoll](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [Verwalten des Routings](managing-routing.md)
-   [Empfangen von Benachrichtigungen über Netzwerkereignisse](receiving-notification-of-network-events.md)
-   [Abrufen von Informationen über das Transmission Control-Protokoll und das User Datagram-Protokoll](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 
