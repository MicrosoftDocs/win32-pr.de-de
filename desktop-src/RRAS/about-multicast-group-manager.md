---
title: Informationen zu Multicast Group Manager
description: In dieser Dokumentation wird die Multicast Group Manager-Technologie (MGM) beschrieben.
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- Multicast-Gruppen-Manager RRAS
- Multicast Group Manager RRAS , beschrieben
- Routing- und RAS-Dienst RRAS, Multicast-Gruppen-Manager
- Routing- und RAS-Dienst RRAS , Multicast-Gruppen-Manager, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f83dc2b212f7d70d04b4a3ec08bf07e664fa2d67d9c638233a4e8e914369c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030930"
---
# <a name="about-multicast-group-manager"></a>Informationen zu Multicast Group Manager

In dieser Dokumentation wird die Multicast Group Manager-Technologie (MGM) beschrieben.

Multicasting ermöglicht es einem Host, Daten nur an die Ziele zu senden, die speziell den Empfang der Daten anfordern. Auf diese Weise unterscheidet sich Multicasting vom Senden von Broadcastdaten, da Broadcastdaten an alle Hosts gesendet werden.

Multicasting spart Netzwerkbandbreite, da Multicastdaten nur von den Hosts empfangen werden, die die Daten anfordern, und die Daten nur einmal über einen beliebigen Link übertragen werden. Multicasting spart Serverbandbreite, da ein Server nur eine Multicastnachricht pro Netzwerk anstelle einer Unicastnachricht pro Empfänger senden muss. Beispiele für beliebte Multicastanwendungen sind Onlinebesprechungen und Internetfunk.

Mit der MGM-API können Entwickler Multicastroutingprotokolle schreiben, die mit Routern zusammenarbeiten, auf denen der Multicastgruppen-Manager ausgeführt wird.

Wenn mehr als ein Multicastroutingprotokoll auf einem Router aktiviert ist, koordiniert der Multicastgruppen-Manager Vorgänge zwischen allen Routingprotokollen. Der Multicastgruppen-Manager informiert jedes Routingprotokoll, wenn Änderungen an der Gruppenmitgliedschaft auftreten und Wenn Multicastdaten aus einer neuen Quelle oder für eine neue Gruppe empfangen werden.

Die MGM-API bietet die folgenden Features:

-   Protokollregistrierung
-   Gruppenverwaltung
-   MULTICAST-Weiterleitungseintragsenumeration (MFE)
-   Rückrufdefinitionen für Multicastroutingprotokolle

In dieser Übersicht werden die Komponenten der Multicastarchitektur, die Clientszenarien, die für die Interoperabilität mit dem Multicastgruppen-Manager verwendet werden, und Programmierüberlegungen für die Verwendung der MGM-API beschrieben.

 

 




