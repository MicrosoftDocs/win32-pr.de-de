---
title: ButtonElement. Down
description: Mit dem Attribut "Down" wird ein Wert angegeben oder abgerufen, der angibt, ob sich das Schaltflächen Element an der nach-oben-oder der
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- ButtonElement. Down-Windows-Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370163"
---
# <a name="buttonelementdown"></a><span data-ttu-id="12750-104">ButtonElement. Down</span><span class="sxs-lookup"><span data-stu-id="12750-104">BUTTONELEMENT.down</span></span>

<span data-ttu-id="12750-105">Mit dem Attribut " **down** " wird ein Wert angegeben oder abgerufen, der angibt, ob sich das Schaltflächen Element an der nach-oben-oder der</span><span class="sxs-lookup"><span data-stu-id="12750-105">The **down** attribute specifies or retrieves a value indicating whether the button element is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="12750-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="12750-106">Possible Values</span></span>

<span data-ttu-id="12750-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="12750-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="12750-108">Wert</span><span class="sxs-lookup"><span data-stu-id="12750-108">Value</span></span> | <span data-ttu-id="12750-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12750-109">Description</span></span>                                                     |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="12750-110">true</span><span class="sxs-lookup"><span data-stu-id="12750-110">true</span></span>  | <span data-ttu-id="12750-111">Gibt an, dass sich das **ButtonElement** an der Position nach unten befindet.</span><span class="sxs-lookup"><span data-stu-id="12750-111">Indicates the **BUTTONELEMENT** is in the down position.</span></span>        |
| <span data-ttu-id="12750-112">false</span><span class="sxs-lookup"><span data-stu-id="12750-112">false</span></span> | <span data-ttu-id="12750-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="12750-113">Default.</span></span> <span data-ttu-id="12750-114">Gibt an, dass sich das **ButtonElement** in der aufwärts-Position befindet.</span><span class="sxs-lookup"><span data-stu-id="12750-114">Indicates the **BUTTONELEMENT** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="12750-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12750-115">Remarks</span></span>

<span data-ttu-id="12750-116">Damit ein Button-Element an der nach-unten-Position verbleibt **, muss die** Kurznotiz auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="12750-116">For a button element to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="12750-117">Standardmäßig ist die Kurznotiz false, und jeder **Versuch, auf true fest** **zulegen, wird** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="12750-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="12750-118">Wenn ein ungültiger Wert angegeben wird, wird der vorherige Zustand beibehalten.</span><span class="sxs-lookup"><span data-stu-id="12750-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="12750-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12750-119">Requirements</span></span>



| <span data-ttu-id="12750-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12750-120">Requirement</span></span> | <span data-ttu-id="12750-121">Wert</span><span class="sxs-lookup"><span data-stu-id="12750-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="12750-122">Version</span><span class="sxs-lookup"><span data-stu-id="12750-122">Version</span></span><br/> | <span data-ttu-id="12750-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="12750-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12750-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12750-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12750-125">**ButtonElement-Element**</span><span class="sxs-lookup"><span data-stu-id="12750-125">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="12750-126">**ButtonElement. downtooltip**</span><span class="sxs-lookup"><span data-stu-id="12750-126">**BUTTONELEMENT.downToolTip**</span></span>](buttonelement-downtooltip.md)
</dt> </dl>

 

 





