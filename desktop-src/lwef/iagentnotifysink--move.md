---
title: Iagentnotifysink verschieben
description: Iagentnotifysink verschieben
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948020"
---
# <a name="iagentnotifysinkmove"></a><span data-ttu-id="5b805-103">Iagentnotifysink:: Move</span><span class="sxs-lookup"><span data-stu-id="5b805-103">IAgentNotifySink::Move</span></span>

<span data-ttu-id="5b805-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5b805-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

<span data-ttu-id="5b805-105">Benachrichtigt eine Client Anwendung, wenn das Zeichen verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="5b805-105">Notifies a client application when the character has been moved.</span></span>

-   <span data-ttu-id="5b805-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="5b805-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="5b805-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="5b805-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="5b805-108">Der Bezeichner des Zeichens, das verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="5b805-108">Identifier of the character that has been moved.</span></span>

</dd> <dt>

<span data-ttu-id="5b805-109"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="5b805-109"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="5b805-110">Die x-Koordinate der neuen Position in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="5b805-110">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="5b805-111">Der Speicherort eines Zeichens basiert auf der linken oberen Ecke des Animations Rahmens.</span><span class="sxs-lookup"><span data-stu-id="5b805-111">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="5b805-112"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="5b805-112"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="5b805-113">Die y-Koordinate der neuen Position in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="5b805-113">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="5b805-114">Der Speicherort eines Zeichens basiert auf der linken oberen Ecke des Animations Rahmens.</span><span class="sxs-lookup"><span data-stu-id="5b805-114">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="5b805-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwcause*</span><span class="sxs-lookup"><span data-stu-id="5b805-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="5b805-116">Die Ursache für die Zeichen Verschiebung.</span><span class="sxs-lookup"><span data-stu-id="5b805-116">The cause of the character move.</span></span> <span data-ttu-id="5b805-117">Der Parameter kann eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="5b805-117">The parameter may be one of the following:</span></span>



| <span data-ttu-id="5b805-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5b805-118">Value</span></span>                                                          | <span data-ttu-id="5b805-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b805-119">Description</span></span>                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b805-120">Konstante **Ganzzahl ohne Vorzeichen Short neververschost** **= 0;**</span><span class="sxs-lookup"><span data-stu-id="5b805-120">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="5b805-121">Das Zeichen wurde nicht verschoben.</span><span class="sxs-lookup"><span data-stu-id="5b805-121">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="5b805-122">" **Ganzzahl ohne Vorzeichen Short userverschost** " **= 1;**</span><span class="sxs-lookup"><span data-stu-id="5b805-122">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="5b805-123">Der Benutzer hat das Zeichen gezogen.</span><span class="sxs-lookup"><span data-stu-id="5b805-123">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="5b805-124">" **Ganzzahl ohne Vorzeichen Short Program verschost** " **= 2;**</span><span class="sxs-lookup"><span data-stu-id="5b805-124">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="5b805-125">Die Anwendung hat das Zeichen verschoben.</span><span class="sxs-lookup"><span data-stu-id="5b805-125">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="5b805-126">Konstante **Ganzzahl ohne Vorzeichen Short** **otherprogrambewegt = 3;**</span><span class="sxs-lookup"><span data-stu-id="5b805-126">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="5b805-127">Das Zeichen wurde von einer anderen Anwendung verschoben.</span><span class="sxs-lookup"><span data-stu-id="5b805-127">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="5b805-128">**Ganzzahl ohne Vorzeichen Short** **systemverschost = 4**</span><span class="sxs-lookup"><span data-stu-id="5b805-128">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="5b805-129">Der Server hat das Zeichen verschoben, um es nach einer Änderung der Bildschirmauflösung auf dem Bildschirm aufzubewahren.</span><span class="sxs-lookup"><span data-stu-id="5b805-129">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

<span data-ttu-id="5b805-130">Dieses Ereignis wird an alle Clients des Zeichens gesendet.</span><span class="sxs-lookup"><span data-stu-id="5b805-130">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b805-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5b805-131">See Also</span></span>

<span data-ttu-id="5b805-132">[**Iagentcharacter:: getmuvecause**](iagentcharacter--getmovecause.md), [ **iagentcharacter:: muveto**](iagentcharacter--moveto.md)</span><span class="sxs-lookup"><span data-stu-id="5b805-132">[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)</span></span>


 

 





