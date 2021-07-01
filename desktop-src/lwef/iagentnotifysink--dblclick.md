---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120923"
---
# <a name="iagentnotifysinkdblclick"></a><span data-ttu-id="b3152-103">IAgentNotifySink::D blClick</span><span class="sxs-lookup"><span data-stu-id="b3152-103">IAgentNotifySink::DblClick</span></span>

<span data-ttu-id="b3152-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b3152-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="b3152-105">Benachrichtigt eine Clientanwendung, wenn der Benutzer auf ein Zeichen doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="b3152-105">Notifies a client application when the user double-clicks a character.</span></span>

-   <span data-ttu-id="b3152-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="b3152-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b3152-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="b3152-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="b3152-108">Bezeichner des doppelgeklickten Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b3152-108">Identifier of the double-clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="b3152-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="b3152-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="b3152-110">Ein Parameter, der den Zustand der Maustaste und des Modifiziererschlüssels angibt.</span><span class="sxs-lookup"><span data-stu-id="b3152-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="b3152-111">Der -Parameter kann eine beliebige Kombination der folgenden Angaben zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="b3152-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="b3152-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b3152-112">Value</span></span>  | <span data-ttu-id="b3152-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3152-113">Description</span></span>                               |
|--------|------------------------------------------------|
| <span data-ttu-id="b3152-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="b3152-114">0x0001</span></span> | <span data-ttu-id="b3152-115">Linke Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="b3152-115">Left Button</span></span>                                    |
| <span data-ttu-id="b3152-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="b3152-116">0x0010</span></span> | <span data-ttu-id="b3152-117">Mittlere Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="b3152-117">Middle Button</span></span>                                  |
| <span data-ttu-id="b3152-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="b3152-118">0x0002</span></span> | <span data-ttu-id="b3152-119">Schaltfläche "Rechts"</span><span class="sxs-lookup"><span data-stu-id="b3152-119">Right Button</span></span>                                   |
| <span data-ttu-id="b3152-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="b3152-120">0x0004</span></span> | <span data-ttu-id="b3152-121">UMSCHALTTASTE NACH-UNTEN</span><span class="sxs-lookup"><span data-stu-id="b3152-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="b3152-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="b3152-122">0x0008</span></span> | <span data-ttu-id="b3152-123">Steuerungsschlüssel nach unten</span><span class="sxs-lookup"><span data-stu-id="b3152-123">Control Key Down</span></span>                               |
| <span data-ttu-id="b3152-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="b3152-124">0x0020</span></span> | <span data-ttu-id="b3152-125">ALT-TASTE NACH-UNTEN</span><span class="sxs-lookup"><span data-stu-id="b3152-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="b3152-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="b3152-126">0x1000</span></span> | <span data-ttu-id="b3152-127">Das Ereignis ist auf dem Taskleistensymbol des Zeichens aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b3152-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="b3152-128"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="b3152-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="b3152-129">Die x-Koordinate des Mauszeigers in Pixel relativ zum Bildschirmursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="b3152-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="b3152-130"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="b3152-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="b3152-131">Die y-Koordinate des Mauszeigers in Pixel relativ zum Bildschirmursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="b3152-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="b3152-132">Dieses Ereignis wird an den eingabeaktiven Client des Zeichens gesendet.</span><span class="sxs-lookup"><span data-stu-id="b3152-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="b3152-133">Wenn keiner der Clients des Zeichens eingabeaktiv ist, benachrichtigt der Server den aktiven Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b3152-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="b3152-134">Wenn das Zeichen sichtbar ist, aktiviert der Server auch den Client input-active und sendet [**IAgentNotifySink::ActivateInputState.**](iagentnotifysink--activateinputstate.md)</span><span class="sxs-lookup"><span data-stu-id="b3152-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="b3152-135">Wenn das Zeichen ausgeblendet ist, wird es auch automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b3152-135">If the character is hidden, the character is also automatically shown.</span></span>

 

 




