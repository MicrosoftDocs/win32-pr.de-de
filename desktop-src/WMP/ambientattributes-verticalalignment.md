---
title: Ambientattribute. VerticalAlignment
description: Mit dem VerticalAlignment-Attribut wird ein Wert angegeben oder abgerufen, der die vertikale Platzierung des-Steuer Elements angibt, wenn die Sicht oder die übergeordnete unter Ansicht gestreckt wird.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- Ambientattribute. VerticalAlignment-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354758"
---
# <a name="ambientattributesverticalalignment"></a><span data-ttu-id="08bd3-104">Ambientattribute. VerticalAlignment</span><span class="sxs-lookup"><span data-stu-id="08bd3-104">AmbientAttributes.verticalAlignment</span></span>

<span data-ttu-id="08bd3-105">Mit dem **VerticalAlignment** -Attribut wird ein Wert angegeben oder abgerufen, der die vertikale Platzierung des-Steuer Elements angibt, wenn die **Sicht** oder die übergeordnete **unter Ansicht** gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="08bd3-105">The **verticalAlignment** attribute specifies or retrieves a value indicating the vertical placement of the control when the **VIEW** or parent **SUBVIEW** is stretched.</span></span>

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="08bd3-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="08bd3-106">Possible Values</span></span>

<span data-ttu-id="08bd3-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="08bd3-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="08bd3-108">Wert</span><span class="sxs-lookup"><span data-stu-id="08bd3-108">Value</span></span>   | <span data-ttu-id="08bd3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08bd3-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08bd3-110">top</span><span class="sxs-lookup"><span data-stu-id="08bd3-110">top</span></span>     | <span data-ttu-id="08bd3-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="08bd3-111">Default.</span></span> <span data-ttu-id="08bd3-112">Behält die Platzierung des-Steuer Elements relativ zum oberen Rand der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="08bd3-112">Maintains the placement of the control relative to the top of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="08bd3-113">bottom</span><span class="sxs-lookup"><span data-stu-id="08bd3-113">bottom</span></span>  | <span data-ttu-id="08bd3-114">Behält die Platzierung des-Steuer Elements relativ zum unteren Rand der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="08bd3-114">Maintains the placement of the control relative to the bottom of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="08bd3-115">Zentrum</span><span class="sxs-lookup"><span data-stu-id="08bd3-115">center</span></span>  | <span data-ttu-id="08bd3-116">Behält die Platzierung des-Steuer Elements relativ zur vertikalen Mitte der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="08bd3-116">Maintains the placement of the control relative to the vertical center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="08bd3-117">strecken</span><span class="sxs-lookup"><span data-stu-id="08bd3-117">stretch</span></span> | <span data-ttu-id="08bd3-118">Verwaltet die Platzierung des-Steuer Elements relativ zum oberen und unteren Rand der Ansicht, wenn die Größe geändert wird.</span><span class="sxs-lookup"><span data-stu-id="08bd3-118">Maintains the placement of the control relative to both the top and bottom margins of the View when resized.</span></span> <span data-ttu-id="08bd3-119">Das Steuerelement wird gestreckt, damit es passt, wenn die **Ansicht** oder die übergeordnete **unter Ansicht** gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="08bd3-119">The control stretches to fit when the **VIEW** or parent **SUBVIEW** is stretched.</span></span> <span data-ttu-id="08bd3-120">Das tatsächliche Bild wird nicht vergrößert oder verkleinert, es sei denn, die Größe kann geändert werden, aber der durch Klicken aktivierbare Bereich wächst oder verkleinert, wenn er nicht von einem **clippingimage** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="08bd3-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="08bd3-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08bd3-121">Remarks</span></span>

<span data-ttu-id="08bd3-122">Wenn **VerticalAlignment** nicht auf "Center" festgelegt ist, behält das Steuerelement seinen ursprünglichen Abstand vom angegebenen Rand oder von beiden Kanten bei Angabe von "Stretch", und die Größe des Steuer Elements kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="08bd3-122">Unless **verticalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="08bd3-123">Wenn das Steuerelement nicht in der Größe geändert werden kann und "Stretch" angegeben ist, wird stattdessen der durch Klicken aktivierbare Bereich gestreckt.</span><span class="sxs-lookup"><span data-stu-id="08bd3-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="08bd3-124">Sie können eine beliebige Kombination der Attribute **HorizontalAlignment** und **VerticalAlignment** festlegen.</span><span class="sxs-lookup"><span data-stu-id="08bd3-124">You can set any combination of the **horizontalAlignment** and **verticalAlignment** attributes.</span></span> <span data-ttu-id="08bd3-125">Wenn Sie z. b. möchten, dass ein Steuerelement sowohl horizontal als auch vertikal zentriert wird, legen Sie **HorizontalAlignment** auf "Center" und **VerticalAlignment** auf "Center" fest.</span><span class="sxs-lookup"><span data-stu-id="08bd3-125">For example, if you want a control to be centered both horizontally and vertically, set **horizontalAlignment** to "center" and **verticalAlignment** to "center".</span></span>

## <a name="requirements"></a><span data-ttu-id="08bd3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08bd3-126">Requirements</span></span>



| <span data-ttu-id="08bd3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08bd3-127">Requirement</span></span> | <span data-ttu-id="08bd3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="08bd3-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="08bd3-129">Version</span><span class="sxs-lookup"><span data-stu-id="08bd3-129">Version</span></span><br/> | <span data-ttu-id="08bd3-130">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="08bd3-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08bd3-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08bd3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bd3-132">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="08bd3-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="08bd3-133">**Ambientattribute. HorizontalAlignment**</span><span class="sxs-lookup"><span data-stu-id="08bd3-133">**AmbientAttributes.horizontalAlignment**</span></span>](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





