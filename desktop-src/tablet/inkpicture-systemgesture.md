---
description: Tritt auf, wenn eine System Bewegung erkannt wird.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.Systemgesten-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918198e4d18a854bb4238ce9d878dc70ab1f2f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352344"
---
# <a name="inkpicturesystemgesture-event"></a><span data-ttu-id="754a7-103">InkPicture.Systemgesten-Ereignis</span><span class="sxs-lookup"><span data-stu-id="754a7-103">InkPicture.SystemGesture event</span></span>

<span data-ttu-id="754a7-104">Tritt auf, wenn eine System Bewegung erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="754a7-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="754a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="754a7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="754a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="754a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="754a7-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="754a7-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754a7-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **systemgesten** -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="754a7-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="754a7-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="754a7-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754a7-110">Der Wert der System Geste.</span><span class="sxs-lookup"><span data-stu-id="754a7-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="754a7-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="754a7-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754a7-112">Die x-Koordinate der Position der Bewegung.</span><span class="sxs-lookup"><span data-stu-id="754a7-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="754a7-113">*J* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="754a7-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754a7-114">Die y-Koordinate der Position der Bewegung.</span><span class="sxs-lookup"><span data-stu-id="754a7-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="754a7-115">*Modifizierer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="754a7-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754a7-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="754a7-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="754a7-117">*Zeichen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="754a7-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754a7-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="754a7-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="754a7-119">*Cursor Mode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="754a7-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754a7-120">Ein Wert, der angibt, ob sich das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt im normalen Modus oder im Radierermodus befindet.</span><span class="sxs-lookup"><span data-stu-id="754a7-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="754a7-121">1 ist für den normalen Modus und 2 für den Radierermodus.</span><span class="sxs-lookup"><span data-stu-id="754a7-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="754a7-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="754a7-122">Return value</span></span>

<span data-ttu-id="754a7-123">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="754a7-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="754a7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="754a7-124">Remarks</span></span>

<span data-ttu-id="754a7-125">System Gesten enthalten Informationen über das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das zum Erstellen der Geste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="754a7-125">System gestures give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="754a7-126">Außerdem stellen Sie Verknüpfungen zu Kombinationen von Mausereignissen bereit und bieten Möglichkeiten, Mausereignisse zu erkennen, die weniger Auswirkungen auf die Leistung haben.</span><span class="sxs-lookup"><span data-stu-id="754a7-126">They also provide shortcuts to combinations of mouse events and are ways to detect mouse events with less impact on performance.</span></span>

<span data-ttu-id="754a7-127">Anstatt z. b. nach einem [**MouseUp-Ereignis \[ \]**](inkpicture-mouseup.md)InkPicture-Steuer / [**\[ \]**](inkpicture-mousedown.md) Element paar-Ereignisse zu suchen, bei denen keine anderen Mausereignisse dazwischen auftreten, können Sie nach der TAP-oder RightTap-System Geste suchen.</span><span class="sxs-lookup"><span data-stu-id="754a7-127">For example, instead of looking for a [**MouseUp Event \[InkPicture Control\]**](inkpicture-mouseup.md)/[**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the Tap or RightTap system gestures.</span></span>

<span data-ttu-id="754a7-128">Ein weiteres Beispiel: anstatt das [**MouseDown \[ \]**](inkpicture-mousedown.md)-Ereignis InkPicture-Steuerelement / [**\[ \] MouseMove-Ereignis InkPicture**](inkpicture-mousemove.md) zu überwachen und zahlreiche **MouseMove- \[ Ereignisbild-Steuer \]** Elemente zu erhalten, können Sie die System Gesten von Drag oder RightDrag ansehen, solange Sie nicht an den (x, y)-Koordinaten jeder Position der Maus interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="754a7-128">As another example, instead of listening for [**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md)/[**MouseMove Event \[InkPicture Control\]**](inkpicture-mousemove.md) events and getting numerous **MouseMove Event \[InkPicture Control\]** messages, you can watch for the Drag or RightDrag system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="754a7-129">Dies ermöglicht es Ihnen, anstelle von zahlreichen **mousmove- \[ ereignissteuerungsmeldungen \]** nur eine Nachricht zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="754a7-129">This allows you to receive only one message instead of numerous **MouseMove Event \[InkPicture Control\]** messages.</span></span>

<span data-ttu-id="754a7-130">Eine Liste der spezifischen System Gesten finden Sie unter der [**inksystemgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="754a7-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="754a7-131">Weitere Informationen zu System Gesten finden Sie unter [Verwenden von Gesten](using-gestures.md) und [Befehlseingaben auf dem Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="754a7-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="754a7-132">Diese Ereignismethode wird in den Schnittstellen **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icesystemgesten definiert.</span><span class="sxs-lookup"><span data-stu-id="754a7-132">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="754a7-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="754a7-133">Requirements</span></span>



| <span data-ttu-id="754a7-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="754a7-134">Requirement</span></span> | <span data-ttu-id="754a7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="754a7-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="754a7-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="754a7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="754a7-137">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="754a7-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="754a7-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="754a7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="754a7-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="754a7-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="754a7-140">Header</span><span class="sxs-lookup"><span data-stu-id="754a7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="754a7-141"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="754a7-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="754a7-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="754a7-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="754a7-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="754a7-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="754a7-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="754a7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="754a7-145">InkPicture</span><span class="sxs-lookup"><span data-stu-id="754a7-145">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="754a7-146">**Inksystemgesten-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="754a7-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="754a7-147">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="754a7-147">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

