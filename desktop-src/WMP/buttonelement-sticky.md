---
title: ButtonElement. Kurznotiz
description: Das Attribut "Kurznotiz" gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob das Button Element eine UMSCHALT Fläche ist, d. h. ob es sich um eine Schaltfläche mit zwei Zuständen oder einem einzelnen Zustand handelt
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- ButtonElement. Sticky-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361548"
---
# <a name="buttonelementsticky"></a><span data-ttu-id="de79c-104">ButtonElement. Kurznotiz</span><span class="sxs-lookup"><span data-stu-id="de79c-104">BUTTONELEMENT.sticky</span></span>

<span data-ttu-id="de79c-105">Das **Attribut "** Kurznotiz" gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob das Button **Element** eine UMSCHALT Fläche ist, d. h. ob es sich um eine Schaltfläche mit zwei Zuständen oder einem einzelnen Zustand handelt</span><span class="sxs-lookup"><span data-stu-id="de79c-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTONELEMENT** is a toggle, that is, whether it is a two-state or single-state button.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="de79c-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="de79c-106">Possible Values</span></span>

<span data-ttu-id="de79c-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="de79c-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="de79c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="de79c-108">Value</span></span> | <span data-ttu-id="de79c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de79c-109">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="de79c-110">true</span><span class="sxs-lookup"><span data-stu-id="de79c-110">true</span></span>  | <span data-ttu-id="de79c-111">**ButtonElement** ist eine Kurznotiz.</span><span class="sxs-lookup"><span data-stu-id="de79c-111">**BUTTONELEMENT** is sticky.</span></span>              |
| <span data-ttu-id="de79c-112">false</span><span class="sxs-lookup"><span data-stu-id="de79c-112">false</span></span> | <span data-ttu-id="de79c-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="de79c-113">Default.</span></span> <span data-ttu-id="de79c-114">**ButtonElement** ist nicht Kurznotiz.</span><span class="sxs-lookup"><span data-stu-id="de79c-114">**BUTTONELEMENT** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="de79c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de79c-115">Remarks</span></span>

<span data-ttu-id="de79c-116">Wenn das **Attribut "** Kurznotiz" auf "true" festgelegt ist, wechselt das Schaltflächen Element in den Zustand "nach unten" und verbleibt in diesem Zustand, bis er erneut geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="de79c-116">If the **sticky** attribute is set to true, the button element will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="de79c-117">Wenn sich das Button-Element im Zustand "nach unten" befindet, ist das Attribut " **nach unten** " auf "true" festgelegt, und der entsprechende Teil der Schaltflächen Gruppe " **downImage** "</span><span class="sxs-lookup"><span data-stu-id="de79c-117">When the button element is in the down state, the **down** attribute will be true and the appropriate portion of the button group **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="de79c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de79c-118">Requirements</span></span>



| <span data-ttu-id="de79c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de79c-119">Requirement</span></span> | <span data-ttu-id="de79c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="de79c-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="de79c-121">Version</span><span class="sxs-lookup"><span data-stu-id="de79c-121">Version</span></span><br/> | <span data-ttu-id="de79c-122">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="de79c-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de79c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de79c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de79c-124">**ButtonElement-Element**</span><span class="sxs-lookup"><span data-stu-id="de79c-124">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="de79c-125">**ButtonElement. Down**</span><span class="sxs-lookup"><span data-stu-id="de79c-125">**BUTTONELEMENT.down**</span></span>](buttonelement-down.md)
</dt> <dt>

[<span data-ttu-id="de79c-126">**ButtonGroup. downImage**</span><span class="sxs-lookup"><span data-stu-id="de79c-126">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> </dl>

 

 





