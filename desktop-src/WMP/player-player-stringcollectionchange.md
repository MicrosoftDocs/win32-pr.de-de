---
title: Player. stringcollectionchange-Ereignis
description: Das stringcollectionchange-Ereignis tritt auf, wenn sich eine Zeichen folgen Auflistung ändert. | Player. stringcollectionchange-Ereignis
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Stringcollectionchange-Ereignisfenster Media Player
- Stringcollectionchange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, stringcollectionchange-Ereignis
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357551"
---
# <a name="playerstringcollectionchange-event"></a><span data-ttu-id="07f9e-107">Player. stringcollectionchange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="07f9e-107">Player.StringCollectionChange event</span></span>

<span data-ttu-id="07f9e-108">Das stringcollectionchange-Ereignis tritt auf, wenn sich eine Zeichen folgen Auflistung ändert.</span><span class="sxs-lookup"><span data-stu-id="07f9e-108">The StringCollectionChange event occurs when a string collection changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f9e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="07f9e-109">Syntax</span></span>


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a><span data-ttu-id="07f9e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07f9e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07f9e-111">*pdispstringcollection*</span><span class="sxs-lookup"><span data-stu-id="07f9e-111">*pdispStringCollection*</span></span> 
</dt> <dd>

<span data-ttu-id="07f9e-112">**StringCollection** -Objekt, das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="07f9e-112">**StringCollection** object that changed.</span></span>

</dd> <dt>

<span data-ttu-id="07f9e-113">*change*</span><span class="sxs-lookup"><span data-stu-id="07f9e-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="07f9e-114">Zahl (Long), die den Typ der Änderung angibt, die in der Zeichen folgen Auflistung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="07f9e-114">Number (long)indicating the type of change that occurred to the string collection.</span></span> <span data-ttu-id="07f9e-115">Enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="07f9e-115">Includes one of the following values.</span></span>



|        |                                    |
|--------|------------------------------------|
| <span data-ttu-id="07f9e-116">Number</span><span class="sxs-lookup"><span data-stu-id="07f9e-116">Number</span></span> | <span data-ttu-id="07f9e-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07f9e-117">Description</span></span>                        |
| <span data-ttu-id="07f9e-118">0</span><span class="sxs-lookup"><span data-stu-id="07f9e-118">0</span></span>      | <span data-ttu-id="07f9e-119">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="07f9e-119">Unknown.</span></span> <span data-ttu-id="07f9e-120">(Kein gültiger Wert)</span><span class="sxs-lookup"><span data-stu-id="07f9e-120">(Not a valid value)</span></span>       |
| <span data-ttu-id="07f9e-121">1</span><span class="sxs-lookup"><span data-stu-id="07f9e-121">1</span></span>      | <span data-ttu-id="07f9e-122">Ein Element wurde eingefügt.</span><span class="sxs-lookup"><span data-stu-id="07f9e-122">An item was inserted.</span></span>              |
| <span data-ttu-id="07f9e-123">2</span><span class="sxs-lookup"><span data-stu-id="07f9e-123">2</span></span>      | <span data-ttu-id="07f9e-124">Die Zeichen folgen Auflistung wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="07f9e-124">The string collection changed.</span></span>     |
| <span data-ttu-id="07f9e-125">3</span><span class="sxs-lookup"><span data-stu-id="07f9e-125">3</span></span>      | <span data-ttu-id="07f9e-126">Ein Element wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="07f9e-126">An item was deleted.</span></span>               |
| <span data-ttu-id="07f9e-127">4</span><span class="sxs-lookup"><span data-stu-id="07f9e-127">4</span></span>      | <span data-ttu-id="07f9e-128">Die Zeichen folgen Auflistung wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="07f9e-128">The string collection was cleared.</span></span> |
| <span data-ttu-id="07f9e-129">5</span><span class="sxs-lookup"><span data-stu-id="07f9e-129">5</span></span>      | <span data-ttu-id="07f9e-130">Massen Aktualisierungen werden gestartet.</span><span class="sxs-lookup"><span data-stu-id="07f9e-130">Bulk updates are beginning.</span></span>        |
| <span data-ttu-id="07f9e-131">6</span><span class="sxs-lookup"><span data-stu-id="07f9e-131">6</span></span>      | <span data-ttu-id="07f9e-132">Massen Aktualisierungen wurden beendet.</span><span class="sxs-lookup"><span data-stu-id="07f9e-132">Bulk updates have ended.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="07f9e-133">*lcollectionindex*</span><span class="sxs-lookup"><span data-stu-id="07f9e-133">*lCollectionIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="07f9e-134">Zahl (Long), die den Index des geänderten Zeichen folgen-Sammel Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="07f9e-134">Number (long) containing the index of the string collection item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07f9e-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07f9e-135">Return value</span></span>

<span data-ttu-id="07f9e-136">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="07f9e-136">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07f9e-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07f9e-137">Remarks</span></span>

<span data-ttu-id="07f9e-138">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="07f9e-138">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="07f9e-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07f9e-139">Requirements</span></span>



| <span data-ttu-id="07f9e-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07f9e-140">Requirement</span></span> | <span data-ttu-id="07f9e-141">Wert</span><span class="sxs-lookup"><span data-stu-id="07f9e-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07f9e-142">Version</span><span class="sxs-lookup"><span data-stu-id="07f9e-142">Version</span></span><br/> | <span data-ttu-id="07f9e-143">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="07f9e-143">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="07f9e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="07f9e-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="07f9e-145"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07f9e-145"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07f9e-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07f9e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f9e-147">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="07f9e-147">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="07f9e-148">**StringCollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="07f9e-148">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





