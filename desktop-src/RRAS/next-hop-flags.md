---
title: Flags für den nächsten Hop
description: Flags für den nächsten Hop
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Nächste
- Flags für den nächsten Hop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037448"
---
# <a name="next-hop-flags"></a><span data-ttu-id="9ebbc-105">Flags für den nächsten Hop</span><span class="sxs-lookup"><span data-stu-id="9ebbc-105">Next Hop Flags</span></span>

## <a name="next-hop-state-flags"></a><span data-ttu-id="9ebbc-106">Statusflags für den nächsten Hop</span><span class="sxs-lookup"><span data-stu-id="9ebbc-106">Next Hop State Flags</span></span>



| <span data-ttu-id="9ebbc-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="9ebbc-107">Constant</span></span>                     | <span data-ttu-id="9ebbc-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9ebbc-108">Value</span></span> | <span data-ttu-id="9ebbc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ebbc-109">Description</span></span>                              |
|------------------------------|-------|------------------------------------------|
| <span data-ttu-id="9ebbc-110">RTM- \_ nexthop- \_ Status \_ erstellt</span><span class="sxs-lookup"><span data-stu-id="9ebbc-110">RTM\_NEXTHOP\_STATE\_CREATED</span></span> | <span data-ttu-id="9ebbc-111">0</span><span class="sxs-lookup"><span data-stu-id="9ebbc-111">0</span></span>     | <span data-ttu-id="9ebbc-112">Gibt an, dass der nächste Hop erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-112">Indicates that the next hop was created.</span></span> |
| <span data-ttu-id="9ebbc-113">RTM- \_ nexthop- \_ Status \_ gelöscht</span><span class="sxs-lookup"><span data-stu-id="9ebbc-113">RTM\_NEXTHOP\_STATE\_DELETED</span></span> | <span data-ttu-id="9ebbc-114">1</span><span class="sxs-lookup"><span data-stu-id="9ebbc-114">1</span></span>     | <span data-ttu-id="9ebbc-115">Gibt an, dass der nächste Hop gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-115">Indicates that the next hop was deleted.</span></span> |



 

## <a name="next-hop-flags"></a><span data-ttu-id="9ebbc-116">Flags für den nächsten Hop</span><span class="sxs-lookup"><span data-stu-id="9ebbc-116">Next Hop Flags</span></span>



| <span data-ttu-id="9ebbc-117">Konstante</span><span class="sxs-lookup"><span data-stu-id="9ebbc-117">Constant</span></span>                    | <span data-ttu-id="9ebbc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9ebbc-118">Value</span></span>  | <span data-ttu-id="9ebbc-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ebbc-119">Description</span></span>                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebbc-120">RTM- \_ nexthop- \_ Flags \_ Remote</span><span class="sxs-lookup"><span data-stu-id="9ebbc-120">RTM\_NEXTHOP\_FLAGS\_REMOTE</span></span> | <span data-ttu-id="9ebbc-121">0x0001</span><span class="sxs-lookup"><span data-stu-id="9ebbc-121">0x0001</span></span> | <span data-ttu-id="9ebbc-122">Der nächste Hop verweist auf ein Remote Ziel, das nicht direkt erreichbar ist.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-122">This next hop points to a remote destination that is not directly reachable.</span></span> <span data-ttu-id="9ebbc-123">Zum Abrufen des vollständigen Pfads muss der Client eine rekursive Suche durchführen.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-123">To obtain the complete path, the client must perform a recursive lookup.</span></span> |
| <span data-ttu-id="9ebbc-124">RTM- \_ nexthop- \_ Flags \_</span><span class="sxs-lookup"><span data-stu-id="9ebbc-124">RTM\_NEXTHOP\_FLAGS\_DOWN</span></span>   | <span data-ttu-id="9ebbc-125">0x0002</span><span class="sxs-lookup"><span data-stu-id="9ebbc-125">0x0002</span></span> | <span data-ttu-id="9ebbc-126">Dieses Flag ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-126">This flag is reserved for future use.</span></span>                                                                                                                 |



 

## <a name="next-hop-added"></a><span data-ttu-id="9ebbc-127">Nächster Hop hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="9ebbc-127">Next Hop Added</span></span>



| <span data-ttu-id="9ebbc-128">Konstante</span><span class="sxs-lookup"><span data-stu-id="9ebbc-128">Constant</span></span>                  | <span data-ttu-id="9ebbc-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9ebbc-129">Value</span></span> | <span data-ttu-id="9ebbc-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ebbc-130">Description</span></span>                 |
|---------------------------|-------|-----------------------------|
| <span data-ttu-id="9ebbc-131">RTM- \_ nexthop- \_ Änderung \_ neu</span><span class="sxs-lookup"><span data-stu-id="9ebbc-131">RTM\_NEXTHOP\_CHANGE\_NEW</span></span> | <span data-ttu-id="9ebbc-132">0x01</span><span class="sxs-lookup"><span data-stu-id="9ebbc-132">0x01</span></span>  | <span data-ttu-id="9ebbc-133">Ein neuer nächster Hop wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ebbc-133">A new next hop was created.</span></span> |



 

 

 




