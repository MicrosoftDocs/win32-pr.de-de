---
title: Effekte. Currency-ffecttype
description: Das Attribut "attributeffecttype" gibt den Registrierungs Namen der aktuellen Visualisierung an oder ruft ihn ab. Dieser Name ist eine eindeutige ID, die vom Visualisierungs Autor definiert wurde.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- Effekte. Currency-ffecttype Windows-Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351228"
---
# <a name="effectscurrenteffecttype"></a><span data-ttu-id="02fe2-105">Effekte. Currency-ffecttype</span><span class="sxs-lookup"><span data-stu-id="02fe2-105">EFFECTS.currentEffectType</span></span>

<span data-ttu-id="02fe2-106">Das Attribut " **attributeffecttype** " gibt den Registrierungs Namen der aktuellen Visualisierung an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="02fe2-106">The **currentEffectType** attribute specifies or retrieves the registry name of the current visualization.</span></span> <span data-ttu-id="02fe2-107">Dieser Name ist eine eindeutige ID, die vom Visualisierungs Autor definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="02fe2-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a><span data-ttu-id="02fe2-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="02fe2-108">Possible Values</span></span>

<span data-ttu-id="02fe2-109">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="02fe2-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="02fe2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02fe2-110">Remarks</span></span>

<span data-ttu-id="02fe2-111">Sie können dieses Attribut zur Laufzeit verwenden, um den aktuell angezeigten Effekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="02fe2-111">You can use this attribute at run time to change the currently displayed effect.</span></span> <span data-ttu-id="02fe2-112">Gehen Sie hierzu folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="02fe2-112">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="02fe2-113">Verwenden Sie **effectcount** , um die Anzahl der registrierten Effekte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="02fe2-113">Use **effectCount** to retrieve the count of registered effects.</span></span>
2.  <span data-ttu-id="02fe2-114">Rufen Sie in einer-Schleife den Namen jedes registrierten Effekts mithilfe von **EffectType** ab.</span><span class="sxs-lookup"><span data-stu-id="02fe2-114">In a loop, retrieve the name of each registered effect by using **effectType**.</span></span>
3.  <span data-ttu-id="02fe2-115">Geben Sie einen der Namen **an, den** Sie für "" "" "" "" "" "" "" "" ""</span><span class="sxs-lookup"><span data-stu-id="02fe2-115">Specify one of the names you retrieved for **currentEffectType** to set the current effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="02fe2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02fe2-116">Requirements</span></span>



| <span data-ttu-id="02fe2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02fe2-117">Requirement</span></span> | <span data-ttu-id="02fe2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="02fe2-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="02fe2-119">Version</span><span class="sxs-lookup"><span data-stu-id="02fe2-119">Version</span></span><br/> | <span data-ttu-id="02fe2-120">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="02fe2-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02fe2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02fe2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02fe2-122">**Effects-Element**</span><span class="sxs-lookup"><span data-stu-id="02fe2-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="02fe2-123">**Effekte. Currency-ffect**</span><span class="sxs-lookup"><span data-stu-id="02fe2-123">**EFFECTS.currentEffect**</span></span>](effects-currenteffect.md)
</dt> <dt>

[<span data-ttu-id="02fe2-124">**Effects. effectcount**</span><span class="sxs-lookup"><span data-stu-id="02fe2-124">**EFFECTS.effectCount**</span></span>](effects-effectcount.md)
</dt> <dt>

[<span data-ttu-id="02fe2-125">**Effects. EffectType**</span><span class="sxs-lookup"><span data-stu-id="02fe2-125">**EFFECTS.effectType**</span></span>](effects-effecttype.md)
</dt> </dl>

 

 





