---
title: Seek-Befehl
description: Der Seek-Befehl wechselt an die angegebene Position und wird beendet. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- Seek-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391545"
---
# <a name="seek-command"></a><span data-ttu-id="07c30-105">Seek-Befehl</span><span class="sxs-lookup"><span data-stu-id="07c30-105">seek command</span></span>

<span data-ttu-id="07c30-106">Der Seek-Befehl wechselt an die angegebene Position und wird beendet.</span><span class="sxs-lookup"><span data-stu-id="07c30-106">The seek command moves to the specified position and stops.</span></span> <span data-ttu-id="07c30-107">CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="07c30-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="07c30-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="07c30-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="07c30-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="07c30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c30-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="07c30-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="07c30-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="07c30-111">Identifier of an MCI device.</span></span> <span data-ttu-id="07c30-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="07c30-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="07c30-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszseekflags*</span><span class="sxs-lookup"><span data-stu-id="07c30-113"><span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszSeekFlags*</span></span>
</dt> <dd>

<span data-ttu-id="07c30-114">Flag zum Verschieben an eine angegebene Position.</span><span class="sxs-lookup"><span data-stu-id="07c30-114">Flag for moving to a specified position.</span></span> <span data-ttu-id="07c30-115">In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Seek** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="07c30-115">The following table lists device types that recognize the **seek** command and the flags used by each type.</span></span>



| <span data-ttu-id="07c30-116">Wert</span><span class="sxs-lookup"><span data-stu-id="07c30-116">Value</span></span>        | <span data-ttu-id="07c30-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="07c30-117">Meaning</span></span>                          | <span data-ttu-id="07c30-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="07c30-118">Meaning</span></span>                      |
|--------------|----------------------------------|------------------------------|
| <span data-ttu-id="07c30-119">CDAudio</span><span class="sxs-lookup"><span data-stu-id="07c30-119">cdaudio</span></span>      | <span data-ttu-id="07c30-120">bis zum Ende der *Position*</span><span class="sxs-lookup"><span data-stu-id="07c30-120">to end to *position*</span></span>             | <span data-ttu-id="07c30-121">zum Starten</span><span class="sxs-lookup"><span data-stu-id="07c30-121">to start</span></span>                     |
| <span data-ttu-id="07c30-122">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="07c30-122">digitalvideo</span></span> | <span data-ttu-id="07c30-123">bis zum Ende der *Position*</span><span class="sxs-lookup"><span data-stu-id="07c30-123">to end to *position*</span></span>             | <span data-ttu-id="07c30-124">zum Starten</span><span class="sxs-lookup"><span data-stu-id="07c30-124">to start</span></span>                     |
| <span data-ttu-id="07c30-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="07c30-125">sequencer</span></span>    | <span data-ttu-id="07c30-126">bis zum Ende der *Position*</span><span class="sxs-lookup"><span data-stu-id="07c30-126">to end to *position*</span></span>             | <span data-ttu-id="07c30-127">zum Starten</span><span class="sxs-lookup"><span data-stu-id="07c30-127">to start</span></span>                     |
| <span data-ttu-id="07c30-128">VCR</span><span class="sxs-lookup"><span data-stu-id="07c30-128">vcr</span></span>          | <span data-ttu-id="07c30-129">zum *Zeitpunkt* der Markierung von *\_ NUM*</span><span class="sxs-lookup"><span data-stu-id="07c30-129">at *time* mark *mark\_num* reverse</span></span> | <span data-ttu-id="07c30-130">So beenden Sie die *Position* zum Starten</span><span class="sxs-lookup"><span data-stu-id="07c30-130">to end to *position* to start</span></span> |
| <span data-ttu-id="07c30-131">Videodisk</span><span class="sxs-lookup"><span data-stu-id="07c30-131">videodisc</span></span>    | <span data-ttu-id="07c30-132">zum Ende umkehren</span><span class="sxs-lookup"><span data-stu-id="07c30-132">reverse to end</span></span>                   | <span data-ttu-id="07c30-133">so *Positionieren* Sie den Start</span><span class="sxs-lookup"><span data-stu-id="07c30-133">to *position* to start</span></span>        |
| <span data-ttu-id="07c30-134">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="07c30-134">waveaudio</span></span>    | <span data-ttu-id="07c30-135">bis zum Ende der *Position*</span><span class="sxs-lookup"><span data-stu-id="07c30-135">to end to *position*</span></span>             | <span data-ttu-id="07c30-136">zum Starten</span><span class="sxs-lookup"><span data-stu-id="07c30-136">to start</span></span>                     |



 

<span data-ttu-id="07c30-137">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszseekflags** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="07c30-137">The following table lists the flags that can be specified in the **lpszSeekFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="07c30-138">Wert</span><span class="sxs-lookup"><span data-stu-id="07c30-138">Value</span></span>            | <span data-ttu-id="07c30-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="07c30-139">Meaning</span></span>                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c30-140">zum *Zeitpunkt*</span><span class="sxs-lookup"><span data-stu-id="07c30-140">at *time*</span></span>        | <span data-ttu-id="07c30-141">Gibt an, wann das Gerät mit der Ausführung dieses Befehls beginnen soll, oder ob das Gerät beim Start des Geräts gecuht wurde.</span><span class="sxs-lookup"><span data-stu-id="07c30-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="07c30-142">Weitere Informationen finden Sie [unter dem Hinweis](cue.md) Befehl.</span><span class="sxs-lookup"><span data-stu-id="07c30-142">For more information, see the [cue](cue.md) command.</span></span>                             |
| <span data-ttu-id="07c30-143">Markierung Nr. *\_ NUM*</span><span class="sxs-lookup"><span data-stu-id="07c30-143">mark *mark\_num*</span></span> | <span data-ttu-id="07c30-144">Sucht die relative Markierung, die von *Mark \_ NUM* angegeben wird. Dies muss ein positiver ganzzahliger Wert sein.</span><span class="sxs-lookup"><span data-stu-id="07c30-144">Seeks to the relative mark indicated by *mark\_num*, which must be a positive integer value.</span></span> <span data-ttu-id="07c30-145">Markierungen sind Signale, die mithilfe des Befehls [Markieren](mark.md) auf das VCR-Band geschrieben werden und für die schnelle Suche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07c30-145">Marks are signals written to the VCR tape using the [mark](mark.md) command and are used for high-speed searching.</span></span> |
| <span data-ttu-id="07c30-146">reverse</span><span class="sxs-lookup"><span data-stu-id="07c30-146">reverse</span></span>          | <span data-ttu-id="07c30-147">Gibt an, dass die Suchrichtung auf VCRs-und CAV-Videodisks rückwärts verläuft.</span><span class="sxs-lookup"><span data-stu-id="07c30-147">Indicates that the seek direction on VCRs and CAV videodiscs is backward.</span></span> <span data-ttu-id="07c30-148">Dieses Flag ist ungültig, wenn das Flag "to" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07c30-148">This flag is invalid if the "to" flag is specified.</span></span> <span data-ttu-id="07c30-149">Für VCRs muss dieses Flag mit dem Flag "Mark" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07c30-149">For VCRs, this flag must be used with the "mark" flag.</span></span>                             |
| <span data-ttu-id="07c30-150">zum Ende</span><span class="sxs-lookup"><span data-stu-id="07c30-150">to end</span></span>           | <span data-ttu-id="07c30-151">Sucht am Ende des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="07c30-151">Seeks to the end of the content.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="07c30-152">an *Position*</span><span class="sxs-lookup"><span data-stu-id="07c30-152">to *position*</span></span>    | <span data-ttu-id="07c30-153">Gibt die Position an, an der die Suche beendet wird.</span><span class="sxs-lookup"><span data-stu-id="07c30-153">Specifies the position to stop the seek.</span></span> <span data-ttu-id="07c30-154">Bei **CDAudio** -Geräten gibt MCI einen Fehler außerhalb des gültigen Bereichs zurück, wenn die angegebene Position größer als die Länge der Festplatte ist.</span><span class="sxs-lookup"><span data-stu-id="07c30-154">For **cdaudio** devices, MCI returns an out-of-range error if the specified position is greater than the length of the disc.</span></span>                                            |
| <span data-ttu-id="07c30-155">zum Starten</span><span class="sxs-lookup"><span data-stu-id="07c30-155">to start</span></span>         | <span data-ttu-id="07c30-156">Versucht, den Inhalt zu starten.</span><span class="sxs-lookup"><span data-stu-id="07c30-156">Seeks to the start of the content.</span></span>                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="07c30-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="07c30-157"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="07c30-158">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="07c30-158">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="07c30-159">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="07c30-159">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="07c30-160">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="07c30-160">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c30-161">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07c30-161">Return Value</span></span>

<span data-ttu-id="07c30-162">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="07c30-162">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="07c30-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07c30-163">Remarks</span></span>

<span data-ttu-id="07c30-164">Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen.</span><span class="sxs-lookup"><span data-stu-id="07c30-164">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

<span data-ttu-id="07c30-165">Digital Video-Geräte unterstützen zwei Suchmodi, die Sie mit dem [Set](set.md) -Befehl ändern können.</span><span class="sxs-lookup"><span data-stu-id="07c30-165">Digital-video devices support two seek modes, which you can change by using the [set](set.md) command.</span></span> <span data-ttu-id="07c30-166">Der "Seek genau on"-Modus bewirkt, dass der Seek-Befehl in den angegebenen Frame verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="07c30-166">The "seek exactly on" mode causes the seek command to move to the specified frame.</span></span> <span data-ttu-id="07c30-167">Der Modus "suchen genau aus" bewirkt, dass der Seek-Befehl in den nächstgelegenen Keyframe vor dem angegebenen Frame verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="07c30-167">The "seek exactly off" mode causes the seek command to move to the closest key frame prior to the specified frame.</span></span>

<span data-ttu-id="07c30-168">Wenn ein CD-Audiogerät abgespielt wird, wenn der Seek-Befehl ausgegeben wird, wird die Wiedergabe angehalten.</span><span class="sxs-lookup"><span data-stu-id="07c30-168">If a CD audio device is playing when the seek command is issued, playback is stopped.</span></span> <span data-ttu-id="07c30-169">Wenn der Befehl "Seek" mit einem Video Disk-Gerät ausgegeben wird, sucht das Gerät mithilfe von "schneller vorwärts" oder "schneller umkehren" mit Video-und Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="07c30-169">When the seek command is issued with a videodisc device, the device searches using fast forward or fast reverse with video and audio off.</span></span>

<span data-ttu-id="07c30-170">Wenn der Seek-Befehl mit einem Waveform-Audiogerät ausgegeben wird, hängt das Verhalten von der Stichprobengröße ab.</span><span class="sxs-lookup"><span data-stu-id="07c30-170">When the seek command is issued with a waveform-audio device, the behavior depends on the sample size.</span></span> <span data-ttu-id="07c30-171">Wenn die Stichprobengröße 16 Bits oder größer ist, wird die Suche bis zum Anfang des nächsten Beispiels fortgesetzt, wenn eine angegebene Position nicht mit dem Anfang eines Beispiels übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="07c30-171">If the sample size is 16 bits or greater, seek moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

## <a name="examples"></a><span data-ttu-id="07c30-172">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07c30-172">Examples</span></span>

<span data-ttu-id="07c30-173">Der folgende Befehl sucht am Anfang der Mediendatei, die dem "mysound"-Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="07c30-173">The following command seeks to the start of the media file associated with the "mysound" device.</span></span>

``` syntax
seek mysound to start
```

## <a name="requirements"></a><span data-ttu-id="07c30-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07c30-174">Requirements</span></span>



| <span data-ttu-id="07c30-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07c30-175">Requirement</span></span> | <span data-ttu-id="07c30-176">Wert</span><span class="sxs-lookup"><span data-stu-id="07c30-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="07c30-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07c30-177">Minimum supported client</span></span><br/> | <span data-ttu-id="07c30-178">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07c30-178">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="07c30-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07c30-179">Minimum supported server</span></span><br/> | <span data-ttu-id="07c30-180">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07c30-180">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="07c30-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07c30-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c30-182">MCI</span><span class="sxs-lookup"><span data-stu-id="07c30-182">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="07c30-183">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="07c30-183">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="07c30-184">STI</span><span class="sxs-lookup"><span data-stu-id="07c30-184">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="07c30-185">mark</span><span class="sxs-lookup"><span data-stu-id="07c30-185">mark</span></span>](mark.md)
</dt> <dt>

[<span data-ttu-id="07c30-186">set</span><span class="sxs-lookup"><span data-stu-id="07c30-186">set</span></span>](set.md)
</dt> </dl>

 

