---
title: Informationen zum Multicast-Gruppen-Manager
description: In dieser Dokumentation wird die Technologie von Multicast Group Manager (MGM) beschrieben.
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- RRAS für Multicast-Gruppen-Manager
- RRAS für Multicast-Gruppen-Manager, beschrieben
- RRAS für den Routing-und RAS-Dienst, Multicast-Gruppen-Manager
- Routing-und RAS-Dienst RRAS, Multicast-Gruppen-Manager, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342058"
---
# <a name="about-multicast-group-manager"></a>Informationen zum Multicast-Gruppen-Manager

In dieser Dokumentation wird die Technologie von Multicast Group Manager (MGM) beschrieben.

Multicasting ermöglicht einem Host das Senden von Daten an nur die Ziele, die speziell den Empfang der Daten anfordern. Auf diese Weise unterscheidet sich Multicasting vom Senden von Broadcast Daten, da Broadcast Daten an alle Hosts gesendet werden.

Multicasting spart Netzwerkbandbreite, da Multicast Daten nur von den Hosts empfangen werden, von denen die Daten angefordert werden, und die Daten werden nur einmal über einen Link übertragen. Multicasting spart Server Bandbreite, da ein Server anstelle einer Unicastnachricht pro Empfänger nur eine Multicast Nachricht pro Netzwerk senden muss. Beispiele für beliebte Multicast Anwendungen sind Online Besprechungen und Internet Radio.

Die MGM-API ermöglicht Entwicklern das Schreiben von Multicast Routing Protokollen, die mit Routern interagieren, auf denen der Multicast-Gruppen-Manager ausgeführt wird.

Wenn mehr als ein Multicast Routing Protokoll auf einem Router aktiviert ist, koordiniert der Multicast-Gruppen-Manager die Vorgänge zwischen allen Routing Protokollen. Der Multicast-Gruppen-Manager informiert jedes Routing Protokoll, wenn Gruppen Mitgliedschafts Änderungen auftreten, und wenn Multicast Daten aus einer neuen Quelle oder einer neuen Gruppe empfangen werden.

Die MGM-API bietet die folgenden Features:

-   Protokoll Registrierung
-   Gruppenverwaltung
-   MFE-Enumeration (Multicast Weiterleitungs Eintrag)
-   Rückruf Definitionen für Multicast Routing Protokolle

In dieser Übersicht werden die Komponenten der Multicast Architektur, die Client Szenarien, die für die Zusammenarbeit mit dem Multicast-Gruppen-Manager verwendet werden, sowie Programmier Überlegungen für die Verwendung der MGM-API beschrieben.

 

 




