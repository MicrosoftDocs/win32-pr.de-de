---
title: Ambientattribute. alphablendto
description: Die alphablendto-Methode passt die AlphaBlend-Eigenschaft über einen Zeitraum an.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- Ambientattribute. alphablendto Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354103"
---
# <a name="ambientattributesalphablendto"></a><span data-ttu-id="182c6-104">Ambientattribute. alphablendto</span><span class="sxs-lookup"><span data-stu-id="182c6-104">AmbientAttributes.alphaBlendTo</span></span>

<span data-ttu-id="182c6-105">Die **alphablendto** -Methode passt die **AlphaBlend** -Eigenschaft über einen Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="182c6-105">The **alphaBlendTo** method adjusts the **alphaBlend** property over a period of time.</span></span>

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a><span data-ttu-id="182c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="182c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="182c6-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*NewVal*</span><span class="sxs-lookup"><span data-stu-id="182c6-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span></span>
</dt> <dd>

<span data-ttu-id="182c6-108">**Number** (Long), der den neuen Deckkraft Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="182c6-108">**Number** (long) specifying the new opacity value.</span></span> <span data-ttu-id="182c6-109">Liegt zwischen 0 (keine Deckkraft) und 255 (vollständige Deckkraft).</span><span class="sxs-lookup"><span data-stu-id="182c6-109">Ranges from 0 (no opacity) to 255 (full opacity).</span></span>

</dd> <dt>

<span data-ttu-id="182c6-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*Alpha Ativ*</span><span class="sxs-lookup"><span data-stu-id="182c6-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span></span>
</dt> <dd>

<span data-ttu-id="182c6-111">**Number** (**Long**), der die Zeit in Millisekunden angibt, die das-Element zum Ändern der Deckkraft benötigt.</span><span class="sxs-lookup"><span data-stu-id="182c6-111">**Number** (**long**) specifying the time, in milliseconds, that it takes the element to change opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182c6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="182c6-112">Return Value</span></span>

<span data-ttu-id="182c6-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="182c6-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="182c6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="182c6-114">Remarks</span></span>

<span data-ttu-id="182c6-115">Diese Methode ist nützlich, wenn Elemente allmählich angezeigt oder ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="182c6-115">This method is useful for making elements gradually appear or disappear.</span></span>

<span data-ttu-id="182c6-116">Wenn Sie **alphablendto** mit einem **Text** Element verwenden, für das die **BackgroundColor** nicht angegeben ist, wird eine Hintergrundfarbe von Schwarz verwendet.</span><span class="sxs-lookup"><span data-stu-id="182c6-116">When you use **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="182c6-117">, Wenn die Vordergrundfarbe ebenfalls schwarz ist (Dies ist der Standardwert für *Text*).**ForegroundColor**), wird der Text möglicherweise nicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="182c6-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="182c6-118">Um dies zu verhindern, geben Sie immer das **BackgroundColor** -Attribut an, oder legen Sie **ForegroundColor** auf eine andere Farbe als schwarz fest.</span><span class="sxs-lookup"><span data-stu-id="182c6-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="182c6-119">Dieses Attribut wird in Windows 98 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="182c6-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="182c6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="182c6-120">Requirements</span></span>



| <span data-ttu-id="182c6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="182c6-121">Requirement</span></span> | <span data-ttu-id="182c6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="182c6-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="182c6-123">Version</span><span class="sxs-lookup"><span data-stu-id="182c6-123">Version</span></span><br/> | <span data-ttu-id="182c6-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="182c6-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="182c6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="182c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182c6-126">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="182c6-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="182c6-127">**Ambientattribute. AlphaBlend**</span><span class="sxs-lookup"><span data-stu-id="182c6-127">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="182c6-128">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="182c6-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="182c6-129">**Text. BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="182c6-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="182c6-130">**Text. ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="182c6-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





