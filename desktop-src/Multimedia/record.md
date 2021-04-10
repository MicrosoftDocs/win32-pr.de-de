---
title: Datensatz-Befehl
description: Der Datensatz-Befehl beginnt mit dem Aufzeichnen von Daten. VCR-und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI-und mciseq-Treiber Sie nicht.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- Datensatz-Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858668"
---
# <a name="record-command"></a><span data-ttu-id="53b49-106">Datensatz-Befehl</span><span class="sxs-lookup"><span data-stu-id="53b49-106">record command</span></span>

<span data-ttu-id="53b49-107">Der Datensatz-Befehl beginnt mit dem Aufzeichnen von Daten.</span><span class="sxs-lookup"><span data-stu-id="53b49-107">The record command starts recording data.</span></span> <span data-ttu-id="53b49-108">VCR-und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="53b49-108">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="53b49-109">Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI-und mciseq-Treiber Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="53b49-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="53b49-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="53b49-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="53b49-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="53b49-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53b49-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="53b49-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="53b49-113">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="53b49-113">Identifier of an MCI device.</span></span> <span data-ttu-id="53b49-114">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="53b49-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="53b49-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszrecordflags*</span><span class="sxs-lookup"><span data-stu-id="53b49-115"><span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*</span></span>
</dt> <dd>

<span data-ttu-id="53b49-116">Flag zum Aufzeichnen von Daten.</span><span class="sxs-lookup"><span data-stu-id="53b49-116">Flag for recording data.</span></span> <span data-ttu-id="53b49-117">In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Datensatz** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="53b49-117">The following table lists device types that recognize the **record** command and the flags used by each type.</span></span>



| <span data-ttu-id="53b49-118">Wert</span><span class="sxs-lookup"><span data-stu-id="53b49-118">Value</span></span>        | <span data-ttu-id="53b49-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="53b49-119">Meaning</span></span>                                                | <span data-ttu-id="53b49-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="53b49-120">Meaning</span></span>                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="53b49-121">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="53b49-121">digitalvideo</span></span> | <span data-ttu-id="53b49-122">bei *Rechteck*-Audiostream von *Position* halten </span><span class="sxs-lookup"><span data-stu-id="53b49-122">at *rectangle* audio stream *stream* from *position* hold</span></span> | <span data-ttu-id="53b49-123">INSERT-Vorgang zum *Positionieren* von *videostreamstream* einfügen</span><span class="sxs-lookup"><span data-stu-id="53b49-123">insert overwrite to *position* video stream *stream*</span></span> |
| <span data-ttu-id="53b49-124">sequencer</span><span class="sxs-lookup"><span data-stu-id="53b49-124">sequencer</span></span>    | <span data-ttu-id="53b49-125">aus *Position* einfügen</span><span class="sxs-lookup"><span data-stu-id="53b49-125">from *position* insert</span></span>                                  | <span data-ttu-id="53b49-126">an *Position* überschreiben</span><span class="sxs-lookup"><span data-stu-id="53b49-126">overwrite to *position*</span></span>                             |
| <span data-ttu-id="53b49-127">VCR</span><span class="sxs-lookup"><span data-stu-id="53b49-127">vcr</span></span>          | <span data-ttu-id="53b49-128">zum *Zeitpunkt* von der *Positions* Initialisierung</span><span class="sxs-lookup"><span data-stu-id="53b49-128">at *time* from *position* initialize</span></span>                     | <span data-ttu-id="53b49-129">Überschreiben an *Position* einfügen</span><span class="sxs-lookup"><span data-stu-id="53b49-129">insert overwrite to *position*</span></span>                      |
| <span data-ttu-id="53b49-130">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="53b49-130">waveaudio</span></span>    | <span data-ttu-id="53b49-131">aus *Position* einfügen</span><span class="sxs-lookup"><span data-stu-id="53b49-131">from *position* insert</span></span>                                  | <span data-ttu-id="53b49-132">an *Position* überschreiben</span><span class="sxs-lookup"><span data-stu-id="53b49-132">overwrite to *position*</span></span>                             |



 

<span data-ttu-id="53b49-133">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszrecordflags** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="53b49-133">The following table lists the flags that can be specified in the **lpszRecordFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="53b49-134">Wert</span><span class="sxs-lookup"><span data-stu-id="53b49-134">Value</span></span>                 | <span data-ttu-id="53b49-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="53b49-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53b49-136">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="53b49-136">at *rectangle*</span></span>        | <span data-ttu-id="53b49-137">Gibt einen rechteckigen Bereich der externen Eingabe an, der als Quelle für die komprimierten und gespeicherten Pixel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53b49-137">Specifies a rectangular region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="53b49-138">Wenn nicht angegeben, wird das Rechteck standardmäßig auf das Rechteck festgelegt, das für [Put](put.md) "Video" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="53b49-138">If not specified, the rectangle defaults to the rectangle specified for [put](put.md) "video".</span></span> <span data-ttu-id="53b49-139">Wenn Sie anders als das Rechteck "Video" festgelegt wird, wird das angezeigte Bild nicht so aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="53b49-139">When it is set differently from the "video" rectangle, the displayed image is not what is recorded.</span></span> |
| <span data-ttu-id="53b49-140">zum *Zeitpunkt*</span><span class="sxs-lookup"><span data-stu-id="53b49-140">at *time*</span></span>             | <span data-ttu-id="53b49-141">Gibt an, wann das Gerät mit der Ausführung dieses Befehls beginnen soll, oder ob das Gerät beim Start des Geräts gecuht wurde.</span><span class="sxs-lookup"><span data-stu-id="53b49-141">Indicates when the device should begin performing this command, or, if the device has been cued, when the cued command begins.</span></span> <span data-ttu-id="53b49-142">Weitere Informationen finden Sie [unter dem Hinweis](cue.md) Befehl.</span><span class="sxs-lookup"><span data-stu-id="53b49-142">For more information, see the [cue](cue.md) command.</span></span>                                                                                                                             |
| <span data-ttu-id="53b49-143">Audiostream- *Stream*</span><span class="sxs-lookup"><span data-stu-id="53b49-143">audio stream *stream*</span></span> | <span data-ttu-id="53b49-144">Gibt den für die Aufzeichnung verwendeten Audiodatenstrom an.</span><span class="sxs-lookup"><span data-stu-id="53b49-144">Specifies the audio stream used for recording.</span></span> <span data-ttu-id="53b49-145">Wenn dieses Flag nicht angegeben wird und das Dateiformat keinen Standardwert definiert, wird es in den physisch ersten Datenstrom aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="53b49-145">If this flag is not specified and the file format does not define a default, it is recorded into the stream that is physically first.</span></span>                                                                                                                             |
| <span data-ttu-id="53b49-146">von *Position*</span><span class="sxs-lookup"><span data-stu-id="53b49-146">from *position*</span></span>       | <span data-ttu-id="53b49-147">Gibt eine Startposition für die Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="53b49-147">Specifies a starting position for the recording.</span></span> <span data-ttu-id="53b49-148">Wenn das Flag "from" nicht angegeben wird, beginnt das Gerät mit der Aufzeichnung an der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="53b49-148">If the "from" flag is not specified, the device starts recording at the current position.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="53b49-149">verfügen</span><span class="sxs-lookup"><span data-stu-id="53b49-149">hold</span></span>                  | <span data-ttu-id="53b49-150">Friert das Bild, wenn die Aufzeichnung abgeschlossen ist, anstatt Livevideos anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="53b49-150">Freezes the image when recording has finished instead of showing live video.</span></span> <span data-ttu-id="53b49-151">Wenn die Aufzeichnung angehalten wird, wird der Befehl "file" des automatischen [Monitors](monitor.md) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53b49-151">When recording stops, an automatic [monitor](monitor.md) "file" command is performed.</span></span> <span data-ttu-id="53b49-152">Um zu Live Videos zurückzukehren, geben Sie den Befehl "Input" für den **Monitor** aus.</span><span class="sxs-lookup"><span data-stu-id="53b49-152">To return to live video, issue the **monitor** "input" command.</span></span>                                                                              |
| <span data-ttu-id="53b49-153">initialisieren</span><span class="sxs-lookup"><span data-stu-id="53b49-153">initialize</span></span>            | <span data-ttu-id="53b49-154">Initialisieren Sie das Band (Medium), das das Aufzeichnen von Zeitcode (sofern möglich) für leeres Video und Audiodaten umfasst.</span><span class="sxs-lookup"><span data-stu-id="53b49-154">Initialize the tape (media), which involves recording timecode (if possible) for blank video and audio.</span></span> <span data-ttu-id="53b49-155">Dieser Befehl kann mehrere Stunden in Anspruch nehmen, wenn das gesamte Band initialisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="53b49-155">This command might take several hours if the entire tape must be initialized.</span></span>                                                                                                                            |
| <span data-ttu-id="53b49-156">insert</span><span class="sxs-lookup"><span data-stu-id="53b49-156">insert</span></span>                | <span data-ttu-id="53b49-157">Gibt an, dass der Datei an der aktuellen Position neue Daten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="53b49-157">Specifies that new data is added to the file at the current position.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="53b49-158">overwrite</span><span class="sxs-lookup"><span data-stu-id="53b49-158">overwrite</span></span>             | <span data-ttu-id="53b49-159">Gibt an, dass neue Daten Daten in der Datei ersetzen.</span><span class="sxs-lookup"><span data-stu-id="53b49-159">Specifies that new data will replace data in the file.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="53b49-160">an *Position*</span><span class="sxs-lookup"><span data-stu-id="53b49-160">to *position*</span></span>         | <span data-ttu-id="53b49-161">Gibt eine Endposition für die Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="53b49-161">Specifies an ending position for the recording.</span></span> <span data-ttu-id="53b49-162">Wenn das Flag "to" nicht angegeben ist, wird das Gerät so lange aufgezeichnet, bis es [einen Befehl zum](pause.md) [Anhalten oder anhalten](stop.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="53b49-162">If the "to" flag is not specified, the device records until it receives a [stop](stop.md) or [pause](pause.md) command.</span></span>                                                                                                                                        |
| <span data-ttu-id="53b49-163">*videostreamstream*</span><span class="sxs-lookup"><span data-stu-id="53b49-163">video stream *stream*</span></span> | <span data-ttu-id="53b49-164">Gibt den für die Aufzeichnung verwendeten Videostream an.</span><span class="sxs-lookup"><span data-stu-id="53b49-164">Specifies the video stream used for recording.</span></span> <span data-ttu-id="53b49-165">Wenn dies nicht angegeben wird und das Dateiformat keinen Standardwert definiert, wird es im Stream aufgezeichnet, der physisch zuerst vorliegt.</span><span class="sxs-lookup"><span data-stu-id="53b49-165">If this is not specified and the file format does not define a default, then it is recorded into the stream that is physically first.</span></span>                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="53b49-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="53b49-166"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="53b49-167">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="53b49-167">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="53b49-168">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="53b49-168">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="53b49-169">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="53b49-169">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53b49-170">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53b49-170">Return Value</span></span>

<span data-ttu-id="53b49-171">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="53b49-171">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="53b49-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53b49-172">Remarks</span></span>

<span data-ttu-id="53b49-173">Die Aufzeichnung wird beendet, wenn ein [Befehl zum](pause.md) [Beenden oder anhalten](stop.md) ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="53b49-173">The recording stops when a [stop](stop.md) or [pause](pause.md) command is issued.</span></span> <span data-ttu-id="53b49-174">Für den MCIWave-Treiber werden alle Daten, die nach dem Öffnen einer Datei aufgezeichnet werden, verworfen, wenn die Datei geschlossen wird, ohne Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="53b49-174">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="53b49-175">Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen.</span><span class="sxs-lookup"><span data-stu-id="53b49-175">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span> <span data-ttu-id="53b49-176">Die aufzuzeichnenden Spuren werden durch die Befehle [settimecode](settimecode.md) "Record", Set "assemblierungsdatensatz", " [setvideo](setvideo.md) " und [setaudiodatensatz](setaudio.md) "Record" angegeben.</span><span class="sxs-lookup"><span data-stu-id="53b49-176">The tracks to be recorded are specified by the [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record", and [setaudio](setaudio.md) "record" commands.</span></span>

## <a name="examples"></a><span data-ttu-id="53b49-177">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53b49-177">Examples</span></span>

<span data-ttu-id="53b49-178">Mit dem folgenden Befehl wird die Aufzeichnung an der aktuellen Position gestartet.</span><span class="sxs-lookup"><span data-stu-id="53b49-178">The following command starts recording at the current position.</span></span>

``` syntax
record mysound
```

## <a name="requirements"></a><span data-ttu-id="53b49-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53b49-179">Requirements</span></span>



| <span data-ttu-id="53b49-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53b49-180">Requirement</span></span> | <span data-ttu-id="53b49-181">Wert</span><span class="sxs-lookup"><span data-stu-id="53b49-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="53b49-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53b49-182">Minimum supported client</span></span><br/> | <span data-ttu-id="53b49-183">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53b49-183">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="53b49-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53b49-184">Minimum supported server</span></span><br/> | <span data-ttu-id="53b49-185">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53b49-185">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="53b49-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53b49-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b49-187">MCI</span><span class="sxs-lookup"><span data-stu-id="53b49-187">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="53b49-188">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="53b49-188">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="53b49-189">STI</span><span class="sxs-lookup"><span data-stu-id="53b49-189">cue</span></span>](cue.md)
</dt> <dt>

[<span data-ttu-id="53b49-190">über</span><span class="sxs-lookup"><span data-stu-id="53b49-190">monitor</span></span>](monitor.md)
</dt> <dt>

[<span data-ttu-id="53b49-191">pause</span><span class="sxs-lookup"><span data-stu-id="53b49-191">pause</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="53b49-192">stellte</span><span class="sxs-lookup"><span data-stu-id="53b49-192">put</span></span>](put.md)
</dt> <dt>

[<span data-ttu-id="53b49-193">set</span><span class="sxs-lookup"><span data-stu-id="53b49-193">set</span></span>](set.md)
</dt> <dt>

[<span data-ttu-id="53b49-194">setaudiodatei</span><span class="sxs-lookup"><span data-stu-id="53b49-194">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="53b49-195">settimecode</span><span class="sxs-lookup"><span data-stu-id="53b49-195">settimecode</span></span>](settimecode.md)
</dt> <dt>

[<span data-ttu-id="53b49-196">setvideo</span><span class="sxs-lookup"><span data-stu-id="53b49-196">setvideo</span></span>](setvideo.md)
</dt> <dt>

[<span data-ttu-id="53b49-197">stop</span><span class="sxs-lookup"><span data-stu-id="53b49-197">stop</span></span>](stop.md)
</dt> </dl>

 

