---
title: Statische und automatische statische Routen
description: In der Regel werden Routen zu Remote Netzwerken durch Routing Protokolle dynamisch abgerufen.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947997"
---
# <a name="static-and-autostatic-routes"></a><span data-ttu-id="a0cce-103">Statische und automatische statische Routen</span><span class="sxs-lookup"><span data-stu-id="a0cce-103">Static and Autostatic Routes</span></span>

<span data-ttu-id="a0cce-104">In der Regel werden Routen zu Remote Netzwerken durch Routing Protokolle dynamisch abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a0cce-104">Typically, routes to remote networks are obtained dynamically through routing protocols.</span></span> <span data-ttu-id="a0cce-105">*Der Administrator kann jedoch auch einen* Ausgangs Ausgangs für die Routing Tabelle angeben, indem er Routen manuell bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a0cce-105">However, the administrator can also *seed* the routing table by providing routes manually.</span></span> <span data-ttu-id="a0cce-106">Diese Routen werden als *statisch* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a0cce-106">These routes are referred to as *static*.</span></span> <span data-ttu-id="a0cce-107">Eine statische Route ist einer Schnittstelle zugeordnet, die das Remote Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0cce-107">A static route is associated with an interface that represents the remote network.</span></span> <span data-ttu-id="a0cce-108">Im Gegensatz zu dynamischen Routen werden statische Routen auch dann beibehalten, wenn der Router neu gestartet wird oder die Schnittstelle deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a0cce-108">Unlike dynamic routes, static routes are retained even if the router is restarted or the interface is disabled.</span></span>

<span data-ttu-id="a0cce-109">Eine *Automatische statische* Route wird durch ein Routing Protokoll abgerufen, aber sobald Sie sich wie eine statische Route verhält, verhält sie sich.</span><span class="sxs-lookup"><span data-stu-id="a0cce-109">An *autostatic* route is obtained through a routing protocol, but once obtained behaves like a static route.</span></span> <span data-ttu-id="a0cce-110">Der Vorgang zum Abrufen von automatisch statischen Routen lautet wie folgt: der IP-oder IPX-routermanager gibt eine Anforderung aus, dass ein Routing Protokoll die Routing Informationen für eine bestimmte Schnittstelle aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a0cce-110">The process for obtaining autostatic routes is as follows: The IP or IPX router manager issues a request that a routing protocol update the routing information for a specific interface.</span></span> <span data-ttu-id="a0cce-111">Die Ergebnisse des Updates werden dann in statische Routen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="a0cce-111">The results of the update are then converted into static routes.</span></span> <span data-ttu-id="a0cce-112">Beachten Sie, dass nur bestimmte Routing Protokolle Anforderungen für automatische, statische Routen Aktualisierungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a0cce-112">Note that only certain routing protocols support requests for autostatic route updates.</span></span>

 

 




