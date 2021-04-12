---
title: Hinzufügen von Routen
description: Nachdem ein Client eine Route ermittelt hat, kann der Client diese Route der Routing Tabelle hinzufügen, indem er die rtmaddnexthop-Funktion aufruft.
ms.assetid: d72c8a84-3eac-4c5d-84af-8edc7b41f0b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276e523f78de99efb981c5ecaf2f33bd2df3d154
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310356"
---
# <a name="adding-routes"></a><span data-ttu-id="80840-103">Hinzufügen von Routen</span><span class="sxs-lookup"><span data-stu-id="80840-103">Adding Routes</span></span>

<span data-ttu-id="80840-104">Nachdem ein Client eine Route ermittelt hat, kann der Client diese Route der Routing Tabelle hinzufügen, indem er die [**rtmaddnexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="80840-104">Once a client has discovered a route, the client can add that route to the routing table by calling the [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop) function.</span></span>

<span data-ttu-id="80840-105">Ein Client kann Routen aus der Routing Tabelle entfernen, indem er die [**rtmdeleteroutetodest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutetodest) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="80840-105">A client can remove routes from the routing table by calling the [**RtmDeleteRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutetodest) function.</span></span>

<span data-ttu-id="80840-106">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden [Sie unter Hinzufügen und Aktualisieren von Routen mithilfe von rtmaddroutededest](add-and-update-routes-using-rtmaddroutetodest.md).</span><span class="sxs-lookup"><span data-stu-id="80840-106">For sample code that shows how to use these functions, see [Add and Update Routes Using RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span></span>

 

 




