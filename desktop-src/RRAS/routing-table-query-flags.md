---
title: Abfrage-Flags für Routing Tabelle
description: Verwenden Sie diese Konstanten für routertabellenabfragen.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Abfrage-Flags für Routing Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857027"
---
# <a name="routing-table-query-flags"></a><span data-ttu-id="5904f-104">Abfrage-Flags für Routing Tabelle</span><span class="sxs-lookup"><span data-stu-id="5904f-104">Routing Table Query Flags</span></span>

<span data-ttu-id="5904f-105">Verwenden Sie diese Konstanten für routertabellenabfragen.</span><span class="sxs-lookup"><span data-stu-id="5904f-105">Use these constants for router table queries.</span></span>



| <span data-ttu-id="5904f-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="5904f-106">Constant</span></span>              | <span data-ttu-id="5904f-107">Wert</span><span class="sxs-lookup"><span data-stu-id="5904f-107">Value</span></span>      | <span data-ttu-id="5904f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5904f-108">Description</span></span>                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="5904f-109">RTM- \_ Übereinstimmung \_</span><span class="sxs-lookup"><span data-stu-id="5904f-109">RTM\_MATCH\_NONE</span></span>      | <span data-ttu-id="5904f-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5904f-110">0x00000000</span></span> | <span data-ttu-id="5904f-111">Entspricht keinem der Kriterien. Alle Routen für das Ziel werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5904f-111">Matches none of the criteria; all routes for the destination are returned.</span></span> |
| <span data-ttu-id="5904f-112">RTM-Übereinstimmungs \_ \_ Besitzer</span><span class="sxs-lookup"><span data-stu-id="5904f-112">RTM\_MATCH\_OWNER</span></span>     | <span data-ttu-id="5904f-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5904f-113">0x00000001</span></span> | <span data-ttu-id="5904f-114">Entspricht Routen mit demselben Besitzer.</span><span class="sxs-lookup"><span data-stu-id="5904f-114">Matches routes with same owner.</span></span>                                            |
| <span data-ttu-id="5904f-115">RTM- \_ Treffer \_ Nachbar</span><span class="sxs-lookup"><span data-stu-id="5904f-115">RTM\_MATCH\_NEIGHBOUR</span></span> | <span data-ttu-id="5904f-116">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5904f-116">0x00000002</span></span> | <span data-ttu-id="5904f-117">Entspricht Routen mit demselben Nachbar.</span><span class="sxs-lookup"><span data-stu-id="5904f-117">Matches routes with the same neighbor.</span></span>                                     |
| <span data-ttu-id="5904f-118">RTM \_ - \_ abgleichpref</span><span class="sxs-lookup"><span data-stu-id="5904f-118">RTM\_MATCH\_PREF</span></span>      | <span data-ttu-id="5904f-119">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5904f-119">0x00000004</span></span> | <span data-ttu-id="5904f-120">Entspricht Routen mit der gleichen Einstellung.</span><span class="sxs-lookup"><span data-stu-id="5904f-120">Matches routes that have the same preference.</span></span>                              |
| <span data-ttu-id="5904f-121">RTM-Entsprechung für \_ \_ nexthop</span><span class="sxs-lookup"><span data-stu-id="5904f-121">RTM\_MATCH\_NEXTHOP</span></span>   | <span data-ttu-id="5904f-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5904f-122">0x00000008</span></span> | <span data-ttu-id="5904f-123">Entspricht Routen mit dem gleichen nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="5904f-123">Matches routes that have the same next hop.</span></span>                                |
| <span data-ttu-id="5904f-124">RTM-Übereinstimmungs \_ \_ Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5904f-124">RTM\_MATCH\_INTERFACE</span></span> | <span data-ttu-id="5904f-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5904f-125">0x00000010</span></span> | <span data-ttu-id="5904f-126">Entspricht Routen, die sich auf derselben Schnittstelle befinden.</span><span class="sxs-lookup"><span data-stu-id="5904f-126">Matches routes that are on the same interface.</span></span>                             |
| <span data-ttu-id="5904f-127">RTM- \_ Übereinstimmung \_ voll</span><span class="sxs-lookup"><span data-stu-id="5904f-127">RTM\_MATCH\_FULL</span></span>      | <span data-ttu-id="5904f-128">0X0000FFFF</span><span class="sxs-lookup"><span data-stu-id="5904f-128">0x0000FFFF</span></span> | <span data-ttu-id="5904f-129">Entspricht Routen mit allen Kriterien.</span><span class="sxs-lookup"><span data-stu-id="5904f-129">Matches routes with all criteria.</span></span>                                          |
| <span data-ttu-id="5904f-130">Bestes RTM- \_ \_ Protokoll</span><span class="sxs-lookup"><span data-stu-id="5904f-130">RTM\_BEST\_PROTOCOL</span></span>   | <span data-ttu-id="5904f-131">0</span><span class="sxs-lookup"><span data-stu-id="5904f-131">0</span></span>          | <span data-ttu-id="5904f-132">Gibt eine Route zurück, unabhängig davon, welchem Protokoll Sie gehört.</span><span class="sxs-lookup"><span data-stu-id="5904f-132">Returns a route regardless of which protocol owns it.</span></span>                      |
| <span data-ttu-id="5904f-133">RTM \_ dieses \_ Protokoll</span><span class="sxs-lookup"><span data-stu-id="5904f-133">RTM\_THIS\_PROTOCOL</span></span>   | <span data-ttu-id="5904f-134">~0</span><span class="sxs-lookup"><span data-stu-id="5904f-134">~0</span></span>         | <span data-ttu-id="5904f-135">Gibt die beste Route für das Aufruf Protokoll zurück.</span><span class="sxs-lookup"><span data-stu-id="5904f-135">Returns the best route for the calling protocol.</span></span>                           |



 

 

 




