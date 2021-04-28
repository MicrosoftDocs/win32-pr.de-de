---
description: 'InkCollector.MouseDown-Ereignis: Tritt auf, wenn sich der Mauszeiger über dem InkCollector- oder InkOverlay-Objekt befindet und eine Maustaste gedrückt wird.'
ms.assetid: db9ec396-b2a7-4f4f-99f2-95aad46eea28
title: InkCollector.MouseDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d29c8d3ba19856a8d6bfa038837b592c0b5f2b36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110178"
---
# <a name="inkcollectormousedown-event"></a><span data-ttu-id="ead0a-103">InkCollector.MouseDown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ead0a-103">InkCollector.MouseDown event</span></span>

<span data-ttu-id="ead0a-104">Tritt ein, wenn sich der Mauszeiger über dem [**InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) befindet und eine Maustaste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="ead0a-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead0a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead0a-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ead0a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ead0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead0a-107">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ead0a-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead0a-108">Die gedrückte Maustaste.</span><span class="sxs-lookup"><span data-stu-id="ead0a-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="ead0a-109">*Umschalten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ead0a-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead0a-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="ead0a-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="ead0a-111">*pX* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ead0a-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead0a-112">Die X-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ead0a-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ead0a-113">*pY* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ead0a-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead0a-114">Die Y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ead0a-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ead0a-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ead0a-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ead0a-116">**VARIANT \_ TRUE,** um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ead0a-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead0a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ead0a-117">Return value</span></span>

<span data-ttu-id="ead0a-118">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ead0a-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ead0a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ead0a-119">Remarks</span></span>

<span data-ttu-id="ead0a-120">Um die Leistung von Ink-Echtzeit zu verbessern, blenden Sie den Mauszeiger in den **MouseDown-** und [**MouseUp-Ereignishandlern**](inkcollector-mouseup.md) aus oder ein.</span><span class="sxs-lookup"><span data-stu-id="ead0a-120">To improve real-time ink performance, hide or show the mouse cursor in the **MouseDown** and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="ead0a-121">Die Eigenschaften *pX* und *pY* sind in Pixel und nicht die HIMETRIC-Einheiten, die dem Freihandraum zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ead0a-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="ead0a-122">Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Anwendung ohne Stift ersetzt und diese Art von Anwendung nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="ead0a-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="ead0a-123">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen **MouseDown-,** [**MouseMove-**](inkcollector-mousemove.md)und [**MouseUp-Ereignissen.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="ead0a-123">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="ead0a-124">Das Abbrechen einiger dieser Ereignisse kann unerwartete Ergebnisse haben.</span><span class="sxs-lookup"><span data-stu-id="ead0a-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="ead0a-125">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseDown definiert.</span><span class="sxs-lookup"><span data-stu-id="ead0a-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead0a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ead0a-126">Requirements</span></span>



| <span data-ttu-id="ead0a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ead0a-127">Requirement</span></span> | <span data-ttu-id="ead0a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ead0a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead0a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ead0a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ead0a-130">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="ead0a-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ead0a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ead0a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ead0a-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ead0a-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ead0a-133">Header</span><span class="sxs-lookup"><span data-stu-id="ead0a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead0a-134"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="ead0a-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ead0a-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ead0a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ead0a-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ead0a-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ead0a-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ead0a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead0a-138">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ead0a-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="ead0a-139">**InkMouseButton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ead0a-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="ead0a-140">**InkShiftKeyModifierFlags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ead0a-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="ead0a-141">**MouseUp-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="ead0a-141">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




