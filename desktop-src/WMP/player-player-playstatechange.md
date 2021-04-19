---
title: Player. PlayStateChange-Ereignis
description: Das PlayStateChange-Ereignis tritt auf, wenn die playstate-Eigenschaft geändert wird.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Media Player "PlayStateChange-Ereignisfenster"
- PlayStateChange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, PlayStateChange-Ereignis
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356377"
---
# <a name="playerplaystatechange-event"></a><span data-ttu-id="eedb2-106">Player. PlayStateChange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="eedb2-106">Player.PlayStateChange event</span></span>

<span data-ttu-id="eedb2-107">Das **PlayStateChange** -Ereignis tritt auf, wenn die **playstate** -Eigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="eedb2-107">The **PlayStateChange** event occurs when there is a change in the **playState** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="eedb2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eedb2-108">Syntax</span></span>


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="eedb2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eedb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eedb2-110">*NewState*</span><span class="sxs-lookup"><span data-stu-id="eedb2-110">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="eedb2-111">Number (**Long**), der den neuen **playstate** angibt.</span><span class="sxs-lookup"><span data-stu-id="eedb2-111">Number (**long**) which specifies the new **playState**.</span></span> <span data-ttu-id="eedb2-112">Eine Tabelle mit möglichen Werten finden Sie unter [playstate](player-playstate.md) .</span><span class="sxs-lookup"><span data-stu-id="eedb2-112">See [playState](player-playstate.md) for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eedb2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eedb2-113">Return value</span></span>

<span data-ttu-id="eedb2-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eedb2-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eedb2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eedb2-115">Remarks</span></span>

<span data-ttu-id="eedb2-116">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="eedb2-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="eedb2-117">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="eedb2-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="eedb2-118">Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="eedb2-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="eedb2-119">Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf.</span><span class="sxs-lookup"><span data-stu-id="eedb2-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="eedb2-120">Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.</span><span class="sxs-lookup"><span data-stu-id="eedb2-120">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="eedb2-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eedb2-121">Examples</span></span>

<span data-ttu-id="eedb2-122">Im folgenden Beispiel wird ein Ereignishandler für den *Player* veranschaulicht. **PlayStateChange** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="eedb2-122">The following example demonstrates an event handler for the *Player*.**playStateChange** event.</span></span> <span data-ttu-id="eedb2-123">Ein HTML-Textelement mit dem Namen "MyText" zeigt den neuen Wiedergabe Zustand an.</span><span class="sxs-lookup"><span data-stu-id="eedb2-123">An HTML text element, named "myText", displays the new play state.</span></span> <span data-ttu-id="eedb2-124">Das Player-Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="eedb2-124">The player object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="eedb2-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eedb2-125">Requirements</span></span>



| <span data-ttu-id="eedb2-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eedb2-126">Requirement</span></span> | <span data-ttu-id="eedb2-127">Wert</span><span class="sxs-lookup"><span data-stu-id="eedb2-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eedb2-128">Version</span><span class="sxs-lookup"><span data-stu-id="eedb2-128">Version</span></span><br/> | <span data-ttu-id="eedb2-129">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="eedb2-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="eedb2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="eedb2-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="eedb2-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eedb2-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eedb2-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eedb2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eedb2-133">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="eedb2-133">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="eedb2-134">**Player. playstate**</span><span class="sxs-lookup"><span data-stu-id="eedb2-134">**Player.playState**</span></span>](player-playstate.md)
</dt> </dl>

 

 





