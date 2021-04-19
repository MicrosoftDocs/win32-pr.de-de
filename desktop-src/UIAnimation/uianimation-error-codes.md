---
title: Fehler Codes für die Windows-Animation (Winerror. h)
description: Wenn ein Fehler auftritt, gibt die Windows-Animation einen Code als HRESULT-Wert zurück. Dieser Abschnitt enthält eine Liste der Fehlercodes, die für die Windows-Animation spezifisch sind. Eine Liste allgemeiner com-Fehlercodes finden Sie unter COM-Fehlercodes.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342424"
---
# <a name="windows-animation-error-codes"></a><span data-ttu-id="7a385-105">Fehler Codes für Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="7a385-105">Windows Animation Error Codes</span></span>

<span data-ttu-id="7a385-106">Wenn ein Fehler auftritt, gibt die Windows-Animation einen Code als **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7a385-106">If an error occurs, Windows Animation returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="7a385-107">Dieser Abschnitt enthält eine Liste der Fehlercodes, die für die Windows-Animation spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="7a385-107">This section provides a list of error codes specific to Windows Animation.</span></span> <span data-ttu-id="7a385-108">Eine Liste allgemeiner com-Fehlercodes finden Sie unter [com-Fehlercodes](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7a385-108">For a list of general COM error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7a385-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**Fehler beim Erstellen der Benutzeroberfläche. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7a385-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI\_E\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-110">0x802a0001</span><span class="sxs-lookup"><span data-stu-id="7a385-110">0x802A0001</span></span>
</dt> <dt>



<span data-ttu-id="7a385-111">Das Objekt konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a385-111">The object could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**Benutzeroberfläche \_ E \_ Herunterfahren \_ aufgerufen**</span><span class="sxs-lookup"><span data-stu-id="7a385-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI\_E\_SHUTDOWN\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-113">0x802a0002</span><span class="sxs-lookup"><span data-stu-id="7a385-113">0x802A0002</span></span>
</dt> <dt>



<span data-ttu-id="7a385-114">Die [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) -Methode wurde im Animations-Manager aufgerufen und bewirkt, dass der Animations-Manager heruntergefahren wurde und alle Animations Variablen und Storyboards, die für die Freigabe erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7a385-114">The [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method has been called on the animation manager, causing the animation manager to shut down and all the animation variables and storyboards it created to be released.</span></span>

> [!Note]  
> <span data-ttu-id="7a385-115">Nach dem [**herunter**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown)fahren können keine Methoden für ein Animations Objekt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7a385-115">No methods can be called on any animation object after [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**Benutzeroberfläche \_ E unzulässig \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7a385-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI\_E\_ILLEGAL\_REENTRANCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-117">0x802a0003</span><span class="sxs-lookup"><span data-stu-id="7a385-117">0x802A0003</span></span>
</dt> <dt>



<span data-ttu-id="7a385-118">Diese Methode kann während dieser Art von Rückruf nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7a385-118">This method cannot be called during this type of callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI- \_ E- \_ Objekt \_ versiegelt**</span><span class="sxs-lookup"><span data-stu-id="7a385-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI\_E\_OBJECT\_SEALED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-120">0x802a0004</span><span class="sxs-lookup"><span data-stu-id="7a385-120">0x802A0004</span></span>
</dt> <dt>



<span data-ttu-id="7a385-121">Dieses Objekt wurde versiegelt, sodass diese Änderung nicht mehr zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7a385-121">This object has been sealed, so this change is no longer allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**\_E/a- \_ Wert \_ nicht \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="7a385-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**UI\_E\_VALUE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-123">0x802a0005</span><span class="sxs-lookup"><span data-stu-id="7a385-123">0x802A0005</span></span>
</dt> <dt>



<span data-ttu-id="7a385-124">Der angeforderte Wert wurde nie festgelegt und kann daher nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7a385-124">The requested value has never been set, and therefore cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**\_E/a-Wert wurde \_ \_ nicht \_ bestimmt**</span><span class="sxs-lookup"><span data-stu-id="7a385-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**UI\_E\_VALUE\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-126">0x802a0006</span><span class="sxs-lookup"><span data-stu-id="7a385-126">0x802A0006</span></span>
</dt> <dt>



<span data-ttu-id="7a385-127">Der angeforderte Wert kann nicht bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="7a385-127">The requested value cannot be determined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**Benutzeroberfläche \_ E \_ ungültige \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="7a385-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI\_E\_INVALID\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-129">0x802a0007</span><span class="sxs-lookup"><span data-stu-id="7a385-129">0x802A0007</span></span>
</dt> <dt>



<span data-ttu-id="7a385-130">Ein Rückruf hat einen ungültigen Ausgabeparameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a385-130">A callback returned an invalid output parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI \_ E \_ boolescher Wert \_ erwartet**</span><span class="sxs-lookup"><span data-stu-id="7a385-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI\_E\_BOOLEAN\_EXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-132">0x802a0008</span><span class="sxs-lookup"><span data-stu-id="7a385-132">0x802A0008</span></span>
</dt> <dt>



<span data-ttu-id="7a385-133">Ein Rückruf hat einen anderen Erfolgs Code als s "OK" oder "false" zurückgegeben \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7a385-133">A callback returned a success code other than S\_OK or S\_FALSE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**Benutzeroberfläche \_ E, \_ anderer \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="7a385-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI\_E\_DIFFERENT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-135">0x802a0009</span><span class="sxs-lookup"><span data-stu-id="7a385-135">0x802A0009</span></span>
</dt> <dt>



<span data-ttu-id="7a385-136">Ein Parameter, dessen Besitzer dieses-Objekt sein sollte, ist im Besitz eines anderen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7a385-136">A parameter that should be owned by this object is owned by a different object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_mehrdeutige UI E- \_ \_ Match**</span><span class="sxs-lookup"><span data-stu-id="7a385-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI\_E\_AMBIGUOUS\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-138">0x802a000a</span><span class="sxs-lookup"><span data-stu-id="7a385-138">0x802A000A</span></span>
</dt> <dt>



<span data-ttu-id="7a385-139">Es wurden mehrere Elemente mit den Suchkriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a385-139">More than one item matched the search criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI \_ E \_ FP- \_ Überlauf**</span><span class="sxs-lookup"><span data-stu-id="7a385-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI\_E\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-141">0x802a000b</span><span class="sxs-lookup"><span data-stu-id="7a385-141">0x802A000B</span></span>
</dt> <dt>



<span data-ttu-id="7a385-142">Ein Gleit Komma Überlauf ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7a385-142">A floating-point overflow occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI \_ E \_ falscher \_ Thread**</span><span class="sxs-lookup"><span data-stu-id="7a385-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI\_E\_WRONG\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-144">0x802a000c</span><span class="sxs-lookup"><span data-stu-id="7a385-144">0x802A000C</span></span>
</dt> <dt>



<span data-ttu-id="7a385-145">Diese Methode kann nur von dem Thread aufgerufen werden, der das Objekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="7a385-145">This method can only be called from the thread that created the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI \_ E \_ Storyboard \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="7a385-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI\_E\_STORYBOARD\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-147">0x802a0101</span><span class="sxs-lookup"><span data-stu-id="7a385-147">0x802A0101</span></span>
</dt> <dt>



<span data-ttu-id="7a385-148">Das Storyboard befindet sich zurzeit im Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="7a385-148">The storyboard is currently in the schedule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI \_ E \_ Storyboard wird \_ nicht \_ abgespielt**</span><span class="sxs-lookup"><span data-stu-id="7a385-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI\_E\_STORYBOARD\_NOT\_PLAYING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-150">0x802a0102</span><span class="sxs-lookup"><span data-stu-id="7a385-150">0x802A0102</span></span>
</dt> <dt>



<span data-ttu-id="7a385-151">Das Storyboard wird nicht abgespielt.</span><span class="sxs-lookup"><span data-stu-id="7a385-151">The storyboard is not playing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI \_ E \_ \_ Keyframe \_ nach \_ Ende starten**</span><span class="sxs-lookup"><span data-stu-id="7a385-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI\_E\_START\_KEYFRAME\_AFTER\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-153">0x802a0103</span><span class="sxs-lookup"><span data-stu-id="7a385-153">0x802A0103</span></span>
</dt> <dt>



<span data-ttu-id="7a385-154">Der Keyframe "Start" kann nach dem endend-Keyframe auftreten.</span><span class="sxs-lookup"><span data-stu-id="7a385-154">The start keyframe might occur after the end keyframe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**E-End-Keyframe der Benutzeroberfläche \_ \_ \_ \_ nicht \_ bestimmt**</span><span class="sxs-lookup"><span data-stu-id="7a385-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI\_E\_END\_KEYFRAME\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-156">0x802a0104</span><span class="sxs-lookup"><span data-stu-id="7a385-156">0x802A0104</span></span>
</dt> <dt>



<span data-ttu-id="7a385-157">Es ist möglicherweise nicht möglich, die Endzeit des Keyframes zu ermitteln, wenn der Start-Keyframe erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="7a385-157">It might not be possible to determine the end keyframe time when the start keyframe is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI- \_ E- \_ Schleifen \_ überlappend**</span><span class="sxs-lookup"><span data-stu-id="7a385-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI\_E\_LOOPS\_OVERLAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-159">0x802a0105</span><span class="sxs-lookup"><span data-stu-id="7a385-159">0x802A0105</span></span>
</dt> <dt>



<span data-ttu-id="7a385-160">Zwei wiederholte Teile eines Storyboards können sich überlappen.</span><span class="sxs-lookup"><span data-stu-id="7a385-160">Two repeated portions of a storyboard might overlap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**UI- \_ E- \_ Übergang \_ \_ wird bereits verwendet**</span><span class="sxs-lookup"><span data-stu-id="7a385-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**UI\_E\_TRANSITION\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-162">0x802a0106</span><span class="sxs-lookup"><span data-stu-id="7a385-162">0x802A0106</span></span>
</dt> <dt>



<span data-ttu-id="7a385-163">Der Übergang wurde bereits einem anderen Storyboard hinzugefügt oder wurde einem Storyboard hinzugefügt, das die Wiedergabe abgeschlossen hat und freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7a385-163">The transition has already been added to a different storyboard or has been added to a storyboard that has finished playing and been released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI- \_ E- \_ Übergang \_ nicht \_ im \_ Storyboard**</span><span class="sxs-lookup"><span data-stu-id="7a385-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI\_E\_TRANSITION\_NOT\_IN\_STORYBOARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-165">0x802a0107</span><span class="sxs-lookup"><span data-stu-id="7a385-165">0x802A0107</span></span>
</dt> <dt>



<span data-ttu-id="7a385-166">Der Übergang wurde keinem Storyboard hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7a385-166">The transition has not been added to any storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**Übertragung der UI \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7a385-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI\_E\_TRANSITION\_ECLIPSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-168">0x802a0108</span><span class="sxs-lookup"><span data-stu-id="7a385-168">0x802A0108</span></span>
</dt> <dt>



<span data-ttu-id="7a385-169">Der Übergang könnte den Anfang eines anderen Übergangs im Storyboard in Eclipse übertragen.</span><span class="sxs-lookup"><span data-stu-id="7a385-169">The transition might eclipse the beginning of another transition in the storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI \_ E \_ Zeit \_ vor dem \_ letzten \_ Update**</span><span class="sxs-lookup"><span data-stu-id="7a385-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI\_E\_TIME\_BEFORE\_LAST\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-171">0x802a0109</span><span class="sxs-lookup"><span data-stu-id="7a385-171">0x802A0109</span></span>
</dt> <dt>



<span data-ttu-id="7a385-172">Die angegebene Zeit ist älter als die Zeit, die an das letzte Update weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7a385-172">The specified time is earlier than the time passed to the last update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a385-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI- \_ E-Timer-Client ist \_ \_ \_ bereits \_ verbunden**</span><span class="sxs-lookup"><span data-stu-id="7a385-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI\_E\_TIMER\_CLIENT\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a385-174">0x802a010a</span><span class="sxs-lookup"><span data-stu-id="7a385-174">0x802A010A</span></span>
</dt> <dt>



<span data-ttu-id="7a385-175">Dieser Client ist bereits mit einem Timer verbunden.</span><span class="sxs-lookup"><span data-stu-id="7a385-175">This client is already connected to a timer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a385-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a385-176">Requirements</span></span>



| <span data-ttu-id="7a385-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a385-177">Requirement</span></span> | <span data-ttu-id="7a385-178">Wert</span><span class="sxs-lookup"><span data-stu-id="7a385-178">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a385-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a385-179">Minimum supported client</span></span><br/> | <span data-ttu-id="7a385-180">Windows 7, Windows Vista und Platt Form Update für Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a385-180">Windows 7, Windows Vista and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7a385-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a385-181">Minimum supported server</span></span><br/> | <span data-ttu-id="7a385-182">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a385-182">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7a385-183">Header</span><span class="sxs-lookup"><span data-stu-id="7a385-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a385-184"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a385-184"><dt>Winerror.h</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="7a385-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a385-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a385-186">Referenz zur Windows-Animation</span><span class="sxs-lookup"><span data-stu-id="7a385-186">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

