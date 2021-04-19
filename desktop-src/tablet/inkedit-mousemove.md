---
description: Tritt ein, wenn der Benutzer die Maus bewegt, während sich der Mauszeiger über dem InkEdit-Steuerelement befindet.
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: InkEdit. mousermove-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0d3e98827a1f0ebcdc80f5d44765ebe768f65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350301"
---
# <a name="inkeditmousemove-event"></a><span data-ttu-id="c34bd-103">InkEdit. mousermove-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c34bd-103">InkEdit.MouseMove event</span></span>

<span data-ttu-id="c34bd-104">Tritt ein, wenn der Benutzer die Maus bewegt, während sich der Mauszeiger über dem [InkEdit](inkedit-control-reference.md) -Steuerelement befindet.</span><span class="sxs-lookup"><span data-stu-id="c34bd-104">Occurs when the user moves the mouse while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="c34bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c34bd-105">Syntax</span></span>


```C++
HRESULT MouseMove(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="c34bd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c34bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c34bd-107">*Schaltfläche*</span><span class="sxs-lookup"><span data-stu-id="c34bd-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="c34bd-108">Ein Member der [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) -Enumeration, der angibt, welche Maustasten gedrückt sind.</span><span class="sxs-lookup"><span data-stu-id="c34bd-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons are depressed.</span></span>



| <span data-ttu-id="c34bd-109">Wert</span><span class="sxs-lookup"><span data-stu-id="c34bd-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="c34bd-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c34bd-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="c34bd-111"><dt>**Nein \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="c34bd-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="c34bd-112">Standard.</span><span class="sxs-lookup"><span data-stu-id="c34bd-112">Default.</span></span> <span data-ttu-id="c34bd-113">Es wurde keine Maustaste gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c34bd-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="c34bd-114"><dt>**Links \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="c34bd-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="c34bd-115">Die linke Maustaste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c34bd-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="c34bd-116"><dt>**Rechts \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="c34bd-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="c34bd-117">Die rechte Maustaste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c34bd-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="c34bd-118"><dt>**Mittel \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="c34bd-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="c34bd-119">Die mittlere Maustaste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c34bd-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="c34bd-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="c34bd-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="c34bd-121">Ein Member der [**inkshiftkeymodifierflags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) -Enumeration, der angibt, welche modifiziererschlüssel zum Zeitpunkt des Ereignisses gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="c34bd-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="c34bd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c34bd-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="c34bd-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c34bd-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="c34bd-124"><dt>**IKM- \_ Schicht**</dt></span><span class="sxs-lookup"><span data-stu-id="c34bd-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="c34bd-125">Gibt an, dass die Umschalttaste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c34bd-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="c34bd-126"><dt>**IKM \_ Steuer** Element</dt></span><span class="sxs-lookup"><span data-stu-id="c34bd-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="c34bd-127">Gibt an, dass die STRG-Taste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c34bd-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="c34bd-128"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="c34bd-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="c34bd-129">Gibt an, dass die Alt-Taste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c34bd-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="c34bd-130">*xmaus*</span><span class="sxs-lookup"><span data-stu-id="c34bd-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="c34bd-131">Die aktuelle x-Koordinate des Mauszeigers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c34bd-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="c34bd-132">*ymouse*</span><span class="sxs-lookup"><span data-stu-id="c34bd-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="c34bd-133">Die aktuelle y-Koordinate des Mauszeigers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c34bd-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c34bd-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c34bd-134">Return value</span></span>

<span data-ttu-id="c34bd-135">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="c34bd-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c34bd-136">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c34bd-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c34bd-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c34bd-137">Remarks</span></span>

<span data-ttu-id="c34bd-138">Wenn eine Maustaste gedrückt wird, während sich der Mauszeiger über einem [InkEdit](inkedit-control-reference.md) -Steuerelement befindet, erfasst das Steuerelement die Maus und empfängt alle Mausereignisse bis einschließlich des letzten [**MouseUp**](inkedit-mouseup.md) -Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="c34bd-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last [**MouseUp**](inkedit-mouseup.md) event.</span></span> <span data-ttu-id="c34bd-139">Dies impliziert, dass die (x, y)-Mauszeiger Koordinaten, die von einem Maus Ereignis zurückgegeben werden, sich nicht immer im internen Bereich des Objekts befinden, das Sie empfängt.</span><span class="sxs-lookup"><span data-stu-id="c34bd-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="c34bd-140">Wenn die Maustasten nacheinander gedrückt werden, empfängt das Objekt, das die Maus nach dem ersten drücken aufzeichnet, alle Mausereignisse, bis alle Schaltflächen losgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="c34bd-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="c34bd-141">Das **MouseMove** -Ereignis wird fortlaufend generiert, wenn der Mauszeiger über Objekte bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="c34bd-141">The **MouseMove** event is generated continually as the mouse pointer moves across objects.</span></span> <span data-ttu-id="c34bd-142">Wenn die Maus von keinem anderen Objekt erfasst wird, erkennt ein [InkEdit](inkedit-control-reference.md) -Steuerelement immer dann ein **MouseMove** -Ereignis, wenn sich die Mausposition innerhalb seines Rahmens befindet.</span><span class="sxs-lookup"><span data-stu-id="c34bd-142">Unless another object has captured the mouse, an [InkEdit](inkedit-control-reference.md) control recognizes a **MouseMove** event whenever the mouse position is within its borders.</span></span>

<span data-ttu-id="c34bd-143">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="c34bd-143">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="c34bd-144">Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieemouabmove.</span><span class="sxs-lookup"><span data-stu-id="c34bd-144">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="c34bd-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c34bd-145">Requirements</span></span>



| <span data-ttu-id="c34bd-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c34bd-146">Requirement</span></span> | <span data-ttu-id="c34bd-147">Wert</span><span class="sxs-lookup"><span data-stu-id="c34bd-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c34bd-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c34bd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c34bd-149">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c34bd-149">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c34bd-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c34bd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c34bd-151">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c34bd-151">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c34bd-152">Header</span><span class="sxs-lookup"><span data-stu-id="c34bd-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c34bd-153"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="c34bd-153"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c34bd-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c34bd-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="c34bd-155"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c34bd-155"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c34bd-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c34bd-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c34bd-157">InkEdit</span><span class="sxs-lookup"><span data-stu-id="c34bd-157">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c34bd-158">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c34bd-158">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="c34bd-159">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="c34bd-159">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="c34bd-160">[**Mousdown-Ereignis, \[ InkEdit-Steuerelement\]**](inkedit-mousedown.md)</span><span class="sxs-lookup"><span data-stu-id="c34bd-160">[**MouseDown Event \[InkEdit Control\]**](inkedit-mousedown.md)</span></span>
</dt> <dt>

<span data-ttu-id="c34bd-161">[**Mousup-Ereignis \[ InkEdit-Steuerelement\]**](inkedit-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="c34bd-161">[**MouseUp Event \[InkEdit Control\]**](inkedit-mouseup.md)</span></span>
</dt> </dl>

 

