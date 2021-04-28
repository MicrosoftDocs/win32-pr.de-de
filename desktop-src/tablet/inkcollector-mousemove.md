---
description: 'InkCollector.MouseMove-Ereignis: Tritt auf, wenn der Mauszeiger über das InkCollector- oder InkOverlay-Objekt bewegt wird.'
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: InkCollector.MouseMove-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3392f2022af39600cb24461b26d37e5d624f4cb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110158"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="f8d6d-103">InkCollector.MouseMove-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f8d6d-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="f8d6d-104">Tritt ein, wenn der Mauszeiger über das [**InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8d6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8d6d-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="f8d6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8d6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8d6d-107">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f8d6d-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8d6d-108">Die gedrückte Maustaste.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="f8d6d-109">*Umschalten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f8d6d-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8d6d-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="f8d6d-111">*pX* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f8d6d-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8d6d-112">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="f8d6d-113">*pY* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f8d6d-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8d6d-114">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="f8d6d-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f8d6d-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8d6d-116">**VARIANT \_ TRUE,** um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8d6d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8d6d-117">Return value</span></span>

<span data-ttu-id="f8d6d-118">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8d6d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8d6d-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8d6d-120">Die Eigenschaften *pX* und *pY* sind in Pixel und nicht die HIMETRIC-Einheiten, die dem Freihandraum zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="f8d6d-121">Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Anwendung ohne Stift ersetzt und diese Art von Anwendung nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="f8d6d-122">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**MouseDown-,**](inkcollector-mousedown.md) **MouseMove-** und [**MouseUp-Ereignissen.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="f8d6d-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="f8d6d-123">Das Abbrechen einiger dieser Ereignisse kann unerwartete Ergebnisse haben.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="f8d6d-124">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseMove definiert.</span><span class="sxs-lookup"><span data-stu-id="f8d6d-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8d6d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8d6d-125">Requirements</span></span>



| <span data-ttu-id="f8d6d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8d6d-126">Requirement</span></span> | <span data-ttu-id="f8d6d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f8d6d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d6d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8d6d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f8d6d-129">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="f8d6d-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f8d6d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8d6d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f8d6d-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f8d6d-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f8d6d-132">Header</span><span class="sxs-lookup"><span data-stu-id="f8d6d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8d6d-133"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="f8d6d-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f8d6d-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f8d6d-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8d6d-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8d6d-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f8d6d-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8d6d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8d6d-137">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f8d6d-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="f8d6d-138">**InkMouseButton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f8d6d-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="f8d6d-139">**InkShiftKeyModifierFlags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f8d6d-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




