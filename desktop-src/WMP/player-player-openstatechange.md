---
title: Player. OpenStateChange-Ereignis
description: Das OpenStateChange-Ereignis tritt auf, wenn die openstate-Eigenschaft den Wert ändert. | Player. OpenStateChange-Ereignis
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Media Player für OpenStateChange-Ereignisfenster
- OpenStateChange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player der Player-Klasse, OpenStateChange-Ereignis
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351255"
---
# <a name="playeropenstatechange-event"></a><span data-ttu-id="20bc8-107">Player. OpenStateChange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="20bc8-107">Player.OpenStateChange event</span></span>

<span data-ttu-id="20bc8-108">Das **OpenStateChange** -Ereignis tritt auf, wenn die **openstate** -Eigenschaft den Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="20bc8-108">The **OpenStateChange** event occurs when the **openState** property changes value.</span></span>

## <a name="syntax"></a><span data-ttu-id="20bc8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="20bc8-109">Syntax</span></span>


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="20bc8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="20bc8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20bc8-111">*NewState*</span><span class="sxs-lookup"><span data-stu-id="20bc8-111">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="20bc8-112">**Zahl** (**Long**), die den neuen geöffneten Zustand angibt.</span><span class="sxs-lookup"><span data-stu-id="20bc8-112">**Number** (**long**) specifying the new open state.</span></span> <span data-ttu-id="20bc8-113">Eine Tabelle mit Werten finden Sie unter [openstate](player-openstate.md) .</span><span class="sxs-lookup"><span data-stu-id="20bc8-113">See [openState](player-openstate.md) for a table of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20bc8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20bc8-114">Return value</span></span>

<span data-ttu-id="20bc8-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="20bc8-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20bc8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20bc8-116">Remarks</span></span>

<span data-ttu-id="20bc8-117">Windows-Media Player können mehrere offene Zustände durchlaufen, während versucht wird, eine Netzwerkdatei zu öffnen, z. b. das Auffinden des Servers, das Herstellen einer Verbindung mit dem Server und schließlich das Öffnen der Datei.</span><span class="sxs-lookup"><span data-stu-id="20bc8-117">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="20bc8-118">Dieses Ereignis wird jedes Mal ausgelöst, wenn sich der Status des geöffneten Zustands ändert.</span><span class="sxs-lookup"><span data-stu-id="20bc8-118">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="20bc8-119">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="20bc8-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="20bc8-120">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="20bc8-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="20bc8-121">Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="20bc8-121">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="20bc8-122">Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf.</span><span class="sxs-lookup"><span data-stu-id="20bc8-122">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="20bc8-123">Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.</span><span class="sxs-lookup"><span data-stu-id="20bc8-123">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="20bc8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20bc8-124">Requirements</span></span>



| <span data-ttu-id="20bc8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20bc8-125">Requirement</span></span> | <span data-ttu-id="20bc8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="20bc8-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="20bc8-127">Version</span><span class="sxs-lookup"><span data-stu-id="20bc8-127">Version</span></span><br/> | <span data-ttu-id="20bc8-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="20bc8-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="20bc8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="20bc8-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="20bc8-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20bc8-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bc8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20bc8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bc8-132">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="20bc8-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="20bc8-133">**Player. openstate**</span><span class="sxs-lookup"><span data-stu-id="20bc8-133">**Player.openState**</span></span>](player-openstate.md)
</dt> </dl>

 

 





