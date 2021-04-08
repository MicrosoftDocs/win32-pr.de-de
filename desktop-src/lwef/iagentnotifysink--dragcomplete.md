---
title: Iagentnotifysink dragcomplete
description: Iagentnotifysink dragcomplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53215591e3d2797c5b57e5586ccb13fc91f5902
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037480"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="61257-103">Iagentnotifysink::D ragcomplete</span><span class="sxs-lookup"><span data-stu-id="61257-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="61257-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="61257-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="61257-105">Benachrichtigt eine Client Anwendung, wenn der Benutzer das Ziehen eines Zeichens stoppt.</span><span class="sxs-lookup"><span data-stu-id="61257-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="61257-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="61257-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="61257-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="61257-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="61257-108">Der Bezeichner des gezogenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="61257-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="61257-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*"f"-Schlüssel*</span><span class="sxs-lookup"><span data-stu-id="61257-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="61257-110">Ein-Parameter, der den Mauszeiger-und modifiziererschlüsselzustand angibt.</span><span class="sxs-lookup"><span data-stu-id="61257-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="61257-111">Der-Parameter kann eine beliebige Kombination der folgenden zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="61257-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="61257-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="61257-112">0x0001</span></span> | <span data-ttu-id="61257-113">Linke Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="61257-113">Left Button</span></span>      |
| <span data-ttu-id="61257-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="61257-114">0x0010</span></span> | <span data-ttu-id="61257-115">Mittlere Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="61257-115">Middle Button</span></span>    |
| <span data-ttu-id="61257-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="61257-116">0x0002</span></span> | <span data-ttu-id="61257-117">Rechte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="61257-117">Right Button</span></span>     |
| <span data-ttu-id="61257-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="61257-118">0x0004</span></span> | <span data-ttu-id="61257-119">Umschalttaste nach unten</span><span class="sxs-lookup"><span data-stu-id="61257-119">Shift Key Down</span></span>   |
| <span data-ttu-id="61257-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="61257-120">0x0008</span></span> | <span data-ttu-id="61257-121">Steuerelement Taste unten</span><span class="sxs-lookup"><span data-stu-id="61257-121">Control Key Down</span></span> |
| <span data-ttu-id="61257-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="61257-122">0x0020</span></span> | <span data-ttu-id="61257-123">Alt-Taste unten</span><span class="sxs-lookup"><span data-stu-id="61257-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="61257-124"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="61257-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="61257-125">Die x-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="61257-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="61257-126"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="61257-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="61257-127">Die y-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="61257-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




