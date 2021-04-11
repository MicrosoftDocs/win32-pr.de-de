---
title: Iagentnotifysink DragStart
description: Iagentnotifysink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031e78319beb0f62ddb0ea340fca0cd7ed88c0a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310079"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="153d1-103">Iagentnotifysink::D ragstart</span><span class="sxs-lookup"><span data-stu-id="153d1-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="153d1-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="153d1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="153d1-105">Benachrichtigt eine Client Anwendung, wenn der Benutzer mit dem Ziehen eines Zeichens beginnt.</span><span class="sxs-lookup"><span data-stu-id="153d1-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="153d1-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="153d1-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="153d1-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="153d1-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="153d1-108">Der Bezeichner des gezogenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="153d1-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="153d1-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*"f"-Schlüssel*</span><span class="sxs-lookup"><span data-stu-id="153d1-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="153d1-110">Ein-Parameter, der den Mauszeiger-und modifiziererschlüsselzustand angibt.</span><span class="sxs-lookup"><span data-stu-id="153d1-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="153d1-111">Der-Parameter kann eine beliebige Kombination der folgenden zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="153d1-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="153d1-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="153d1-112">0x0001</span></span> | <span data-ttu-id="153d1-113">Linke Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="153d1-113">Left Button</span></span>      |
| <span data-ttu-id="153d1-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="153d1-114">0x0010</span></span> | <span data-ttu-id="153d1-115">Mittlere Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="153d1-115">Middle Button</span></span>    |
| <span data-ttu-id="153d1-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="153d1-116">0x0002</span></span> | <span data-ttu-id="153d1-117">Rechte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="153d1-117">Right Button</span></span>     |
| <span data-ttu-id="153d1-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="153d1-118">0x0004</span></span> | <span data-ttu-id="153d1-119">Umschalttaste nach unten</span><span class="sxs-lookup"><span data-stu-id="153d1-119">Shift Key Down</span></span>   |
| <span data-ttu-id="153d1-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="153d1-120">0x0008</span></span> | <span data-ttu-id="153d1-121">Steuerelement Taste unten</span><span class="sxs-lookup"><span data-stu-id="153d1-121">Control Key Down</span></span> |
| <span data-ttu-id="153d1-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="153d1-122">0x0020</span></span> | <span data-ttu-id="153d1-123">Alt-Taste unten</span><span class="sxs-lookup"><span data-stu-id="153d1-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="153d1-124"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="153d1-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="153d1-125">Die x-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="153d1-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="153d1-126"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="153d1-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="153d1-127">Die y-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="153d1-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




