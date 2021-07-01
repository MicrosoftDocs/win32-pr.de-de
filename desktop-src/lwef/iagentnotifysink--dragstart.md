---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120824"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="a16a5-103">IAgentNotifySink::D ragStart</span><span class="sxs-lookup"><span data-stu-id="a16a5-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="a16a5-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a16a5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="a16a5-105">Benachrichtigt eine Clientanwendung, wenn der Benutzer mit dem Ziehen eines Zeichens beginnt.</span><span class="sxs-lookup"><span data-stu-id="a16a5-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="a16a5-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a16a5-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="a16a5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="a16a5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="a16a5-108">Bezeichner des gezogenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="a16a5-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="a16a5-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="a16a5-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="a16a5-110">Ein Parameter, der den Zustand der Maustaste und des Modifizierers angibt.</span><span class="sxs-lookup"><span data-stu-id="a16a5-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="a16a5-111">Der -Parameter kann eine beliebige Kombination der folgenden Punkte zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="a16a5-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="a16a5-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a16a5-112">Value</span></span>  | <span data-ttu-id="a16a5-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a16a5-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="a16a5-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="a16a5-114">0x0001</span></span> | <span data-ttu-id="a16a5-115">Linke Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="a16a5-115">Left Button</span></span>      |
| <span data-ttu-id="a16a5-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="a16a5-116">0x0010</span></span> | <span data-ttu-id="a16a5-117">Mittlere Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="a16a5-117">Middle Button</span></span>    |
| <span data-ttu-id="a16a5-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="a16a5-118">0x0002</span></span> | <span data-ttu-id="a16a5-119">Rechte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="a16a5-119">Right Button</span></span>     |
| <span data-ttu-id="a16a5-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="a16a5-120">0x0004</span></span> | <span data-ttu-id="a16a5-121">UMSCHALTTASTE NACH UNTEN</span><span class="sxs-lookup"><span data-stu-id="a16a5-121">Shift Key Down</span></span>   |
| <span data-ttu-id="a16a5-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="a16a5-122">0x0008</span></span> | <span data-ttu-id="a16a5-123">Steuertaste nach unten</span><span class="sxs-lookup"><span data-stu-id="a16a5-123">Control Key Down</span></span> |
| <span data-ttu-id="a16a5-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="a16a5-124">0x0020</span></span> | <span data-ttu-id="a16a5-125">ALT-TASTE NACH UNTEN</span><span class="sxs-lookup"><span data-stu-id="a16a5-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="a16a5-126"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="a16a5-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="a16a5-127">Die x-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).</span><span class="sxs-lookup"><span data-stu-id="a16a5-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a16a5-128"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="a16a5-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="a16a5-129">Die y-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).</span><span class="sxs-lookup"><span data-stu-id="a16a5-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




