---
description: 'InkCollector.SystemGesture-Ereignis: Tritt auf, wenn eine Systemgeste erkannt wird.'
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.SystemGesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f753807d8aaaf03c2de2fd9810ef1e044bcbe05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110050"
---
# <a name="inkcollectorsystemgesture-event"></a><span data-ttu-id="222e7-103">InkCollector.SystemGesture-Ereignis</span><span class="sxs-lookup"><span data-stu-id="222e7-103">InkCollector.SystemGesture event</span></span>

<span data-ttu-id="222e7-104">Tritt ein, wenn eine Systemgeste erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="222e7-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="222e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="222e7-105">Syntax</span></span>


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a><span data-ttu-id="222e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="222e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="222e7-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="222e7-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222e7-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **SystemGesture-Ereignis** generiert hat.</span><span class="sxs-lookup"><span data-stu-id="222e7-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="222e7-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="222e7-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222e7-110">Der Wert der Systemgeste.</span><span class="sxs-lookup"><span data-stu-id="222e7-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="222e7-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="222e7-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222e7-112">Die x-Koordinate der Position der Geste.</span><span class="sxs-lookup"><span data-stu-id="222e7-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="222e7-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="222e7-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222e7-114">Die y-Koordinate der Position der Geste.</span><span class="sxs-lookup"><span data-stu-id="222e7-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="222e7-115">*Modifizierer* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="222e7-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222e7-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="222e7-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="222e7-117">*Zeichen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="222e7-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222e7-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="222e7-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="222e7-119">*CursorMode* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="222e7-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222e7-120">Ein -Wert, der angibt, ob sich das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) im Normalen- oder Radierermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="222e7-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="222e7-121">1 gilt für den normalen Modus und 2 für den Radierermodus.</span><span class="sxs-lookup"><span data-stu-id="222e7-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="222e7-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="222e7-122">Return value</span></span>

<span data-ttu-id="222e7-123">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="222e7-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="222e7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="222e7-124">Remarks</span></span>

<span data-ttu-id="222e7-125">Systemgesten sind nützlich, da sie Informationen über das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) liefern, das zum Erstellen der Geste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="222e7-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="222e7-126">Sie bieten auch Verknüpfungen zu Kombinationen von Mausereignissen und sind "kostengünstigere" Methoden zum Erkennen von Mausereignissen.</span><span class="sxs-lookup"><span data-stu-id="222e7-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="222e7-127">Anstatt beispielsweise nach einem [**MouseDown-Ereignispaar**](inkcollector-mouseup.md)für MouseUp-Ereignisse zu suchen, in dem keine anderen Mausereignisse dazwischen auftreten, können Sie nach den Systemgesten Tap oder  /  [](inkcollector-mousedown.md) **RightTap** suchen. [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="222e7-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="222e7-128">Ein weiteres Beispiel: Anstatt auf [**MouseDown Event**](inkcollector-mousedown.md)MouseMove Event-Ereignisse zu lauschen und zahlreiche  /  [](inkcollector-mousemove.md) **MouseMove-Ereignismeldungen** zu erhalten, können Sie nach den Drag- oder **RightDrag-Systemgesten** sehen, solange Sie nicht an den Koordinaten (x, y) jeder Position der Maus interessiert sind. [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="222e7-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="222e7-129">Dadurch können Sie anstelle zahlreicher **MouseMove-Ereignismeldungen nur** eine Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="222e7-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="222e7-130">Eine Liste mit bestimmten Systemgesten finden Sie unter [**InkSystemGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="222e7-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="222e7-131">Weitere Informationen zu Systemgesten finden Sie unter Verwenden von Gesten und [Befehlseingabe](using-gestures.md) [auf dem Tablet PC.](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="222e7-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="222e7-132">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICESystemGesture definiert.</span><span class="sxs-lookup"><span data-stu-id="222e7-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="222e7-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="222e7-133">Requirements</span></span>



| <span data-ttu-id="222e7-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="222e7-134">Requirement</span></span> | <span data-ttu-id="222e7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="222e7-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="222e7-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="222e7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="222e7-137">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="222e7-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="222e7-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="222e7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="222e7-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="222e7-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="222e7-140">Header</span><span class="sxs-lookup"><span data-stu-id="222e7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="222e7-141"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="222e7-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="222e7-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="222e7-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="222e7-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="222e7-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="222e7-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="222e7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="222e7-145">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="222e7-145">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="222e7-146">**InkSystemGesture-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="222e7-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="222e7-147">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="222e7-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="222e7-148">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="222e7-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="222e7-149">Stifteingabe, Ink und Erkennung</span><span class="sxs-lookup"><span data-stu-id="222e7-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="222e7-150">[Befehlseingabe auf dem Tablet-PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="222e7-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

