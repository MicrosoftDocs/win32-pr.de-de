---
description: Die Peer Gruppierungs-API kombiniert die Technologie der PNRP-Namespace Anbieter-API und der grapherstellungsapi.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Informationen zur Gruppierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362238"
---
# <a name="about-the-grouping-api"></a>Informationen zur Gruppierungs-API

Die Peer Gruppierungs-API kombiniert die Technologie der PNRP-Namespace Anbieter-API und der [grapherstellungsapi](graphing-api.md). [](pnrp-namespace-provider-api.md) Durch die Gruppierung werden die folgenden zwei Teile der Technologie hinzugefügt:

-   Eine Multiplexing-Ebene, die es mehreren Anwendungen ermöglicht, ein Diagramm, einen Port und eine datensatzdatenbank zu verwenden.
-   Sicherheit, durch die sichergestellt wird, dass nur Peers, die in eine Gruppe eingeladen wurden, während der gesamten Lebensdauer einer Gruppe beitreten und

Die Gruppierung bietet eine barrierefreie und einfache Herangehensweise an das Peer Netzwerk aufgrund des einfachen aufrufflusses und sicheren Messaging. Diese API nutzt PNRP für die Gruppen Ermittlung und einen standardmäßigen PKI-basierten Sicherheitsanbieter, anstatt einen Entwickler zum Implementieren eines solchen zu benötigen. Wenn Ihre Anwendung jedoch mehr Flexibilität im Hinblick auf Sicherheitsoptionen erfordert, sollten Sie die [graphingapi](about-the-graphing-api.md)in Erwägung gezogen.

In der folgenden Tabelle sind die Themen dieses Gruppierungs-API-Abschnitts aufgeführt:

| Thema                                                                | BESCHREIBUNG                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Arbeiten mit Gruppen](how-to-work-with-groups.md)               | Beschreibt den Aufruffluss in einer Peer Gruppierungs Anwendung vom Start bis zum Herunterfahren.         |
| [Funktionsweise der Gruppen Sicherheit](how-group-security-works.md)             | Beschreibt, wie Peer Gruppenmitgliedschaft und Datenaustausch geschützt werden.                      |
| [Einladen eines Peers zu einer Gruppe](inviting-a-peer-to-a-group.md)         | Beschreibt den Prozess, mit dem Peers eingeladen und einer Peer Gruppe hinzugefügt werden.              |
| [Vorgehensweise beim Herstellen einer Verbindung mit einer Peer Gruppe](how-to-connect-to-a-peer-group.md) | Beschreibt, wie ein Peer eine Verbindung mit einer Peer Gruppe herstellt und mit dieser interagiert.                        |
| [Verwalten von Gruppendaten Sätzen](managing-group-records.md)                 | Beschreibt Peer Gruppen-Datensätze und deren Verwaltung als Mitglied und Administrator. |



 

> [!Note]  
> Anwendungen, die die Gruppierungs-API in einer Umgebung mit einer Firewall verwenden, benötigen Ausnahme Gruppen, die den für die Anwendung spezifischen Port abdecken, sowie den Port "3587-TCP" für die Gruppierungs-API und den Port "3540-UDP" für PNRP. Diese Ausnahme Gruppen sollten immer dann aktiviert werden, wenn die Anwendung ausgeführt wird.

 

 

 



