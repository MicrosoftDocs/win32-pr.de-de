---
title: Wiedergabe Befehl
description: Der Play-Befehl beginnt mit der Wiedergabe eines Geräts. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- Wiedergabe Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340781"
---
# <a name="play-command"></a><span data-ttu-id="9ac24-105">Wiedergabe Befehl</span><span class="sxs-lookup"><span data-stu-id="9ac24-105">play command</span></span>

<span data-ttu-id="9ac24-106">Der Play-Befehl beginnt mit der Wiedergabe eines Geräts.</span><span class="sxs-lookup"><span data-stu-id="9ac24-106">The play command starts playing a device.</span></span> <span data-ttu-id="9ac24-107">CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="9ac24-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="9ac24-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="9ac24-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="9ac24-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ac24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ac24-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="9ac24-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9ac24-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="9ac24-111">Identifier of an MCI device.</span></span> <span data-ttu-id="9ac24-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9ac24-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="9ac24-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszplayflags*</span><span class="sxs-lookup"><span data-stu-id="9ac24-113"><span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9ac24-114">Flag für die Wiedergabe eines Geräts.</span><span class="sxs-lookup"><span data-stu-id="9ac24-114">Flag for playing a device.</span></span> <span data-ttu-id="9ac24-115">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Wiedergabe** Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="9ac24-115">The following table lists device types that recognize the **play** command and the flags used by each type.</span></span>



| <span data-ttu-id="9ac24-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9ac24-116">Value</span></span>        | <span data-ttu-id="9ac24-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9ac24-117">Meaning</span></span>                          | <span data-ttu-id="9ac24-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9ac24-118">Meaning</span></span>                           |
|--------------|----------------------------------|-----------------------------------|
| <span data-ttu-id="9ac24-119">CDAudio</span><span class="sxs-lookup"><span data-stu-id="9ac24-119">cdaudio</span></span>      | <span data-ttu-id="9ac24-120">von *Position*</span><span class="sxs-lookup"><span data-stu-id="9ac24-120">from *position*</span></span>                  | <span data-ttu-id="9ac24-121">an *Position*</span><span class="sxs-lookup"><span data-stu-id="9ac24-121">to *position*</span></span>                     |
| <span data-ttu-id="9ac24-122">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="9ac24-122">digitalvideo</span></span> | <span data-ttu-id="9ac24-123">von *Position* voll Bildwiederholung</span><span class="sxs-lookup"><span data-stu-id="9ac24-123">from *position* fullscreen repeat</span></span> | <span data-ttu-id="9ac24-124">an *Positions* Fenster umkehren</span><span class="sxs-lookup"><span data-stu-id="9ac24-124">reverse to *position* window</span></span>       |
| <span data-ttu-id="9ac24-125">sequencer</span><span class="sxs-lookup"><span data-stu-id="9ac24-125">sequencer</span></span>    | <span data-ttu-id="9ac24-126">von *Position*</span><span class="sxs-lookup"><span data-stu-id="9ac24-126">from *position*</span></span>                  | <span data-ttu-id="9ac24-127">an *Position*</span><span class="sxs-lookup"><span data-stu-id="9ac24-127">to *position*</span></span>                     |
| <span data-ttu-id="9ac24-128">VCR</span><span class="sxs-lookup"><span data-stu-id="9ac24-128">vcr</span></span>          | <span data-ttu-id="9ac24-129">zum *Zeitpunkt* von der *Position* umkehren</span><span class="sxs-lookup"><span data-stu-id="9ac24-129">at *time* from *position* reverse</span></span>  | <span data-ttu-id="9ac24-130">an *Position* überprüfen</span><span class="sxs-lookup"><span data-stu-id="9ac24-130">scan to *position*</span></span>                |
| <span data-ttu-id="9ac24-131">Videodisk</span><span class="sxs-lookup"><span data-stu-id="9ac24-131">videodisc</span></span>    | <span data-ttu-id="9ac24-132">schnelle from- *Position*-Reverse-Scan</span><span class="sxs-lookup"><span data-stu-id="9ac24-132">fast from *position* reverse scan</span></span> | <span data-ttu-id="9ac24-133">*ganze* Zahl mit langsamer Geschwindigkeit an *Position*</span><span class="sxs-lookup"><span data-stu-id="9ac24-133">slow speed *integer* to *position*</span></span> |
| <span data-ttu-id="9ac24-134">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="9ac24-134">waveaudio</span></span>    | <span data-ttu-id="9ac24-135">von *Position*</span><span class="sxs-lookup"><span data-stu-id="9ac24-135">from *position*</span></span>                  | <span data-ttu-id="9ac24-136">an *Position*</span><span class="sxs-lookup"><span data-stu-id="9ac24-136">to *position*</span></span>                     |



 

<span data-ttu-id="9ac24-137">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszplayflags** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="9ac24-137">The following table lists the flags that can be specified in the **lpszPlayFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="9ac24-138">Wert</span><span class="sxs-lookup"><span data-stu-id="9ac24-138">Value</span></span>           | <span data-ttu-id="9ac24-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9ac24-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac24-140">zum *Zeitpunkt*</span><span class="sxs-lookup"><span data-stu-id="9ac24-140">at *time*</span></span>       | <span data-ttu-id="9ac24-141">Gibt an, wann das Gerät mit der Ausführung dieses Befehls beginnen soll, oder ob das Gerät beim Start des Geräts gecuht wurde.</span><span class="sxs-lookup"><span data-stu-id="9ac24-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="9ac24-142">Weitere Informationen finden Sie [unter dem Hinweis](cue.md) Befehl.</span><span class="sxs-lookup"><span data-stu-id="9ac24-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9ac24-143">fast</span><span class="sxs-lookup"><span data-stu-id="9ac24-143">fast</span></span>            | <span data-ttu-id="9ac24-144">Gibt an, dass das Gerät schneller als normal abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ac24-144">Indicates that the device should play faster than normal.</span></span> <span data-ttu-id="9ac24-145">Um die genaue Geschwindigkeit eines Video Disk Players zu ermitteln, verwenden Sie das Flag "Geschwindigkeit" des [Status](status.md) -Befehls.</span><span class="sxs-lookup"><span data-stu-id="9ac24-145">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="9ac24-146">Um die Geschwindigkeit genauer anzugeben, verwenden Sie das Flag "Geschwindigkeit" dieses Befehls.</span><span class="sxs-lookup"><span data-stu-id="9ac24-146">To specify the speed more precisely, use the "speed" flag of this command.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="9ac24-147">von *Position*</span><span class="sxs-lookup"><span data-stu-id="9ac24-147">from *position*</span></span> | <span data-ttu-id="9ac24-148">Gibt eine Startposition für die Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="9ac24-148">Specifies a starting position for the playback.</span></span> <span data-ttu-id="9ac24-149">Wenn das Flag "from" nicht angegeben wird, beginnt die Wiedergabe an der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="9ac24-149">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="9ac24-150">Bei **CDAudio** -Geräten gibt der Treiber einen Fehler zurück, wenn die "von"-Position größer als die Endposition der Festplatte ist oder wenn die "von"-Position größer als die "an"-Position ist.</span><span class="sxs-lookup"><span data-stu-id="9ac24-150">For **cdaudio** devices, if the "from" position is greater than the end position of the disc, or if the "from" position is greater than the "to" position, the driver returns an error.</span></span> <span data-ttu-id="9ac24-151">Bei **Videodisk** -Geräten befinden sich die Standardpositionen in Frames für CAV-Festplatten und in Stunden, Minuten und Sekunden für CLV-Festplatten.</span><span class="sxs-lookup"><span data-stu-id="9ac24-151">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span> |
| <span data-ttu-id="9ac24-152">Vollbild</span><span class="sxs-lookup"><span data-stu-id="9ac24-152">fullscreen</span></span>      | <span data-ttu-id="9ac24-153">Gibt an, dass eine voll Bild Anzeige verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ac24-153">Specifies that a full-screen display should be used.</span></span> <span data-ttu-id="9ac24-154">Verwenden Sie dieses Flag nur, wenn Sie komprimierte Dateien abspielen.</span><span class="sxs-lookup"><span data-stu-id="9ac24-154">Use this flag only when playing compressed files.</span></span> <span data-ttu-id="9ac24-155">(Nicht komprimierte Dateien werden nicht voll Bildschirm abgespielt.)</span><span class="sxs-lookup"><span data-stu-id="9ac24-155">(Uncompressed files won't play full-screen.)</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="9ac24-156">wiederholen</span><span class="sxs-lookup"><span data-stu-id="9ac24-156">repeat</span></span>          | <span data-ttu-id="9ac24-157">Gibt an, dass die Wiedergabe neu gestartet werden soll, wenn das Ende des Inhalts erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="9ac24-157">Specifies that playback should restart when the end of the content is reached.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9ac24-158">reverse</span><span class="sxs-lookup"><span data-stu-id="9ac24-158">reverse</span></span>         | <span data-ttu-id="9ac24-159">Gibt an, dass die Wiedergabe Richtung rückwärts verläuft.</span><span class="sxs-lookup"><span data-stu-id="9ac24-159">Specifies that the play direction is backward.</span></span> <span data-ttu-id="9ac24-160">Sie können keine Endposition mit dem Flag "Reverse" angeben.</span><span class="sxs-lookup"><span data-stu-id="9ac24-160">You cannot specify an ending location with the "reverse" flag.</span></span> <span data-ttu-id="9ac24-161">Bei Videodisks gilt "Scan" nur für das CAV-Format.</span><span class="sxs-lookup"><span data-stu-id="9ac24-161">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="9ac24-162">fein</span><span class="sxs-lookup"><span data-stu-id="9ac24-162">scan</span></span>            | <span data-ttu-id="9ac24-163">Wird so schnell wie möglich abgespielt, ohne das Video zu deaktivieren (obwohl Audiodaten möglicherweise deaktiviert sind).</span><span class="sxs-lookup"><span data-stu-id="9ac24-163">Plays as fast as possible without disabling video (although audio might be disabled).</span></span> <span data-ttu-id="9ac24-164">Bei Videodisks gilt "Scan" nur für das CAV-Format.</span><span class="sxs-lookup"><span data-stu-id="9ac24-164">For videodiscs, "scan" applies only to CAV format.</span></span>                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9ac24-165">langsam</span><span class="sxs-lookup"><span data-stu-id="9ac24-165">slow</span></span>            | <span data-ttu-id="9ac24-166">Wird langsam abgespielt.</span><span class="sxs-lookup"><span data-stu-id="9ac24-166">Plays slowly.</span></span> <span data-ttu-id="9ac24-167">Um die genaue Geschwindigkeit eines Video Disk Players zu ermitteln, verwenden Sie das Flag "Geschwindigkeit" des [Status](status.md) -Befehls.</span><span class="sxs-lookup"><span data-stu-id="9ac24-167">To determine the exact speed on a videodisc player, use the "speed" flag of the [status](status.md) command.</span></span> <span data-ttu-id="9ac24-168">Um die Geschwindigkeit genauer anzugeben, verwenden Sie das Flag "Geschwindigkeit" dieses Befehls.</span><span class="sxs-lookup"><span data-stu-id="9ac24-168">To specify the speed more precisely, use the "speed" flag of this command.</span></span> <span data-ttu-id="9ac24-169">Bei Videodisks gilt "langsam" nur für das CAV-Format.</span><span class="sxs-lookup"><span data-stu-id="9ac24-169">For videodiscs, "slow" applies only to CAV format.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="9ac24-170">*ganzzahlige* Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="9ac24-170">speed *integer*</span></span> | <span data-ttu-id="9ac24-171">Gibt eine Video Disk mit der angegebenen Geschwindigkeit in Frames pro Sekunde wieder.</span><span class="sxs-lookup"><span data-stu-id="9ac24-171">Plays a videodisc at the specified speed, in frames per second.</span></span> <span data-ttu-id="9ac24-172">Dieses Flag gilt nur für CAV-CDs.</span><span class="sxs-lookup"><span data-stu-id="9ac24-172">This flag applies only to CAV discs.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9ac24-173">an *Position*</span><span class="sxs-lookup"><span data-stu-id="9ac24-173">to *position*</span></span>   | <span data-ttu-id="9ac24-174">Gibt eine Endposition für die Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="9ac24-174">Specifies an ending position for the playback.</span></span> <span data-ttu-id="9ac24-175">Wenn das Flag "to" nicht angegeben wird, wird die Wiedergabe am Ende des Inhalts angehalten.</span><span class="sxs-lookup"><span data-stu-id="9ac24-175">If the "to" flag is not specified, playback stops at the end of the content.</span></span> <span data-ttu-id="9ac24-176">Bei **CDAudio** -Geräten gibt der Treiber einen Fehler zurück, wenn die "an"-Position größer als die Endposition der Festplatte ist.</span><span class="sxs-lookup"><span data-stu-id="9ac24-176">For **cdaudio** devices, if the "to" position is greater than the end position of the disc, the driver returns an error.</span></span> <span data-ttu-id="9ac24-177">Bei **Videodisk** -Geräten befinden sich die Standardpositionen in Frames für CAV-Festplatten und in Stunden, Minuten und Sekunden für CLV-Festplatten.</span><span class="sxs-lookup"><span data-stu-id="9ac24-177">For **videodisc** devices, the default positions are in frames for CAV discs and in hours, minutes, and seconds for CLV discs.</span></span>                                                                  |
| <span data-ttu-id="9ac24-178">Fenster</span><span class="sxs-lookup"><span data-stu-id="9ac24-178">window</span></span>          | <span data-ttu-id="9ac24-179">Gibt an, dass die Wiedergabe das Fenster verwenden soll, das der Geräte Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9ac24-179">Specifies that playing should use the window associated with the device instance.</span></span> <span data-ttu-id="9ac24-180">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9ac24-180">This is the default setting.</span></span>                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="9ac24-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="9ac24-181"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9ac24-182">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="9ac24-182">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="9ac24-183">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9ac24-183">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="9ac24-184">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9ac24-184">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ac24-185">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ac24-185">Return Value</span></span>

<span data-ttu-id="9ac24-186">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="9ac24-186">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ac24-187">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ac24-187">Remarks</span></span>

<span data-ttu-id="9ac24-188">Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen.</span><span class="sxs-lookup"><span data-stu-id="9ac24-188">Before issuing commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="9ac24-189">Dieser Befehl beginnt mit der aktuellen Geschwindigkeit, wie Sie mit dem Befehl "Geschwindigkeit" festlegen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9ac24-189">This command begins playing at the current speed, as set with the set "speed" command.</span></span> <span data-ttu-id="9ac24-190">Die Richtung ist umgekehrt, wenn das Flag "Reverse" angegeben wird, oder wenn das Flag "to" als Wert kleiner als das Flag "from" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ac24-190">The direction is reverse if the "reverse" flag is specified, or if the "to" flag is specified as a value less than the "from" flag.</span></span> <span data-ttu-id="9ac24-191">Wenn das Flag "from" nicht angegeben wird, beginnt die Wiedergabe an der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="9ac24-191">If the "from" flag is not specified, playback begins at the current position.</span></span> <span data-ttu-id="9ac24-192">Die Flags "to" und "Reverse" können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ac24-192">The "to" and "reverse" flags cannot be used together.</span></span>

## <a name="examples"></a><span data-ttu-id="9ac24-193">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ac24-193">Examples</span></span>

<span data-ttu-id="9ac24-194">Der folgende Befehl gibt das "mysound"-Gerät von der Position 1000 bis zur Position 2000 wieder und sendet eine Benachrichtigungs Meldung, wenn die Wiedergabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9ac24-194">The following command plays the "mysound" device from position 1000 through position 2000, sending a notification message when the playback completes.</span></span>

``` syntax
play mysound from 1000 to 2000 notify
```

## <a name="requirements"></a><span data-ttu-id="9ac24-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ac24-195">Requirements</span></span>



| <span data-ttu-id="9ac24-196">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ac24-196">Requirement</span></span> | <span data-ttu-id="9ac24-197">Wert</span><span class="sxs-lookup"><span data-stu-id="9ac24-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9ac24-198">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ac24-198">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac24-199">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ac24-199">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9ac24-200">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ac24-200">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac24-201">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ac24-201">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9ac24-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ac24-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac24-203">MCI</span><span class="sxs-lookup"><span data-stu-id="9ac24-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9ac24-204">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="9ac24-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="9ac24-205">STI</span><span class="sxs-lookup"><span data-stu-id="9ac24-205">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="9ac24-206">set</span><span class="sxs-lookup"><span data-stu-id="9ac24-206">set</span></span>](set.md)
</dt> </dl>

 

