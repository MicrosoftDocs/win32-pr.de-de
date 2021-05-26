---
title: Player.StringCollectionChange-Ereignis
description: Das StringCollectionChange-Ereignis tritt auf, wenn sich eine Zeichenfolgenauflistung ändert. | Player.StringCollectionChange-Ereignis
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- StringCollectionChange-Ereignis Windows Media Player
- StringCollectionChange-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , StringCollectionChange-Ereignis
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
ms.openlocfilehash: e6a61b8e1e09e749579f323d506371138b0d9b59
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424090"
---
# <a name="playerstringcollectionchange-event"></a><span data-ttu-id="b4af1-107">Player.StringCollectionChange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b4af1-107">Player.StringCollectionChange event</span></span>

<span data-ttu-id="b4af1-108">Das StringCollectionChange-Ereignis tritt auf, wenn sich eine Zeichenfolgenauflistung ändert.</span><span class="sxs-lookup"><span data-stu-id="b4af1-108">The StringCollectionChange event occurs when a string collection changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4af1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4af1-109">Syntax</span></span>


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a><span data-ttu-id="b4af1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4af1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4af1-111">*pdispStringCollection*</span><span class="sxs-lookup"><span data-stu-id="b4af1-111">*pdispStringCollection*</span></span> 
</dt> <dd>

<span data-ttu-id="b4af1-112">**StringCollection-Objekt,** das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b4af1-112">**StringCollection** object that changed.</span></span>

</dd> <dt>

<span data-ttu-id="b4af1-113">*change*</span><span class="sxs-lookup"><span data-stu-id="b4af1-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="b4af1-114">Zahl (long), die den Typ der Änderung angibt, die an der Zeichenfolgenauflistung vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="b4af1-114">Number (long)indicating the type of change that occurred to the string collection.</span></span> <span data-ttu-id="b4af1-115">Enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="b4af1-115">Includes one of the following values.</span></span>



| <span data-ttu-id="b4af1-116">Number</span><span class="sxs-lookup"><span data-stu-id="b4af1-116">Number</span></span> | <span data-ttu-id="b4af1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4af1-117">Description</span></span>                        |
|--------|------------------------------------|
| <span data-ttu-id="b4af1-118">0</span><span class="sxs-lookup"><span data-stu-id="b4af1-118">0</span></span>      | <span data-ttu-id="b4af1-119">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="b4af1-119">Unknown.</span></span> <span data-ttu-id="b4af1-120">(Kein gültiger Wert)</span><span class="sxs-lookup"><span data-stu-id="b4af1-120">(Not a valid value)</span></span>       |
| <span data-ttu-id="b4af1-121">1</span><span class="sxs-lookup"><span data-stu-id="b4af1-121">1</span></span>      | <span data-ttu-id="b4af1-122">Ein Element wurde eingefügt.</span><span class="sxs-lookup"><span data-stu-id="b4af1-122">An item was inserted.</span></span>              |
| <span data-ttu-id="b4af1-123">2</span><span class="sxs-lookup"><span data-stu-id="b4af1-123">2</span></span>      | <span data-ttu-id="b4af1-124">Die Zeichenfolgenauflistung wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="b4af1-124">The string collection changed.</span></span>     |
| <span data-ttu-id="b4af1-125">3</span><span class="sxs-lookup"><span data-stu-id="b4af1-125">3</span></span>      | <span data-ttu-id="b4af1-126">Ein Element wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b4af1-126">An item was deleted.</span></span>               |
| <span data-ttu-id="b4af1-127">4</span><span class="sxs-lookup"><span data-stu-id="b4af1-127">4</span></span>      | <span data-ttu-id="b4af1-128">Die Zeichenfolgenauflistung wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b4af1-128">The string collection was cleared.</span></span> |
| <span data-ttu-id="b4af1-129">5</span><span class="sxs-lookup"><span data-stu-id="b4af1-129">5</span></span>      | <span data-ttu-id="b4af1-130">Massenaktualisierungen beginnen.</span><span class="sxs-lookup"><span data-stu-id="b4af1-130">Bulk updates are beginning.</span></span>        |
| <span data-ttu-id="b4af1-131">6</span><span class="sxs-lookup"><span data-stu-id="b4af1-131">6</span></span>      | <span data-ttu-id="b4af1-132">Massenupdates wurden beendet.</span><span class="sxs-lookup"><span data-stu-id="b4af1-132">Bulk updates have ended.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="b4af1-133">*lCollectionIndex*</span><span class="sxs-lookup"><span data-stu-id="b4af1-133">*lCollectionIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="b4af1-134">Zahl (long), die den Index des geänderten Zeichenfolgensammlungselements enthält.</span><span class="sxs-lookup"><span data-stu-id="b4af1-134">Number (long) containing the index of the string collection item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4af1-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4af1-135">Return value</span></span>

<span data-ttu-id="b4af1-136">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b4af1-136">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4af1-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4af1-137">Remarks</span></span>

<span data-ttu-id="b4af1-138">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b4af1-138">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4af1-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4af1-139">Requirements</span></span>



| <span data-ttu-id="b4af1-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4af1-140">Requirement</span></span> | <span data-ttu-id="b4af1-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b4af1-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4af1-142">Version</span><span class="sxs-lookup"><span data-stu-id="b4af1-142">Version</span></span><br/> | <span data-ttu-id="b4af1-143">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="b4af1-143">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="b4af1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b4af1-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="b4af1-145"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4af1-145"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4af1-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4af1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4af1-147">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b4af1-147">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="b4af1-148">**StringCollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b4af1-148">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





