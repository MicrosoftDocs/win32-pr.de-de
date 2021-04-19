---
description: Tritt auf, wenn eine System Bewegung erkannt wird.
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: InkOverlay.Systemgesten-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b1e6ac7c02bc308856a89043bc0b1824b0fab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350281"
---
# <a name="inkoverlaysystemgesture-event"></a><span data-ttu-id="f1f9c-103">InkOverlay.Systemgesten-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f1f9c-103">InkOverlay.SystemGesture event</span></span>

<span data-ttu-id="f1f9c-104">Tritt auf, wenn eine System Bewegung erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f9c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1f9c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f1f9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1f9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f9c-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1f9c-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f9c-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das [**systemgesten**](inkcollector-systemgesture.md) -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**SystemGesture**](inkcollector-systemgesture.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="f1f9c-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1f9c-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f9c-110">Der Wert der System Geste.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="f1f9c-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1f9c-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f9c-112">Die x-Koordinate der Position der Bewegung.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="f1f9c-113">*J* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1f9c-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f9c-114">Die y-Koordinate der Position der Bewegung.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="f1f9c-115">*Modifizierer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1f9c-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f9c-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f1f9c-117">*Zeichen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1f9c-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f9c-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f1f9c-119">*Cursor Mode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1f9c-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f9c-120">Ein Wert, der angibt, ob sich das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt im normalen Modus oder im Radierermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="f1f9c-121">1 ist für den normalen Modus und 2 für den Radierermodus.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f9c-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1f9c-122">Return value</span></span>

<span data-ttu-id="f1f9c-123">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1f9c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1f9c-124">Remarks</span></span>

<span data-ttu-id="f1f9c-125">System Gesten sind nützlich, da Sie Informationen über das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt enthalten, das zum Erstellen der Geste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="f1f9c-126">Außerdem stellen Sie Verknüpfungen zu Kombinationen von Mausereignissen bereit und sind "kostengünstiger" Möglichkeiten zum Erkennen von Mausereignissen.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="f1f9c-127">Anstatt z. b. nach einem [**MouseUp Event**](inkcollector-mouseup.md)  /  [**MouseDown-Ereignis**](inkcollector-mousedown.md) paar von Ereignissen zu suchen, bei denen keine anderen Mausereignisse zwischen auftreten, können Sie nach der [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -oder **RightTap** -System Gesten suchen.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="f1f9c-128">Ein weiteres Beispiel: statt auf [**MouseDown**](inkcollector-mousedown.md)  /  -Ereignis [**MouseMove**](inkcollector-mousemove.md) -Ereignis Ereignisse zu lauschen und zahlreiche **MouseMove-Ereignis** Meldungen zu erhalten, können Sie die Bewegungen des [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -oder **RightDrag** -Systems überwachen, solange Sie nicht an den (x, y)-Koordinaten jeder Position der Maus interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="f1f9c-129">Dies ermöglicht es Ihnen, anstelle von zahlreichen **mougmove-Ereignis** Nachrichten nur eine Nachricht zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="f1f9c-130">Eine Liste der spezifischen System Gesten finden Sie unter der [**inksystemgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="f1f9c-131">Weitere Informationen zu System Gesten finden Sie unter [Verwenden von Gesten](using-gestures.md) und [Befehlseingaben auf dem Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1f9c-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="f1f9c-132">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icesystemgesten definiert.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f9c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1f9c-133">Requirements</span></span>



| <span data-ttu-id="f1f9c-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1f9c-134">Requirement</span></span> | <span data-ttu-id="f1f9c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f1f9c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f9c-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1f9c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f1f9c-137">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1f9c-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f1f9c-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1f9c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f1f9c-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f1f9c-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f1f9c-140">Header</span><span class="sxs-lookup"><span data-stu-id="f1f9c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1f9c-141"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f1f9c-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f1f9c-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f1f9c-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1f9c-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1f9c-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f1f9c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1f9c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f9c-145">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f1f9c-145">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="f1f9c-146">**Inksystemgesten-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="f1f9c-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="f1f9c-147">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f1f9c-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="f1f9c-148">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="f1f9c-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="f1f9c-149">Stift Eingabe, frei Hand Eingabe und-Erkennung</span><span class="sxs-lookup"><span data-stu-id="f1f9c-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="f1f9c-150">[Befehls Eingabe auf dem Tablet PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1f9c-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

