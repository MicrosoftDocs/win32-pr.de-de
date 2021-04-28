---
description: 'InkOverlay.MouseMove-Ereignis: Tritt auf, wenn der Mauszeiger über das InkCollector- oder InkOverlay-Objekt bewegt wird.'
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: InkOverlay.MouseMove-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8290a11b00dcf97b3f3d8568ebe9890f715454
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116908"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="f9af4-103">InkOverlay.MouseMove-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f9af4-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="f9af4-104">Tritt ein, wenn der Mauszeiger über das [**InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="f9af4-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9af4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9af4-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="f9af4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9af4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9af4-107">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f9af4-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9af4-108">Die gedrückte Maustaste.</span><span class="sxs-lookup"><span data-stu-id="f9af4-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="f9af4-109">*Umschalten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f9af4-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9af4-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="f9af4-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="f9af4-111">*pX* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f9af4-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9af4-112">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f9af4-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="f9af4-113">*pY* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f9af4-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9af4-114">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f9af4-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="f9af4-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f9af4-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9af4-116">Gibt an, ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9af4-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="f9af4-117">Der Standardwert ist **FALSE,** der angibt, dass das Ereignis nicht abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9af4-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9af4-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9af4-118">Return value</span></span>

<span data-ttu-id="f9af4-119">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f9af4-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9af4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9af4-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f9af4-121">Die Eigenschaften *pX* und *pY* sind in Pixel und nicht die HIMETRIC-Einheiten, die dem Freihandraum zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f9af4-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="f9af4-122">Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Anwendung ohne Stift ersetzt und diese Art von Anwendung nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="f9af4-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="f9af4-123">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**MouseDown-,**](inkcollector-mousedown.md) [**MouseMove-**](inkcollector-mousemove.md)und [**MouseUp-Ereignissen.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="f9af4-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="f9af4-124">Das Abbrechen einiger dieser Ereignisse kann unerwartete Ergebnisse haben.</span><span class="sxs-lookup"><span data-stu-id="f9af4-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="f9af4-125">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseMove definiert.</span><span class="sxs-lookup"><span data-stu-id="f9af4-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9af4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9af4-126">Requirements</span></span>



| <span data-ttu-id="f9af4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9af4-127">Requirement</span></span> | <span data-ttu-id="f9af4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f9af4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9af4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9af4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f9af4-130">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="f9af4-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f9af4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9af4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f9af4-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f9af4-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f9af4-133">Header</span><span class="sxs-lookup"><span data-stu-id="f9af4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9af4-134"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="f9af4-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f9af4-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9af4-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9af4-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9af4-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f9af4-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f9af4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9af4-138">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f9af4-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="f9af4-139">**InkMouseButton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f9af4-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="f9af4-140">**InkShiftKeyModifierFlags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f9af4-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




