---
description: 'InkPicture.SystemGesture-Ereignis: Tritt auf, wenn eine Systemgeste erkannt wird.'
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.SystemGesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cde11b73b6b0d3861a79538a7f9ee19487b6384
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113688"
---
# <a name="inkpicturesystemgesture-event"></a><span data-ttu-id="6d72a-103">InkPicture.SystemGesture-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6d72a-103">InkPicture.SystemGesture event</span></span>

<span data-ttu-id="6d72a-104">Tritt ein, wenn eine Systemgeste erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="6d72a-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d72a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d72a-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="6d72a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d72a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d72a-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6d72a-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d72a-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **SystemGesture-Ereignis generiert** hat.</span><span class="sxs-lookup"><span data-stu-id="6d72a-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="6d72a-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d72a-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d72a-110">Der Wert der Systemgeste.</span><span class="sxs-lookup"><span data-stu-id="6d72a-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="6d72a-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d72a-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d72a-112">Die x-Koordinate der Position der Geste.</span><span class="sxs-lookup"><span data-stu-id="6d72a-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="6d72a-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d72a-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d72a-114">Die y-Koordinate der Position der Geste.</span><span class="sxs-lookup"><span data-stu-id="6d72a-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="6d72a-115">*Modifizierer* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6d72a-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d72a-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6d72a-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6d72a-117">*Zeichen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6d72a-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d72a-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="6d72a-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6d72a-119">*CursorMode* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6d72a-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d72a-120">Ein -Wert, der angibt, ob sich [**das IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) im normalen Modus oder Radierermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="6d72a-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="6d72a-121">1 ist für den normalen Modus und 2 für radierermodus.</span><span class="sxs-lookup"><span data-stu-id="6d72a-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d72a-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d72a-122">Return value</span></span>

<span data-ttu-id="6d72a-123">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6d72a-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d72a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d72a-124">Remarks</span></span>

<span data-ttu-id="6d72a-125">Systemgesten enthalten Informationen zum [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das zum Erstellen der Geste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d72a-125">System gestures give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="6d72a-126">Sie bieten auch Verknüpfungen zu Kombinationen von Mausereignissen und sind Möglichkeiten, Mausereignisse mit geringeren Auswirkungen auf die Leistung zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="6d72a-126">They also provide shortcuts to combinations of mouse events and are ways to detect mouse events with less impact on performance.</span></span>

<span data-ttu-id="6d72a-127">Anstatt beispielsweise nach einem [**MouseUp Event \[ InkPicture Control \]**](inkpicture-mouseup.md) / [**MouseDown Event \[ InkPicture Control-Paar \]**](inkpicture-mousedown.md) von Ereignissen zu suchen, bei dem keine anderen Mausereignisse dazwischen auftreten, können Sie nach den Systemgesten Tap oder RightTap suchen.</span><span class="sxs-lookup"><span data-stu-id="6d72a-127">For example, instead of looking for a [**MouseUp Event \[InkPicture Control\]**](inkpicture-mouseup.md)/[**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the Tap or RightTap system gestures.</span></span>

<span data-ttu-id="6d72a-128">Ein weiteres Beispiel: Anstatt auf [**MouseDown Event \[ InkPicture Control \]**](inkpicture-mousedown.md) / [**MouseMove Event \[ InkPicture \] Control-Ereignisse**](inkpicture-mousemove.md) zu lauschen und zahlreiche **MouseMove Event \[ InkPicture Control-Meldungen \]** zu erhalten, können Sie auf die Drag- oder RightDrag-Systemgesten achten, solange Sie nicht an den (x, y) Koordinaten jeder Position der Maus interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="6d72a-128">As another example, instead of listening for [**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md)/[**MouseMove Event \[InkPicture Control\]**](inkpicture-mousemove.md) events and getting numerous **MouseMove Event \[InkPicture Control\]** messages, you can watch for the Drag or RightDrag system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="6d72a-129">Dadurch können Sie anstelle zahlreicher **MouseMove Event \[ InkPicture \] Control-Meldungen** nur eine Nachricht empfangen.</span><span class="sxs-lookup"><span data-stu-id="6d72a-129">This allows you to receive only one message instead of numerous **MouseMove Event \[InkPicture Control\]** messages.</span></span>

<span data-ttu-id="6d72a-130">Eine Liste der spezifischen Systemgesten finden Sie unter [**InkSystemGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="6d72a-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="6d72a-131">Weitere Informationen zu Systemgesten finden Sie unter Verwenden von Gesten und [Befehlseingaben auf dem Tablet PC.](/previous-versions//dd314533(v=vs.85)) [](using-gestures.md)</span><span class="sxs-lookup"><span data-stu-id="6d72a-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="6d72a-132">Diese Ereignismethode wird in den Dispatch-Only-Schnittstellen **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICESystemGesture definiert.</span><span class="sxs-lookup"><span data-stu-id="6d72a-132">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d72a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d72a-133">Requirements</span></span>



| <span data-ttu-id="6d72a-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d72a-134">Requirement</span></span> | <span data-ttu-id="6d72a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="6d72a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d72a-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d72a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6d72a-137">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6d72a-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6d72a-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d72a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6d72a-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6d72a-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6d72a-140">Header</span><span class="sxs-lookup"><span data-stu-id="6d72a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d72a-141"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="6d72a-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6d72a-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d72a-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d72a-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d72a-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6d72a-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d72a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d72a-145">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="6d72a-145">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="6d72a-146">**InkSystemGesture-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6d72a-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="6d72a-147">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="6d72a-147">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

