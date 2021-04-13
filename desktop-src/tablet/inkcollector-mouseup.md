---
description: Tritt auf, wenn sich der Mauszeiger über dem InkCollector-oder InkOverlay-Objekt befindet und eine Maustaste losgelassen wird.
ms.assetid: 6dcc6c68-89f7-4020-b378-56df9d46974b
title: InkCollector. mouberup-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f217cf6f5eeff930c1746d1a5ceac180686942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484371"
---
# <a name="inkcollectormouseup-event"></a><span data-ttu-id="fb2d3-103">InkCollector. mouberup-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fb2d3-103">InkCollector.MouseUp event</span></span>

<span data-ttu-id="fb2d3-104">Tritt auf, wenn sich der Mauszeiger über dem [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt befindet und eine Maustaste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb2d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb2d3-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="fb2d3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb2d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb2d3-107">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb2d3-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2d3-108">Die Maustaste, die freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="fb2d3-109">*UMSCHALT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb2d3-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2d3-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="fb2d3-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb2d3-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2d3-112">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fb2d3-113">*pY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb2d3-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2d3-114">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fb2d3-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fb2d3-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2d3-116">**Variant \_ TRUE** , um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb2d3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb2d3-117">Return value</span></span>

<span data-ttu-id="fb2d3-118">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb2d3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb2d3-119">Remarks</span></span>

<span data-ttu-id="fb2d3-120">Um die Echtzeitleistung zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown**](inkcollector-mousedown.md) -und **MouseUp** -Ereignis Handlern aus, oder zeigen Sie ihn an.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-120">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and **MouseUp** event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="fb2d3-121">Die Eigenschaften *px* und *pY* befinden sich in Pixel und nicht in den HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="fb2d3-122">Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung, für die ein Stift nicht gilt, ersetzt und dieser Anwendungstyp nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb2d3-123">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**mouledown**](inkcollector-mousedown.md)-, [**mousermove**](inkcollector-mousemove.md)-und **mouberup** -Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="fb2d3-124">Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="fb2d3-125">Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemouseup definiert.</span><span class="sxs-lookup"><span data-stu-id="fb2d3-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb2d3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb2d3-126">Requirements</span></span>



| <span data-ttu-id="fb2d3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb2d3-127">Requirement</span></span> | <span data-ttu-id="fb2d3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fb2d3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2d3-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb2d3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fb2d3-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb2d3-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fb2d3-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb2d3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fb2d3-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fb2d3-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fb2d3-133">Header</span><span class="sxs-lookup"><span data-stu-id="fb2d3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb2d3-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fb2d3-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fb2d3-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb2d3-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb2d3-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb2d3-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fb2d3-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb2d3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb2d3-138">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb2d3-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="fb2d3-139">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="fb2d3-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="fb2d3-140">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="fb2d3-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




