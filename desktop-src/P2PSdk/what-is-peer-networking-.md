---
description: Peer-zu-Peer-Netzwerke ist eine serverlose Netzwerktechnologie, die es mehreren Netzwerkgeräten ermöglicht, Ressourcen freizugeben und direkt miteinander zu kommunizieren.
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: Was ist Peernetzwerk?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f6ce2175aa32e37c80c4cde5c231540a48c448360974ecbd022c21eb552ccdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034100"
---
# <a name="what-is-peer-networking"></a>Was ist Peernetzwerk?

Peer-zu-Peer-Netzwerke ist eine serverlose Netzwerktechnologie, die es mehreren Netzwerkgeräten ermöglicht, Ressourcen freizugeben und direkt miteinander zu kommunizieren. Diese Technologie ist für Windows XP mit Service Pack 1 (SP1) und höheren Clients verfügbar, auf denen das Advanced Networking Pack für die Peer-zu-Peer-Infrastruktur ausgeführt wird.

Die Peer-zu-Peer-Infrastruktur ist eine Reihe von Netzwerk-APIs, mit denen Sie dezentralisierte Netzwerkanwendungen entwickeln können, die die gemeinsame Leistungsfähigkeit von Computern in einem Netzwerk nutzen. Peer-zu-Peer-Anwendungen können z. B. gemeinsame Kommunikation, Technologien für die Inhaltsverteilung usw. sein.

Die Peer-zu-Peer-Infrastruktur bietet eine solide Netzwerkinfrastruktur, sodass Sie sich auf die Entwicklung von Anwendungen konzentrieren können, da die Infrastruktur für Sie entwickelt wird.

Die Peer-zu-Peer-Infrastruktur umfasst die folgenden Hauptkomponenten:

-   [Skalierbare und sichere Peernamensauflösung](#scalable-and-secure-peer-name-resolution)
-   [Effiziente Multipointkommunikation](#efficient-multipoint-communication)
-   [Verteilte Datenverwaltung](#distributed-data-management)
-   [Schützen von Peeridentitäten](#secure-peer-identities)
-   [Schützen von Peer-zu-Peer-Gruppen](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a>Skalierbare und sichere Peernamensauflösung

Die [PNRP-Namespaceanbieter-API (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) ist ein Namens-zu-IP-Auflösungsprotokoll. Der IPv6-Bereich oder -Kontext, der alle beteiligten Peers enthält, wird als [Cloud](clouds.md)bezeichnet. PNRP ermöglicht Peers die Interaktion untereinander innerhalb einer Cloud.

## <a name="efficient-multipoint-communication"></a>Effiziente Multipointkommunikation

Die Peer-zu-Peer-Infrastruktur enthält die [Graphing-API,](graphing-api.md) die eine effiziente Multipointkommunikation ermöglicht. Wie PNRP ermöglicht peer-to-peer graphing eine Gruppe von Knoten zu interagieren und Daten in Form eines [Datensatzes](records.md)an und von einander zu übergeben. Jeder Datensatz, den ein Peer generiert oder aktualisiert, wird an alle Knoten in einem Diagramm gesendet.

## <a name="distributed-data-management"></a>Verteilte Datenverwaltung

Die verteilte Datenverwaltung speichert automatisch alle An peer-to-Peer-Diagramme gesendeten Datensätze bis zur angegebenen Ablaufzeit für jeden Datensatz. Peer-zu-Peer-Netzwerke stellen sicher, dass jeder Knoten in einem Peer-zu-Peer-Diagramm über eine ähnliche Ansicht der Datensatzdatenbank verfügt. Wenn einem Peer-zu-Peer-Diagramm ein Sicherheitsmodell zugeordnet ist, enthält das Diagramm die folgenden Informationen:

-   Wer können und können keine Verbindung mit einem Diagramm herstellen.
-   Wer können Datensätze basierend auf extern definierten Kriterien sichern und überprüfen.

## <a name="secure-peer-identities"></a>Schützen von Peeridentitäten

Die Peer-zu-Peer-Infrastruktur bietet eine Peer-to-Peer [Identity Manager-API,](identity-manager-api.md) mit der Sie die Peeridentitäten erstellen, verwalten und bearbeiten können. Peeridentitäten werden verwendet, um Namen für sichere Endpunkte in PNRP zu definieren, und können jede Ressource darstellen, die an einem Peer-zu-Peer-Netzwerk beteiligt ist, einschließlich sicherer Peer-zu-Peer-Gruppen und -Dienste.

## <a name="secure-peer-to-peer-groups"></a>Schützen von Peer-zu-Peer-Gruppen

Die [Peer-zu-Peer-Gruppierungs-API](grouping-api.md) kombiniert die Peer-zu-Peer-Graphing-, Identity Manager- und PNRP-APIs zu einer zusammenhängenden und praktischen Lösung für die Entwicklung von Peer-zu-Peer-Netzwerkanwendungen. Die Peer-zu-Peer-Gruppierungs-API verwendet die Peer-to-Peer Identity Manager-API und ein selbstsigniertes Zertifikatschema, um die Sicherheit innerhalb der Graphinginfrastruktur sicherzustellen. Jede Gruppe kann über PNRP aufgelöst und registriert werden, wodurch die Namensauflösung zufälliger Peers innerhalb einer registrierten Peer-zu-Peer-Gruppe ermöglicht wird. Eine Gruppe kann wie ein Peer ein Endpunkt in PNRP sein.

Eine Übersicht über die Peer-zu-Peer-Infrastruktur finden Sie im Artikel[Einführung in Windows XP-Peer-zu-Peer-Netzwerke.](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)

Eine Übersicht über die APIs in der Peer-zu-Peer-Infrastruktur finden Sie im Thema [Was ist die Peerinfrastruktur?](what-is-the-peer-infrastructure-.md).

 

 



