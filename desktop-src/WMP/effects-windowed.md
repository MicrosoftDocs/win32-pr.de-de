---
title: Effekte. Windowed
description: Das Fenster-Attribut gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob die Visualisierung Fenster Weise angezeigt wird, d. h. ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist, oder ob es abgeschnitten werden kann.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- Effekte. Fenster Media Player
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367198"
---
# <a name="effectswindowed"></a><span data-ttu-id="0bc1a-104">Effekte. Windowed</span><span class="sxs-lookup"><span data-stu-id="0bc1a-104">EFFECTS.windowed</span></span>

<span data-ttu-id="0bc1a-105">Das **Fenster** -Attribut gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob die Visualisierung Fenster Weise angezeigt wird, d. h. ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist, oder ob es abgeschnitten werden kann.</span><span class="sxs-lookup"><span data-stu-id="0bc1a-105">The **windowed** attribute specifies or retrieves a value indicating whether the visualization will be windowed or windowless, that is, whether the entire rectangle of the control will be visible at all times, or whether it can be clipped.</span></span> <span data-ttu-id="0bc1a-106">Dieses Attribut kann nur zur Entwurfszeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0bc1a-106">This attribute can only be set at design time.</span></span>

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a><span data-ttu-id="0bc1a-107">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0bc1a-107">Possible Values</span></span>

<span data-ttu-id="0bc1a-108">Dieses Attribut ist ein **boolescher** Wert, der zur Entwurfszeit angegeben wird, und anschließend schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0bc1a-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="0bc1a-109">Wert</span><span class="sxs-lookup"><span data-stu-id="0bc1a-109">Value</span></span> | <span data-ttu-id="0bc1a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bc1a-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="0bc1a-111">true</span><span class="sxs-lookup"><span data-stu-id="0bc1a-111">true</span></span>  | <span data-ttu-id="0bc1a-112">Das-Steuerelement wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0bc1a-112">The control will be windowed.</span></span>            |
| <span data-ttu-id="0bc1a-113">false</span><span class="sxs-lookup"><span data-stu-id="0bc1a-113">false</span></span> | <span data-ttu-id="0bc1a-114">Standard.</span><span class="sxs-lookup"><span data-stu-id="0bc1a-114">Default.</span></span> <span data-ttu-id="0bc1a-115">Das Steuerelement ist fensterloser.</span><span class="sxs-lookup"><span data-stu-id="0bc1a-115">The control will be windowless.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0bc1a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bc1a-116">Remarks</span></span>

<span data-ttu-id="0bc1a-117">Wenn ein nicht rechteckiges Visualisierungs Fenster erwünscht ist oder ein Teil des Fensters durch ein Bild abgedeckt ist, muss dieses Attribut auf "false" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0bc1a-117">If a non-rectangular visualization window is desired, or if any part of the window is covered by an image, this attribute must be set to false.</span></span> <span data-ttu-id="0bc1a-118">Dadurch wird eine gewisse Leistung erzielt, um das erforderliche Clipping durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="0bc1a-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="0bc1a-119">Wenn **Fenster** auf true festgelegt ist, wird jedes Bild, das das Visualisierungs Fenster abdeckt, ignoriert, und das Visualisierungs Fenster hat die oberste z-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="0bc1a-119">If **windowed** is set to true, any image covering the visualization window is ignored, and the visualization window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bc1a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bc1a-120">Requirements</span></span>



| <span data-ttu-id="0bc1a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bc1a-121">Requirement</span></span> | <span data-ttu-id="0bc1a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0bc1a-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0bc1a-123">Version</span><span class="sxs-lookup"><span data-stu-id="0bc1a-123">Version</span></span><br/> | <span data-ttu-id="0bc1a-124">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0bc1a-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0bc1a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bc1a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc1a-126">**Effects-Element**</span><span class="sxs-lookup"><span data-stu-id="0bc1a-126">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





