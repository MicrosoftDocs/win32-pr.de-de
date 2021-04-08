---
title: Monitor Befehl
description: Der Monitor-Befehl gibt die Präsentations Quelle an. (Die Standard Präsentations Quelle ist der Arbeitsbereich.) Wenn Sie die Präsentations Quelle wechseln, werden alle Audio-und Videostreams in der Quelle gewechselt. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- Monitor Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741425"
---
# <a name="monitor-command"></a><span data-ttu-id="33b1e-106">Monitor Befehl</span><span class="sxs-lookup"><span data-stu-id="33b1e-106">monitor command</span></span>

<span data-ttu-id="33b1e-107">Der Monitor-Befehl gibt die Präsentations Quelle an.</span><span class="sxs-lookup"><span data-stu-id="33b1e-107">The monitor command specifies the presentation source.</span></span> <span data-ttu-id="33b1e-108">(Die Standard Präsentations Quelle ist der Arbeitsbereich.) Wenn Sie die Präsentations Quelle wechseln, werden alle Audio-und Videostreams in der Quelle gewechselt.</span><span class="sxs-lookup"><span data-stu-id="33b1e-108">(The default presentation source is the workspace.) Switching the presentation source switches all audio and video streams in the source.</span></span> <span data-ttu-id="33b1e-109">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="33b1e-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="33b1e-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="33b1e-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="33b1e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="33b1e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33b1e-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="33b1e-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="33b1e-113">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="33b1e-113">Identifier of an MCI device.</span></span> <span data-ttu-id="33b1e-114">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="33b1e-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="33b1e-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszmonitor*</span><span class="sxs-lookup"><span data-stu-id="33b1e-115"><span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="33b1e-116">Mindestens eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="33b1e-116">One or more of the following flags.</span></span>



| <span data-ttu-id="33b1e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="33b1e-117">Value</span></span>           | <span data-ttu-id="33b1e-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="33b1e-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33b1e-119">file</span><span class="sxs-lookup"><span data-stu-id="33b1e-119">file</span></span>            | <span data-ttu-id="33b1e-120">Gibt an, dass der Arbeitsbereich die Präsentations Quelle ist.</span><span class="sxs-lookup"><span data-stu-id="33b1e-120">Specifies that the workspace is the presentation source.</span></span> <span data-ttu-id="33b1e-121">Dies ist die Standard Quelle.</span><span class="sxs-lookup"><span data-stu-id="33b1e-121">This is the default source.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="33b1e-122">input</span><span class="sxs-lookup"><span data-stu-id="33b1e-122">input</span></span>           | <span data-ttu-id="33b1e-123">Gibt an, dass die externe Eingabe die Präsentations Quelle ist.</span><span class="sxs-lookup"><span data-stu-id="33b1e-123">Specifies that the external input is the presentation source.</span></span> <span data-ttu-id="33b1e-124">Wenn ein [Wiedergabe](play.md) Befehl ausgeführt wird, wird er zuerst angehalten.</span><span class="sxs-lookup"><span data-stu-id="33b1e-124">If a [play](play.md) command is in progress, it is first paused.</span></span> <span data-ttu-id="33b1e-125">Wenn [setvideo](setvideo.md) "on" ist, zeigt dieses Flag ein standardmäßiges ausgeblendetes Fenster an.</span><span class="sxs-lookup"><span data-stu-id="33b1e-125">If [setvideo](setvideo.md) is "on", this flag displays a default hidden window.</span></span> <span data-ttu-id="33b1e-126">Geräte können beim Überwachen von Eingaben möglicherweise die Vorgänge anderer Geräte Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="33b1e-126">Devices might limit what other device instances can do while monitoring input.</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="33b1e-127">method- *Methode*</span><span class="sxs-lookup"><span data-stu-id="33b1e-127">method *method*</span></span> | <span data-ttu-id="33b1e-128">Bei Verwendung mit dem **Monitor** "Input" wählt dieses Flag die Methode für die Überwachung aus.</span><span class="sxs-lookup"><span data-stu-id="33b1e-128">When used with **monitor** "input", this flag selects the method of monitoring.</span></span> <span data-ttu-id="33b1e-129">Die *Methode* ist entweder "Pre", "Post" oder "Direct".</span><span class="sxs-lookup"><span data-stu-id="33b1e-129">The *method* is either "pre", "post", or "direct".</span></span> <span data-ttu-id="33b1e-130">Die direkte Überwachung verlangt, dass das Gerät während der Überwachung für die optimale Anzeigequalität konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="33b1e-130">Direct monitoring requests that the device be configured for optimum display quality during monitoring.</span></span> <span data-ttu-id="33b1e-131">Die direkte Überwachungsmethode ist möglicherweise nicht mit der Motion-Videoaufzeichnung kompatibel. Videoaufzeichnung vor und nach der Überwachung zulassen</span><span class="sxs-lookup"><span data-stu-id="33b1e-131">The direct monitoring method might be incompatible with motion video recording.Pre- and post-monitoring allow motion video recording.</span></span> <span data-ttu-id="33b1e-132">Vor der Überwachung wird die externe Eingabe vor der Komprimierung angezeigt, während nach der Überwachung die externe Eingabe nach der Komprimierung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="33b1e-132">Pre-monitoring shows the external input prior to compression, while post-monitoring shows the external input after compression.</span></span> <span data-ttu-id="33b1e-133">In der Regel haben unterschiedliche Überwachungsmethoden andere Auswirkungen auf die Hardware.</span><span class="sxs-lookup"><span data-stu-id="33b1e-133">Typically, different monitoring methods have different hardware implications.</span></span> <span data-ttu-id="33b1e-134">Die Standard Überwachungsmethode wird vom Gerät ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="33b1e-134">The default monitoring method is selected by the device.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="33b1e-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="33b1e-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="33b1e-136">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="33b1e-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="33b1e-137">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="33b1e-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33b1e-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33b1e-138">Return Value</span></span>

<span data-ttu-id="33b1e-139">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="33b1e-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="33b1e-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33b1e-140">Remarks</span></span>

<span data-ttu-id="33b1e-141">Die Präsentations Quelle wechselt automatisch zum Arbeitsbereich, nachdem eine [Wiedergabe](play.md), ein [Schritt](step.md), eine [Pause](pause.md), ein Hinweis "Output" oder ein [Such](seek.md) Befehl [angezeigt wurde.](cue.md)</span><span class="sxs-lookup"><span data-stu-id="33b1e-141">The presentation source automatically switches to the workspace after a [play](play.md), [step](step.md), [pause](pause.md), [cue](cue.md) "output", or [seek](seek.md) command.</span></span> <span data-ttu-id="33b1e-142">Der [Datensatz](record.md) -Befehl wechselt nicht automatisch in die Präsentations Quellen, was Ihrer Anwendung die Möglichkeit bietet, während der Aufzeichnung keine Videos anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="33b1e-142">The [record](record.md) command does not automatically switch presentation sources, which gives your application the option of not showing video while it is being recorded.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b1e-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33b1e-143">Requirements</span></span>



| <span data-ttu-id="33b1e-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33b1e-144">Requirement</span></span> | <span data-ttu-id="33b1e-145">Wert</span><span class="sxs-lookup"><span data-stu-id="33b1e-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="33b1e-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33b1e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="33b1e-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33b1e-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="33b1e-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33b1e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="33b1e-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33b1e-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="33b1e-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33b1e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33b1e-151">MCI</span><span class="sxs-lookup"><span data-stu-id="33b1e-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="33b1e-152">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="33b1e-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="33b1e-153">STI</span><span class="sxs-lookup"><span data-stu-id="33b1e-153">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="33b1e-154">pause</span><span class="sxs-lookup"><span data-stu-id="33b1e-154">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="33b1e-155">Theater</span><span class="sxs-lookup"><span data-stu-id="33b1e-155">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="33b1e-156">record</span><span class="sxs-lookup"><span data-stu-id="33b1e-156">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="33b1e-157">einzuholen</span><span class="sxs-lookup"><span data-stu-id="33b1e-157">seek</span></span>](seek.md)
</dt> <dt>

[<span data-ttu-id="33b1e-158">Schritt</span><span class="sxs-lookup"><span data-stu-id="33b1e-158">step</span></span>](step.md)
</dt> </dl>

 

