---
description: Die Peer Infrastruktur ist eine Reihe von verschiedenen APIs, die leistungsstark und flexibel sind.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: Was ist die Peer Infrastruktur?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362472"
---
# <a name="what-is-the-peer-infrastructure"></a>Was ist die Peer Infrastruktur?

Die Peer Infrastruktur ist eine Reihe von verschiedenen APIs, die leistungsstark und flexibel sind. Die Hauptkomponenten umfassen Folgendes:

-   [Peer graphende-API](#peer-graphing-api)
-   [Peer Gruppierungs-API](#peer-grouping-api)
-   [Peer Identity Manager-API](#peer-identity-manager-api)
-   [PNRP-Namespace Anbieter-API](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a>Peer graphende-API

Die Peer Infrastruktur bietet eine graphingtechnologie, die Informationen effizient und zuverlässig zwischen Peers in einem Peer Diagramm übergibt. Die [Peer graphende-API](graphing-api.md) stellt sicher, dass jeder Knoten über eine konsistente Sicht der Daten in einem Diagramm verfügt.

Mit der [Peer graphingapi](graphing-api.md) können Sie folgende Aufgaben ausführen:

-   Erstellen und Verwalten von Peer Diagrammen
-   Auflisten von und interagieren mit anderen Peers in einem Peer Diagramm
-   Senden von Daten in Form eines Daten [Satzes](records.md) an jeden Knoten in einem Peer Diagramm

## <a name="peer-grouping-api"></a>Peer Gruppierungs-API

Die [Peer Gruppierungs-API](grouping-api.md) kombiniert und erweitert die Peer- [PNRP](#pnrp-namespace-provider-api) -und [graphingapis](#peer-graphing-api) und fügt die folgenden beiden Komponenten hinzu:

-   Eine Multiplexing-Ebene, die es ermöglicht, dass mehrere Anwendungen auf einer Peer Entität eine Verbindung mit einer Gruppe herstellen.
-   Ein bestimmtes Sicherheitsmodell, das sicherstellt, dass nur Peers, die an eine Gruppe eingeladen wurden, über die Lebensdauer der Gruppe eine Verbindung mit der Gruppe herstellen

Mit der Peer Gruppierungs-API können Sie folgende Aufgaben ausführen:

-   Erstellen und Verwalten von sicheren Peer Gruppen
-   Auflisten von und interagieren mit anderen Peers in einer Gruppe
-   Senden von Daten in Form eines Daten [Satzes](records.md) an jeden Knoten in einer Peer Gruppe

## <a name="peer-identity-manager-api"></a>Peer Identity Manager-API

Mithilfe der [Peer Identity Manager-API](identity-manager-api.md) können Sie sichere [Peer Namen](peer-names.md) erstellen, mit denen PNRP sicherstellen kann, dass eine Person, die einen Namen veröffentlicht, den Namen offiziell besitzt. Peer Namen werden auch als Identitäten bezeichnet und in der Peer Gruppierungs-API verwendet, um die einzelnen Personen in einer Gruppe zu identifizieren.

Mit der [Peer Identity Manager-API](identity-manager-api.md) können Sie folgende Aufgaben ausführen:

-   Erstellen, auflisten und Verwalten von Peer Identitäten.

## <a name="pnrp-namespace-provider-api"></a>PNRP-Namespace Anbieter-API

Die Peer Infrastruktur bietet eine Server lose namens Auflösungs Technologie, die als [PNRP-Namespace Anbieter-API](pnrp-namespace-provider-api.md)bezeichnet wird. Mithilfe der Anbieter-API für den Winsock 2-PNRP-Namespace können Peer-, Dienst-, Computer-und Peer Gruppen Endpunkte einen anderen Endpunkt in einer PNRP- [Cloud](clouds.md)verwalten, registrieren, seine Registrierung aufheben und auflösen.

> [!Note]  
> PNRP ist ein Akronym für das **Peer Name Resolution-Protokoll**.

 

 

 



