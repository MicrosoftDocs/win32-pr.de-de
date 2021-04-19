---
title: Text. scrollingamount
description: Das scrollingamount-Attribut gibt die Anzahl der Pixel an, die der Text während jeder scrollbewegung bewegt, oder ruft diese ab.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- Text. scrollingamount-Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356500"
---
# <a name="textscrollingamount"></a><span data-ttu-id="2a964-104">Text. scrollingamount</span><span class="sxs-lookup"><span data-stu-id="2a964-104">TEXT.scrollingAmount</span></span>

<span data-ttu-id="2a964-105">Das **scrollingamount** -Attribut gibt die Anzahl der Pixel an, die der Text während jeder scrollbewegung bewegt, oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="2a964-105">The **scrollingAmount** attribute specifies or retrieves the number of pixels that the text moves during each scrolling movement.</span></span>

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a><span data-ttu-id="2a964-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="2a964-106">Possible Values</span></span>

<span data-ttu-id="2a964-107">Dieses Attribut ist eine positive Lese-/schreibzahl (**int**) mit einem Standardwert von 6. </span><span class="sxs-lookup"><span data-stu-id="2a964-107">This attribute is a positive read/write **Number** (**int**) with a default value of 6.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a964-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a964-108">Remarks</span></span>

<span data-ttu-id="2a964-109">Für einen reibungslosen Bildlauf sollte " **scrollingamount** " klein sein.</span><span class="sxs-lookup"><span data-stu-id="2a964-109">For smooth scrolling, **scrollingAmount** should be small.</span></span> <span data-ttu-id="2a964-110">Für schnelles zeichnen mit großen Lücken sollte das **scrollingamount** größer sein.</span><span class="sxs-lookup"><span data-stu-id="2a964-110">For fast drawing with big gaps, the **scrollingAmount** should be larger.</span></span> <span data-ttu-id="2a964-111">Wenn **Scroll** = "false", wird **scrollingamount** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2a964-111">If **scrolling** ="false", **scrollingAmount** is ignored.</span></span>

<span data-ttu-id="2a964-112">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a964-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a964-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a964-113">Requirements</span></span>



| <span data-ttu-id="2a964-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a964-114">Requirement</span></span> | <span data-ttu-id="2a964-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2a964-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2a964-116">Version</span><span class="sxs-lookup"><span data-stu-id="2a964-116">Version</span></span><br/> | <span data-ttu-id="2a964-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2a964-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a964-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a964-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a964-119">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="2a964-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="2a964-120">**Text. Scroll**</span><span class="sxs-lookup"><span data-stu-id="2a964-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





