---
description: Die Peergruppierungs-API kombiniert die Technologie der PNRP-Namensraumanbieter-API und der Graphing-API.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Informationen zur Gruppierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b4cd1b2783d7605f9198e3c8171177e70b531944a8f2f707def5750dd6d985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612794"
---
# <a name="about-the-grouping-api"></a>Informationen zur Gruppierungs-API

Die Peergruppierungs-API kombiniert die Technologie der [PNRP-Namensraumanbieter-API](pnrp-namespace-provider-api.md) und der [Graphing-API.](graphing-api.md) Die Gruppierung fügt die folgenden beiden Technologieteile hinzu:

-   Eine Multiplexingebene, die es mehreren Anwendungen ermöglicht, ein Diagramm, einen Port und eine Datensatzdatenbank zu verwenden.
-   Sicherheit, die sicherstellt, dass nur Peers, die zu einer Gruppe eingeladen sind, während der gesamten Lebensdauer einer Gruppe beitreten und eine Verbindung herstellen können.

Die Gruppierung bietet aufgrund des einfachen Anrufflusses und des sicheren Messagings einen zugänglichen und einfachen Ansatz für Peernetzwerke. Diese API verwendet PNRP für die Gruppenermittlung und einen PKI-basierten Standardsicherheitsanbieter, anstatt dass ein Entwickler einen implementieren muss. Wenn Ihre Anwendung jedoch mehr Flexibilität in Bezug auf Sicherheitsoptionen erfordert, sollten Sie die [Graphing-API](about-the-graphing-api.md)verwenden.

In der folgenden Tabelle sind die Themen in diesem Abschnitt zur Gruppierungs-API aufgeführt:

| Thema                                                                | Beschreibung                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Arbeiten mit Gruppen](how-to-work-with-groups.md)               | Beschreibt den Aufruffluss in einer Peergruppierungsanwendung vom Start bis zum Herunterfahren.         |
| [Funktionsweise der Gruppensicherheit](how-group-security-works.md)             | Beschreibt, wie Peergruppenmitgliedschaften und Datenaustausche geschützt werden.                      |
| [Einladen eines Peers zu einer Gruppe](inviting-a-peer-to-a-group.md)         | Beschreibt den Prozess, mit dem Peers eingeladen und einer Peergruppe hinzugefügt werden.              |
| [Verbinden zu einer Peergruppe](how-to-connect-to-a-peer-group.md) | Beschreibt, wie ein Peer eine Verbindung mit einer Peergruppe herstellt und mit dieser interagiert.                        |
| [Verwalten von Gruppendatensätzen](managing-group-records.md)                 | Beschreibt Peergruppendatensätze und ihre Verwaltung als Mitglied und Administrator. |



 

> [!Note]  
> Anwendungen, die die Gruppierungs-API in einer Umgebung mit einer Firewall verwenden, erfordern Ausnahmegruppen, die den anwendungsspezifischen Port abdecken, sowie Port "3587-TCP" für die Gruppierungs-API und Port "3540-UDP" für PNRP. Diese Ausnahmegruppen sollten immer dann aktiviert werden, wenn die Anwendung ausgeführt wird.

 

 

 



