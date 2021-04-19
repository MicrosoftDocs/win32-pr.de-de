---
title: Ambientattribute. slideto
description: Die Methode "diasto" verschiebt das Steuerelement an eine neue Position. Das-Steuerelement bewegt sich im angegebenen Zeitraum nicht linear.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- Ambientattribute. slideto Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371297"
---
# <a name="ambientattributesslideto"></a><span data-ttu-id="4848b-105">Ambientattribute. slideto</span><span class="sxs-lookup"><span data-stu-id="4848b-105">AmbientAttributes.slideTo</span></span>

<span data-ttu-id="4848b-106">Die Methode " **diasto** " verschiebt das Steuerelement an eine neue Position.</span><span class="sxs-lookup"><span data-stu-id="4848b-106">The **slideTo** method moves the control to a new location.</span></span> <span data-ttu-id="4848b-107">Das-Steuerelement bewegt sich im angegebenen Zeitraum nicht linear.</span><span class="sxs-lookup"><span data-stu-id="4848b-107">The control moves in a non-linear fashion over the specified time period.</span></span>

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a><span data-ttu-id="4848b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4848b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4848b-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newx*</span><span class="sxs-lookup"><span data-stu-id="4848b-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="4848b-110">**Number** (**Long**) gibt den neuen Wert für das **linke** Attribut des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="4848b-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="4848b-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*Newy*</span><span class="sxs-lookup"><span data-stu-id="4848b-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="4848b-112">**Number** (**Long**) gibt den neuen Wert für das **Top** -Attribut des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="4848b-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="4848b-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*-Zeit*</span><span class="sxs-lookup"><span data-stu-id="4848b-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="4848b-114">**Number** (**Long**) gibt die Zeit in Millisekunden an, die das Steuerelement benötigt, um zum neuen Speicherort zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="4848b-114">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4848b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4848b-115">Return Value</span></span>

<span data-ttu-id="4848b-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4848b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4848b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4848b-117">Remarks</span></span>

<span data-ttu-id="4848b-118">Diese Methode unterscheidet sich von " **muveto**", wodurch beim Verschieben des Steuer Elements eine lineare Bewegung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4848b-118">This method is different from **moveTo**, which creates a linear motion when moving the control.</span></span> <span data-ttu-id="4848b-119">Die nichtlineare Bewegung, die von dieser Methode erstellt wird, ist eine gleitende Bewegung, die sich am Anfang der Bewegung von einer Geschwindigkeit von NULL beschleunigt und am Ende wieder auf 0 (null) zurücksetzt, um einen Smooth-Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="4848b-119">The non-linear motion created by this method is a sliding motion that accelerates from a speed of zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="4848b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4848b-120">Requirements</span></span>



| <span data-ttu-id="4848b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4848b-121">Requirement</span></span> | <span data-ttu-id="4848b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4848b-122">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="4848b-123">Version</span><span class="sxs-lookup"><span data-stu-id="4848b-123">Version</span></span><br/> | <span data-ttu-id="4848b-124">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="4848b-124">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4848b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4848b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4848b-126">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="4848b-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="4848b-127">**Ambientattribute. Left**</span><span class="sxs-lookup"><span data-stu-id="4848b-127">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="4848b-128">**Ambientattribute. muveto**</span><span class="sxs-lookup"><span data-stu-id="4848b-128">**AmbientAttributes.moveTo**</span></span>](ambientattributes-moveto.md)
</dt> <dt>

[<span data-ttu-id="4848b-129">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="4848b-129">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





