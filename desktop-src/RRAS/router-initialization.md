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
# <a name="router-initialization"></a><span data-ttu-id="e53b6-104">Routerinitialisierung</span><span class="sxs-lookup"><span data-stu-id="e53b6-104">Router Initialization</span></span>

<span data-ttu-id="e53b6-105">Konfigurationsinformationen für den Router, die Router-Manager und die Routing Protokolle/-Clients werden in globale Informationen und Schnittstellen Informationen unterteilt und in der Registrierung und in der Telefonbuchdatei Router. pbk des Routers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e53b6-105">Configuration information for the router, the router managers and the routing protocols/clients is divided into global information and per interface information and is stored in the registry and the router's phone-book file, Router.pbk.</span></span>

<span data-ttu-id="e53b6-106">Wenn der Routerprozess gestartet wird, liest Dim (Dynamic Interface Manager) die Routerkonfiguration aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="e53b6-106">When the router process starts, DIM (Dynamic Interface Manager) reads the router configuration from the registry.</span></span> <span data-ttu-id="e53b6-107">Dim erstellt die Schnittstellen, die von den Schnittstellen Informationen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e53b6-107">DIM creates the interfaces that are specified by the interface information.</span></span>

<span data-ttu-id="e53b6-108">Dim ruft auch die Informationen des globalen routermanagers ab.</span><span class="sxs-lookup"><span data-stu-id="e53b6-108">DIM also retrieves the global router manager information.</span></span> <span data-ttu-id="e53b6-109">Dim startet die routermanager, die diesen Informationen entsprechen, und übergibt Ihnen die Informationen.</span><span class="sxs-lookup"><span data-stu-id="e53b6-109">DIM starts the router managers that correspond to this information, and passes them the information.</span></span> <span data-ttu-id="e53b6-110">Wenn Dim beispielsweise globale Informationen für den IP-routermanager in der Registrierung findet, startet Dim den IP-routermanager und übergibt die globalen Informationen.</span><span class="sxs-lookup"><span data-stu-id="e53b6-110">For example, if DIM finds global information for the IP router manager in the registry, DIM starts the IP router manager and passes it the global information.</span></span> <span data-ttu-id="e53b6-111">Wenn für einen bestimmten routermanager keine globalen Informationen in der Registrierung vorhanden sind, wird der Router-Manager von Dim nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="e53b6-111">If no global information is present in the registry for a particular router manager, DIM does not start that router manager.</span></span>

<span data-ttu-id="e53b6-112">Die routermanager untersuchen die globalen Informationen, die von Dim empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="e53b6-112">The router managers examine the global information received from DIM.</span></span> <span data-ttu-id="e53b6-113">Wenn der routermanager Informationen zu einem bestimmten Client innerhalb der globalen Informationen findet, lädt der routermanager die DLL für den Client (z. b. IpNAT.dll) und initialisiert den Client durch Aufrufen der [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) -und [**startprotocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) -Funktionen des Clients.</span><span class="sxs-lookup"><span data-stu-id="e53b6-113">If the router manager finds information specific to a particular client within the global information, the router manager loads the DLL for the client (for example IpNAT.dll) and initializes the client by calling the client's [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) and [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) functions.</span></span> <span data-ttu-id="e53b6-114">Der routermanager übergibt die Client spezifischen globalen Informationen im Aufrufen von [**startprotocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)an den Client.</span><span class="sxs-lookup"><span data-stu-id="e53b6-114">The router manager passes the client-specific global information to the client in the call to [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span></span>

<span data-ttu-id="e53b6-115">In jeder Phase sind die Informationen, die an die nächste Entität weitergegeben werden, für die vorangehende Entität nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="e53b6-115">At each stage, the information being passed to the next entity is opaque to the entity preceding it.</span></span> <span data-ttu-id="e53b6-116">Das heißt, Dim interpretiert nicht die globalen Informationen für den IP-routermanager, außer der Tatsache, dass die Informationen für den IP-routermanager gedacht sind.</span><span class="sxs-lookup"><span data-stu-id="e53b6-116">That is, DIM does not interpret the global information for the IP Router Manager, beyond the fact that the information is meant for the IP Router Manager.</span></span> <span data-ttu-id="e53b6-117">Ebenso interpretiert der IP-Router-Manager die OSPF-spezifischen Informationen nicht so, als ob es sich um OSPF-Informationen handelt.</span><span class="sxs-lookup"><span data-stu-id="e53b6-117">Similarly, the IP Router Manager does not interpret the OSPF specific information beyond the fact that it is OSPF information.</span></span>

 

 




