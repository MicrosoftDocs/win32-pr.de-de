---
title: Routerinitialisierung
description: Konfigurationsinformationen für den Router, die Router-Manager und die Routing Protokolle/-Clients werden in globale Informationen und Schnittstellen Informationen unterteilt und in der Registrierung und in der Telefonbuchdatei Router. pbk des Routers gespeichert.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- routerrras, Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707049"
---
# <a name="router-initialization"></a>Routerinitialisierung

Konfigurationsinformationen für den Router, die Router-Manager und die Routing Protokolle/-Clients werden in globale Informationen und Schnittstellen Informationen unterteilt und in der Registrierung und in der Telefonbuchdatei Router. pbk des Routers gespeichert.

Wenn der Routerprozess gestartet wird, liest Dim (Dynamic Interface Manager) die Routerkonfiguration aus der Registrierung. Dim erstellt die Schnittstellen, die von den Schnittstellen Informationen angegeben werden.

Dim ruft auch die Informationen des globalen routermanagers ab. Dim startet die routermanager, die diesen Informationen entsprechen, und übergibt Ihnen die Informationen. Wenn Dim beispielsweise globale Informationen für den IP-routermanager in der Registrierung findet, startet Dim den IP-routermanager und übergibt die globalen Informationen. Wenn für einen bestimmten routermanager keine globalen Informationen in der Registrierung vorhanden sind, wird der Router-Manager von Dim nicht gestartet.

Die routermanager untersuchen die globalen Informationen, die von Dim empfangen werden. Wenn der routermanager Informationen zu einem bestimmten Client innerhalb der globalen Informationen findet, lädt der routermanager die DLL für den Client (z. b. IpNAT.dll) und initialisiert den Client durch Aufrufen der [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) -und [**startprotocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) -Funktionen des Clients. Der routermanager übergibt die Client spezifischen globalen Informationen im Aufrufen von [**startprotocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)an den Client.

In jeder Phase sind die Informationen, die an die nächste Entität weitergegeben werden, für die vorangehende Entität nicht transparent. Das heißt, Dim interpretiert nicht die globalen Informationen für den IP-routermanager, außer der Tatsache, dass die Informationen für den IP-routermanager gedacht sind. Ebenso interpretiert der IP-Router-Manager die OSPF-spezifischen Informationen nicht so, als ob es sich um OSPF-Informationen handelt.

 

 




