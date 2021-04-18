---
title: Player. playstate
description: Die playstate-Eigenschaft ruft einen Wert ab, der den Zustand des Windows-Media Player Vorgangs angibt.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Player. playstate-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351306"
---
# <a name="playerplaystate"></a><span data-ttu-id="bf666-104">Player. playstate</span><span class="sxs-lookup"><span data-stu-id="bf666-104">Player.playState</span></span>

<span data-ttu-id="bf666-105">Die **playstate** -Eigenschaft ruft einen Wert ab, der den Zustand des Windows-Media Player Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="bf666-105">The **playState** property retrieves a value indicating the state of the Windows Media Player operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf666-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf666-106">Syntax</span></span>

<span data-ttu-id="bf666-107">*Player* . **playstate**</span><span class="sxs-lookup"><span data-stu-id="bf666-107">*player* .**playState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="bf666-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="bf666-108">Possible Values</span></span>

<span data-ttu-id="bf666-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="bf666-109">This property is a read-only **Number** (**long**).</span></span> <span data-ttu-id="bf666-110">Die Enumerationskonstante im C-Stil kann durch Voranstellen des Zustands Werts mit "wmpps" abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="bf666-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpps".</span></span> <span data-ttu-id="bf666-111">Beispielsweise ist die Konstante für den Wiedergabe Zustand **wmppsplay**.</span><span class="sxs-lookup"><span data-stu-id="bf666-111">For example, the constant for the Playing state is **wmppsPlaying**.</span></span>



| <span data-ttu-id="bf666-112">Wert</span><span class="sxs-lookup"><span data-stu-id="bf666-112">Value</span></span> | <span data-ttu-id="bf666-113">State</span><span class="sxs-lookup"><span data-stu-id="bf666-113">State</span></span>         | <span data-ttu-id="bf666-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf666-114">Description</span></span>                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf666-115">0</span><span class="sxs-lookup"><span data-stu-id="bf666-115">0</span></span>     | <span data-ttu-id="bf666-116">Nicht definiert</span><span class="sxs-lookup"><span data-stu-id="bf666-116">Undefined</span></span>     | <span data-ttu-id="bf666-117">Windows Media Player befindet sich in einem nicht definierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="bf666-117">Windows Media Player is in an undefined state.</span></span>                                                                              |
| <span data-ttu-id="bf666-118">1</span><span class="sxs-lookup"><span data-stu-id="bf666-118">1</span></span>     | <span data-ttu-id="bf666-119">Beendet</span><span class="sxs-lookup"><span data-stu-id="bf666-119">Stopped</span></span>       | <span data-ttu-id="bf666-120">Die Wiedergabe des aktuellen Medien Elements wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="bf666-120">Playback of the current media item is stopped.</span></span>                                                                              |
| <span data-ttu-id="bf666-121">2</span><span class="sxs-lookup"><span data-stu-id="bf666-121">2</span></span>     | <span data-ttu-id="bf666-122">Angehalten</span><span class="sxs-lookup"><span data-stu-id="bf666-122">Paused</span></span>        | <span data-ttu-id="bf666-123">Die Wiedergabe des aktuellen Medien Elements wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="bf666-123">Playback of the current media item is paused.</span></span> <span data-ttu-id="bf666-124">Wenn ein Medien Element angehalten wird, beginnt das Fortsetzen der Wiedergabe am gleichen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="bf666-124">When a media item is paused, resuming playback begins from the same location.</span></span> |
| <span data-ttu-id="bf666-125">3</span><span class="sxs-lookup"><span data-stu-id="bf666-125">3</span></span>     | <span data-ttu-id="bf666-126">Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="bf666-126">Playing</span></span>       | <span data-ttu-id="bf666-127">Das aktuelle Medien Element wird abgespielt.</span><span class="sxs-lookup"><span data-stu-id="bf666-127">The current media item is playing.</span></span>                                                                                          |
| <span data-ttu-id="bf666-128">4</span><span class="sxs-lookup"><span data-stu-id="bf666-128">4</span></span>     | <span data-ttu-id="bf666-129">Scanforward</span><span class="sxs-lookup"><span data-stu-id="bf666-129">ScanForward</span></span>   | <span data-ttu-id="bf666-130">Das aktuelle Medien Element ist eine schnelle Weiterleitung.</span><span class="sxs-lookup"><span data-stu-id="bf666-130">The current media item is fast forwarding.</span></span>                                                                                  |
| <span data-ttu-id="bf666-131">5</span><span class="sxs-lookup"><span data-stu-id="bf666-131">5</span></span>     | <span data-ttu-id="bf666-132">Scanreverse</span><span class="sxs-lookup"><span data-stu-id="bf666-132">ScanReverse</span></span>   | <span data-ttu-id="bf666-133">Das aktuelle Medien Element ist schnelles reaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf666-133">The current media item is fast rewinding.</span></span>                                                                                   |
| <span data-ttu-id="bf666-134">6</span><span class="sxs-lookup"><span data-stu-id="bf666-134">6</span></span>     | <span data-ttu-id="bf666-135">Pufferung</span><span class="sxs-lookup"><span data-stu-id="bf666-135">Buffering</span></span>     | <span data-ttu-id="bf666-136">Das aktuelle Medien Element erhält zusätzliche Daten vom Server.</span><span class="sxs-lookup"><span data-stu-id="bf666-136">The current media item is getting additional data from the server.</span></span>                                                          |
| <span data-ttu-id="bf666-137">7</span><span class="sxs-lookup"><span data-stu-id="bf666-137">7</span></span>     | <span data-ttu-id="bf666-138">Warten</span><span class="sxs-lookup"><span data-stu-id="bf666-138">Waiting</span></span>       | <span data-ttu-id="bf666-139">Die Verbindung wird hergestellt, aber der Server sendet keine Daten.</span><span class="sxs-lookup"><span data-stu-id="bf666-139">Connection is established, but the server is not sending data.</span></span> <span data-ttu-id="bf666-140">Warten auf das Starten der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bf666-140">Waiting for session to begin.</span></span>                                |
| <span data-ttu-id="bf666-141">8</span><span class="sxs-lookup"><span data-stu-id="bf666-141">8</span></span>     | <span data-ttu-id="bf666-142">MediaEnded</span><span class="sxs-lookup"><span data-stu-id="bf666-142">MediaEnded</span></span>    | <span data-ttu-id="bf666-143">Die Wiedergabe des Medien Elements wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="bf666-143">Media item has completed playback.</span></span>                                                                                          |
| <span data-ttu-id="bf666-144">9</span><span class="sxs-lookup"><span data-stu-id="bf666-144">9</span></span>     | <span data-ttu-id="bf666-145">Im Übergang</span><span class="sxs-lookup"><span data-stu-id="bf666-145">Transitioning</span></span> | <span data-ttu-id="bf666-146">Neues Medien Element wird vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="bf666-146">Preparing new media item.</span></span>                                                                                                   |
| <span data-ttu-id="bf666-147">10</span><span class="sxs-lookup"><span data-stu-id="bf666-147">10</span></span>    | <span data-ttu-id="bf666-148">Bereit</span><span class="sxs-lookup"><span data-stu-id="bf666-148">Ready</span></span>         | <span data-ttu-id="bf666-149">Bereit für die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="bf666-149">Ready to begin playing.</span></span>                                                                                                     |
| <span data-ttu-id="bf666-150">11</span><span class="sxs-lookup"><span data-stu-id="bf666-150">11</span></span>    | <span data-ttu-id="bf666-151">Verbindung</span><span class="sxs-lookup"><span data-stu-id="bf666-151">Reconnecting</span></span>  | <span data-ttu-id="bf666-152">Verbindung mit Stream wird wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="bf666-152">Reconnecting to stream.</span></span>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="bf666-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf666-153">Remarks</span></span>

<span data-ttu-id="bf666-154">Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="bf666-154">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="bf666-155">Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf.</span><span class="sxs-lookup"><span data-stu-id="bf666-155">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="bf666-156">Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.</span><span class="sxs-lookup"><span data-stu-id="bf666-156">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="bf666-157">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf666-157">Examples</span></span>

<span data-ttu-id="bf666-158">Der folgende JScript-Code zeigt die Verwendung des *Players*. **playstate** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bf666-158">The following JScript code shows the use of the *player*.**playState** property.</span></span> <span data-ttu-id="bf666-159">Ein HTML-Textelement mit dem Namen "MyText" zeigt den aktuellen Status an.</span><span class="sxs-lookup"><span data-stu-id="bf666-159">An HTML text element, named "myText", displays the current status.</span></span> <span data-ttu-id="bf666-160">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf666-160">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a><span data-ttu-id="bf666-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf666-161">Requirements</span></span>



| <span data-ttu-id="bf666-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf666-162">Requirement</span></span> | <span data-ttu-id="bf666-163">Wert</span><span class="sxs-lookup"><span data-stu-id="bf666-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf666-164">Version</span><span class="sxs-lookup"><span data-stu-id="bf666-164">Version</span></span><br/> | <span data-ttu-id="bf666-165">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="bf666-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bf666-166">DLL</span><span class="sxs-lookup"><span data-stu-id="bf666-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="bf666-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf666-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf666-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf666-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf666-169">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="bf666-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="bf666-170">**Player. PlayStateChange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="bf666-170">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> </dl>

 

 





