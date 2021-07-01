---
title: IAgentNotifySink-Klick
description: IAgentNotifySink-Klick
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0e63244a89467225a7bfd045af6dc112431d12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120903"
---
# <a name="iagentnotifysinkclick"></a><span data-ttu-id="fa5b7-103">IAgentNotifySink::Click</span><span class="sxs-lookup"><span data-stu-id="fa5b7-103">IAgentNotifySink::Click</span></span>

<span data-ttu-id="fa5b7-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="fa5b7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="fa5b7-105">Benachrichtigt eine Clientanwendung, wenn der Benutzer auf das Taskleistensymbol eines Zeichens oder Zeichens klickt.</span><span class="sxs-lookup"><span data-stu-id="fa5b7-105">Notifies a client application when the user clicks a character or character's taskbar icon.</span></span>

-   <span data-ttu-id="fa5b7-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="fa5b7-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="fa5b7-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="fa5b7-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="fa5b7-108">Bezeichner des geklickten Zeichens.</span><span class="sxs-lookup"><span data-stu-id="fa5b7-108">Identifier of the clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="fa5b7-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="fa5b7-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="fa5b7-110">Ein Parameter, der den Zustand der Maustaste und des Modifizierers angibt.</span><span class="sxs-lookup"><span data-stu-id="fa5b7-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="fa5b7-111">Der -Parameter kann eine beliebige Kombination der folgenden Punkte zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="fa5b7-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="fa5b7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fa5b7-112">Value</span></span>  | <span data-ttu-id="fa5b7-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa5b7-113">Description</span></span>                                    |
|--------|------------------------------------------------|
| <span data-ttu-id="fa5b7-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="fa5b7-114">0x0001</span></span> | <span data-ttu-id="fa5b7-115">Linke Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="fa5b7-115">Left Button</span></span>                                    |
| <span data-ttu-id="fa5b7-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="fa5b7-116">0x0010</span></span> | <span data-ttu-id="fa5b7-117">Mittlere Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="fa5b7-117">Middle Button</span></span>                                  |
| <span data-ttu-id="fa5b7-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="fa5b7-118">0x0002</span></span> | <span data-ttu-id="fa5b7-119">Rechte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="fa5b7-119">Right Button</span></span>                                   |
| <span data-ttu-id="fa5b7-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="fa5b7-120">0x0004</span></span> | <span data-ttu-id="fa5b7-121">UMSCHALTTASTE NACH UNTEN</span><span class="sxs-lookup"><span data-stu-id="fa5b7-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="fa5b7-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="fa5b7-122">0x0008</span></span> | <span data-ttu-id="fa5b7-123">Steuertaste nach unten</span><span class="sxs-lookup"><span data-stu-id="fa5b7-123">Control Key Down</span></span>                               |
| <span data-ttu-id="fa5b7-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="fa5b7-124">0x0020</span></span> | <span data-ttu-id="fa5b7-125">ALT-TASTE NACH UNTEN</span><span class="sxs-lookup"><span data-stu-id="fa5b7-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="fa5b7-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="fa5b7-126">0x1000</span></span> | <span data-ttu-id="fa5b7-127">Das Ereignis ist auf dem Taskleistensymbol des Zeichens aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="fa5b7-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="fa5b7-128"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="fa5b7-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="fa5b7-129">Die x-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).</span><span class="sxs-lookup"><span data-stu-id="fa5b7-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="fa5b7-130"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="fa5b7-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="fa5b7-131">Die y-Koordinate des Mauszeigers in Pixel relativ zum Ursprung des Bildschirms (links oben).</span><span class="sxs-lookup"><span data-stu-id="fa5b7-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="fa5b7-132">Dieses Ereignis wird an den eingabeaktiven Client des Zeichens gesendet.</span><span class="sxs-lookup"><span data-stu-id="fa5b7-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="fa5b7-133">Wenn keiner der Clients des Zeichens eingabeaktiv ist, benachrichtigt der Server den aktiven Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="fa5b7-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="fa5b7-134">Wenn das Zeichen sichtbar ist, macht der Server diesen Client auch eingabeaktiv und sendet [**den IAgentNotifySink::ActivateInputState.**](iagentnotifysink--activateinputstate.md)</span><span class="sxs-lookup"><span data-stu-id="fa5b7-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="fa5b7-135">Wenn das Zeichen ausgeblendet ist, wird das Zeichen ebenfalls automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa5b7-135">If the character hidden, the character is also automatically shown.</span></span>

 

 




