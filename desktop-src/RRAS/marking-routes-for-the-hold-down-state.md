---
title: Markieren von Routen für den Hold-Down Status
description: Einige Clients, wie z. b. Entfernungs Vektor Protokolle wie RIP und DVMRP, erfordern, dass Ziele für einen bestimmten Zeitraum als nicht erreichbar angekündigt werden, nachdem die letzte Route zum Ziel gelöscht wurde.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947809"
---
# <a name="marking-routes-for-the-hold-down-state"></a><span data-ttu-id="5b1bb-103">Markieren von Routen für den Hold-Down Status</span><span class="sxs-lookup"><span data-stu-id="5b1bb-103">Marking Routes for the Hold-Down State</span></span>

<span data-ttu-id="5b1bb-104">Einige Clients, wie z. b. Entfernungs Vektor Protokolle wie RIP und DVMRP, erfordern, dass Ziele für einen bestimmten Zeitraum als nicht erreichbar angekündigt werden, nachdem die letzte Route zum Ziel gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-104">Some clients, such as distance vector protocols like RIP and DVMRP, require that destinations be advertised as unreachable for a certain time after the last route to the destination is deleted.</span></span> <span data-ttu-id="5b1bb-105">Die letzte gelöschte Route muss als nicht erreichbar angekündigt werden, auch wenn in der Zwischenzeit neuere Routen eintreffen.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-105">The last route that is deleted must be advertised as unreachable even if newer routes arrive in the meantime.</span></span> <span data-ttu-id="5b1bb-106">Die letzte gelöschte Route ist als " *Hold-Down*" markiert.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-106">The last route deleted is marked as being in a *hold-down state*.</span></span> <span data-ttu-id="5b1bb-107">Der Hold-Down-Prozess verhindert die Bildung von Routing Schleifen.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-107">The hold-down process prevents the formation of routing loops.</span></span> <span data-ttu-id="5b1bb-108">Routing Schleifen werden ausgelöst, wenn ein Routing Protokoll veraltete Routing Informationen auslöst.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-108">Routing loops are caused when a routing protocol advertises obsolete routing information.</span></span> <span data-ttu-id="5b1bb-109">Wenn die Aufbewahrung abgelaufen ist, setzen diese Protokolle ihre Ankündigung mit der neuen optimalen Route fort.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-109">When the hold-down expires, these protocols resume their advertisement with the new best route.</span></span>

<span data-ttu-id="5b1bb-110">Ein Protokoll, das Hold-Down-Zustände implementiert, gibt an, dass sich ein Ziel mithilfe der [**rtmholddestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) -Funktion in einem Hold-Down-Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-110">A protocol that implements hold-down states indicates that a destination is in a hold-down state by using the [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) function.</span></span> <span data-ttu-id="5b1bb-111">Der Client ruft diese Funktion auf, wenn die beste Route zu diesem Ziel angekündigt wird.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-111">The client calls this function when it advertises the best route to this destination.</span></span> <span data-ttu-id="5b1bb-112">Wenn alle Routen zu diesem Ziel später gelöscht werden, wird die letzte Route, die gelöscht wird, für den Zeitraum, der im vorherigen Aufruf von **rtmholddestination** angegeben ist, in einem Hold-Down-Zustand aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-112">If all routes to this destination are later deleted, the last route that is deleted is kept in a hold-down state for the period of time specified in the earlier call to **RtmHoldDestination**.</span></span>

<span data-ttu-id="5b1bb-113">Wenn ein Protokoll ein Ziel angekündigt hat, sind die verwendeten Routeninformationen davon abhängig, ob das Protokoll Hold-Down-Zustände verwendet und ob eine Route im Hold-Down-Zustand für das Ziel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-113">When a protocol advertises a destination, the route information that is used depends on whether the protocol uses hold-down states and if a route in the hold-down state exists for the destination.</span></span>

<span data-ttu-id="5b1bb-114">Protokolle, die keine Hold-Down-Zustände verwenden, können Routeninformationen ignorieren, die sich auf den Hold-Down-Status für ein Ziel beziehen, und immer die beste Route ankündigen.</span><span class="sxs-lookup"><span data-stu-id="5b1bb-114">Protocols that do not use hold-down states can ignore route information that relates to hold-down states for a destination, and always advertise the best route.</span></span>

<span data-ttu-id="5b1bb-115">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [use the Route Hold-Down State](use-the-route-hold-down-state.md).</span><span class="sxs-lookup"><span data-stu-id="5b1bb-115">For sample code that shows how to use these functions, see [Use the Route Hold-Down State](use-the-route-hold-down-state.md).</span></span>

 

 




