---
title: Befehl "Hinweis"
description: Der Hinweis Befehl bereitet die Wiedergabe oder Aufzeichnung vor. Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- Hinweis Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859313"
---
# <a name="cue-command"></a><span data-ttu-id="4f3fb-105">Befehl "Hinweis"</span><span class="sxs-lookup"><span data-stu-id="4f3fb-105">cue command</span></span>

<span data-ttu-id="4f3fb-106">Der Hinweis Befehl bereitet die Wiedergabe oder Aufzeichnung vor.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-106">The cue command prepares for playing or recording.</span></span> <span data-ttu-id="4f3fb-107">Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="4f3fb-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4f3fb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f3fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f3fb-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="4f3fb-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4f3fb-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-111">Identifier of an MCI device.</span></span> <span data-ttu-id="4f3fb-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4f3fb-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszinoutto*</span><span class="sxs-lookup"><span data-stu-id="4f3fb-113"><span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*</span></span>
</dt> <dd>

<span data-ttu-id="4f3fb-114">Flag, mit dem ein Gerät für die Wiedergabe oder Aufzeichnung vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-114">Flag that prepares a device for playing or recording.</span></span> <span data-ttu-id="4f3fb-115">In der folgenden Tabelle sind die Gerätetypen aufgeführt **, die den Hinweis Befehl und** die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-115">The following table lists device types that recognize the **cue** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f3fb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4f3fb-116">Value</span></span></th>
<th><span data-ttu-id="4f3fb-117">Position (Cue)</span><span class="sxs-lookup"><span data-stu-id="4f3fb-117">Cue</span></span></th>
<th><span data-ttu-id="4f3fb-118">Position (Cue)</span><span class="sxs-lookup"><span data-stu-id="4f3fb-118">Cue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4f3fb-119">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="4f3fb-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="4f3fb-120">input</span><span class="sxs-lookup"><span data-stu-id="4f3fb-120">input</span></span></li>
<li><span data-ttu-id="4f3fb-121">noshow</span><span class="sxs-lookup"><span data-stu-id="4f3fb-121">noshow</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4f3fb-122">output</span><span class="sxs-lookup"><span data-stu-id="4f3fb-122">output</span></span></li>
<li><span data-ttu-id="4f3fb-123">an <em>Position</em></span><span class="sxs-lookup"><span data-stu-id="4f3fb-123">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f3fb-124">VCR</span><span class="sxs-lookup"><span data-stu-id="4f3fb-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="4f3fb-125">von <em>Position</em></span><span class="sxs-lookup"><span data-stu-id="4f3fb-125">from <em>position</em></span></span></li>
<li><span data-ttu-id="4f3fb-126">input</span><span class="sxs-lookup"><span data-stu-id="4f3fb-126">input</span></span></li>
<li><span data-ttu-id="4f3fb-127">output</span><span class="sxs-lookup"><span data-stu-id="4f3fb-127">output</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4f3fb-128">ein Vorlauf ausgeführt</span><span class="sxs-lookup"><span data-stu-id="4f3fb-128">preroll</span></span></li>
<li><span data-ttu-id="4f3fb-129">reverse</span><span class="sxs-lookup"><span data-stu-id="4f3fb-129">reverse</span></span></li>
<li><span data-ttu-id="4f3fb-130">an <em>Position</em></span><span class="sxs-lookup"><span data-stu-id="4f3fb-130">to <em>position</em></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f3fb-131">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="4f3fb-131">waveaudio</span></span></td>
<td><span data-ttu-id="4f3fb-132">input</span><span class="sxs-lookup"><span data-stu-id="4f3fb-132">input</span></span></td>
<td><span data-ttu-id="4f3fb-133">output</span><span class="sxs-lookup"><span data-stu-id="4f3fb-133">output</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4f3fb-134">In der folgenden Tabelle werden die Flags aufgelistet, die im *lpszinoutto* -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-134">The following table lists the flags that can be specified in the *lpszInOutTo* parameter and their meanings.</span></span>



| <span data-ttu-id="4f3fb-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4f3fb-135">Value</span></span>           | <span data-ttu-id="4f3fb-136">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4f3fb-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3fb-137">von *Position*</span><span class="sxs-lookup"><span data-stu-id="4f3fb-137">from *position*</span></span> | <span data-ttu-id="4f3fb-138">Gibt an, wohin begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-138">Indicates where to start.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4f3fb-139">input</span><span class="sxs-lookup"><span data-stu-id="4f3fb-139">input</span></span>           | <span data-ttu-id="4f3fb-140">Bereitet die Aufzeichnung vor.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-140">Prepares for recording.</span></span> <span data-ttu-id="4f3fb-141">Für Digital Video-Geräte kann dieses Flag weggelassen werden, wenn die aktuelle Präsentations Quelle bereits die externe Eingabe ist.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-141">For digital-video devices, this flag can be omitted if the current presentation source is already the external input.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="4f3fb-142">noshow</span><span class="sxs-lookup"><span data-stu-id="4f3fb-142">noshow</span></span>          | <span data-ttu-id="4f3fb-143">Bereitet das Abspielen eines Frames vor, ohne es anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-143">Prepares for playing a frame without displaying it.</span></span> <span data-ttu-id="4f3fb-144">Wenn dieses Flag angegeben wird, zeigt die Anzeige weiterhin das Bild im Frame Puffer an, auch wenn der entsprechende Frame nicht die aktuelle Position ist.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-144">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="4f3fb-145">Mit einem nachfolgenden Hinweis Befehl ohne dieses Flag und ohne das Flag "to" wird der aktuelle Frame angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-145">A subsequent cue command without this flag and without the "to" flag displays the current frame.</span></span> |
| <span data-ttu-id="4f3fb-146">output</span><span class="sxs-lookup"><span data-stu-id="4f3fb-146">output</span></span>          | <span data-ttu-id="4f3fb-147">Bereitet das Abspielen vor.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-147">Prepares for playing.</span></span> <span data-ttu-id="4f3fb-148">Wenn weder "Input" noch "Output" angegeben ist, lautet die Standardeinstellung "Output".</span><span class="sxs-lookup"><span data-stu-id="4f3fb-148">If neither "input" nor "output" is specified, the default setting is "output".</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="4f3fb-149">ein Vorlauf ausgeführt</span><span class="sxs-lookup"><span data-stu-id="4f3fb-149">preroll</span></span>         | <span data-ttu-id="4f3fb-150">Verschiebt die Entfernung des vorab *-und des-Punkts*.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-150">Moves the preroll distance from the *in-point*.</span></span> <span data-ttu-id="4f3fb-151">Der-Punkt ist die aktuelle Position oder die durch das Flag "from" angegebene Position.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-151">The in-point is the current position, or the position specified by the "from" flag.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="4f3fb-152">reverse</span><span class="sxs-lookup"><span data-stu-id="4f3fb-152">reverse</span></span>         | <span data-ttu-id="4f3fb-153">Gibt an, dass die Wiedergabe Richtung rückwärts (rückwärts) ist.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-153">Indicates play direction is in reverse (backward).</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="4f3fb-154">an *Position*</span><span class="sxs-lookup"><span data-stu-id="4f3fb-154">to *position*</span></span>   | <span data-ttu-id="4f3fb-155">Verschiebt den Arbeitsbereich an die angegebene Position.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-155">Moves the workspace to the specified position.</span></span> <span data-ttu-id="4f3fb-156">Bei VCR-Geräten gibt dieses Flag an, wo der Vorgang beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-156">For VCR devices, this flag indicates where to stop.</span></span>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="4f3fb-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="4f3fb-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4f3fb-158">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="4f3fb-159">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="4f3fb-160">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4f3fb-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f3fb-161">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f3fb-161">Return Value</span></span>

<span data-ttu-id="4f3fb-162">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f3fb-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f3fb-163">Remarks</span></span>

<span data-ttu-id="4f3fb-164">Obwohl es nicht erforderlich ist, kann die Verzögerung vor dem Starten oder aufzeichnen auf einigen Geräten die Verzögerung verringern, bevor das Gerät die Aktion startet.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-164">Although it is not necessary, issuing the cue command before playing or recording on some devices might reduce the delay before the device starts the action.</span></span>

<span data-ttu-id="4f3fb-165">Dieser Befehl schlägt fehl, wenn die Wiedergabe oder Aufzeichnung ausgeführt wird oder wenn das Gerät angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-165">This command fails if playing or recording is in progress or if the device is paused.</span></span>

<span data-ttu-id="4f3fb-166">Wenn Sie die Wiedergabe (mit dem Hinweis "Output") übernehmen, wird der Befehl "Befehl" mit dem Flag "from", "to" oder "Reverse" durch Ausgeben des [Befehls Befehls abgeb](play.md) Rochen.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-166">When cueing for playback (using cue "output"), issuing the [play](play.md) command with the "from", "to", or "reverse" flag cancels the cue command.</span></span>

<span data-ttu-id="4f3fb-167">Beim Durchsuchen der Aufzeichnung (mit der "Input"-Eingabe) wird der "Befehl"-Befehl ausgegeben, wenn der [Datensatz](record.md) -Befehl mit dem Flag "from", "to" oder "Initialize" ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-167">When cueing for recording (using cue "input"), issuing the [record](record.md) command with the "from", "to", or "initialize" flag cancels the cue command.</span></span>

## <a name="examples"></a><span data-ttu-id="4f3fb-168">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f3fb-168">Examples</span></span>

<span data-ttu-id="4f3fb-169">Der folgende Befehl bereitet das "mysound"-Gerät für die Aufzeichnung vor.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-169">The following command prepares the "mysound" device for recording.</span></span>

``` syntax
cue mysound input
```

## <a name="requirements"></a><span data-ttu-id="4f3fb-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f3fb-170">Requirements</span></span>



| <span data-ttu-id="4f3fb-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f3fb-171">Requirement</span></span> | <span data-ttu-id="4f3fb-172">Wert</span><span class="sxs-lookup"><span data-stu-id="4f3fb-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4f3fb-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f3fb-173">Minimum supported client</span></span><br/> | <span data-ttu-id="4f3fb-174">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f3fb-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4f3fb-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f3fb-175">Minimum supported server</span></span><br/> | <span data-ttu-id="4f3fb-176">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f3fb-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4f3fb-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f3fb-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f3fb-178">MCI</span><span class="sxs-lookup"><span data-stu-id="4f3fb-178">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4f3fb-179">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="4f3fb-179">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="4f3fb-180">Theater</span><span class="sxs-lookup"><span data-stu-id="4f3fb-180">play</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="4f3fb-181">record</span><span class="sxs-lookup"><span data-stu-id="4f3fb-181">record</span></span>](record.md)
</dt> </dl>

 

