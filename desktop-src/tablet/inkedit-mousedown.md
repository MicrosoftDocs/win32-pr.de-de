---
description: Tritt ein, wenn der Benutzer eine Maustaste drückt, während sich der Mauszeiger über dem InkEdit-Steuerelement befindet.
ms.assetid: 8985fee5-7b63-46ab-b229-046e2f0ee004
title: InkEdit. moumendown-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78e684fe2d75e5eaaf2b0064e8c7c78cbfe281a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868296"
---
# <a name="inkeditmousedown-event"></a><span data-ttu-id="5aa81-103">InkEdit. moueindown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5aa81-103">InkEdit.MouseDown event</span></span>

<span data-ttu-id="5aa81-104">Tritt ein, wenn der Benutzer eine Maustaste drückt, während sich der Mauszeiger über dem [InkEdit](inkedit-control-reference.md) -Steuerelement befindet.</span><span class="sxs-lookup"><span data-stu-id="5aa81-104">Occurs when the user presses a mouse button while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa81-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aa81-105">Syntax</span></span>


```C++
HRESULT MouseDown(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="5aa81-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aa81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa81-107">*Schaltfläche*</span><span class="sxs-lookup"><span data-stu-id="5aa81-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa81-108">Ein Member der [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) -Enumeration, der angibt, welche Maustasten gedrückt wurden.</span><span class="sxs-lookup"><span data-stu-id="5aa81-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons were pressed.</span></span>



| <span data-ttu-id="5aa81-109">Wert</span><span class="sxs-lookup"><span data-stu-id="5aa81-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="5aa81-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5aa81-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="5aa81-111"><dt>**Nein \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="5aa81-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="5aa81-112">Standard.</span><span class="sxs-lookup"><span data-stu-id="5aa81-112">Default.</span></span> <span data-ttu-id="5aa81-113">Es wurde keine Maustaste gedrückt.</span><span class="sxs-lookup"><span data-stu-id="5aa81-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="5aa81-114"><dt>**Links \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="5aa81-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="5aa81-115">Die linke Maustaste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="5aa81-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="5aa81-116"><dt>**Rechts \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="5aa81-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="5aa81-117">Die rechte Maustaste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="5aa81-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="5aa81-118"><dt>**Mittel \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="5aa81-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="5aa81-119">Die mittlere Maustaste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="5aa81-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="5aa81-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="5aa81-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa81-121">Ein Member der [**inkshiftkeymodifierflags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) -Enumeration, der angibt, welche modifiziererschlüssel zum Zeitpunkt des Ereignisses gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="5aa81-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="5aa81-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5aa81-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="5aa81-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5aa81-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="5aa81-124"><dt>**IKM- \_ Schicht**</dt></span><span class="sxs-lookup"><span data-stu-id="5aa81-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="5aa81-125">Gibt an, dass die Umschalttaste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5aa81-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="5aa81-126"><dt>**IKM \_ Steuer** Element</dt></span><span class="sxs-lookup"><span data-stu-id="5aa81-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="5aa81-127">Gibt an, dass die STRG-Taste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5aa81-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="5aa81-128"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="5aa81-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="5aa81-129">Gibt an, dass die Alt-Taste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5aa81-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="5aa81-130">*xmaus*</span><span class="sxs-lookup"><span data-stu-id="5aa81-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa81-131">Die aktuelle x-Koordinate des Mauszeigers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5aa81-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="5aa81-132">*ymouse*</span><span class="sxs-lookup"><span data-stu-id="5aa81-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa81-133">Die aktuelle y-Koordinate des Mauszeigers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5aa81-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa81-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5aa81-134">Return value</span></span>

<span data-ttu-id="5aa81-135">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="5aa81-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5aa81-136">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5aa81-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aa81-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5aa81-137">Remarks</span></span>

<span data-ttu-id="5aa81-138">Wenn eine Maustaste gedrückt wird, während sich der Mauszeiger über einem [InkEdit](inkedit-control-reference.md) -Steuerelement befindet, erfasst das Steuerelement die Maus und empfängt alle Mausereignisse bis einschließlich des letzten [**MouseUp**](inkedit-mouseup.md) -Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="5aa81-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last [**MouseUp**](inkedit-mouseup.md) event.</span></span> <span data-ttu-id="5aa81-139">Dies impliziert, dass die (x, y)-Mauszeiger Koordinaten, die von einem Maus Ereignis zurückgegeben werden, sich nicht immer im internen Bereich des Objekts befinden, das Sie empfängt.</span><span class="sxs-lookup"><span data-stu-id="5aa81-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="5aa81-140">Wenn die Maustasten nacheinander gedrückt werden, empfängt das Objekt, das die Maus nach dem ersten drücken aufzeichnet, alle Mausereignisse, bis alle Schaltflächen losgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="5aa81-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="5aa81-141">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="5aa81-141">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="5aa81-142">Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieemouabdown.</span><span class="sxs-lookup"><span data-stu-id="5aa81-142">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa81-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5aa81-143">Requirements</span></span>



| <span data-ttu-id="5aa81-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5aa81-144">Requirement</span></span> | <span data-ttu-id="5aa81-145">Wert</span><span class="sxs-lookup"><span data-stu-id="5aa81-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa81-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5aa81-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa81-147">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5aa81-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5aa81-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5aa81-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa81-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5aa81-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5aa81-150">Header</span><span class="sxs-lookup"><span data-stu-id="5aa81-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="5aa81-151"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="5aa81-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5aa81-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5aa81-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="5aa81-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aa81-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5aa81-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5aa81-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa81-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="5aa81-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="5aa81-156">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="5aa81-156">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="5aa81-157">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="5aa81-157">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="5aa81-158">[**Mousmove-Ereignis \[ InkEdit-Steuerelement\]**](inkedit-mousemove.md)</span><span class="sxs-lookup"><span data-stu-id="5aa81-158">[**MouseMove Event \[InkEdit Control\]**](inkedit-mousemove.md)</span></span>
</dt> <dt>

<span data-ttu-id="5aa81-159">[**Mousup-Ereignis \[ InkEdit-Steuerelement\]**](inkedit-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="5aa81-159">[**MouseUp Event \[InkEdit Control\]**](inkedit-mouseup.md)</span></span>
</dt> </dl>

 

