---
title: Ambientattribute. HorizontalAlignment
description: Mit dem HorizontalAlignment-Attribut wird ein Wert angegeben oder abgerufen, der die horizontale Platzierung des Steuer Elements angibt, wenn die Größe der Sicht oder der übergeordneten unter Ansicht geändert wird.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- Ambientattribute. HorizontalAlignment-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359222"
---
# <a name="ambientattributeshorizontalalignment"></a><span data-ttu-id="fb4de-104">Ambientattribute. HorizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="fb4de-104">AmbientAttributes.horizontalAlignment</span></span>

<span data-ttu-id="fb4de-105">Mit dem **HorizontalAlignment** -Attribut wird ein Wert angegeben oder abgerufen, der die horizontale Platzierung des Steuer Elements angibt, wenn die Größe der **Sicht** oder der übergeordneten **unter Ansicht** geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fb4de-105">The **horizontalAlignment** attribute specifies or retrieves a value that indicates the horizontal placement of the control when the **VIEW** or parent **SUBVIEW** is resized.</span></span>

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="fb4de-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="fb4de-106">Possible Values</span></span>

<span data-ttu-id="fb4de-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="fb4de-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="fb4de-108">Wert</span><span class="sxs-lookup"><span data-stu-id="fb4de-108">Value</span></span>   | <span data-ttu-id="fb4de-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb4de-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4de-110">Linker Join</span><span class="sxs-lookup"><span data-stu-id="fb4de-110">left</span></span>    | <span data-ttu-id="fb4de-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="fb4de-111">Default.</span></span> <span data-ttu-id="fb4de-112">Behält die Platzierung des-Steuer Elements relativ zur linken Seite der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fb4de-112">Maintains the placement of the control relative to the left of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="fb4de-113">Rechts</span><span class="sxs-lookup"><span data-stu-id="fb4de-113">right</span></span>   | <span data-ttu-id="fb4de-114">Behält die Platzierung des Steuer Elements relativ zur rechten Ecke der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fb4de-114">Maintains the placement of the control relative to the right of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="fb4de-115">Zentrum</span><span class="sxs-lookup"><span data-stu-id="fb4de-115">center</span></span>  | <span data-ttu-id="fb4de-116">Behält die Platzierung des-Steuer Elements relativ zur horizontalen Mitte der **Ansicht** oder übergeordneten **unter Ansicht** bei, wenn die Größe der Ansicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fb4de-116">Maintains the placement of the control relative to the horizontal center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="fb4de-117">strecken</span><span class="sxs-lookup"><span data-stu-id="fb4de-117">stretch</span></span> | <span data-ttu-id="fb4de-118">Verwaltet die Platzierung des-Steuer Elements relativ zum linken und rechten Rand der **Sicht** oder übergeordneten **unter Ansicht** , wenn die Größe geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fb4de-118">Maintains the placement of the control relative to both the left and right margins of the **VIEW** or parent **SUBVIEW** when resized.</span></span> <span data-ttu-id="fb4de-119">Das Steuerelement wird gestreckt, damit es passt, wenn die **Ansicht** oder die **unter Ansicht** gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="fb4de-119">The control stretches to fit when the **VIEW** or **SUBVIEW** is stretched.</span></span> <span data-ttu-id="fb4de-120">Das tatsächliche Bild wird nicht vergrößert oder verkleinert, es sei denn, die Größe kann geändert werden, aber der durch Klicken aktivierbare Bereich wächst oder verkleinert, wenn er nicht von einem **clippingimage** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fb4de-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb4de-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb4de-121">Remarks</span></span>

<span data-ttu-id="fb4de-122">Wenn " **HorizontalAlignment** " nicht auf "Center" festgelegt ist, behält das Steuerelement seinen ursprünglichen Abstand vom angegebenen Rand oder von beiden Kanten, wenn "Stretch" angegeben ist und die Größe des Steuer Elements geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb4de-122">Unless **horizontalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="fb4de-123">Wenn das Steuerelement nicht in der Größe geändert werden kann und "Stretch" angegeben ist, wird stattdessen der durch Klicken aktivierbare Bereich gestreckt.</span><span class="sxs-lookup"><span data-stu-id="fb4de-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="fb4de-124">Sie können eine beliebige Kombination von **HorizontalAlignment** und **VerticalAlignment** festlegen.</span><span class="sxs-lookup"><span data-stu-id="fb4de-124">You can set any combination of **horizontalAlignment** and **verticalAlignment**.</span></span> <span data-ttu-id="fb4de-125">Wenn Sie z. b. ein Steuerelement sowohl horizontal als auch vertikal zentrieren möchten, legen Sie HorizontalAlignment = "Center" VerticalAlignment = "Center" fest.</span><span class="sxs-lookup"><span data-stu-id="fb4de-125">For example, if you want to center a control both horizontally and vertically, set horizontalAlignment="center" verticalAlignment="center".</span></span>

## <a name="requirements"></a><span data-ttu-id="fb4de-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb4de-126">Requirements</span></span>



| <span data-ttu-id="fb4de-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb4de-127">Requirement</span></span> | <span data-ttu-id="fb4de-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fb4de-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fb4de-129">Version</span><span class="sxs-lookup"><span data-stu-id="fb4de-129">Version</span></span><br/> | <span data-ttu-id="fb4de-130">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fb4de-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb4de-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb4de-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4de-132">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="fb4de-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="fb4de-133">**Ambientattribute. VerticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="fb4de-133">**AmbientAttributes.verticalAlignment**</span></span>](ambientattributes-verticalalignment.md)
</dt> <dt>

[<span data-ttu-id="fb4de-134">**Ambientattribute. clippingimage**</span><span class="sxs-lookup"><span data-stu-id="fb4de-134">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





