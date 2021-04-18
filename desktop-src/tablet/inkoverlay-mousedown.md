---
description: Tritt auf, wenn sich der Mauszeiger über dem InkCollector-oder InkOverlay-Objekt befindet und eine Maustaste gedrückt wird.
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: InkOverlay. moutardown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c011de55543bee08aeda1a8a986b597523ad805d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351028"
---
# <a name="inkoverlaymousedown-event"></a><span data-ttu-id="6d4af-103">InkOverlay. moutardown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6d4af-103">InkOverlay.MouseDown event</span></span>

<span data-ttu-id="6d4af-104">Tritt auf, wenn sich der Mauszeiger über dem [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt befindet und eine Maustaste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="6d4af-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d4af-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="6d4af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d4af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d4af-107">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d4af-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4af-108">Die Maustaste, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d4af-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="6d4af-109">*UMSCHALT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d4af-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4af-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="6d4af-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="6d4af-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d4af-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4af-112">Die X-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="6d4af-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="6d4af-113">*pY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d4af-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4af-114">Die Y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="6d4af-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="6d4af-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6d4af-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4af-116">**Variant \_ TRUE** , wenn das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="6d4af-116">**VARIANT\_TRUE** to cancelt he event forthe parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="6d4af-117">Der Standardwert ist **Variant \_ false** .</span><span class="sxs-lookup"><span data-stu-id="6d4af-117">The default value is **VARIANT\_FALSE**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d4af-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d4af-118">Return value</span></span>

<span data-ttu-id="6d4af-119">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6d4af-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d4af-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d4af-120">Remarks</span></span>

<span data-ttu-id="6d4af-121">Um die Echtzeitleistung zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown**](inkcollector-mousedown.md) -und [**MouseUp**](inkcollector-mouseup.md) -Ereignis Handlern aus, oder zeigen Sie ihn an.</span><span class="sxs-lookup"><span data-stu-id="6d4af-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="6d4af-122">Die Eigenschaften px und pY befinden sich in Pixel und nicht in den HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6d4af-122">The properties pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="6d4af-123">Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung, für die ein Stift nicht gilt, ersetzt und dieser Anwendungstyp nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="6d4af-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="6d4af-124">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**mouledown**](inkcollector-mousedown.md)-, [**mousermove**](inkcollector-mousemove.md)-und [**mouberup**](inkcollector-mouseup.md) -Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="6d4af-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="6d4af-125">Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="6d4af-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="6d4af-126">Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemousedown definiert.</span><span class="sxs-lookup"><span data-stu-id="6d4af-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4af-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d4af-127">Requirements</span></span>



| <span data-ttu-id="6d4af-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d4af-128">Requirement</span></span> | <span data-ttu-id="6d4af-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6d4af-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4af-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d4af-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6d4af-131">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d4af-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6d4af-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d4af-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6d4af-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6d4af-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6d4af-134">Header</span><span class="sxs-lookup"><span data-stu-id="6d4af-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d4af-135"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6d4af-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6d4af-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d4af-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d4af-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d4af-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6d4af-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d4af-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4af-139">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6d4af-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="6d4af-140">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6d4af-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="6d4af-141">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6d4af-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="6d4af-142">**Mouberup-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="6d4af-142">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




