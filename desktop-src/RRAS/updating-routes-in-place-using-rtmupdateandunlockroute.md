---
title: Direktes Aktualisieren von Routen mithilfe von rtmupdateandunlockroute
description: Eine direkte Aktualisierung ist im Allgemeinen effizienter als das Aktualisieren der Routing Tabelle mit einer indirekten Methode, z. b. der von der rtmaddroutededest-Funktion verwendeten Methode.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037121"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="15409-103">Direktes Aktualisieren von Routen mithilfe von rtmupdateandunlockroute</span><span class="sxs-lookup"><span data-stu-id="15409-103">Updating Routes In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="15409-104">Eine direkte Aktualisierung ist im Allgemeinen effizienter als das Aktualisieren der Routing Tabelle mit einer indirekten Methode, z. b. der von der [**rtmaddroutededest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) -Funktion verwendeten Methode.</span><span class="sxs-lookup"><span data-stu-id="15409-104">Updating in place is generally more efficient than updating the routing table with an indirect method such as that used by the [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) function.</span></span> <span data-ttu-id="15409-105">Diese Methode ist effizienter, da der Client kein Handle abrufen muss und die RTM-Weiterleitungs [**\_ \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur nicht an den und aus dem Routing Tabellen-Manager übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="15409-105">This method is more efficient because the client is not required to obtain a handle, nor to pass the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="15409-106">Diese Methode benötigt auch weniger Zeit.</span><span class="sxs-lookup"><span data-stu-id="15409-106">This method also takes less time.</span></span> <span data-ttu-id="15409-107">Das direkte Aktualisieren der Routing Tabelle kann jedoch riskant sein, da der Routing Tabellen-Manager nicht als Vermittler fungiert.</span><span class="sxs-lookup"><span data-stu-id="15409-107">However, directly updating the routing table can be risky, since the routing table manager is not functioning as an intermediary.</span></span>

<span data-ttu-id="15409-108">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden [Sie unter Aktualisieren einer Route direkt mithilfe von rtmupdateandunlockroute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span><span class="sxs-lookup"><span data-stu-id="15409-108">For sample code that shows how to use these functions, see [Update a Route In Place Using RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span></span>

 

 




