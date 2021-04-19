---
title: Zeigernachrichtenflags
description: Werte, die in verschiedenen Zeiger Makros verwendet werden (siehe Makros).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346736"
---
# <a name="pointer-message-flags"></a><span data-ttu-id="becd5-103">Zeigernachrichtenflags</span><span class="sxs-lookup"><span data-stu-id="becd5-103">Pointer Message Flags</span></span>

<span data-ttu-id="becd5-104">Werte, die in verschiedenen Zeiger Makros verwendet werden (siehe [Makros](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="becd5-104">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span>

<dl> <dt>

<span data-ttu-id="becd5-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="becd5-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="becd5-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="becd5-107">Gibt den Eingang eines neuen Zeigers an.</span><span class="sxs-lookup"><span data-stu-id="becd5-107">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="becd5-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="becd5-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="becd5-110">Gibt an, dass dieser Zeiger weiterhin vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="becd5-110">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="becd5-111">Wenn dieses Flag nicht festgelegt ist, gibt es an, dass der Zeiger den linken Erkennungsbereich aufweist.</span><span class="sxs-lookup"><span data-stu-id="becd5-111">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="becd5-112">Dieses Flag wird in der Regel nicht festgelegt, wenn ein Mauszeiger den Erkennungsbereich verlässt (**POINTER_FLAG_UPDATE** festgelegt ist) oder wenn ein Zeiger im Kontakt mit einer Fenster Oberfläche den Erkennungsbereich verlässt (**POINTER_FLAG_UP** ist festgelegt).</span><span class="sxs-lookup"><span data-stu-id="becd5-112">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="becd5-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="becd5-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="becd5-115">Gibt an, dass sich dieser Zeiger in Verbindung mit der Digitalisierungs Oberfläche befindet.</span><span class="sxs-lookup"><span data-stu-id="becd5-115">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="becd5-116">Wenn dieses Flag nicht festgelegt ist, gibt es einen Mauszeiger an.</span><span class="sxs-lookup"><span data-stu-id="becd5-116">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="becd5-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-118">0x00000010</span><span class="sxs-lookup"><span data-stu-id="becd5-118">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="becd5-119">Gibt eine primäre Aktion an, analog zu einer linken Maustaste.</span><span class="sxs-lookup"><span data-stu-id="becd5-119">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="becd5-120">Für einen Fingerabdruck wird dieses Flag festgelegt, wenn es sich im Kontakt mit der Digitalisierungs Oberfläche befindet.</span><span class="sxs-lookup"><span data-stu-id="becd5-120">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="becd5-121">Bei einem Stift Zeiger wird dieses Flag festgelegt, wenn es sich auf der digitalisiereroberfläche befindet und keine Schaltflächen gedrückt sind.</span><span class="sxs-lookup"><span data-stu-id="becd5-121">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="becd5-122">Ein Mauszeiger hat dieses Flag festgelegt, wenn die linke Maustaste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="becd5-122">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="becd5-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-124">0x00000020</span><span class="sxs-lookup"><span data-stu-id="becd5-124">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="becd5-125">Gibt eine sekundäre Aktion analog zu einer rechten Maustaste an.</span><span class="sxs-lookup"><span data-stu-id="becd5-125">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="becd5-126">Ein Fingerabdruck verwendet dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="becd5-126">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="becd5-127">Bei einem Stift Zeiger wird dieses Flag festgelegt, wenn es sich im Kontakt mit der Digitalisierungs Oberfläche befindet, auf die die Stift Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="becd5-127">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="becd5-128">Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die Rechte Maustaste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="becd5-128">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="becd5-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-130">0x00000040</span><span class="sxs-lookup"><span data-stu-id="becd5-130">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="becd5-131">Analog zu einem Mausrad-Button.</span><span class="sxs-lookup"><span data-stu-id="becd5-131">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="becd5-132">Ein Fingerabdruck verwendet dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="becd5-132">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="becd5-133">Dieses Flag wird von einem Stift Zeiger nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="becd5-133">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="becd5-134">Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die Maustaste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="becd5-134">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="becd5-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-136">0x00000080</span><span class="sxs-lookup"><span data-stu-id="becd5-136">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="becd5-137">Analog zu einer ersten erweiterten mouseschaltfläche (XButton1).</span><span class="sxs-lookup"><span data-stu-id="becd5-137">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="becd5-138">Ein Fingerabdruck verwendet dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="becd5-138">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="becd5-139">Dieses Flag wird von einem Stift Zeiger nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="becd5-139">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="becd5-140">Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die erste erweiterte Maus (XButton1) gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="becd5-140">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="becd5-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="becd5-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="becd5-143">Analog zu einer zweiten erweiterten mouseschaltfläche (XButton2).</span><span class="sxs-lookup"><span data-stu-id="becd5-143">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="becd5-144">Ein Fingerabdruck verwendet dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="becd5-144">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="becd5-145">Dieses Flag wird von einem Stift Zeiger nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="becd5-145">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="becd5-146">Ein Mauszeiger hat dieses Flag festgelegt, wenn die zweite erweiterte Maus (XButton2) gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="becd5-146">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="becd5-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-148">0x00002000</span><span class="sxs-lookup"><span data-stu-id="becd5-148">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="becd5-149">Gibt an, dass dieser Zeiger als primärer Zeiger festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="becd5-149">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="becd5-150">Ein primärer Zeiger ist ein einzelner Zeiger, der über diejenigen hinaus Aktionen ausführen kann, die für nicht-primär Zeiger verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="becd5-150">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="becd5-151">Wenn ein primärer Zeiger z. b. einen Kontakt mit einer Fenster-Oberfläche herstellt, kann er das Fenster aktivieren, indem er eine WM_POINTERACTIVATE Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="becd5-151">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a WM_POINTERACTIVATE message.</span></span>

<span data-ttu-id="becd5-152">Der primäre Zeiger wird von allen aktuellen Benutzerinteraktionen im System (Maus, Toucheingabe, Stift usw.) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="becd5-152">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="becd5-153">Daher ist der primäre Zeiger möglicherweise nicht mit Ihrer APP verknüpft.</span><span class="sxs-lookup"><span data-stu-id="becd5-153">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="becd5-154">Der erste Kontakt in einer Multitouch-Interaktion ist als primärer Zeiger festgelegt.</span><span class="sxs-lookup"><span data-stu-id="becd5-154">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="becd5-155">Wenn ein primärer Zeiger identifiziert wird, müssen alle Kontakte angehoben werden, bevor ein neuer Kontakt als primärer Zeiger identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="becd5-155">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="becd5-156">Für apps, die keine Zeiger Eingaben verarbeiten, werden nur die Ereignisse des primären Zeigers zu Mausereignissen herauf gestuft.</span><span class="sxs-lookup"><span data-stu-id="becd5-156">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="becd5-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-158">0x00000400</span><span class="sxs-lookup"><span data-stu-id="becd5-158">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="becd5-159">Vertrauen ist ein Vorschlag vom Quellgerät, ob der Zeiger eine beabsichtigte oder versehentliche Interaktion darstellt. Dies ist besonders relevant für PT_TOUCH Zeiger, bei denen eine versehentliche Interaktion (z. b. mit der Handtasche) Eingaben auslöst.</span><span class="sxs-lookup"><span data-stu-id="becd5-159">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="becd5-160">Das vorhanden sein dieses Flags gibt an, dass das Quellgerät sehr sicher ist, dass diese Eingabe Teil einer beabsichtigten Interaktion ist.</span><span class="sxs-lookup"><span data-stu-id="becd5-160">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="becd5-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="becd5-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="becd5-162">0x00000800</span><span class="sxs-lookup"><span data-stu-id="becd5-162">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="becd5-163">Gibt an, dass der Zeiger nicht ordnungsgemäß abbricht, z. b. wenn das System ungültige Eingaben für den Zeiger empfängt oder wenn ein Gerät mit aktiven Zeigern abrupt abweicht.</span><span class="sxs-lookup"><span data-stu-id="becd5-163">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="becd5-164">Wenn sich die Anwendung, die die Eingabe empfängt, an einer anderen Position befindet, sollte Sie die Interaktion als nicht abgeschlossen behandeln und alle Auswirkungen des betreffenden Zeigers umkehren.</span><span class="sxs-lookup"><span data-stu-id="becd5-164">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="becd5-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="becd5-165">Remarks</span></span>

<span data-ttu-id="becd5-166">XButton1 und XButton2 sind zusätzliche Schaltflächen, die auf vielen Maus Geräten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="becd5-166">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="becd5-167">Sie geben dieselben Daten zurück wie Standard-Maustasten.</span><span class="sxs-lookup"><span data-stu-id="becd5-167">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="becd5-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="becd5-168">Requirements</span></span>



| <span data-ttu-id="becd5-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="becd5-169">Requirement</span></span> | <span data-ttu-id="becd5-170">Wert</span><span class="sxs-lookup"><span data-stu-id="becd5-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="becd5-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="becd5-171">Minimum supported client</span></span><br/> | <span data-ttu-id="becd5-172">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="becd5-172">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="becd5-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="becd5-173">Minimum supported server</span></span><br/> | <span data-ttu-id="becd5-174">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="becd5-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="becd5-175">Header</span><span class="sxs-lookup"><span data-stu-id="becd5-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="becd5-176"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="becd5-176"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="becd5-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="becd5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="becd5-178">Konstanten</span><span class="sxs-lookup"><span data-stu-id="becd5-178">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="becd5-179">Makros</span><span class="sxs-lookup"><span data-stu-id="becd5-179">Macros</span></span>](macros.md)
</dt> </dl>

 

 





