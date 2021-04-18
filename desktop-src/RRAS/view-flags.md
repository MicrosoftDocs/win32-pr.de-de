---
title: Anzeigen von Flags
description: Verwenden Sie die Ansichts-Flags, um Routing Tabellen Sichten zu steuern.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338216"
---
# <a name="view-flags"></a><span data-ttu-id="c705f-103">Anzeigen von Flags</span><span class="sxs-lookup"><span data-stu-id="c705f-103">View Flags</span></span>

<span data-ttu-id="c705f-104">Verwenden Sie die Ansichts-Flags, um Routing Tabellen Sichten zu steuern.</span><span class="sxs-lookup"><span data-stu-id="c705f-104">Use the View Flags to control routing table views.</span></span>



| <span data-ttu-id="c705f-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="c705f-105">Constant</span></span>                 | <span data-ttu-id="c705f-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c705f-106">Value</span></span>      | <span data-ttu-id="c705f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c705f-107">Description</span></span>                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| <span data-ttu-id="c705f-108">maximale RTM- \_ \_ Adress \_ Größe</span><span class="sxs-lookup"><span data-stu-id="c705f-108">RTM\_MAX \_ADDRESS\_SIZE</span></span> | <span data-ttu-id="c705f-109">16</span><span class="sxs-lookup"><span data-stu-id="c705f-109">16</span></span>         | <span data-ttu-id="c705f-110">Maximale Adressgröße für eine Adressfamilie.</span><span class="sxs-lookup"><span data-stu-id="c705f-110">Max address size for an address family.</span></span>                          |
| <span data-ttu-id="c705f-111">maximale RTM- \_ \_ Ansichten</span><span class="sxs-lookup"><span data-stu-id="c705f-111">RTM\_MAX\_VIEWS</span></span>          | <span data-ttu-id="c705f-112">32</span><span class="sxs-lookup"><span data-stu-id="c705f-112">32</span></span>         | <span data-ttu-id="c705f-113">Maximale Anzahl von Sichten, die in der Routing Tabelle aktiv sein können.</span><span class="sxs-lookup"><span data-stu-id="c705f-113">Maximum number of views that can be active in the routing table.</span></span> |
| <span data-ttu-id="c705f-114">RTM- \_ Ansichts- \_ ID- \_ ucast</span><span class="sxs-lookup"><span data-stu-id="c705f-114">RTM\_VIEW\_ID\_UCAST</span></span>     | <span data-ttu-id="c705f-115">0</span><span class="sxs-lookup"><span data-stu-id="c705f-115">0</span></span>          | <span data-ttu-id="c705f-116">Gibt eine unicastansicht an.</span><span class="sxs-lookup"><span data-stu-id="c705f-116">Specifies a unicast view.</span></span>                                        |
| <span data-ttu-id="c705f-117">RTM- \_ Ansichts- \_ ID- \_ mcast</span><span class="sxs-lookup"><span data-stu-id="c705f-117">RTM\_VIEW\_ID\_MCAST</span></span>     | <span data-ttu-id="c705f-118">1</span><span class="sxs-lookup"><span data-stu-id="c705f-118">1</span></span>          | <span data-ttu-id="c705f-119">Gibt eine Multicast Ansicht an.</span><span class="sxs-lookup"><span data-stu-id="c705f-119">Specifies a multicast view.</span></span>                                      |
| <span data-ttu-id="c705f-120">RTM- \_ Ansichts \_ Masken \_ Größe</span><span class="sxs-lookup"><span data-stu-id="c705f-120">RTM\_VIEW\_MASK\_SIZE</span></span>    | <span data-ttu-id="c705f-121">0x20</span><span class="sxs-lookup"><span data-stu-id="c705f-121">0x20</span></span>       | <span data-ttu-id="c705f-122">Gibt die maximale Anzahl von Sichten an, die konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="c705f-122">Specifies the maximum number of views that can be configured.</span></span>    |
| <span data-ttu-id="c705f-123">RTM- \_ Ansicht \_ Maske nicht \_</span><span class="sxs-lookup"><span data-stu-id="c705f-123">RTM\_VIEW\_MASK\_NONE</span></span>    | <span data-ttu-id="c705f-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c705f-124">0x00000000</span></span> | <span data-ttu-id="c705f-125">Gibt Informationen unabhängig von der Sicht zurück.</span><span class="sxs-lookup"><span data-stu-id="c705f-125">Returns information regardless of the view.</span></span>                      |
| <span data-ttu-id="c705f-126">RTM- \_ Ansicht \_ maskieren \_</span><span class="sxs-lookup"><span data-stu-id="c705f-126">RTM\_VIEW\_MASK\_ANY</span></span>     | <span data-ttu-id="c705f-127">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c705f-127">0x00000000</span></span> | <span data-ttu-id="c705f-128">Gibt Ziele aus allen Ansichten zurück.</span><span class="sxs-lookup"><span data-stu-id="c705f-128">Returns destinations from all views.</span></span> <span data-ttu-id="c705f-129">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="c705f-129">This is the default value.</span></span>  |
| <span data-ttu-id="c705f-130">RTM- \_ Ansichts \_ Maske ( \_ ucast)</span><span class="sxs-lookup"><span data-stu-id="c705f-130">RTM\_VIEW\_MASK\_UCAST</span></span>   | <span data-ttu-id="c705f-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c705f-131">0x00000001</span></span> | <span data-ttu-id="c705f-132">Gibt Ziele aus der unicastansicht zurück.</span><span class="sxs-lookup"><span data-stu-id="c705f-132">Returns destinations from the unicast view.</span></span>                      |
| <span data-ttu-id="c705f-133">RTM- \_ Ansicht \_ mask \_ mcast</span><span class="sxs-lookup"><span data-stu-id="c705f-133">RTM\_VIEW\_MASK\_MCAST</span></span>   | <span data-ttu-id="c705f-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c705f-134">0x00000002</span></span> | <span data-ttu-id="c705f-135">Gibt Ziele aus der Multicast Ansicht zurück.</span><span class="sxs-lookup"><span data-stu-id="c705f-135">Returns destinations from the multicast view.</span></span>                    |
| <span data-ttu-id="c705f-136">RTM- \_ Ansicht \_ maskieren \_</span><span class="sxs-lookup"><span data-stu-id="c705f-136">RTM\_VIEW\_MASK\_ALL</span></span>     | <span data-ttu-id="c705f-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c705f-137">0xFFFFFFFF</span></span> | <span data-ttu-id="c705f-138">Gibt Informationen aus allen Sichten zurück.</span><span class="sxs-lookup"><span data-stu-id="c705f-138">Returns information from all views.</span></span>                              |



 

 

 




