---
title: Arbeiten mit den nächsten Hops
description: Mit der RTMv2-API können Clients mit der Liste der nächsten Hops arbeiten, die Routen und Zielen zugeordnet sind.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388679"
---
# <a name="working-with-next-hops"></a><span data-ttu-id="eceef-103">Arbeiten mit den nächsten Hops</span><span class="sxs-lookup"><span data-stu-id="eceef-103">Working with Next Hops</span></span>

<span data-ttu-id="eceef-104">Mit der RTMv2-API können Clients mit der Liste der nächsten Hops arbeiten, die Routen und Zielen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="eceef-104">The RTMv2 API allows clients to work with the list of next hops that are associated with routes and destinations.</span></span> <span data-ttu-id="eceef-105">Clients können einen nächsten Hop durch Aufrufen von [**rtmaddnexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop)hinzufügen oder aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="eceef-105">Clients can add or update a next hop by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="eceef-106">Clients können einen nächsten Hop mit [**rtmdeletenexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop)löschen.</span><span class="sxs-lookup"><span data-stu-id="eceef-106">Clients can delete a next hop using [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span></span> <span data-ttu-id="eceef-107">Clients können durch Aufrufen von [**rtmfindnexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop)nach den nächsten Hops suchen.</span><span class="sxs-lookup"><span data-stu-id="eceef-107">Clients can search for next hops by calling [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span></span>

<span data-ttu-id="eceef-108">Clients können den nächsten Hop auch direkt aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="eceef-108">Clients can also update the next hop directly.</span></span> <span data-ttu-id="eceef-109">Zu diesem Zweck muss der Client zunächst den nächsten Hop mit der Funktion [**rtmlocknexthop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) sperren.</span><span class="sxs-lookup"><span data-stu-id="eceef-109">To do so, the client must first lock the next hop with the [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) function.</span></span> <span data-ttu-id="eceef-110">Anschließend kann der Client den direkten Zeiger zur [**RTM \_ nexthop- \_ Informations**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) Struktur des Routing Tabellen-Managers verwenden, um die erforderlichen Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="eceef-110">Then the client can use the direct pointer to the routing table manager's [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure to make necessary modifications.</span></span> <span data-ttu-id="eceef-111">Schließlich kann der Client den nächsten Hop entsperren.</span><span class="sxs-lookup"><span data-stu-id="eceef-111">Finally, the client can unlock the next hop.</span></span>

> [!Note]  
> <span data-ttu-id="eceef-112">Die Felder "Address" und "Interface Index" im nächsten Hop identifizieren den nächsten Hop eindeutig und sollten nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="eceef-112">The next-hop address and interface index fields in the next hop uniquely identify the next hop and should not be modified.</span></span>

 

 

 




