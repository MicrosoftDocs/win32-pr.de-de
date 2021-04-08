---
description: Peer-to-Peer-Netzwerke sind eine Server lose Netzwerktechnologie, die es mehreren Netzwerkgeräten ermöglicht, Ressourcen gemeinsam zu nutzen und direkt miteinander zu kommunizieren.
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: Was ist Peer Netzwerk?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c456fac9b7695a2846765ee0ccd38c1e5df646e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959776"
---
# <a name="what-is-peer-networking"></a>Was ist Peer Netzwerk?

Peer-to-Peer-Netzwerke sind eine Server lose Netzwerktechnologie, die es mehreren Netzwerkgeräten ermöglicht, Ressourcen gemeinsam zu nutzen und direkt miteinander zu kommunizieren. Diese Technologie ist für Windows XP mit Service Pack 1 (SP1) und spätere Clients verfügbar, auf denen das erweiterte Netzwerk Paket für die Peer-to-Peer-Infrastruktur ausgeführt wird.

Die Peer-to-Peer-Infrastruktur ist ein Satz von Netzwerk-APIs, mit denen Sie dezentralisierte Netzwerkanwendungen entwickeln können, die die gemeinsame Leistung von Computern in einem Netzwerk nutzen. Peer-to-Peer-Anwendungen können z. b. Kollaborations Kommunikation, Technologien zur Inhalts Verteilung usw. sein.

Die Peer-to-Peer-Infrastruktur bietet eine solide Netzwerkinfrastruktur, sodass Sie sich auf die Anwendungsentwicklung konzentrieren können, da die Infrastruktur für Sie entwickelt wurde.

Die Peer-to-Peer-Infrastruktur umfasst die folgenden Hauptkomponenten:

-   [Skalierbare und sichere Peer Namensauflösung](#scalable-and-secure-peer-name-resolution)
-   [Effiziente Multipoint-Kommunikation](#efficient-multipoint-communication)
-   [Verwaltung verteilter Daten](#distributed-data-management)
-   [Sichere Peer Identitäten](#secure-peer-identities)
-   [Sichern von Peer-zu-Peer-Gruppen](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a>Skalierbare und sichere Peer Namensauflösung

Die [PNRP-Namespace Anbieter-API (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) ist ein namens-zu-IP-Auflösungs Protokoll. Der IPv6-Bereich oder der IPv6-Kontext, der alle teilnehmenden Peers einschließt, wird als [Cloud](clouds.md)bezeichnet. PNRP ermöglicht Peers die Interaktion untereinander in einer Cloud.

## <a name="efficient-multipoint-communication"></a>Effiziente Multipoint-Kommunikation

Die Peer-to-Peer-Infrastruktur umfasst die [graphende-API](graphing-api.md) , die eine effiziente Multipoint-Kommunikation bereitstellt. Wie bei PNRP ermöglicht die Peer-zu-Peer-Darstellung die Interaktion einer Gruppe von Knoten und das Übergeben von Daten an und von einander in Form eines [Datensatzes](records.md). Jeder Datensatz, der von einem Peer generiert oder aktualisiert wird, wird an alle Knoten in einem Diagramm gesendet.

## <a name="distributed-data-management"></a>Verteilte Datenverwaltung

Die Verwaltung verteilter Daten speichert automatisch alle Datensätze, die an ein Peer-to-Peer-Diagramm gesendet werden, bis zur angegebenen Ablaufzeit für jeden Datensatz. Peer-to-Peer-Netzwerke stellen sicher, dass jeder Knoten in einem Peer-zu-Peer-Diagramm eine ähnliche Ansicht der datensatzdatenbank aufweist. Wenn einem Peer-zu-Peer-Diagramm ein Sicherheitsmodell zugeordnet ist, enthält das Diagramm die folgenden Informationen:

-   Wer kann keine Verbindung mit einem Diagramm herstellen?
-   Wer kann Datensätze basierend auf extern definierten Kriterien sichern und validieren

## <a name="secure-peer-identities"></a>Sichere Peer Identitäten

Die Peer-to-Peer-Infrastruktur stellt eine Peer-to-Peer- [Identitäts-Manager-API](identity-manager-api.md) bereit, die Ihnen das Erstellen, verwalten und manipulieren von Peer Identitäten ermöglicht. Peer Identitäten werden zum Definieren von Namen für sichere Endpunkte in PNRP verwendet und können beliebige Ressourcen darstellen, die an einem Peer-zu-Peer-Netzwerk beteiligt sind, einschließlich sicherer Peer-to-Peer-Gruppen und-Dienste.

## <a name="secure-peer-to-peer-groups"></a>Sichern von Peer-zu-Peer-Gruppen

Die Peer-to-Peer- [Gruppierungs-API](grouping-api.md) kombiniert die Peer-to-Peer-Graphing-, Identity Manager-und PNRP-APIs, um eine kohärente und bequeme Lösung für die Entwicklung von Peer-zu-Peer-Netzwerkanwendungen zu bilden. Die Peer-to-Peer-Gruppierungs-API verwendet die Peer-to-Peer-Identitäts-Manager-API und ein selbst signiertes Zertifikat Schema, um die Sicherheit innerhalb der graphinginfrastruktur sicherzustellen. Jede Gruppe kann über PNRP aufgelöst und registriert werden, was die Namensauflösung zufälliger Peers innerhalb einer registrierten Peer-to-Peer-Gruppe ermöglicht. Eine Gruppe kann ein Endpunkt in PNRP sein, ebenso wie ein Peer.

Eine Übersicht über die Peer-to-Peer-Infrastruktur finden Sie im Artikel "[Einführung in Windows XP-Peer-to-Peer-Netzwerke](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)".

Eine Übersicht über die APIs in der Peer-zu-Peer-Infrastruktur finden Sie im Thema [Was ist die Peer Infrastruktur?](what-is-the-peer-infrastructure-.md).

 

 



