---
title: Ambientattribute. muvesizeto
description: Die Methode "muvesizeto" verschiebt das Steuerelement und gibt eine neue Größe für das Steuerelement am neuen Speicherort an. Das-Steuerelement verschiebt und ändert seine Größe im Verlauf des angegebenen Zeitraums auf animierte Weise.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- Media Player "ambientattribute. muvesizeto"
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366941"
---
# <a name="ambientattributesmovesizeto"></a><span data-ttu-id="1b61d-105">Ambientattribute. muvesizeto</span><span class="sxs-lookup"><span data-stu-id="1b61d-105">AmbientAttributes.moveSizeTo</span></span>

<span data-ttu-id="1b61d-106">Die Methode " **muvesizeto** " verschiebt das Steuerelement und gibt eine neue Größe für das Steuerelement am neuen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="1b61d-106">The **moveSizeTo** method moves the control and specifies a new size for the control in the new location.</span></span> <span data-ttu-id="1b61d-107">Das-Steuerelement verschiebt und ändert seine Größe im Verlauf des angegebenen Zeitraums auf animierte Weise.</span><span class="sxs-lookup"><span data-stu-id="1b61d-107">The control moves and resizes in an animated fashion over the specified time period.</span></span>

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a><span data-ttu-id="1b61d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b61d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b61d-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newx*</span><span class="sxs-lookup"><span data-stu-id="1b61d-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="1b61d-110">**Number** (**Long**) gibt den neuen Wert für das **linke** Attribut des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="1b61d-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1b61d-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*Newy*</span><span class="sxs-lookup"><span data-stu-id="1b61d-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="1b61d-112">**Number** (**Long**) gibt den neuen Wert für das **Top** -Attribut des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="1b61d-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1b61d-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*neubreite*</span><span class="sxs-lookup"><span data-stu-id="1b61d-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span></span>
</dt> <dd>

<span data-ttu-id="1b61d-114">**Number** (**Long**) gibt den neuen Wert für das **Width** -Attribut des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="1b61d-114">**Number** (**long**) specifying the new value for the **width** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1b61d-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*netwheight*</span><span class="sxs-lookup"><span data-stu-id="1b61d-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span></span>
</dt> <dd>

<span data-ttu-id="1b61d-116">**Number** (**Long**) gibt den neuen Wert für das **height** -Attribut des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="1b61d-116">**Number** (**long**) specifying the new value for the **height** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1b61d-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*-Zeit*</span><span class="sxs-lookup"><span data-stu-id="1b61d-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="1b61d-118">**Number** (**Long**) gibt die Zeit in Millisekunden an, die das Steuerelement benötigt, um zum neuen Speicherort zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="1b61d-118">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> <dt>

<span data-ttu-id="1b61d-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*Folie*</span><span class="sxs-lookup"><span data-stu-id="1b61d-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span></span>
</dt> <dd>

<span data-ttu-id="1b61d-120">**Boolescher** Wert, der den Typ der beim Verschieben des Steuer Elements erstellten Bewegung angibt.</span><span class="sxs-lookup"><span data-stu-id="1b61d-120">**Boolean** specifying the type of motion created when moving the control.</span></span>



| <span data-ttu-id="1b61d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1b61d-121">Value</span></span> | <span data-ttu-id="1b61d-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b61d-122">Description</span></span>                                                             |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="1b61d-123">true</span><span class="sxs-lookup"><span data-stu-id="1b61d-123">true</span></span>  | <span data-ttu-id="1b61d-124">Bewegung ist nicht linear (gleitende Bewegung, die beschleunigt und verlangsamt).</span><span class="sxs-lookup"><span data-stu-id="1b61d-124">Motion is non-linear (sliding motion that accelerates and decelerates).</span></span> |
| <span data-ttu-id="1b61d-125">false</span><span class="sxs-lookup"><span data-stu-id="1b61d-125">false</span></span> | <span data-ttu-id="1b61d-126">Bewegung ist linear.</span><span class="sxs-lookup"><span data-stu-id="1b61d-126">Motion is linear.</span></span>                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b61d-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b61d-127">Return Value</span></span>

<span data-ttu-id="1b61d-128">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1b61d-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b61d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b61d-129">Remarks</span></span>

<span data-ttu-id="1b61d-130">Die Bewegung des Steuer Elements kann linear oder nicht linear sein.</span><span class="sxs-lookup"><span data-stu-id="1b61d-130">The motion of the control can be linear or non-linear.</span></span> <span data-ttu-id="1b61d-131">Lineare Bewegung bedeutet, dass das Steuerelement mit konstanter Geschwindigkeit an die neue Position bewegt wird, wobei der Start und das Beenden plötzlich beendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b61d-131">Linear motion means the control moves at a constant speed to its new location, starting and stopping abruptly.</span></span> <span data-ttu-id="1b61d-132">Wenn eine nichtlineare Bewegung angegeben wird, wird eine gleitende Bewegung erstellt, die zu Beginn der Bewegung von NULL beschleunigt und am Ende wieder auf 0 (null) zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="1b61d-132">When non-linear motion is specified, a sliding motion is created that accelerates from zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b61d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b61d-133">Requirements</span></span>



| <span data-ttu-id="1b61d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b61d-134">Requirement</span></span> | <span data-ttu-id="1b61d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="1b61d-135">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="1b61d-136">Version</span><span class="sxs-lookup"><span data-stu-id="1b61d-136">Version</span></span><br/> | <span data-ttu-id="1b61d-137">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="1b61d-137">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b61d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b61d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b61d-139">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="1b61d-139">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b61d-140">**Ambientattribute. Height**</span><span class="sxs-lookup"><span data-stu-id="1b61d-140">**AmbientAttributes.height**</span></span>](ambientattributes-height.md)
</dt> <dt>

[<span data-ttu-id="1b61d-141">**Ambientattribute. Left**</span><span class="sxs-lookup"><span data-stu-id="1b61d-141">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="1b61d-142">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="1b61d-142">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> <dt>

[<span data-ttu-id="1b61d-143">**Ambientattribute. Width**</span><span class="sxs-lookup"><span data-stu-id="1b61d-143">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> </dl>

 

 





