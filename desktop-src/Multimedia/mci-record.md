---
title: MCI_RECORD Befehl (MMSYSTEM. h)
description: Der Befehl MCI- \_ Datensatz startet die Aufzeichnung von der aktuellen Position aus oder von einem angegebenen Speicherort an einen anderen angegebenen Speicherort.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- MCI_RECORD Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104012"
---
# <a name="mci_record-command"></a><span data-ttu-id="78612-104">Befehl "MCI- \_ Datensatz"</span><span class="sxs-lookup"><span data-stu-id="78612-104">MCI\_RECORD command</span></span>

<span data-ttu-id="78612-105">Der Befehl [**MCI- \_ Datensatz**](mci-record-parms.md) startet die Aufzeichnung von der aktuellen Position aus oder von einem angegebenen Speicherort an einen anderen angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="78612-105">The [**MCI\_RECORD**](mci-record-parms.md) command starts recording from the current position or from one specified location to another specified location.</span></span> <span data-ttu-id="78612-106">VCR-und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="78612-106">VCR and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="78612-107">Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI-und mciseq-Treiber Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="78612-107">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="78612-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="78612-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
);
```



## <a name="parameters"></a><span data-ttu-id="78612-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="78612-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78612-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="78612-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="78612-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="78612-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="78612-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="78612-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="78612-113">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="78612-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="78612-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="78612-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="78612-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lprecord*</span><span class="sxs-lookup"><span data-stu-id="78612-115"><span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*</span></span>
</dt> <dd>

<span data-ttu-id="78612-116">Zeiger auf eine Struktur des [**MCI- \_ Daten Satz- \_ Parametern**](mci-record-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="78612-116">Pointer to an [**MCI\_RECORD\_PARMS**](mci-record-parms.md) structure.</span></span> <span data-ttu-id="78612-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="78612-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78612-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78612-118">Return Value</span></span>

<span data-ttu-id="78612-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="78612-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="78612-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78612-120">Remarks</span></span>

<span data-ttu-id="78612-121">Dieser Befehl wird von Geräten unterstützt, die " **true** " zurückgeben, wenn Sie den [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl mit dem MCI \_ getdevcaps-Flag zum Aufzeichnen von Einträgen aufrufen \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="78612-121">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_RECORD flag.</span></span> <span data-ttu-id="78612-122">Für den MCIWave-Treiber werden alle Daten, die nach dem Öffnen einer Datei aufgezeichnet werden, verworfen, wenn die Datei geschlossen wird, ohne Sie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="78612-122">For the MCIWAVE driver, all data recorded after a file is opened is discarded if the file is closed without saving it.</span></span>

<span data-ttu-id="78612-123">Die folgenden zusätzlichen Flags gelten für alle Geräte, die den MCI-Datensatz unterstützen \_ :</span><span class="sxs-lookup"><span data-stu-id="78612-123">The following additional flags apply to all devices supporting MCI\_RECORD:</span></span>

<dl> <dt>

<span data-ttu-id="78612-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von</span><span class="sxs-lookup"><span data-stu-id="78612-124"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="78612-125">Ein Start Speicherort ist im **dwfrom** -Member der durch *lprecord* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="78612-125">A starting location is included in the **dwFrom** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="78612-126">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="78612-126">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="78612-127">Wenn MCI \_ from nicht angegeben wird, wird der Start Speicherort standardmäßig auf die aktuelle Position festgelegt.</span><span class="sxs-lookup"><span data-stu-id="78612-127">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="78612-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI- \_ Datensatz \_ Einfügen</span><span class="sxs-lookup"><span data-stu-id="78612-128"><span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>MCI\_RECORD\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="78612-129">Neu aufgezeichnete Informationen sollten eingefügt oder in die vorhandenen Daten eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="78612-129">Newly recorded information should be inserted or pasted into the existing data.</span></span> <span data-ttu-id="78612-130">Von einigen Geräten wird dies möglicherweise nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="78612-130">Some devices might not support this.</span></span> <span data-ttu-id="78612-131">Wenn dies unterstützt wird, ist dies die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="78612-131">If supported, this is the default.</span></span>

</dd> <dt>

<span data-ttu-id="78612-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI- \_ Daten Satz \_ Überschreibung</span><span class="sxs-lookup"><span data-stu-id="78612-132"><span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>MCI\_RECORD\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="78612-133">Die Daten sollten vorhandene Daten überschreiben.</span><span class="sxs-lookup"><span data-stu-id="78612-133">Data should overwrite existing data.</span></span> <span data-ttu-id="78612-134">Die MCIWave. Das drv-Gerät gibt \_ \_ als Antwort auf dieses Flag eine nicht unterstützte mcierr-Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="78612-134">The MCIWAVE.DRV device returns MCIERR\_UNSUPPORTED\_FUNCTION in response to this flag.</span></span>

</dd> <dt>

<span data-ttu-id="78612-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="78612-135"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="78612-136">Eine Endposition ist im **dwto** -Member der durch *lprecord* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="78612-136">An ending location is included in the **dwTo** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="78612-137">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="78612-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="78612-138">Wenn MCI \_ in nicht angegeben wird, wird die Endposition standardmäßig auf das Ende des Inhalts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="78612-138">If MCI\_TO is not specified, the ending location defaults to the end of the content.</span></span>

</dd> </dl>

<span data-ttu-id="78612-139">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="78612-139">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="78612-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>Audiostream für MCI \_ DGV \_ \_ -Datensatz \_</span><span class="sxs-lookup"><span data-stu-id="78612-140"><span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>MCI\_DGV\_RECORD\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="78612-141">Im **dwaudiostream** -Member der durch *lprecord* identifizierten Struktur ist eine audiostreamnummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="78612-141">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="78612-142">Wenn Sie dieses Flag weglassen, werden Audiodaten im ersten physischen Stream aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="78612-142">If you omit this flag, audio data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="78612-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI- \_ DGV- \_ Daten Satz \_ Aufbewahrung</span><span class="sxs-lookup"><span data-stu-id="78612-143"><span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>MCI\_DGV\_RECORD\_HOLD</span></span>
</dt> <dd>

<span data-ttu-id="78612-144">Wenn die Aufzeichnung angehalten wird, wird auf dem Bildschirm das letzte Bild angezeigt, und das Video wird erst angezeigt, wenn ein [MCI- \_ Monitor](mci-monitor.md) Befehl ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="78612-144">When recording stops, the screen will hold the last image and will not resume showing the video until an [MCI\_MONITOR](mci-monitor.md) command is issued.</span></span>

</dd> <dt>

<span data-ttu-id="78612-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI- \_ DGV- \_ Datensatz- \_ \_ Videostream</span><span class="sxs-lookup"><span data-stu-id="78612-145"><span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>MCI\_DGV\_RECORD\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="78612-146">Im **dwvideostream** -Member der durch *lprecord* identifizierten Struktur ist eine Video Strom Nummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="78612-146">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="78612-147">Wenn Sie dieses Flag weglassen, werden die Videodaten im ersten physischen Stream aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="78612-147">If you omit this flag, video data is recorded into the first physical stream.</span></span>

</dd> <dt>

<span data-ttu-id="78612-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI- \_ DGV- \_ Rect</span><span class="sxs-lookup"><span data-stu-id="78612-148"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="78612-149">Im **RC** -Member der durch *lprecord* identifizierten-Struktur wird ein Rechteck angegeben.</span><span class="sxs-lookup"><span data-stu-id="78612-149">A rectangle is specified in the **rc** member of the structure identified by *lpRecord*.</span></span> <span data-ttu-id="78612-150">Das Rechteck gibt den Bereich der externen Eingabe an, der als Quelle für die komprimierten und gespeicherten Pixel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78612-150">The rectangle specifies the region of the external input used as the source for the pixels compressed and saved.</span></span> <span data-ttu-id="78612-151">Dieses Rechteck ist standardmäßig auf das Rechteck festgelegt (oder standardmäßig), das vom MCI \_ DGV \_ Put- \_ videoflag für den Befehl " [MCI \_ Put](mci-put.md) " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="78612-151">This rectangle defaults to the rectangle specified (or defaulted) by the MCI\_DGV\_PUT\_VIDEO flag for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="78612-152">Wenn Sie anders festgelegt ist als das Video Rechteck, wird angezeigt, was nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="78612-152">When it is set differently than the video rectangle, what is displayed is not what is recorded</span></span>

</dd> </dl>

<span data-ttu-id="78612-153">Für Digital Video-Geräte verweist *lprecord* auf eine [**MCI- \_ DGV \_ - \_ Daten Satz**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) Struktur.</span><span class="sxs-lookup"><span data-stu-id="78612-153">For digital-video devices, *lpRecord* points to an [**MCI\_DGV\_RECORD\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) structure.</span></span>

<span data-ttu-id="78612-154">Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="78612-154">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="78612-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI- \_ VCR- \_ Datensatz \_ unter</span><span class="sxs-lookup"><span data-stu-id="78612-155"><span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>MCI\_VCR\_RECORD\_AT</span></span>
</dt> <dd>

<span data-ttu-id="78612-156">Der **dwat** -Member der durch *lprecord* identifizierten Struktur enthält einen Zeitpunkt, zu dem der gesamte Befehl beginnt, oder, wenn das Gerät gecuht wird, wenn das Gerät die vom Befehl angegebenen Position erreicht.</span><span class="sxs-lookup"><span data-stu-id="78612-156">The **dwAt** member of the structure identified by *lpRecord* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the cue command.</span></span>

</dd> <dt>

<span data-ttu-id="78612-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI \_ VCR- \_ Daten Satz \_ initialisieren</span><span class="sxs-lookup"><span data-stu-id="78612-157"><span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>MCI\_VCR\_RECORD\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="78612-158">Suchen Sie das Gerät nach dem Start des Mediums, beginnen Sie mit dem Aufzeichnen von leeren Videos und Audiodaten, und notieren Sie sich, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="78612-158">Seek the device to the start of the media, begin recording blank video and audio, and record timecode, if possible.</span></span>

</dd> </dl>

<span data-ttu-id="78612-159">Für VCR-Geräte verweist *lprecord* auf eine [**MCI- \_ VCR- \_ Daten Satz \_**](mci-vcr-record-parms.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="78612-159">For VCR devices, *lpRecord* points to an [**MCI\_VCR\_RECORD\_PARMS**](mci-vcr-record-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="78612-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78612-160">Requirements</span></span>



| <span data-ttu-id="78612-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78612-161">Requirement</span></span> | <span data-ttu-id="78612-162">Wert</span><span class="sxs-lookup"><span data-stu-id="78612-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78612-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78612-163">Minimum supported client</span></span><br/> | <span data-ttu-id="78612-164">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78612-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="78612-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78612-165">Minimum supported server</span></span><br/> | <span data-ttu-id="78612-166">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78612-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="78612-167">Header</span><span class="sxs-lookup"><span data-stu-id="78612-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="78612-168"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78612-168"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78612-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78612-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78612-170">MCI</span><span class="sxs-lookup"><span data-stu-id="78612-170">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="78612-171">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="78612-171">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

