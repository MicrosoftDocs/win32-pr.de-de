---
title: Zeigerflags
description: Werte, die im Feld pointerflags der POINTER_INFO Struktur angezeigt werden können.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742329"
---
# <a name="pointer-flags"></a><span data-ttu-id="e4437-103">Zeigerflags</span><span class="sxs-lookup"><span data-stu-id="e4437-103">Pointer Flags</span></span>

<span data-ttu-id="e4437-104">Werte, die im Feld **pointerflags** der [**POINTER_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="e4437-104">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="e4437-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="e4437-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4437-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-107">Standard</span><span class="sxs-lookup"><span data-stu-id="e4437-107">Default</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="e4437-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4437-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="e4437-110">Gibt den Eingang eines neuen Zeigers an.</span><span class="sxs-lookup"><span data-stu-id="e4437-110">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="e4437-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-112">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e4437-112">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="e4437-113">Gibt an, dass dieser Zeiger weiterhin vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e4437-113">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="e4437-114">Wenn dieses Flag nicht festgelegt ist, gibt es an, dass der Zeiger den linken Erkennungsbereich aufweist.</span><span class="sxs-lookup"><span data-stu-id="e4437-114">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="e4437-115">Dieses Flag wird in der Regel nicht festgelegt, wenn ein Mauszeiger den Erkennungsbereich verlässt (**POINTER_FLAG_UPDATE** festgelegt ist) oder wenn ein Zeiger im Kontakt mit einer Fenster Oberfläche den Erkennungsbereich verlässt (**POINTER_FLAG_UP** ist festgelegt).</span><span class="sxs-lookup"><span data-stu-id="e4437-115">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="e4437-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-117">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e4437-117">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="e4437-118">Gibt an, dass sich dieser Zeiger in Verbindung mit der Digitalisierungs Oberfläche befindet.</span><span class="sxs-lookup"><span data-stu-id="e4437-118">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="e4437-119">Wenn dieses Flag nicht festgelegt ist, gibt es einen Mauszeiger an.</span><span class="sxs-lookup"><span data-stu-id="e4437-119">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e4437-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-121">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4437-121">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="e4437-122">Gibt eine primäre Aktion an, analog zu einer linken Maustaste.</span><span class="sxs-lookup"><span data-stu-id="e4437-122">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="e4437-123">Für einen Fingerabdruck wird dieses Flag festgelegt, wenn es sich im Kontakt mit der Digitalisierungs Oberfläche befindet.</span><span class="sxs-lookup"><span data-stu-id="e4437-123">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="e4437-124">Bei einem Stift Zeiger wird dieses Flag festgelegt, wenn es sich auf der digitalisiereroberfläche befindet und keine Schaltflächen gedrückt sind.</span><span class="sxs-lookup"><span data-stu-id="e4437-124">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="e4437-125">Ein Mauszeiger hat dieses Flag festgelegt, wenn die linke Maustaste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="e4437-125">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e4437-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-127">0x00000020</span><span class="sxs-lookup"><span data-stu-id="e4437-127">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="e4437-128">Gibt eine sekundäre Aktion analog zu einer rechten Maustaste an.</span><span class="sxs-lookup"><span data-stu-id="e4437-128">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="e4437-129">Ein Fingerabdruck verwendet dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="e4437-129">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e4437-130">Bei einem Stift Zeiger wird dieses Flag festgelegt, wenn es sich im Kontakt mit der Digitalisierungs Oberfläche befindet, auf die die Stift Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="e4437-130">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="e4437-131">Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die Rechte Maustaste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="e4437-131">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e4437-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-133">0x00000040</span><span class="sxs-lookup"><span data-stu-id="e4437-133">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="e4437-134">Analog zu einem Mausrad-Button.</span><span class="sxs-lookup"><span data-stu-id="e4437-134">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="e4437-135">Ein Fingerabdruck verwendet dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="e4437-135">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e4437-136">Dieses Flag wird von einem Stift Zeiger nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4437-136">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e4437-137">Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die Maustaste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="e4437-137">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e4437-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="e4437-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="e4437-140">Analog zu einer ersten erweiterten mouseschaltfläche (XButton1).</span><span class="sxs-lookup"><span data-stu-id="e4437-140">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="e4437-141">Ein Fingerabdruck verwendet dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="e4437-141">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e4437-142">Dieses Flag wird von einem Stift Zeiger nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4437-142">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e4437-143">Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die erste erweiterte Maus (XButton1) gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="e4437-143">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e4437-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-145">0x00000100</span><span class="sxs-lookup"><span data-stu-id="e4437-145">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="e4437-146">Analog zu einer zweiten erweiterten mouseschaltfläche (XButton2).</span><span class="sxs-lookup"><span data-stu-id="e4437-146">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="e4437-147">Ein Fingerabdruck verwendet dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="e4437-147">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e4437-148">Dieses Flag wird von einem Stift Zeiger nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4437-148">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e4437-149">Ein Mauszeiger hat dieses Flag festgelegt, wenn die zweite erweiterte Maus (XButton2) gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="e4437-149">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="e4437-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="e4437-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-152">Gibt an, dass dieser Zeiger als primärer Zeiger festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="e4437-152">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="e4437-153">Ein primärer Zeiger ist ein einzelner Zeiger, der über diejenigen hinaus Aktionen ausführen kann, die für nicht-primär Zeiger verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e4437-153">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="e4437-154">Wenn ein primärer Zeiger z. b. einen Kontakt mit einer Fenster-Oberfläche herstellt, kann er das Fenster aktivieren, indem er eine [**WM_POINTERACTIVATE**](wm-pointeractivate.md) Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="e4437-154">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a [**WM_POINTERACTIVATE**](wm-pointeractivate.md) message.</span></span>

<span data-ttu-id="e4437-155">Der primäre Zeiger wird von allen aktuellen Benutzerinteraktionen im System (Maus, Toucheingabe, Stift usw.) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e4437-155">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="e4437-156">Daher ist der primäre Zeiger möglicherweise nicht mit Ihrer APP verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e4437-156">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="e4437-157">Der erste Kontakt in einer Multitouch-Interaktion ist als primärer Zeiger festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e4437-157">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="e4437-158">Wenn ein primärer Zeiger identifiziert wird, müssen alle Kontakte angehoben werden, bevor ein neuer Kontakt als primärer Zeiger identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4437-158">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="e4437-159">Für apps, die keine Zeiger Eingaben verarbeiten, werden nur die Ereignisse des primären Zeigers zu Mausereignissen herauf gestuft.</span><span class="sxs-lookup"><span data-stu-id="e4437-159">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="e4437-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-161">0x000004000</span><span class="sxs-lookup"><span data-stu-id="e4437-161">0x000004000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-162">Vertrauen ist ein Vorschlag vom Quellgerät, ob der Zeiger eine beabsichtigte oder versehentliche Interaktion darstellt. Dies ist besonders relevant für PT_TOUCH Zeiger, bei denen eine versehentliche Interaktion (z. b. mit der Handtasche) Eingaben auslöst.</span><span class="sxs-lookup"><span data-stu-id="e4437-162">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="e4437-163">Das vorhanden sein dieses Flags gibt an, dass das Quellgerät sehr sicher ist, dass diese Eingabe Teil einer beabsichtigten Interaktion ist.</span><span class="sxs-lookup"><span data-stu-id="e4437-163">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="e4437-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-165">0x000008000</span><span class="sxs-lookup"><span data-stu-id="e4437-165">0x000008000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-166">Gibt an, dass der Zeiger nicht ordnungsgemäß abbricht, z. b. wenn das System ungültige Eingaben für den Zeiger empfängt oder wenn ein Gerät mit aktiven Zeigern abrupt abweicht.</span><span class="sxs-lookup"><span data-stu-id="e4437-166">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="e4437-167">Wenn sich die Anwendung, die die Eingabe empfängt, an einer anderen Position befindet, sollte Sie die Interaktion als nicht abgeschlossen behandeln und alle Auswirkungen des betreffenden Zeigers umkehren.</span><span class="sxs-lookup"><span data-stu-id="e4437-167">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span><span class="sxs-lookup"><span data-stu-id="e4437-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-169">0x00010000</span><span class="sxs-lookup"><span data-stu-id="e4437-169">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-170">Gibt an, dass dieser Zeiger in den Zustand "nach unten" übergeht. Das heißt, es wurde eine Verbindung mit der digitalisiereroberfläche hergestellt.</span><span class="sxs-lookup"><span data-stu-id="e4437-170">Indicates that this pointer transitioned to a down state; that is, it made contact with the digitizer surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span><span class="sxs-lookup"><span data-stu-id="e4437-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-172">0x00020000</span><span class="sxs-lookup"><span data-stu-id="e4437-172">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-173">Gibt an, dass es sich hierbei um ein einfaches Update handelt, das keine Zeiger Zustandsänderungen einschließt.</span><span class="sxs-lookup"><span data-stu-id="e4437-173">Indicates that this is a simple update that does not include pointer state changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span><span class="sxs-lookup"><span data-stu-id="e4437-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-175">0x00040000</span><span class="sxs-lookup"><span data-stu-id="e4437-175">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-176">Gibt an, dass dieser Zeiger in den Zustand "up" übergeht. Das heißt, der Kontakt mit der digitalisiereroberfläche wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="e4437-176">Indicates that this pointer transitioned to an up state; that is, contact with the digitizer surface ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span><span class="sxs-lookup"><span data-stu-id="e4437-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-178">0x00080000</span><span class="sxs-lookup"><span data-stu-id="e4437-178">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-179">Gibt Eingaben an, die einem zeigerrad zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e4437-179">Indicates input associated with a pointer wheel.</span></span> <span data-ttu-id="e4437-180">Bei Maus Zeigern entspricht dies der Aktion des Mausrades ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="e4437-180">For mouse pointers, this is equivalent to the action of the mouse scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span><span class="sxs-lookup"><span data-stu-id="e4437-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="e4437-182">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-183">Gibt Eingaben an, die einem Zeiger-h-Rad zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e4437-183">Indicates input associated with a pointer h-wheel.</span></span> <span data-ttu-id="e4437-184">Bei Maus Zeigern entspricht dies der Aktion des horizontalen Mausrads ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="e4437-184">For mouse pointers, this is equivalent to the action of the mouse horizontal scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span><span class="sxs-lookup"><span data-stu-id="e4437-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-186">0x00200000</span><span class="sxs-lookup"><span data-stu-id="e4437-186">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-187">Gibt an, dass dieser Zeiger von einem anderen Element (zugeordnet) aufgezeichnet und das ursprüngliche Element die Erfassung verloren hat (siehe [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span><span class="sxs-lookup"><span data-stu-id="e4437-187">Indicates that this pointer was captured by (associated with) another element and the original element has lost capture (see [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4437-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="e4437-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4437-189">0x00400000</span><span class="sxs-lookup"><span data-stu-id="e4437-189">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="e4437-190">Gibt an, dass dieser Zeiger über eine zugeordnete Transformation verfügt.</span><span class="sxs-lookup"><span data-stu-id="e4437-190">Indicates that this pointer has an associated transform.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4437-191">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4437-191">Remarks</span></span>

<span data-ttu-id="e4437-192">XButton1 und XButton2 sind zusätzliche Schaltflächen, die auf vielen Maus Geräten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4437-192">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="e4437-193">Sie geben dieselben Daten zurück wie Standard-Maustasten.</span><span class="sxs-lookup"><span data-stu-id="e4437-193">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4437-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4437-194">Requirements</span></span>



| <span data-ttu-id="e4437-195">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4437-195">Requirement</span></span> | <span data-ttu-id="e4437-196">Wert</span><span class="sxs-lookup"><span data-stu-id="e4437-196">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e4437-197">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4437-197">Minimum supported client</span></span><br/> | <span data-ttu-id="e4437-198">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4437-198">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e4437-199">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4437-199">Minimum supported server</span></span><br/> | <span data-ttu-id="e4437-200">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4437-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e4437-201">Header</span><span class="sxs-lookup"><span data-stu-id="e4437-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4437-202"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4437-202"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4437-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4437-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4437-204">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e4437-204">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="e4437-205">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="e4437-205">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="e4437-206">**POINTER_BUTTON_CHANGE_TYPE**</span><span class="sxs-lookup"><span data-stu-id="e4437-206">**POINTER_BUTTON_CHANGE_TYPE**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

