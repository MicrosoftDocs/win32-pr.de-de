---
description: Tritt ein, wenn der Benutzer eine Maustaste loslässt, während sich der Mauszeiger über dem InkEdit-Steuerelement befindet.
ms.assetid: 3c9e0229-c7e2-4b5c-9532-18fbf8a3667d
title: InkEdit. moumenup-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c331ec5dd0dd6a39ec956eda6980ee02cddd298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218054"
---
# <a name="inkeditmouseup-event"></a><span data-ttu-id="508db-103">InkEdit. mousetup-Ereignis</span><span class="sxs-lookup"><span data-stu-id="508db-103">InkEdit.MouseUp event</span></span>

<span data-ttu-id="508db-104">Tritt ein, wenn der Benutzer eine Maustaste loslässt, während sich der Mauszeiger über dem [InkEdit](inkedit-control-reference.md) -Steuerelement befindet.</span><span class="sxs-lookup"><span data-stu-id="508db-104">Occurs when the user releases a mouse button while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="508db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="508db-105">Syntax</span></span>


```C++
HRESULT MouseUp(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="508db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="508db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="508db-107">*Schaltfläche*</span><span class="sxs-lookup"><span data-stu-id="508db-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="508db-108">Ein Member der [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) -Enumeration, der angibt, welche Maustasten losgelassen wurden.</span><span class="sxs-lookup"><span data-stu-id="508db-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons were released.</span></span>



| <span data-ttu-id="508db-109">Wert</span><span class="sxs-lookup"><span data-stu-id="508db-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="508db-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="508db-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="508db-111"><dt>**Nein \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="508db-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="508db-112">Standard.</span><span class="sxs-lookup"><span data-stu-id="508db-112">Default.</span></span> <span data-ttu-id="508db-113">Es wurde keine Maustaste gedrückt.</span><span class="sxs-lookup"><span data-stu-id="508db-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="508db-114"><dt>**Links \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="508db-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="508db-115">Die linke Maustaste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="508db-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="508db-116"><dt>**Rechts \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="508db-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="508db-117">Die rechte Maustaste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="508db-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="508db-118"><dt>**Mittel \_ Schaltfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="508db-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="508db-119">Die mittlere Maustaste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="508db-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="508db-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="508db-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="508db-121">Ein Member der [**inkshiftkeymodifierflags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) -Enumeration, der angibt, welche modifiziererschlüssel zum Zeitpunkt des Ereignisses gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="508db-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="508db-122">Wert</span><span class="sxs-lookup"><span data-stu-id="508db-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="508db-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="508db-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="508db-124"><dt>**IKM- \_ Schicht**</dt></span><span class="sxs-lookup"><span data-stu-id="508db-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="508db-125">Gibt an, dass die Umschalttaste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="508db-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="508db-126"><dt>**IKM \_ Steuer** Element</dt></span><span class="sxs-lookup"><span data-stu-id="508db-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="508db-127">Gibt an, dass die STRG-Taste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="508db-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="508db-128"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="508db-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="508db-129">Gibt an, dass die Alt-Taste als Modifizierer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="508db-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="508db-130">*xmaus*</span><span class="sxs-lookup"><span data-stu-id="508db-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="508db-131">Die aktuelle x-Koordinate des Mauszeigers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="508db-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="508db-132">*ymouse*</span><span class="sxs-lookup"><span data-stu-id="508db-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="508db-133">Die aktuelle y-Koordinate des Mauszeigers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="508db-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="508db-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="508db-134">Return value</span></span>

<span data-ttu-id="508db-135">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="508db-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="508db-136">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="508db-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="508db-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="508db-137">Remarks</span></span>

<span data-ttu-id="508db-138">Wenn eine Maustaste gedrückt wird, während sich der Mauszeiger über einem [InkEdit](inkedit-control-reference.md) -Steuerelement befindet, erfasst das Steuerelement die Maus und empfängt alle Mausereignisse bis einschließlich des letzten **MouseUp** -Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="508db-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last **MouseUp** event.</span></span> <span data-ttu-id="508db-139">Dies impliziert, dass die (x, y)-Mauszeiger Koordinaten, die von einem Maus Ereignis zurückgegeben werden, sich nicht immer im internen Bereich des Objekts befinden, das Sie empfängt.</span><span class="sxs-lookup"><span data-stu-id="508db-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="508db-140">Wenn die Maustasten nacheinander gedrückt werden, empfängt das Objekt, das die Maus nach dem ersten drücken aufzeichnet, alle Mausereignisse, bis alle Schaltflächen losgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="508db-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="508db-141">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="508db-141">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="508db-142">Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieemouberup.</span><span class="sxs-lookup"><span data-stu-id="508db-142">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="508db-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="508db-143">Requirements</span></span>



| <span data-ttu-id="508db-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="508db-144">Requirement</span></span> | <span data-ttu-id="508db-145">Wert</span><span class="sxs-lookup"><span data-stu-id="508db-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="508db-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="508db-146">Minimum supported client</span></span><br/> | <span data-ttu-id="508db-147">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="508db-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="508db-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="508db-148">Minimum supported server</span></span><br/> | <span data-ttu-id="508db-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="508db-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="508db-150">Header</span><span class="sxs-lookup"><span data-stu-id="508db-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="508db-151"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="508db-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="508db-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="508db-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="508db-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="508db-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="508db-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="508db-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="508db-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="508db-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="508db-156">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="508db-156">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="508db-157">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="508db-157">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="508db-158">[**Mousdown-Ereignis, \[ InkEdit-Steuerelement\]**](inkedit-mousedown.md)</span><span class="sxs-lookup"><span data-stu-id="508db-158">[**MouseDown Event \[InkEdit Control\]**](inkedit-mousedown.md)</span></span>
</dt> <dt>

<span data-ttu-id="508db-159">[**Mousmove-Ereignis \[ InkEdit-Steuerelement\]**](inkedit-mousemove.md)</span><span class="sxs-lookup"><span data-stu-id="508db-159">[**MouseMove Event \[InkEdit Control\]**](inkedit-mousemove.md)</span></span>
</dt> </dl>

 

