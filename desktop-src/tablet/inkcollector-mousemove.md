---
description: Tritt auf, wenn der Mauszeiger über das InkCollector-oder InkOverlay-Objekt bewegt wird.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: InkCollector. mousermove-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ad88c35871ed73125be73b66329ede464f0c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348765"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="f0133-103">InkCollector. mousermove-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f0133-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="f0133-104">Tritt auf, wenn der Mauszeiger über das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="f0133-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0133-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0133-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="f0133-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0133-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0133-107">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0133-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0133-108">Die Maustaste, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="f0133-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="f0133-109">*UMSCHALT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0133-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0133-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="f0133-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="f0133-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0133-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0133-112">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f0133-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="f0133-113">*pY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0133-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0133-114">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f0133-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="f0133-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0133-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0133-116">**Variant \_ TRUE** , um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="f0133-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0133-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0133-117">Return value</span></span>

<span data-ttu-id="f0133-118">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f0133-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0133-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0133-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f0133-120">Die Eigenschaften *px* und *pY* befinden sich in Pixel und nicht in den HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f0133-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="f0133-121">Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung, für die ein Stift nicht gilt, ersetzt und dieser Anwendungstyp nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="f0133-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0133-122">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**mouledown**](inkcollector-mousedown.md)-, **mousermove**-und [**mouberup**](inkcollector-mouseup.md) -Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="f0133-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="f0133-123">Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="f0133-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="f0133-124">Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemousemove definiert.</span><span class="sxs-lookup"><span data-stu-id="f0133-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0133-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0133-125">Requirements</span></span>



| <span data-ttu-id="f0133-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0133-126">Requirement</span></span> | <span data-ttu-id="f0133-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f0133-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0133-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0133-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f0133-129">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0133-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f0133-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0133-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f0133-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0133-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f0133-132">Header</span><span class="sxs-lookup"><span data-stu-id="f0133-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0133-133"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f0133-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f0133-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0133-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0133-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0133-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f0133-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0133-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0133-137">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f0133-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="f0133-138">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f0133-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="f0133-139">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f0133-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




