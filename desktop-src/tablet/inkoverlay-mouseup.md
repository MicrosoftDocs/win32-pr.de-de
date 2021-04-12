---
description: Tritt auf, wenn sich der Mauszeiger über dem InkCollector-oder InkOverlay-Objekt befindet und eine Maustaste losgelassen wird.
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: InkOverlay. mouberup-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16fd3dc5006f43e09e093cb2c474a8578f56c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217679"
---
# <a name="inkoverlaymouseup-event"></a><span data-ttu-id="eb9d6-103">InkOverlay. mouberup-Ereignis</span><span class="sxs-lookup"><span data-stu-id="eb9d6-103">InkOverlay.MouseUp event</span></span>

<span data-ttu-id="eb9d6-104">Tritt auf, wenn sich der Mauszeiger über dem [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt befindet und eine Maustaste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb9d6-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="eb9d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb9d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb9d6-107">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb9d6-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9d6-108">Die Maustaste, die freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="eb9d6-109">*UMSCHALT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb9d6-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9d6-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="eb9d6-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb9d6-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9d6-112">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="eb9d6-113">*pY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb9d6-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9d6-114">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="eb9d6-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eb9d6-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9d6-116">Ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="eb9d6-117">Der Standardwert ist **false**. er gibt an, dass das Ereignis nicht abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb9d6-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb9d6-118">Return value</span></span>

<span data-ttu-id="eb9d6-119">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb9d6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb9d6-120">Remarks</span></span>

<span data-ttu-id="eb9d6-121">Um die Echtzeitleistung zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown**](inkcollector-mousedown.md) -und [**MouseUp**](inkcollector-mouseup.md) -Ereignis Handlern aus, oder zeigen Sie ihn an.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="eb9d6-122">Die Eigenschaften *px* und *pY* befinden sich in Pixel und nicht in den HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-122">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="eb9d6-123">Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung, für die ein Stift nicht gilt, ersetzt und dieser Anwendungstyp nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="eb9d6-124">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**mouledown**](inkcollector-mousedown.md)-, [**mousermove**](inkcollector-mousemove.md)-und [**mouberup**](inkcollector-mouseup.md) -Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="eb9d6-125">Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="eb9d6-126">Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemouseup definiert.</span><span class="sxs-lookup"><span data-stu-id="eb9d6-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9d6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb9d6-127">Requirements</span></span>



| <span data-ttu-id="eb9d6-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb9d6-128">Requirement</span></span> | <span data-ttu-id="eb9d6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="eb9d6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9d6-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb9d6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eb9d6-131">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb9d6-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="eb9d6-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb9d6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eb9d6-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eb9d6-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="eb9d6-134">Header</span><span class="sxs-lookup"><span data-stu-id="eb9d6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb9d6-135"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eb9d6-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eb9d6-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb9d6-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb9d6-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb9d6-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="eb9d6-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb9d6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9d6-139">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eb9d6-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="eb9d6-140">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="eb9d6-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="eb9d6-141">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="eb9d6-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




