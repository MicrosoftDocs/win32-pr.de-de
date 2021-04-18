---
title: Customslider. onpositionchange
description: Der onpositionchange-Ereignishandler behandelt ein Ereignis, das auftritt, wenn sich die Position des Schiebereglers durch Klicken oder ziehen ändert. | Customslider. onpositionchange
ms.assetid: d8fe99a2-69ff-4e75-8d7d-506bcb2f75bf
keywords:
- Customslider. onpositionchange-Fenster Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3d5547d66ca6dc1b770242301bd95ed010a8d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368547"
---
# <a name="customslideronpositionchange"></a><span data-ttu-id="5f9ef-105">Customslider. onpositionchange</span><span class="sxs-lookup"><span data-stu-id="5f9ef-105">CUSTOMSLIDER.onPositionChange</span></span>

<span data-ttu-id="5f9ef-106">Der **onpositionchange** -Ereignishandler behandelt ein Ereignis, das auftritt, wenn sich die Position des Schiebereglers durch Klicken oder ziehen ändert.</span><span class="sxs-lookup"><span data-stu-id="5f9ef-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="5f9ef-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f9ef-107">Remarks</span></span>

<span data-ttu-id="5f9ef-108">Wenn sich die Position des benutzerdefinierten Schiebereglers aufgrund des im Skript geänderten **Wert** Attributs ändert, wird dieses Ereignis nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="5f9ef-108">If the position of the custom slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="5f9ef-109">Um diese Möglichkeit zu berücksichtigen, implementieren Sie stattdessen den **Wert des \_ OnChange** -Ereignis Handlers.</span><span class="sxs-lookup"><span data-stu-id="5f9ef-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f9ef-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f9ef-110">Requirements</span></span>



| <span data-ttu-id="5f9ef-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f9ef-111">Requirement</span></span> | <span data-ttu-id="5f9ef-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5f9ef-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5f9ef-113">Version</span><span class="sxs-lookup"><span data-stu-id="5f9ef-113">Version</span></span><br/> | <span data-ttu-id="5f9ef-114">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5f9ef-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f9ef-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f9ef-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f9ef-116">**Customslider-Element**</span><span class="sxs-lookup"><span data-stu-id="5f9ef-116">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





