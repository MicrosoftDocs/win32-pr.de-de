---
title: Schaltfläche. nach unten
description: Mit dem Attribut "Down" wird ein Wert angegeben oder abgerufen, der angibt, ob sich die Schaltfläche an der nach-oben-oder der
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- Button. Windows-Media Player nach unten
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372096"
---
# <a name="buttondown"></a><span data-ttu-id="cfad6-104">Schaltfläche. nach unten</span><span class="sxs-lookup"><span data-stu-id="cfad6-104">BUTTON.down</span></span>

<span data-ttu-id="cfad6-105">Mit dem Attribut " **down** " wird ein Wert angegeben oder abgerufen, der angibt, ob sich die **Schaltfläche** an der nach-oben-oder der</span><span class="sxs-lookup"><span data-stu-id="cfad6-105">The **down** attribute specifies or retrieves a value indicating whether the **BUTTON** is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="cfad6-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="cfad6-106">Possible Values</span></span>

<span data-ttu-id="cfad6-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cfad6-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="cfad6-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cfad6-108">Value</span></span> | <span data-ttu-id="cfad6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfad6-109">Description</span></span>                                                   |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="cfad6-110">true</span><span class="sxs-lookup"><span data-stu-id="cfad6-110">true</span></span>  | <span data-ttu-id="cfad6-111">Gibt an, dass sich die **Schaltfläche** an der Position nach unten befindet.</span><span class="sxs-lookup"><span data-stu-id="cfad6-111">Indicates that the **BUTTON** is in the down position.</span></span>        |
| <span data-ttu-id="cfad6-112">false</span><span class="sxs-lookup"><span data-stu-id="cfad6-112">false</span></span> | <span data-ttu-id="cfad6-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="cfad6-113">Default.</span></span> <span data-ttu-id="cfad6-114">Gibt an, dass sich die **Schaltfläche** in der up-Position befindet.</span><span class="sxs-lookup"><span data-stu-id="cfad6-114">Indicates that the **BUTTON** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cfad6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfad6-115">Remarks</span></span>

<span data-ttu-id="cfad6-116">Damit eine **Schaltfläche** an der nach-unten-Position verbleibt **, muss die** Kurznotiz auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cfad6-116">For a **BUTTON** to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="cfad6-117">Standardmäßig ist die Kurznotiz false, und jeder **Versuch, auf true fest** **zulegen, wird** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cfad6-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="cfad6-118">Wenn ein ungültiger Wert angegeben wird, wird der vorherige Zustand beibehalten.</span><span class="sxs-lookup"><span data-stu-id="cfad6-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfad6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfad6-119">Requirements</span></span>



| <span data-ttu-id="cfad6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfad6-120">Requirement</span></span> | <span data-ttu-id="cfad6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="cfad6-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cfad6-122">Version</span><span class="sxs-lookup"><span data-stu-id="cfad6-122">Version</span></span><br/> | <span data-ttu-id="cfad6-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="cfad6-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cfad6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfad6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfad6-125">**Button-Element**</span><span class="sxs-lookup"><span data-stu-id="cfad6-125">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="cfad6-126">**Button. downImage**</span><span class="sxs-lookup"><span data-stu-id="cfad6-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> <dt>

[<span data-ttu-id="cfad6-127">**Button. downtooltip**</span><span class="sxs-lookup"><span data-stu-id="cfad6-127">**BUTTON.downToolTip**</span></span>](button-downtooltip.md)
</dt> </dl>

 

 





