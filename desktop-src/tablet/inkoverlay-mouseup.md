---
description: 'InkOverlay.MouseUp-Ereignis: Tritt auf, wenn sich der Mauszeiger über dem InkCollector- oder InkOverlay-Objekt befindet und eine Maustaste losgelassen wird.'
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: InkOverlay.MouseUp-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402083aa677b134ea469980227a482ac5546da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086808"
---
# <a name="inkoverlaymouseup-event"></a><span data-ttu-id="c308b-103">InkOverlay.MouseUp-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c308b-103">InkOverlay.MouseUp event</span></span>

<span data-ttu-id="c308b-104">Tritt ein, wenn sich der Mauszeiger über dem [**InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) befindet und eine Maustaste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="c308b-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="c308b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c308b-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="c308b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c308b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c308b-107">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c308b-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c308b-108">Die Maustaste, die losgelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="c308b-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="c308b-109">*Umschalten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c308b-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c308b-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="c308b-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="c308b-111">*pX* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c308b-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c308b-112">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c308b-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="c308b-113">*pY* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c308b-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c308b-114">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c308b-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="c308b-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c308b-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c308b-116">Gibt an, ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c308b-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="c308b-117">Der Standardwert ist **FALSE,** der angibt, dass das Ereignis nicht abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c308b-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c308b-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c308b-118">Return value</span></span>

<span data-ttu-id="c308b-119">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c308b-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c308b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c308b-120">Remarks</span></span>

<span data-ttu-id="c308b-121">Um die Leistung von Ink in Echtzeit zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown-**](inkcollector-mousedown.md) und [**MouseUp-Ereignishandlern**](inkcollector-mouseup.md) aus oder ein.</span><span class="sxs-lookup"><span data-stu-id="c308b-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="c308b-122">Die Eigenschaften *pX* und *pY* befinden sich in Pixeln und nicht in den HIMETRIC-Einheiten, die dem Freiraum zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c308b-122">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="c308b-123">Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Nicht-Stiftanwendung ersetzt und diese Art von Anwendung nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="c308b-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="c308b-124">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**MouseDown-,**](inkcollector-mousedown.md) [**MouseMove-**](inkcollector-mousemove.md)und [**MouseUp-Ereignissen.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="c308b-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="c308b-125">Das Abbrechen einiger dieser Ereignisse kann unerwartete Ergebnisse haben.</span><span class="sxs-lookup"><span data-stu-id="c308b-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="c308b-126">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseUp definiert.</span><span class="sxs-lookup"><span data-stu-id="c308b-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="c308b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c308b-127">Requirements</span></span>



| <span data-ttu-id="c308b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c308b-128">Requirement</span></span> | <span data-ttu-id="c308b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c308b-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c308b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c308b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c308b-131">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c308b-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c308b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c308b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c308b-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c308b-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c308b-134">Header</span><span class="sxs-lookup"><span data-stu-id="c308b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c308b-135"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="c308b-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c308b-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c308b-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="c308b-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c308b-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c308b-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c308b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c308b-139">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c308b-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="c308b-140">**InkMouseButton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c308b-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="c308b-141">**InkShiftKeyModifierFlags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c308b-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




