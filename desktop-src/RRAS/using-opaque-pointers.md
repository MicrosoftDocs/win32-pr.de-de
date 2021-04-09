---
title: Verwenden undurchsichtiger Zeiger
description: Clients müssen häufig zusätzliche Client spezifische Informationen zu Zielen speichern.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856532"
---
# <a name="using-opaque-pointers"></a><span data-ttu-id="5f2db-103">Verwenden undurchsichtiger Zeiger</span><span class="sxs-lookup"><span data-stu-id="5f2db-103">Using Opaque Pointers</span></span>

<span data-ttu-id="5f2db-104">Clients müssen häufig zusätzliche Client spezifische Informationen zu Zielen speichern.</span><span class="sxs-lookup"><span data-stu-id="5f2db-104">Clients often must store additional, client-specific information about destinations.</span></span> <span data-ttu-id="5f2db-105">Mithilfe des Routing Tabellen-Managers können Clients diese Informationen in Zielstrukturen in der Routing Tabelle speichern.</span><span class="sxs-lookup"><span data-stu-id="5f2db-105">The routing table manager enables clients to store this information in destination structures in the routing table.</span></span> <span data-ttu-id="5f2db-106">Die Informationen werden mithilfe von nicht transparenten *Zeigern* gespeichert und abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5f2db-106">The information is stored and retrieved by using *opaque pointers*.</span></span> <span data-ttu-id="5f2db-107">Die gespeicherten Informationen sind privat und können nur für den Client zugänglich sein, der den nicht transparenten Zeiger besitzt.</span><span class="sxs-lookup"><span data-stu-id="5f2db-107">The information stored is private, and accessible only to the client that owns the opaque pointer.</span></span>

<span data-ttu-id="5f2db-108">Beispielsweise behält der Multicast-Gruppen-Manager eine Liste von Multicast-Weiterleitungs Einträgen bei, die von einem bestimmten Ziel abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="5f2db-108">For example, the multicast group manager keeps a list of multicast forwarding entries that are dependent on a particular destination.</span></span> <span data-ttu-id="5f2db-109">Der Multicast-Gruppen-Manager verwendet einen nicht transparenten Zeiger in diesem Ziel.</span><span class="sxs-lookup"><span data-stu-id="5f2db-109">The multicast group manager uses an opaque pointer in that destination.</span></span> <span data-ttu-id="5f2db-110">In einem anderen Beispiel kann ein Routing Protokoll, das ein bestimmtes Ziel angekündigt hat, Informationen im Zusammenhang mit der eigenen Routen Ankündigung des Ziels mithilfe eines nicht transparenten Zeigers aufbewahren, auch wenn er nicht die beste Route besitzt.</span><span class="sxs-lookup"><span data-stu-id="5f2db-110">In another example, a routing protocol that advertises a particular destination can keep information related to its own route advertisement of the destination using an opaque pointer, even though it does not own the best route.</span></span>

<span data-ttu-id="5f2db-111">Die Anzahl der nicht transparenten Zeiger ist beschränkt. Diese Zeiger werden den Clients auf der Basis von First-come-first-served-Basis zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5f2db-111">The number of opaque pointers is limited; these pointers are allocated to clients on a first-come, first-served basis.</span></span> <span data-ttu-id="5f2db-112">Der Routeradministrator muss die richtige Anzahl von Zeigern während der Routerkonfiguration zuordnen. Daher müssen Routing Protokolle und andere Clients ihre Verwendung undurchsichtiger Zeiger dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="5f2db-112">The router administrator must allocate the correct number of pointers during the router configuration; therefore, routing protocols and other clients must document their use of opaque pointers.</span></span>

 

 




