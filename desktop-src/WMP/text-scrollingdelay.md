---
title: Text. scrollingdelay
description: Das scrollingdelay-Attribut gibt die Zeitverzögerung zwischen Scrollbewegungen an oder ruft diese ab.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- Text. scrollingdelay-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365459"
---
# <a name="textscrollingdelay"></a><span data-ttu-id="ac814-104">Text. scrollingdelay</span><span class="sxs-lookup"><span data-stu-id="ac814-104">TEXT.scrollingDelay</span></span>

<span data-ttu-id="ac814-105">Das **scrollingdelay** -Attribut gibt die Zeitverzögerung zwischen Scrollbewegungen an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="ac814-105">The **scrollingDelay** attribute specifies or retrieves the time delay between scrolling movements.</span></span>

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a><span data-ttu-id="ac814-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="ac814-106">Possible Values</span></span>

<span data-ttu-id="ac814-107">Dieses Attribut ist eine Lese-/schreibzahl (**int**), die die Verzögerung in Millisekunden angibt. </span><span class="sxs-lookup"><span data-stu-id="ac814-107">This attribute is a read/write **Number** (**int**) specifying the delay in milliseconds.</span></span> <span data-ttu-id="ac814-108">Er verfügt über einen Mindestwert von 30 und einen Standardwert von 85.</span><span class="sxs-lookup"><span data-stu-id="ac814-108">It has a minimum value of 30, and a default value of 85.</span></span> <span data-ttu-id="ac814-109">Wenn ein Wert kleiner als der minimale Wert angegeben ist, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac814-109">If a value less than the minimum is specified, the default is used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac814-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac814-110">Remarks</span></span>

<span data-ttu-id="ac814-111">Wenn **Scroll** auf false festgelegt ist, wird **scrollingdelay** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ac814-111">If **scrolling** is set to false, **scrollingDelay** is ignored.</span></span>

<span data-ttu-id="ac814-112">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac814-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac814-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac814-113">Requirements</span></span>



| <span data-ttu-id="ac814-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac814-114">Requirement</span></span> | <span data-ttu-id="ac814-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ac814-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ac814-116">Version</span><span class="sxs-lookup"><span data-stu-id="ac814-116">Version</span></span><br/> | <span data-ttu-id="ac814-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ac814-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac814-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac814-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac814-119">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="ac814-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="ac814-120">**Text. Scroll**</span><span class="sxs-lookup"><span data-stu-id="ac814-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





