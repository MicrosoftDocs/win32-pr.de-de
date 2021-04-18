---
title: Ambientattribute. muveto
description: Die Methode "muveto" verschiebt das Steuerelement mit einer linearen Geschwindigkeit an einen neuen Speicherort.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- Ambientattribute. muveto-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358362"
---
# <a name="ambientattributesmoveto"></a><span data-ttu-id="7d44c-104">Ambientattribute. muveto</span><span class="sxs-lookup"><span data-stu-id="7d44c-104">AmbientAttributes.moveTo</span></span>

<span data-ttu-id="7d44c-105">Die Methode " **muveto** " verschiebt das Steuerelement mit einer linearen Geschwindigkeit an einen neuen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="7d44c-105">The **moveTo** method moves the control to a new location at a linear speed.</span></span>

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a><span data-ttu-id="7d44c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d44c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d44c-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newleft*</span><span class="sxs-lookup"><span data-stu-id="7d44c-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span></span>
</dt> <dd>

<span data-ttu-id="7d44c-108">**Number** (**Long**) gibt den neuen Wert für das **linke** Attribut des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="7d44c-108">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="7d44c-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newtop*</span><span class="sxs-lookup"><span data-stu-id="7d44c-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span></span>
</dt> <dd>

<span data-ttu-id="7d44c-110">**Number** (**Long**) gibt den neuen Wert für das **Top** -Attribut des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="7d44c-110">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="7d44c-111"><span id="time"></span><span id="TIME"></span>*Zeit*</span><span class="sxs-lookup"><span data-stu-id="7d44c-111"><span id="time"></span><span id="TIME"></span>*time*</span></span>
</dt> <dd>

<span data-ttu-id="7d44c-112">**Number** (**Long**) gibt die Zeit in Millisekunden an, die das Steuerelement benötigt, um zum neuen Speicherort zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="7d44c-112">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d44c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d44c-113">Return Value</span></span>

<span data-ttu-id="7d44c-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7d44c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d44c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d44c-115">Remarks</span></span>

<span data-ttu-id="7d44c-116">Diese Methode ist hilfreich für animierte **unter Ansicht** -Elemente (z. b. wenn der Benutzer auf eine Leiste klickt und die Steuerelemente auf die Folie nach unten klicken).</span><span class="sxs-lookup"><span data-stu-id="7d44c-116">This method is useful for animated **SUBVIEW** elements (for example, if the user clicks a tray and the controls slide down).</span></span>

<span data-ttu-id="7d44c-117">Diese Methode erstellt eine lineare Bewegung, wenn das Steuerelement verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="7d44c-117">This method creates a linear motion when moving the control.</span></span> <span data-ttu-id="7d44c-118">Dies unterscheidet sich von " **diasto**", wodurch eine nichtlineare Bewegung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d44c-118">This differs from **slideTo**, which creates a non-linear motion.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d44c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d44c-119">Requirements</span></span>



| <span data-ttu-id="7d44c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d44c-120">Requirement</span></span> | <span data-ttu-id="7d44c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7d44c-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7d44c-122">Version</span><span class="sxs-lookup"><span data-stu-id="7d44c-122">Version</span></span><br/> | <span data-ttu-id="7d44c-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7d44c-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d44c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d44c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d44c-125">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="7d44c-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="7d44c-126">**Ambientattribute. Left**</span><span class="sxs-lookup"><span data-stu-id="7d44c-126">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="7d44c-127">**Ambientattribute. slideto**</span><span class="sxs-lookup"><span data-stu-id="7d44c-127">**AmbientAttributes.slideTo**</span></span>](ambientattributes-slideto.md)
</dt> <dt>

[<span data-ttu-id="7d44c-128">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="7d44c-128">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





