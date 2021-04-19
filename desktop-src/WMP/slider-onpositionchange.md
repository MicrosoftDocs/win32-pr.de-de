---
title: Schieberegler. onpositionchange
description: Der onpositionchange-Ereignishandler behandelt ein Ereignis, das auftritt, wenn sich die Position des Schiebereglers durch Klicken oder ziehen ändert. | Schieberegler. onpositionchange
ms.assetid: c18e9a49-9576-42ae-9f30-249c44d40f41
keywords:
- Schieberegler. onpositionchange-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68faa9e7addd85b9b5f02b8a6c445e7ddf54e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366806"
---
# <a name="slideronpositionchange"></a><span data-ttu-id="ce4c4-105">Schieberegler. onpositionchange</span><span class="sxs-lookup"><span data-stu-id="ce4c4-105">SLIDER.onPositionChange</span></span>

<span data-ttu-id="ce4c4-106">Der **onpositionchange** -Ereignishandler behandelt ein Ereignis, das auftritt, wenn sich die Position des Schiebereglers durch Klicken oder ziehen ändert.</span><span class="sxs-lookup"><span data-stu-id="ce4c4-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="ce4c4-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce4c4-107">Remarks</span></span>

<span data-ttu-id="ce4c4-108">Wenn sich die Position des Schiebereglers aufgrund des im Skript geänderten **Wert** Attributs ändert, wird dieses Ereignis nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ce4c4-108">If the position of the slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="ce4c4-109">Um diese Möglichkeit zu berücksichtigen, implementieren Sie stattdessen den **Wert des \_ OnChange** -Ereignis Handlers.</span><span class="sxs-lookup"><span data-stu-id="ce4c4-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4c4-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce4c4-110">Requirements</span></span>



| <span data-ttu-id="ce4c4-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce4c4-111">Requirement</span></span> | <span data-ttu-id="ce4c4-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ce4c4-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ce4c4-113">Version</span><span class="sxs-lookup"><span data-stu-id="ce4c4-113">Version</span></span><br/> | <span data-ttu-id="ce4c4-114">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ce4c4-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce4c4-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce4c4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce4c4-116">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="ce4c4-116">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





