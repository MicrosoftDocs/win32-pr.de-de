---
title: Informationen zum Routing Table Manager Version 2
description: In der folgenden Dokumentation wird die RTMv2-Technologie (Routing Table Manager Version 2) beschrieben.
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- RRAS für den Routing-und RAS-Dienst, Routing-Tabellen-Manager Version 2
- Routing-und RAS-Dienst RRAS, Routing-Tabellen-Manager Version 2, beschrieben
- Routing Table Manager Version 2 RRAS
- Routing Table Manager Version 2 RRAS, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037084"
---
# <a name="about-routing-table-manager-version-2"></a><span data-ttu-id="ff23b-107">Informationen zum Routing Table Manager Version 2</span><span class="sxs-lookup"><span data-stu-id="ff23b-107">About Routing Table Manager Version 2</span></span>

<span data-ttu-id="ff23b-108">In der folgenden Dokumentation wird die RTMv2-Technologie (Routing Table Manager Version 2) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff23b-108">The following documentation describes the Routing Table Manager Version 2 (RTMv2) technology.</span></span> <span data-ttu-id="ff23b-109">Die RTMv2-API ist eine Funktion von Windows 2000 und neueren Betriebssystemen, die Sie verwenden können, um Routing Protokolle zu schreiben, die mit dem Routing Tabellen-Manager interagieren.</span><span class="sxs-lookup"><span data-stu-id="ff23b-109">The RTMv2 API is a feature of Windows 2000 and later operating systems that you can use to write routing protocols that interact with the routing table manager.</span></span>

<span data-ttu-id="ff23b-110">Der Routing Tabellen-Manager ist das zentrale Repository von Routing Informationen für alle Routing Protokolle, die unter dem Routing-und RAS-Dienst (RRAS) betrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ff23b-110">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span>

<span data-ttu-id="ff23b-111">RTMv2 ist für Windows NT-Version 4,0 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ff23b-111">RTMv2 is not available for Windows NT version 4.0.</span></span> <span data-ttu-id="ff23b-112">Außerdem kann RTMv2 nicht für IPX-Routing Protokolle verwendet werden, die unter Windows NT 4,0 oder Windows 2000 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ff23b-112">Additionally, RTMv2 cannot be used for IPX routing protocols that run on Windows NT 4.0 or Windows 2000.</span></span> <span data-ttu-id="ff23b-113">Wenn Sie IPX verwenden oder Routing Protokolle für Windows NT 4,0 schreiben, finden Sie weitere Informationen unter [Routing Table Manager Version 1](about-routing-table-manager-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="ff23b-113">If you are using IPX or writing routing protocols for Windows NT 4.0, please refer to [About Routing Table Manager Version 1](about-routing-table-manager-version-1.md).</span></span>

<span data-ttu-id="ff23b-114">In dieser Übersicht werden die folgenden Themen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="ff23b-114">This overview describes the following topics:</span></span>

-   [<span data-ttu-id="ff23b-115">Komponenten der Architektur des Routing Tabellen-Managers</span><span class="sxs-lookup"><span data-stu-id="ff23b-115">Components of the Routing Table Manager Architecture</span></span>](components-of-the-routing-table-manager-architecture.md)
-   [<span data-ttu-id="ff23b-116">Registrieren beim Routing Tabellen-Manager</span><span class="sxs-lookup"><span data-stu-id="ff23b-116">Registering with the Routing Table Manager</span></span>](registering-with-the-routing-table-manager.md)
-   [<span data-ttu-id="ff23b-117">Auflisten registrierter Entitäten</span><span class="sxs-lookup"><span data-stu-id="ff23b-117">Enumerating Registered Entities</span></span>](enumerating-registered-entities.md)
-   [<span data-ttu-id="ff23b-118">Verwenden von Methoden</span><span class="sxs-lookup"><span data-stu-id="ff23b-118">Using Methods</span></span>](using-methods.md)
-   [<span data-ttu-id="ff23b-119">Verwenden undurchsichtiger Zeiger</span><span class="sxs-lookup"><span data-stu-id="ff23b-119">Using Opaque Pointers</span></span>](using-opaque-pointers.md)
-   [<span data-ttu-id="ff23b-120">Markieren von Routen für den Hold-Down Status</span><span class="sxs-lookup"><span data-stu-id="ff23b-120">Marking Routes for the Hold-Down State</span></span>](marking-routes-for-the-hold-down-state.md)
-   [<span data-ttu-id="ff23b-121">Hinzufügen von Routen</span><span class="sxs-lookup"><span data-stu-id="ff23b-121">Adding Routes</span></span>](adding-routes.md)
-   [<span data-ttu-id="ff23b-122">Abrufen von Routeninformationen</span><span class="sxs-lookup"><span data-stu-id="ff23b-122">Retrieving Route Information</span></span>](retrieving-route-information.md)
-   [<span data-ttu-id="ff23b-123">Aktualisieren von Routen</span><span class="sxs-lookup"><span data-stu-id="ff23b-123">Updating Routes</span></span>](updating-routes.md)
-   [<span data-ttu-id="ff23b-124">Empfangen von Benachrichtigungen über Änderungen</span><span class="sxs-lookup"><span data-stu-id="ff23b-124">Receiving Notification of Changes</span></span>](receiving-notification-of-changes.md)
-   [<span data-ttu-id="ff23b-125">Arbeiten mit den nächsten Hops</span><span class="sxs-lookup"><span data-stu-id="ff23b-125">Working with Next Hops</span></span>](working-with-next-hops.md)
-   [<span data-ttu-id="ff23b-126">Auflisten von Routing Tabellen Einträgen</span><span class="sxs-lookup"><span data-stu-id="ff23b-126">Enumerating Routing Table Entries</span></span>](enumerating-routing-table-entries.md)
-   [<span data-ttu-id="ff23b-127">Suchen nach bestimmten Informationen in der Routing Tabelle</span><span class="sxs-lookup"><span data-stu-id="ff23b-127">Finding Specific Information in the Routing Table</span></span>](finding-specific-information-in-the-routing-table.md)
-   [<span data-ttu-id="ff23b-128">Verwalten von Client-Specific Listen</span><span class="sxs-lookup"><span data-stu-id="ff23b-128">Maintaining Client-Specific Lists</span></span>](maintaining-client-specific-lists.md)
-   [<span data-ttu-id="ff23b-129">Verwalten von Handles</span><span class="sxs-lookup"><span data-stu-id="ff23b-129">Managing Handles</span></span>](managing-handles.md)

 

 




