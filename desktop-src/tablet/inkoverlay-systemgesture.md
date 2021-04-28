---
description: 'InkOverlay.SystemGesture-Ereignis: Tritt auf, wenn eine Systemgeste erkannt wird.'
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: InkOverlay.SystemGesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3498d6b5fa779f6a15866ac93d53be8348f3d1a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086668"
---
# <a name="inkoverlaysystemgesture-event"></a><span data-ttu-id="951f2-103">InkOverlay.SystemGesture-Ereignis</span><span class="sxs-lookup"><span data-stu-id="951f2-103">InkOverlay.SystemGesture event</span></span>

<span data-ttu-id="951f2-104">Tritt ein, wenn eine Systemgeste erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="951f2-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="951f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="951f2-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="951f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="951f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="951f2-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="951f2-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951f2-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**SystemGesture-Ereignis**](inkcollector-systemgesture.md) generiert hat.</span><span class="sxs-lookup"><span data-stu-id="951f2-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**SystemGesture**](inkcollector-systemgesture.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="951f2-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="951f2-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951f2-110">Der Wert der Systemgeste.</span><span class="sxs-lookup"><span data-stu-id="951f2-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="951f2-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="951f2-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951f2-112">Die x-Koordinate der Position der Geste.</span><span class="sxs-lookup"><span data-stu-id="951f2-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="951f2-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="951f2-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951f2-114">Die y-Koordinate der Position der Geste.</span><span class="sxs-lookup"><span data-stu-id="951f2-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="951f2-115">*Modifizierer* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="951f2-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951f2-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="951f2-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="951f2-117">*Zeichen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="951f2-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951f2-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="951f2-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="951f2-119">*CursorMode* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="951f2-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951f2-120">Ein -Wert, der angibt, ob sich das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) im Normalen- oder Radierermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="951f2-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="951f2-121">1 gilt für den normalen Modus und 2 für den Radierermodus.</span><span class="sxs-lookup"><span data-stu-id="951f2-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="951f2-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="951f2-122">Return value</span></span>

<span data-ttu-id="951f2-123">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="951f2-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="951f2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="951f2-124">Remarks</span></span>

<span data-ttu-id="951f2-125">Systemgesten sind nützlich, da sie Informationen über das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) liefern, das zum Erstellen der Geste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="951f2-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="951f2-126">Sie bieten auch Verknüpfungen zu Kombinationen von Mausereignissen und sind "kostengünstigere" Methoden zum Erkennen von Mausereignissen.</span><span class="sxs-lookup"><span data-stu-id="951f2-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="951f2-127">Anstatt beispielsweise nach einem [**MouseDown Event MouseDown**](inkcollector-mouseup.md)Event-Ereignispaar zu suchen, bei dem  /  [](inkcollector-mousedown.md) keine anderen Mausereignisse dazwischen auftreten, können Sie nach den [**Systemgesten Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) oder **RightTap** suchen.</span><span class="sxs-lookup"><span data-stu-id="951f2-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="951f2-128">Ein weiteres Beispiel: Anstatt auf [**MouseDown Event**](inkcollector-mousedown.md)  /  [**MouseMove Event-Ereignisse**](inkcollector-mousemove.md) zu lauschen und zahlreiche **MouseMove Event-Meldungen** zu erhalten, können Sie auf die [**Drag-**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) oder **RightDrag-Systemgesten** achten, solange Sie nicht an den (x, y) Koordinaten jeder Position der Maus interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="951f2-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="951f2-129">Dadurch können Sie anstelle zahlreicher **MouseMove-Ereignismeldungen** nur eine Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="951f2-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="951f2-130">Eine Liste der spezifischen Systemgesten finden Sie unter [**InkSystemGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="951f2-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="951f2-131">Weitere Informationen zu Systemgesten finden Sie unter Verwenden von Gesten und [Befehlseingaben auf dem Tablet PC.](/previous-versions//dd314533(v=vs.85)) [](using-gestures.md)</span><span class="sxs-lookup"><span data-stu-id="951f2-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="951f2-132">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICESystemGesture definiert.</span><span class="sxs-lookup"><span data-stu-id="951f2-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="951f2-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="951f2-133">Requirements</span></span>



| <span data-ttu-id="951f2-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="951f2-134">Requirement</span></span> | <span data-ttu-id="951f2-135">Wert</span><span class="sxs-lookup"><span data-stu-id="951f2-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="951f2-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="951f2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="951f2-137">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="951f2-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="951f2-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="951f2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="951f2-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="951f2-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="951f2-140">Header</span><span class="sxs-lookup"><span data-stu-id="951f2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="951f2-141"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="951f2-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="951f2-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="951f2-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="951f2-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="951f2-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="951f2-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="951f2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="951f2-145">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="951f2-145">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="951f2-146">**InkSystemGesture-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="951f2-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="951f2-147">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="951f2-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="951f2-148">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="951f2-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="951f2-149">Stifteingabe, Ink und Erkennung</span><span class="sxs-lookup"><span data-stu-id="951f2-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="951f2-150">[Befehlseingabe auf dem Tablet-PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="951f2-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

