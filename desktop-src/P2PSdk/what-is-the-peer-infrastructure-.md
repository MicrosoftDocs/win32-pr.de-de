---
description: Die Peerinfrastruktur besteht aus mehreren APIs, die leistungsstark und flexibel sind.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: Was ist die Peerinfrastruktur?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e80a5cdcc190fe47ea0a37efd5348ec5f718eaff654543c68bd6e9d355d4d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119287640"
---
# <a name="what-is-the-peer-infrastructure"></a>Was ist die Peerinfrastruktur?

Die Peerinfrastruktur besteht aus mehreren APIs, die leistungsstark und flexibel sind. Die Hauptkomponenten umfassen Folgendes:

-   [Peergraphing-API](#peer-graphing-api)
-   [Peergruppierungs-API](#peer-grouping-api)
-   [PeerIdentitäts-Manager-API](#peer-identity-manager-api)
-   [PNRP-Namespaceanbieter-API](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a>Peergraphing-API

Die Peerinfrastruktur bietet eine Graphingtechnologie, die Informationen effizient und zuverlässig zwischen Peers in einem Peerdiagramm übergeben kann. Die [Peergraphing-API](graphing-api.md) stellt sicher, dass jeder Knoten über eine konsistente Ansicht der Daten in einem Diagramm verfügt.

Sie können die [Peergraphing-API](graphing-api.md) verwenden, um folgende Schritte zu erledigen:

-   Erstellen und Verwalten von Peerdiagrammen
-   Aufzählen und Interagieren mit anderen Peers in einem Peerdiagramm
-   Senden von Daten in Form eines [Datensatzes](records.md) an jeden Knoten in einem Peerdiagramm

## <a name="peer-grouping-api"></a>Peergruppierungs-API

Die [Peergruppierungs-API](grouping-api.md) kombiniert und erweitert die [Peer-PNRP-](#pnrp-namespace-provider-api) und [Graphing-APIs](#peer-graphing-api) und fügt die folgenden beiden Komponenten hinzu:

-   Eine Multiplexingebene, die es mehreren Anwendungen, die auf einer Peerentität ausgeführt werden, ermöglicht, eine Verbindung mit einer Gruppe herzustellen
-   Ein bestimmtes Sicherheitsmodell, das sicherstellt, dass nur Peers, die zu einer Gruppe eingeladen sind, über die Lebensdauer der Gruppe eine Verbindung mit der Gruppe herstellen können.

Sie können die Peergruppierungs-API für folgende Zwecke verwenden:

-   Erstellen und Verwalten sicherer Peergruppen
-   Aufzählen und Interagieren mit anderen Peers in einer Gruppe
-   Senden von Daten in Form eines [Datensatzes](records.md) an jeden Knoten in einer Peergruppe

## <a name="peer-identity-manager-api"></a>PeerIdentitäts-Manager-API

Mithilfe der [Peer Identity Manager-API](identity-manager-api.md) können Sie sichere [Peernamen](peer-names.md) erstellen, die PNRP verwenden kann, um sicherzustellen, dass eine Person, die einen Namen veröffentlicht, den Namen offiziell besitzt. Peernamen werden auch als Identitäten bezeichnet und in der Peergruppierungs-API verwendet, um die Personen in einer Gruppe zu identifizieren.

Sie können die [Peer Identity Manager-API](identity-manager-api.md) verwenden, um folgende Schritte zu erledigen:

-   Erstellen, Aufzählen und Verwalten von Peeridentitäten.

## <a name="pnrp-namespace-provider-api"></a>PNRP-Namespaceanbieter-API

Die Peerinfrastruktur stellt eine serverlose Namensauflösungstechnologie bereit, die als [PNRP-Namespaceanbieter-API](pnrp-namespace-provider-api.md)bezeichnet wird. Mithilfe der Winsock 2 PNRP-Namespaceanbieter-API kann ein Peer-, Dienst-, Computinggerät- und Peergruppenendpunkt einen anderen Endpunkt in einer [PNRP-Cloud](clouds.md)verwalten, registrieren, aufheben und auflösen.

> [!Note]  
> PNRP ist ein Akronym für **das Peernamensauflösungsprotokoll**.

 

 

 



