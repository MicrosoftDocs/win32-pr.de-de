---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb93fbc7bae1ac43d534962659b850561bd50a6d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120805"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="3010f-103">IAgentNotifySink::D ragComplete</span><span class="sxs-lookup"><span data-stu-id="3010f-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="3010f-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3010f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="3010f-105">Benachrichtigt eine Clientanwendung, wenn der Benutzer das Ziehen eines Zeichens beendet.</span><span class="sxs-lookup"><span data-stu-id="3010f-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="3010f-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="3010f-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="3010f-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="3010f-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="3010f-108">Bezeichner des gezogenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3010f-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="3010f-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="3010f-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="3010f-110">Ein Parameter, der den Zustand der Maustaste und des Modifizierers angibt.</span><span class="sxs-lookup"><span data-stu-id="3010f-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="3010f-111">Der -Parameter kann eine beliebige Kombination der folgenden Punkte zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="3010f-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="3010f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3010f-112">Value</span></span>  | <span data-ttu-id="3010f-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3010f-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="3010f-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="3010f-114">0x0001</span></span> | <span data-ttu-id="3010f-115">Linke Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="3010f-115">Left Button</span></span>      |
| <span data-ttu-id="3010f-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="3010f-116">0x0010</span></span> | <span data-ttu-id="3010f-117">Mittlere Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="3010f-117">Middle Button</span></span>    |
| <span data-ttu-id="3010f-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="3010f-118">0x0002</span></span> | <span data-ttu-id="3010f-119">Rechte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="3010f-119">Right Button</span></span>     |
| <span data-ttu-id="3010f-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="3010f-120">0x0004</span></span> | <span data-ttu-id="3010f-121">UMSCHALTTASTE NACH UNTEN</span><span class="sxs-lookup"><span data-stu-id="3010f-121">Shift Key Down</span></span>   |
| <span data-ttu-id="3010f-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="3010f-122">0x0008</span></span> | <span data-ttu-id="3010f-123">Steuertaste nach unten</span><span class="sxs-lookup"><span data-stu-id="3010f-123">Control Key Down</span></span> |
| <span data-ttu-id="3010f-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="3010f-124">0x0020</span></span> | <span data-ttu-id="3010f-125">ALT-TASTE NACH UNTEN</span><span class="sxs-lookup"><span data-stu-id="3010f-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="3010f-126"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="3010f-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="3010f-127">Die x-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).</span><span class="sxs-lookup"><span data-stu-id="3010f-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="3010f-128"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="3010f-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="3010f-129">Die y-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).</span><span class="sxs-lookup"><span data-stu-id="3010f-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




