---
description: Tritt auf, wenn eine Anwendungs Geste erkannt wird.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: InkEdit. Gesten-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216594"
---
# <a name="inkeditgesture-event"></a><span data-ttu-id="ce47a-103">InkEdit. Gesten-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ce47a-103">InkEdit.Gesture event</span></span>

<span data-ttu-id="ce47a-104">Tritt auf, wenn eine Anwendungs Geste erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="ce47a-104">Occurs when an application gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce47a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce47a-105">Syntax</span></span>


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ce47a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce47a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce47a-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce47a-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce47a-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das zum Erstellen dieser Geste verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ce47a-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that was used to create this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="ce47a-109">*Striche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce47a-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce47a-110">Die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte enthält, die diese Geste bilden.</span><span class="sxs-lookup"><span data-stu-id="ce47a-110">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that contains the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that make up this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="ce47a-111">*Gesten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce47a-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce47a-112">Ein Array von [**iinkgesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) -Objekten in der richtigen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ce47a-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence.</span></span>

<span data-ttu-id="ce47a-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="ce47a-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce47a-114">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ce47a-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce47a-115">Gibt an, ob die [inkstroke](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, aus der diese Geste besteht, abgebrochen werden soll, um die frei Hand Eingabe zu löschen und das [**Stroke**](inkedit-stroke.md) -Ereignis auszulösen.</span><span class="sxs-lookup"><span data-stu-id="ce47a-115">Whether the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that makes up this gesture should be canceled, so as not to erase the ink and to fire the [**Stroke**](inkedit-stroke.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce47a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce47a-116">Return value</span></span>

<span data-ttu-id="ce47a-117">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="ce47a-117">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce47a-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ce47a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce47a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce47a-119">Remarks</span></span>

<span data-ttu-id="ce47a-120">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="ce47a-120">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="ce47a-121">Die **\_ iinkeditevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner DISPID \_ ieegesten.</span><span class="sxs-lookup"><span data-stu-id="ce47a-121">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of DISPID\_IeeGesture.</span></span>

<span data-ttu-id="ce47a-122">Ein **Gesten** Ereignis wird nur ausgelöst, wenn das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt für das [**iinkgesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) -Objekt das erste **IInkStrokeDisp** -Objekt seit dem letzten aufzurufenden [**Rückruf der Erkennungsmethode oder**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) der letzten Auslösung des Erkennungs Timeouts ist.</span><span class="sxs-lookup"><span data-stu-id="ce47a-122">A **Gesture** event is raised only if the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) for the [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object is the first **IInkStrokeDisp** object since the last call to the [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or the last firing of the recognition timeout.</span></span>

<span data-ttu-id="ce47a-123">Wenn das **Gesten** Ereignis abgebrochen wird, wird das [**Stroke**](inkedit-stroke.md) -Ereignis für die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ausgelöst, die das **Gesten** Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="ce47a-123">If the **Gesture** event is canceled, the [**Stroke**](inkedit-stroke.md) event is raised for the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that raised the **Gesture** event.</span></span>

<span data-ttu-id="ce47a-124">Damit dieses Ereignis auftritt, muss das [InkEdit](inkedit-control-reference.md) -Steuerelement einen Satz von Anwendungs Gesten abonnieren.</span><span class="sxs-lookup"><span data-stu-id="ce47a-124">For this event to occur, the [InkEdit](inkedit-control-reference.md) control must subscribe to a set of application gestures.</span></span> <span data-ttu-id="ce47a-125">Um das Interesse des InkEdit-Steuer Elements in einem Satz von Gesten festzulegen, müssen Sie die [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ce47a-125">To set the InkEdit control's interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) method.</span></span>

<span data-ttu-id="ce47a-126">Eine Liste der Anwendungs Gesten finden Sie unter der [**inkapplicationgesten-Enumerationstyp**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="ce47a-126">For a list of application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

<span data-ttu-id="ce47a-127">Das [InkEdit](inkedit-control-reference.md) -Steuerelement erkennt nicht mehrere Strich Gesten.</span><span class="sxs-lookup"><span data-stu-id="ce47a-127">The [InkEdit](inkedit-control-reference.md) control does not recognize multiple stroke gestures.</span></span>

<span data-ttu-id="ce47a-128">Das [InkEdit](inkedit-control-reference.md) -Steuerelement abonniert die folgenden Gesten.</span><span class="sxs-lookup"><span data-stu-id="ce47a-128">The [InkEdit](inkedit-control-reference.md) control subscribes to the following gestures.</span></span>



| <span data-ttu-id="ce47a-129">Geste</span><span class="sxs-lookup"><span data-stu-id="ce47a-129">Gesture</span></span>                              | <span data-ttu-id="ce47a-130">Aktion</span><span class="sxs-lookup"><span data-stu-id="ce47a-130">Action</span></span>               |
|--------------------------------------|----------------------|
| <span data-ttu-id="ce47a-131">Nach unten links, nach unten links</span><span class="sxs-lookup"><span data-stu-id="ce47a-131">Down-left ,Down-left-long</span></span><br/> | <span data-ttu-id="ce47a-132">EINGABETASTE</span><span class="sxs-lookup"><span data-stu-id="ce47a-132">Enter</span></span><br/>     |
| <span data-ttu-id="ce47a-133">Rechts</span><span class="sxs-lookup"><span data-stu-id="ce47a-133">Right</span></span><br/>                     | <span data-ttu-id="ce47a-134">LeerZchn</span><span class="sxs-lookup"><span data-stu-id="ce47a-134">Space</span></span><br/>     |
| <span data-ttu-id="ce47a-135">Links</span><span class="sxs-lookup"><span data-stu-id="ce47a-135">Left</span></span><br/>                      | <span data-ttu-id="ce47a-136">Rücktaste</span><span class="sxs-lookup"><span data-stu-id="ce47a-136">Backspace</span></span><br/> |
| <span data-ttu-id="ce47a-137">Rechts oben, rechts oben</span><span class="sxs-lookup"><span data-stu-id="ce47a-137">Up-right, Up-right-long</span></span><br/>   | <span data-ttu-id="ce47a-138">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ce47a-138">Tab</span></span><br/>       |



 

<span data-ttu-id="ce47a-139">So ändern Sie die Standardaktion für eine Geste:</span><span class="sxs-lookup"><span data-stu-id="ce47a-139">To alter the default action for a gesture:</span></span>

1.  <span data-ttu-id="ce47a-140">Fügen Sie Ereignishandler für die **Gesten** -und [**hubereignisse**](inkedit-stroke.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="ce47a-140">Add event handlers for the **Gesture** and [**Stroke**](inkedit-stroke.md) events.</span></span>
2.  <span data-ttu-id="ce47a-141">Brechen Sie im **Gesten** Ereignishandler das **Gesten** Ereignis für die Geste ab, und führen Sie die alternative Aktion für die Geste aus.</span><span class="sxs-lookup"><span data-stu-id="ce47a-141">In the **Gesture** event handler, cancel the **Gesture** event for the gesture, and perform the alternate action for the gesture.</span></span>
3.  <span data-ttu-id="ce47a-142">Brechen Sie im [**Stroke**](inkedit-stroke.md) -Ereignishandler das **Stroke** -Ereignis für das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt ab, das das abgebrochene **Gesten** Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="ce47a-142">In the [**Stroke**](inkedit-stroke.md) event handler, cancel the **Stroke** event for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that raised the canceled **Gesture** event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce47a-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce47a-143">Requirements</span></span>



| <span data-ttu-id="ce47a-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce47a-144">Requirement</span></span> | <span data-ttu-id="ce47a-145">Wert</span><span class="sxs-lookup"><span data-stu-id="ce47a-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce47a-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce47a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ce47a-147">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce47a-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ce47a-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce47a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ce47a-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ce47a-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ce47a-150">Header</span><span class="sxs-lookup"><span data-stu-id="ce47a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce47a-151"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="ce47a-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ce47a-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce47a-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce47a-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce47a-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ce47a-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce47a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce47a-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="ce47a-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ce47a-156">**Inkapplicationgesten-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="ce47a-156">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

<span data-ttu-id="ce47a-157">[**SetGestureStatus-Methode, \[ InkEdit-Steuerelement\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span><span class="sxs-lookup"><span data-stu-id="ce47a-157">[**SetGestureStatus Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span></span>
</dt> <dt>

[<span data-ttu-id="ce47a-158">**RecoTimeout (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ce47a-158">**RecoTimeout Property**</span></span>](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

<span data-ttu-id="ce47a-159">[**InkEdit-Steuerelement für Stroke-Ereignis \[\]**](inkedit-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="ce47a-159">[**Stroke Event \[InkEdit Control\]**](inkedit-stroke.md)</span></span>
</dt> <dt>

[<span data-ttu-id="ce47a-160">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="ce47a-160">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

