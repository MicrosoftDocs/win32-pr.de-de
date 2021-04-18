---
description: Tritt auf, wenn sich der Mauszeiger über dem InkCollector-oder InkOverlay-Objekt befindet und eine Maustaste gedrückt wird.
ms.assetid: db9ec396-b2a7-4f4f-99f2-95aad46eea28
title: InkCollector. mouabdown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760801fb5c578ddbdd67b15a4201c21c4981b097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525271"
---
# <a name="inkcollectormousedown-event"></a><span data-ttu-id="a681b-103">InkCollector. mousegdown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a681b-103">InkCollector.MouseDown event</span></span>

<span data-ttu-id="a681b-104">Tritt auf, wenn sich der Mauszeiger über dem [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt befindet und eine Maustaste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="a681b-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a681b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a681b-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="a681b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a681b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a681b-107">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a681b-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a681b-108">Die Maustaste, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="a681b-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="a681b-109">*UMSCHALT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a681b-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a681b-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="a681b-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="a681b-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a681b-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a681b-112">Die X-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a681b-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="a681b-113">*pY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a681b-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a681b-114">Die Y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a681b-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="a681b-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a681b-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a681b-116">**Variant \_ TRUE** , um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="a681b-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a681b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a681b-117">Return value</span></span>

<span data-ttu-id="a681b-118">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a681b-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a681b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a681b-119">Remarks</span></span>

<span data-ttu-id="a681b-120">Um die Echtzeitleistung zu verbessern, blenden Sie den Mauszeiger in den **MouseDown** -und [**MouseUp**](inkcollector-mouseup.md) -Ereignis Handlern aus, oder zeigen Sie ihn an.</span><span class="sxs-lookup"><span data-stu-id="a681b-120">To improve real-time ink performance, hide or show the mouse cursor in the **MouseDown** and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="a681b-121">Die Eigenschaften *px* und *pY* befinden sich in Pixel und nicht in den HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a681b-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="a681b-122">Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung, für die ein Stift nicht gilt, ersetzt und dieser Anwendungstyp nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="a681b-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="a681b-123">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen **mouledown**-, [**mousermove**](inkcollector-mousemove.md)-und [**mouberup**](inkcollector-mouseup.md) -Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="a681b-123">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="a681b-124">Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="a681b-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="a681b-125">Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemousedown definiert.</span><span class="sxs-lookup"><span data-stu-id="a681b-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="a681b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a681b-126">Requirements</span></span>



| <span data-ttu-id="a681b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a681b-127">Requirement</span></span> | <span data-ttu-id="a681b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a681b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a681b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a681b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a681b-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a681b-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a681b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a681b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a681b-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a681b-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a681b-133">Header</span><span class="sxs-lookup"><span data-stu-id="a681b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a681b-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a681b-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a681b-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a681b-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a681b-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a681b-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a681b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a681b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a681b-138">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a681b-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="a681b-139">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a681b-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="a681b-140">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="a681b-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="a681b-141">**Mouberup-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="a681b-141">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




