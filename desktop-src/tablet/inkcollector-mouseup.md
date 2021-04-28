---
description: 'InkCollector.MouseUp-Ereignis: Tritt auf, wenn sich der Mauszeiger über dem InkCollector- oder InkOverlay-Objekt befindet und eine Maustaste losgelassen wird.'
ms.assetid: 6dcc6c68-89f7-4020-b378-56df9d46974b
title: InkCollector.MouseUp-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc4fde64603a00ecb8a47d3869f2eb90352fcc4f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110148"
---
# <a name="inkcollectormouseup-event"></a><span data-ttu-id="81ad3-103">InkCollector.MouseUp-Ereignis</span><span class="sxs-lookup"><span data-stu-id="81ad3-103">InkCollector.MouseUp event</span></span>

<span data-ttu-id="81ad3-104">Tritt ein, wenn sich der Mauszeiger über dem [**InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) befindet und eine Maustaste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="81ad3-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ad3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81ad3-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="81ad3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81ad3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ad3-107">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="81ad3-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ad3-108">Die Maustaste, die losgelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="81ad3-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="81ad3-109">*Umschalten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="81ad3-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ad3-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="81ad3-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="81ad3-111">*pX* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="81ad3-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ad3-112">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="81ad3-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="81ad3-113">*pY* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="81ad3-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81ad3-114">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="81ad3-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="81ad3-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="81ad3-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="81ad3-116">**VARIANT \_ TRUE,** um das Ereignis für das übergeordnete Steuerelement abzubricht; andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="81ad3-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ad3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81ad3-117">Return value</span></span>

<span data-ttu-id="81ad3-118">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="81ad3-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81ad3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81ad3-119">Remarks</span></span>

<span data-ttu-id="81ad3-120">Um die Leistung von Ink in Echtzeit zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown-**](inkcollector-mousedown.md) und **MouseUp-Ereignishandlern** aus oder ein.</span><span class="sxs-lookup"><span data-stu-id="81ad3-120">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and **MouseUp** event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="81ad3-121">Die Eigenschaften *pX* und *pY* befinden sich in Pixeln und nicht in den HIMETRIC-Einheiten, die dem Freiraum zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="81ad3-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="81ad3-122">Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Nicht-Stiftanwendung ersetzt und diese Art von Anwendung nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="81ad3-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="81ad3-123">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**MouseDown-,**](inkcollector-mousedown.md) [**MouseMove-**](inkcollector-mousemove.md)und **MouseUp-Ereignissen.**</span><span class="sxs-lookup"><span data-stu-id="81ad3-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="81ad3-124">Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="81ad3-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="81ad3-125">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseUp definiert.</span><span class="sxs-lookup"><span data-stu-id="81ad3-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ad3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81ad3-126">Requirements</span></span>



| <span data-ttu-id="81ad3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81ad3-127">Requirement</span></span> | <span data-ttu-id="81ad3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="81ad3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81ad3-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81ad3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="81ad3-130">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="81ad3-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="81ad3-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81ad3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="81ad3-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="81ad3-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="81ad3-133">Header</span><span class="sxs-lookup"><span data-stu-id="81ad3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="81ad3-134"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="81ad3-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="81ad3-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81ad3-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="81ad3-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81ad3-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="81ad3-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="81ad3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ad3-138">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="81ad3-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="81ad3-139">**InkMouseButton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="81ad3-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="81ad3-140">**InkShiftKeyModifierFlags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="81ad3-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




