---
title: Slider. Wert
description: Das value-Attribut gibt die aktuelle Position des Schiebereglers an oder ruft diese ab. | Slider. Wert
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Schieberegler. Wert-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369516"
---
# <a name="slidervalue"></a><span data-ttu-id="b5aa9-105">Slider. Wert</span><span class="sxs-lookup"><span data-stu-id="b5aa9-105">SLIDER.value</span></span>

<span data-ttu-id="b5aa9-106">Das **value** -Attribut gibt die aktuelle Position des Schiebereglers an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="b5aa9-106">The **value** attribute specifies or retrieves the current position of the slider.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="b5aa9-107">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b5aa9-107">Possible Values</span></span>

<span data-ttu-id="b5aa9-108">Dieses Attribut ist eine Lese-/schreibnummer (**float**) mit einem Standardwert von **Min**. </span><span class="sxs-lookup"><span data-stu-id="b5aa9-108">This attribute is a read/write **Number** (**float**) with a default value of **min**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5aa9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5aa9-109">Remarks</span></span>

<span data-ttu-id="b5aa9-110">Der **Wert** muss immer größer als oder gleich **Min** und kleiner oder gleich dem **maximalen** Wert sein. Wenn Sie einen Wert außerhalb dieses Bereichs angeben, werden der **Wert** und die Position des Schiebereglers nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="b5aa9-110">The **value** should always be greater than or equal to **min** and less than or equal to **max**. If you specify a value outside this range, **value** and the position of the slider are not changed.</span></span>

<span data-ttu-id="b5aa9-111">Weitere Informationen finden Sie unter **customslider**. [positionImage](customslider-positionimage.md) -Attribut für ein Beispiel, das veranschaulicht, wie die Attribute des **Slider** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5aa9-111">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5aa9-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5aa9-112">Requirements</span></span>



| <span data-ttu-id="b5aa9-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5aa9-113">Requirement</span></span> | <span data-ttu-id="b5aa9-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b5aa9-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b5aa9-115">Version</span><span class="sxs-lookup"><span data-stu-id="b5aa9-115">Version</span></span><br/> | <span data-ttu-id="b5aa9-116">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b5aa9-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5aa9-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5aa9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5aa9-118">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="b5aa9-118">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="b5aa9-119">**Schieberegler. min.**</span><span class="sxs-lookup"><span data-stu-id="b5aa9-119">**SLIDER.min**</span></span>](slider-min.md)
</dt> </dl>

 

 





