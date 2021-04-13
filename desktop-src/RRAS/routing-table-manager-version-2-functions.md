---
title: Routing Table Manager Version 2-Funktionen
description: Die folgenden Funktionen werden für die Interaktion mit dem Routing Tabellen-Manager verwendet.
ms.assetid: ac5c6ada-c38e-476a-9896-cdd8c51cc0be
keywords:
- RRAS für den Routing-und RAS-Dienst, Routing-Tabellen-Manager Version 2, Funktionen
- Routing Table Manager Version 2 RRAS, Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f59e4a1ad2bf091d8a74672f1f473589c5fa1d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388448"
---
# <a name="routing-table-manager-version-2-functions"></a><span data-ttu-id="4ff8c-105">Routing Table Manager Version 2-Funktionen</span><span class="sxs-lookup"><span data-stu-id="4ff8c-105">Routing Table Manager Version 2 Functions</span></span>

<span data-ttu-id="4ff8c-106">Die folgenden Funktionen werden für die Interaktion mit dem Routing Tabellen-Manager verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ff8c-106">The following functions are used to interact with the routing table manager.</span></span>

## <a name="registration-functions"></a><span data-ttu-id="4ff8c-107">Registrierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4ff8c-107">Registration Functions</span></span>

[<span data-ttu-id="4ff8c-108">**Rtmregisterentity**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-108">**RtmRegisterEntity**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)

[<span data-ttu-id="4ff8c-109">**Rtmderegisterentity**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-109">**RtmDeregisterEntity**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)

[<span data-ttu-id="4ff8c-110">**Rtmgetregisteredentities**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-110">**RtmGetRegisteredEntities**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities)

[<span data-ttu-id="4ff8c-111">**Rtmreleaseentities**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-111">**RtmReleaseEntities**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities)

## <a name="opaque-pointer-functions"></a><span data-ttu-id="4ff8c-112">Nicht transparente Zeiger Funktionen</span><span class="sxs-lookup"><span data-stu-id="4ff8c-112">Opaque Pointer Functions</span></span>

[<span data-ttu-id="4ff8c-113">**Rtmlockdestination**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-113">**RtmLockDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination)

[<span data-ttu-id="4ff8c-114">**Rtmgetopaqueingeformationpointer**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-114">**RtmGetOpaqueInformationPointer**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer)

## <a name="export-method-functions"></a><span data-ttu-id="4ff8c-115">Methoden Funktionen exportieren</span><span class="sxs-lookup"><span data-stu-id="4ff8c-115">Export Method Functions</span></span>

[<span data-ttu-id="4ff8c-116">**Rtmgetentitymethods**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-116">**RtmGetEntityMethods**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods)

[<span data-ttu-id="4ff8c-117">**Rtminvokemethod**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-117">**RtmInvokeMethod**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod)

[<span data-ttu-id="4ff8c-118">**Rtmblockmethods**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-118">**RtmBlockMethods**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)

## <a name="handle-to-information-structure-functions"></a><span data-ttu-id="4ff8c-119">Handle für Informationsstruktur Funktionen</span><span class="sxs-lookup"><span data-stu-id="4ff8c-119">Handle to Information Structure Functions</span></span>

[<span data-ttu-id="4ff8c-120">**Rtmgetentityinfo**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-120">**RtmGetEntityInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)

[<span data-ttu-id="4ff8c-121">**Rtmgetdestinfo**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-121">**RtmGetDestInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)

[<span data-ttu-id="4ff8c-122">**Rtmgetrouteingefo**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-122">**RtmGetRouteInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)

[<span data-ttu-id="4ff8c-123">**Rtmgetnexthopinfo**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-123">**RtmGetNextHopInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

[<span data-ttu-id="4ff8c-124">**Rtmreleaseentityinfo**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-124">**RtmReleaseEntityInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)

[<span data-ttu-id="4ff8c-125">**Rtmreleasedestinfo**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-125">**RtmReleaseDestInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)

[<span data-ttu-id="4ff8c-126">**Rtmreleaserouteingefo**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-126">**RtmReleaseRouteInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo)

[<span data-ttu-id="4ff8c-127">**Rtmreleasenexthopinfo**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-127">**RtmReleaseNextHopInfo**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)

## <a name="routing-table-insertion-and-deletion-functions"></a><span data-ttu-id="4ff8c-128">Funktionen zum Einfügen und Löschen von Routing Tabellen</span><span class="sxs-lookup"><span data-stu-id="4ff8c-128">Routing Table Insertion and Deletion Functions</span></span>

[<span data-ttu-id="4ff8c-129">**Rtmaddroutededest**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-129">**RtmAddRouteToDest**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest)

[<span data-ttu-id="4ff8c-130">**Rtmdeleteroutededest**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-130">**RtmDeleteRouteToDest**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutetodest)

[<span data-ttu-id="4ff8c-131">**Rtmholddestination**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-131">**RtmHoldDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination)

[<span data-ttu-id="4ff8c-132">**Rtmgetroutepointer**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-132">**RtmGetRoutePointer**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetroutepointer)

[<span data-ttu-id="4ff8c-133">**Rtmlockroute**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-133">**RtmLockRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute)

[<span data-ttu-id="4ff8c-134">**Rtmupdateandunlockroute**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-134">**RtmUpdateAndUnlockRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute)

## <a name="routing-table-query-functions"></a><span data-ttu-id="4ff8c-135">Routing Tabellen-Abfragefunktionen</span><span class="sxs-lookup"><span data-stu-id="4ff8c-135">Routing Table Query Functions</span></span>

[<span data-ttu-id="4ff8c-136">**Rtmgetexactmatchdestination**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-136">**RtmGetExactMatchDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination)

[<span data-ttu-id="4ff8c-137">**Rtmgetmuspecificdestination**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-137">**RtmGetMostSpecificDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)

[<span data-ttu-id="4ff8c-138">**Rtmgetlessspecificdestination**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-138">**RtmGetLessSpecificDestination**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination)

[<span data-ttu-id="4ff8c-139">**Rtmgetexactmatchroute**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-139">**RtmGetExactMatchRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute)

[<span data-ttu-id="4ff8c-140">**Rtmisbestroute**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-140">**RtmIsBestRoute**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute)

## <a name="next-hop-insertion-and-deletion-functions"></a><span data-ttu-id="4ff8c-141">Funktionen zum Einfügen und löschen im nächsten Hop</span><span class="sxs-lookup"><span data-stu-id="4ff8c-141">Next-Hop Insertion and Deletion Functions</span></span>

[<span data-ttu-id="4ff8c-142">**Rtmaddnexthop**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-142">**RtmAddNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)

[<span data-ttu-id="4ff8c-143">**Rtmfindnexthop**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-143">**RtmFindNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)

[<span data-ttu-id="4ff8c-144">**Rtmdeletenexthop**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-144">**RtmDeleteNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)

[<span data-ttu-id="4ff8c-145">**Rtmgetnexthoppointer**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-145">**RtmGetNextHopPointer**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthoppointer)

[<span data-ttu-id="4ff8c-146">**Rtmlocknexthop**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-146">**RtmLockNextHop**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop)

## <a name="routing-table-enumeration-functions"></a><span data-ttu-id="4ff8c-147">Routing Tabellen-Enumerationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4ff8c-147">Routing Table Enumeration Functions</span></span>

[<span data-ttu-id="4ff8c-148">**Rtmkreatedesterum**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-148">**RtmCreateDestEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum)

[<span data-ttu-id="4ff8c-149">**Rtmgetenumschlag**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-149">**RtmGetEnumDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests)

[<span data-ttu-id="4ff8c-150">**Rtmreleasedests**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-150">**RtmReleaseDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests)

[<span data-ttu-id="4ff8c-151">**Rtmkreaterouteenum**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-151">**RtmCreateRouteEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum)

[<span data-ttu-id="4ff8c-152">**Rtmgetenumroutes**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-152">**RtmGetEnumRoutes**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes)

[<span data-ttu-id="4ff8c-153">**Rtmreleaseroutes**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-153">**RtmReleaseRoutes**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes)

[<span data-ttu-id="4ff8c-154">**Rtmkreatenexthopenum**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-154">**RtmCreateNextHopEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum)

[<span data-ttu-id="4ff8c-155">**Rtmgetenrenexthops**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-155">**RtmGetEnumNextHops**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops)

[<span data-ttu-id="4ff8c-156">**Rtmreleasenexthops**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-156">**RtmReleaseNextHops**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops)

[<span data-ttu-id="4ff8c-157">**Rtmdeleteenumschlag handle**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-157">**RtmDeleteEnumHandle**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle)

## <a name="change-notification-functions"></a><span data-ttu-id="4ff8c-158">Änderungs Benachrichtigungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4ff8c-158">Change Notification Functions</span></span>

[<span data-ttu-id="4ff8c-159">**Rtmregisterforchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-159">**RtmRegisterForChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)

[<span data-ttu-id="4ff8c-160">**Rtmgetchangeddebug**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-160">**RtmGetChangedDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)

[<span data-ttu-id="4ff8c-161">**Rtmreleasechangeddebug**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-161">**RtmReleaseChangedDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests)

[<span data-ttu-id="4ff8c-162">**Rtmignorechangedentsts**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-162">**RtmIgnoreChangedDests**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests)

[<span data-ttu-id="4ff8c-163">**Rtmgetchangestatus**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-163">**RtmGetChangeStatus**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus)

[<span data-ttu-id="4ff8c-164">**Rtmmarkdestforchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-164">**RtmMarkDestForChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)

[<span data-ttu-id="4ff8c-165">**Rtmismarkedforchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-165">**RtmIsMarkedForChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmismarkedforchangenotification)

[<span data-ttu-id="4ff8c-166">**Rtmderegisterfromchangenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-166">**RtmDeregisterFromChangeNotification**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)

## <a name="route-list-function"></a><span data-ttu-id="4ff8c-167">Routenlisten Funktion</span><span class="sxs-lookup"><span data-stu-id="4ff8c-167">Route List Function</span></span>

[<span data-ttu-id="4ff8c-168">**Rtmkreateroutelist**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-168">**RtmCreateRouteList**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist)

[<span data-ttu-id="4ff8c-169">**Rtminsertinroutelist**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-169">**RtmInsertInRouteList**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist)

[<span data-ttu-id="4ff8c-170">**Rtmkreateroutelistenum**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-170">**RtmCreateRouteListEnum**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum)

[<span data-ttu-id="4ff8c-171">**Rtmgetlistenumroutes**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-171">**RtmGetListEnumRoutes**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes)

[<span data-ttu-id="4ff8c-172">**Rtmdeleteroutelist**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-172">**RtmDeleteRouteList**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist)

## <a name="handle-management-functions"></a><span data-ttu-id="4ff8c-173">Verwalten von Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="4ff8c-173">Handle Management Functions</span></span>

[<span data-ttu-id="4ff8c-174">**Rtmreferencehandles**</span><span class="sxs-lookup"><span data-stu-id="4ff8c-174">**RtmReferenceHandles**</span></span>](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles)

 

 




