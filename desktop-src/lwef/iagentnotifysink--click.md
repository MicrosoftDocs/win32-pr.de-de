---
title: Iagentnotifysink klicken
description: Iagentnotifysink klicken
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d1dccd838152503c603d158f043a0279d4b5c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037156"
---
# <a name="iagentnotifysinkclick"></a><span data-ttu-id="63b5e-103">Iagentnotifysink:: Click</span><span class="sxs-lookup"><span data-stu-id="63b5e-103">IAgentNotifySink::Click</span></span>

<span data-ttu-id="63b5e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="63b5e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="63b5e-105">Benachrichtigt eine Client Anwendung, wenn der Benutzer auf das Task leisten Symbol eines Zeichens oder Zeichens klickt.</span><span class="sxs-lookup"><span data-stu-id="63b5e-105">Notifies a client application when the user clicks a character or character's taskbar icon.</span></span>

-   <span data-ttu-id="63b5e-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="63b5e-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="63b5e-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="63b5e-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="63b5e-108">Der Bezeichner des angeklickten Zeichens.</span><span class="sxs-lookup"><span data-stu-id="63b5e-108">Identifier of the clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="63b5e-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*"f"-Schlüssel*</span><span class="sxs-lookup"><span data-stu-id="63b5e-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="63b5e-110">Ein-Parameter, der den Mauszeiger-und modifiziererschlüsselzustand angibt.</span><span class="sxs-lookup"><span data-stu-id="63b5e-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="63b5e-111">Der-Parameter kann eine beliebige Kombination der folgenden zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="63b5e-111">The parameter can return any combination of the following:</span></span>



|        |                                                |
|--------|------------------------------------------------|
| <span data-ttu-id="63b5e-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="63b5e-112">0x0001</span></span> | <span data-ttu-id="63b5e-113">Linke Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="63b5e-113">Left Button</span></span>                                    |
| <span data-ttu-id="63b5e-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="63b5e-114">0x0010</span></span> | <span data-ttu-id="63b5e-115">Mittlere Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="63b5e-115">Middle Button</span></span>                                  |
| <span data-ttu-id="63b5e-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="63b5e-116">0x0002</span></span> | <span data-ttu-id="63b5e-117">Rechte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="63b5e-117">Right Button</span></span>                                   |
| <span data-ttu-id="63b5e-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="63b5e-118">0x0004</span></span> | <span data-ttu-id="63b5e-119">Umschalttaste nach unten</span><span class="sxs-lookup"><span data-stu-id="63b5e-119">Shift Key Down</span></span>                                 |
| <span data-ttu-id="63b5e-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="63b5e-120">0x0008</span></span> | <span data-ttu-id="63b5e-121">Steuerelement Taste unten</span><span class="sxs-lookup"><span data-stu-id="63b5e-121">Control Key Down</span></span>                               |
| <span data-ttu-id="63b5e-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="63b5e-122">0x0020</span></span> | <span data-ttu-id="63b5e-123">Alt-Taste unten</span><span class="sxs-lookup"><span data-stu-id="63b5e-123">Alt Key Down</span></span>                                   |
| <span data-ttu-id="63b5e-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="63b5e-124">0x1000</span></span> | <span data-ttu-id="63b5e-125">Das Ereignis ist auf dem Task leisten Symbol des Zeichens aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="63b5e-125">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="63b5e-126"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="63b5e-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="63b5e-127">Die x-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="63b5e-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="63b5e-128"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="63b5e-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="63b5e-129">Die y-Koordinate des Mauszeigers in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="63b5e-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="63b5e-130">Dieses Ereignis wird an den Eingabe aktiven Client des Zeichens gesendet.</span><span class="sxs-lookup"><span data-stu-id="63b5e-130">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="63b5e-131">Wenn keiner der Clients des Zeichens Eingabe aktiv ist, benachrichtigt der Server den aktiven Client des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="63b5e-131">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="63b5e-132">Wenn das Zeichen sichtbar ist, bewirkt der Server, dass der Client die Eingabe aktiv durchführt, und sendet [**iagentnotifysink:: activateinputstate**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="63b5e-132">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="63b5e-133">Wenn das Zeichen ausgeblendet ist, wird auch das Zeichen automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="63b5e-133">If the character hidden, the character is also automatically shown.</span></span>

 

 




