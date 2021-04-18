---
title: Button. Kurznotiz
description: Mit dem Attribut "Kurznotiz" wird ein Wert angegeben oder abgerufen, der angibt, ob die Schaltfläche eine UMSCHALT Fläche ist, d. h. ob es sich um eine Schaltfläche mit zwei Zuständen oder einem Bundesstaat handelt
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- Button. Kurztaste für Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372247"
---
# <a name="buttonsticky"></a><span data-ttu-id="723f0-104">Button. Kurznotiz</span><span class="sxs-lookup"><span data-stu-id="723f0-104">BUTTON.sticky</span></span>

<span data-ttu-id="723f0-105">Mit **dem Attribut "** Kurznotiz" wird ein Wert angegeben oder abgerufen, der angibt, ob die **Schaltfläche** eine UMSCHALT Fläche ist, d. h. ob es sich um eine **Schaltfläche** mit zwei Zuständen oder einem Bundesstaat handelt</span><span class="sxs-lookup"><span data-stu-id="723f0-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTON** is a toggle, that is, whether it is a two-state or single-state **BUTTON**.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="723f0-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="723f0-106">Possible Values</span></span>

<span data-ttu-id="723f0-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="723f0-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="723f0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="723f0-108">Value</span></span> | <span data-ttu-id="723f0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="723f0-109">Description</span></span>                        |
|-------|------------------------------------|
| <span data-ttu-id="723f0-110">true</span><span class="sxs-lookup"><span data-stu-id="723f0-110">true</span></span>  | <span data-ttu-id="723f0-111">Die **Schaltfläche** ist kurz.</span><span class="sxs-lookup"><span data-stu-id="723f0-111">**BUTTON** is sticky.</span></span>              |
| <span data-ttu-id="723f0-112">false</span><span class="sxs-lookup"><span data-stu-id="723f0-112">false</span></span> | <span data-ttu-id="723f0-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="723f0-113">Default.</span></span> <span data-ttu-id="723f0-114">Die **Schaltfläche** ist nicht kurz.</span><span class="sxs-lookup"><span data-stu-id="723f0-114">**BUTTON** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="723f0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="723f0-115">Remarks</span></span>

<span data-ttu-id="723f0-116">Wenn **für** "Kurznotiz" der Wert "true" festgelegt ist, wechselt die **Schaltfläche** in den Zustand "nach unten" und bleibt so lange in diesem Zustand</span><span class="sxs-lookup"><span data-stu-id="723f0-116">If **sticky** is set to true, the **BUTTON** will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="723f0-117">Wenn sich die **Schaltfläche** im Zustand "herunter" befindet, ist das Attribut " **nach unten** " auf "true" festgelegt, und das **Fenster Mage** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="723f0-117">When the **BUTTON** is in the down state, the **down** attribute will be true and the **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="723f0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="723f0-118">Requirements</span></span>



| <span data-ttu-id="723f0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="723f0-119">Requirement</span></span> | <span data-ttu-id="723f0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="723f0-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="723f0-121">Version</span><span class="sxs-lookup"><span data-stu-id="723f0-121">Version</span></span><br/> | <span data-ttu-id="723f0-122">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="723f0-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="723f0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="723f0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723f0-124">**Button-Element**</span><span class="sxs-lookup"><span data-stu-id="723f0-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="723f0-125">**Schaltfläche. nach unten**</span><span class="sxs-lookup"><span data-stu-id="723f0-125">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="723f0-126">**Button. downImage**</span><span class="sxs-lookup"><span data-stu-id="723f0-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





