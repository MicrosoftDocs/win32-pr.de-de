---
title: Aktualisieren von Routen mithilfe von rtmaddroutededest
description: Wenn der Client beim Hinzufügen einer Route keine Effizienz benötigt, sollte er die folgenden Methoden zum Aktualisieren von Routen verwenden.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947995"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a><span data-ttu-id="c8707-103">Aktualisieren von Routen mithilfe von rtmaddroutededest</span><span class="sxs-lookup"><span data-stu-id="c8707-103">Updating Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="c8707-104">Wenn der Client beim Hinzufügen einer Route keine Effizienz benötigt, sollte er die folgenden Methoden zum Aktualisieren von Routen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8707-104">If the client does not require efficiency when adding a route, it should use the following method of updating routes.</span></span> <span data-ttu-id="c8707-105">Diese Methode ist weniger effizient, da Sie das Abrufen eines Handles für die Route und das übergeben der [**RTM- \_ Routen \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) Struktur an den Routing Tabellen-Manager erfordert.</span><span class="sxs-lookup"><span data-stu-id="c8707-105">This method is less efficient since it requires obtaining a handle to the route and passing the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="c8707-106">Diese Methode benötigt auch mehr Zeit.</span><span class="sxs-lookup"><span data-stu-id="c8707-106">This method also takes more time.</span></span> <span data-ttu-id="c8707-107">Da [**rtmaddroutededest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) die Routing Tabelle nicht direkt bearbeitet, funktioniert die Verwendung dieser Methode zur Vereinfachung.</span><span class="sxs-lookup"><span data-stu-id="c8707-107">Since [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) does not manipulate the routing table directly, using this method trades efficiency for simplicity.</span></span>

<span data-ttu-id="c8707-108">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden [Sie unter Hinzufügen und Aktualisieren von Routen mithilfe von rtmaddroutededest](add-and-update-routes-using-rtmaddroutetodest.md).</span><span class="sxs-lookup"><span data-stu-id="c8707-108">For sample code that shows how to use these functions, see [Add and Update Routes Using RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).</span></span>

 

 




