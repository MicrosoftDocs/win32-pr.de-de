---
title: Verwenden von Routing Table Manager Version 2
description: Bevor Sie mit der Entwicklung von Clients beginnen, die die RTMv2-APIs verwenden, überprüfen Sie die Programmierprobleme RTMv2.
ms.assetid: c0187b65-3cb2-4ab0-8d5f-ca37e8bc0ad7
keywords:
- RRAS für den Routing-und RAS-Dienst, Routing-Tabellen-Manager Version 2, Tasks
- Routing Table Manager Version 2 RRAS, Tasks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bc7acab213325a0683de215995eeb2f635b102
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947820"
---
# <a name="using-routing-table-manager-version-2"></a><span data-ttu-id="7df5f-105">Verwenden von Routing Table Manager Version 2</span><span class="sxs-lookup"><span data-stu-id="7df5f-105">Using Routing Table Manager Version 2</span></span>

<span data-ttu-id="7df5f-106">Bevor Sie mit der Entwicklung von Clients beginnen, die die RTMv2-APIs verwenden, überprüfen Sie die [Programmierprobleme RTMv2](rtmv2-programming-issues.md).</span><span class="sxs-lookup"><span data-stu-id="7df5f-106">Before you begin developing clients that use the RTMv2 APIs, review the [RTMv2 Programming Issues](rtmv2-programming-issues.md).</span></span>

<span data-ttu-id="7df5f-107">Dieser Abschnitt enthält Beispielcode, der bei der Entwicklung von Clients wie Routing Protokollen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7df5f-107">This section contains sample code that can be used when developing clients such as routing protocols.</span></span>

-   [<span data-ttu-id="7df5f-108">RTMv2-Programmierprobleme</span><span class="sxs-lookup"><span data-stu-id="7df5f-108">RTMv2 Programming Issues</span></span>](rtmv2-programming-issues.md)
-   [<span data-ttu-id="7df5f-109">Registrieren beim Routing Tabellen-Manager</span><span class="sxs-lookup"><span data-stu-id="7df5f-109">Register with the Routing Table Manager</span></span>](register-with-the-routing-table-manager.md)
-   [<span data-ttu-id="7df5f-110">Auflisten der registrierten Entitäten</span><span class="sxs-lookup"><span data-stu-id="7df5f-110">Enumerate the Registered Entities</span></span>](enumerate-the-registered-entities.md)
-   [<span data-ttu-id="7df5f-111">Abrufen und Abrufen der exportierten Methoden für einen Client</span><span class="sxs-lookup"><span data-stu-id="7df5f-111">Obtain and Call the Exported Methods for a Client</span></span>](obtain-and-call-the-exported-methods-for-a-client.md)
-   [<span data-ttu-id="7df5f-112">Für Änderungs Benachrichtigung registrieren</span><span class="sxs-lookup"><span data-stu-id="7df5f-112">Register for Change Notification</span></span>](register-for-change-notification.md)
-   [<span data-ttu-id="7df5f-113">Hinzufügen und Aktualisieren von Routen mithilfe von rtmaddroutededest</span><span class="sxs-lookup"><span data-stu-id="7df5f-113">Add and Update Routes Using RtmAddRouteToDest</span></span>](add-and-update-routes-using-rtmaddroutetodest.md)
-   [<span data-ttu-id="7df5f-114">Direktes Aktualisieren einer Route mithilfe von rtmupdateandunlockroute</span><span class="sxs-lookup"><span data-stu-id="7df5f-114">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>](update-a-route-in-place-using-rtmupdateandunlockroute.md)
-   [<span data-ttu-id="7df5f-115">Verwenden der Route Hold-Down Status</span><span class="sxs-lookup"><span data-stu-id="7df5f-115">Use the Route Hold-Down State</span></span>](use-the-route-hold-down-state.md)
-   [<span data-ttu-id="7df5f-116">Alle Ziele auflisten</span><span class="sxs-lookup"><span data-stu-id="7df5f-116">Enumerate All Destinations</span></span>](enumerate-all-destinations.md)
-   [<span data-ttu-id="7df5f-117">Alle Routen aufzählen</span><span class="sxs-lookup"><span data-stu-id="7df5f-117">Enumerate All Routes</span></span>](enumerate-all-routes.md)
-   [<span data-ttu-id="7df5f-118">Suchen nach der optimalen Route</span><span class="sxs-lookup"><span data-stu-id="7df5f-118">Search for the Best Route</span></span>](search-for-the-best-route.md)
-   [<span data-ttu-id="7df5f-119">Suchen nach Routen mithilfe eines Präfix Baums</span><span class="sxs-lookup"><span data-stu-id="7df5f-119">Search for Routes Using a Prefix Tree</span></span>](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)
-   [<span data-ttu-id="7df5f-120">Zugreifen auf den nicht transparenten Zeiger in einem Ziel</span><span class="sxs-lookup"><span data-stu-id="7df5f-120">Access the Opaque Pointer in a Destination</span></span>](access-the-opaque-pointer-in-a-destination.md)
-   [<span data-ttu-id="7df5f-121">Client-Specific Routenliste verwenden</span><span class="sxs-lookup"><span data-stu-id="7df5f-121">Use a Client-Specific Route List</span></span>](use-a-client-specific-route-list.md)
-   [<span data-ttu-id="7df5f-122">Verwenden des Ereignis Benachrichtigungs Rückrufs</span><span class="sxs-lookup"><span data-stu-id="7df5f-122">Use the Event Notification Callback</span></span>](use-the-event-notification-callback.md)

 

 




