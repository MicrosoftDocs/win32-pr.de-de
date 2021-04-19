---
title: MCI_CUE Befehl (MMSYSTEM. h)
description: Der MCI-Hinweis \_ Befehl gibt ein Gerät an, sodass die Wiedergabe oder Aufzeichnung mit minimaler Verzögerung beginnt. Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- MCI_CUE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8463c68f304fe216049568e0df518cbe1d0090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344691"
---
# <a name="mci_cue-command"></a><span data-ttu-id="c25d9-105">MCI-Hinweis \_ Befehl</span><span class="sxs-lookup"><span data-stu-id="c25d9-105">MCI\_CUE command</span></span>

<span data-ttu-id="c25d9-106">Der MCI-Hinweis \_ Befehl gibt ein Gerät an, sodass die Wiedergabe oder Aufzeichnung mit minimaler Verzögerung beginnt.</span><span class="sxs-lookup"><span data-stu-id="c25d9-106">The MCI\_CUE command cues a device so that playback or recording begins with minimum delay.</span></span> <span data-ttu-id="c25d9-107">Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.</span><span class="sxs-lookup"><span data-stu-id="c25d9-107">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="c25d9-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="c25d9-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
);
```



## <a name="parameters"></a><span data-ttu-id="c25d9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c25d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c25d9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="c25d9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="c25d9-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c25d9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-113">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="c25d9-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="c25d9-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c25d9-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpcue*</span><span class="sxs-lookup"><span data-stu-id="c25d9-115"><span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c25d9-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="c25d9-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="c25d9-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c25d9-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c25d9-118">Return Value</span></span>

<span data-ttu-id="c25d9-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c25d9-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c25d9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c25d9-120">Remarks</span></span>

<span data-ttu-id="c25d9-121">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="c25d9-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c25d9-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI \_ DGV-Hinweis \_ \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="c25d9-122"><span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>MCI\_DGV\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-123">Eine Digital Video-Instanz sollte sich auf die Aufzeichnung vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="c25d9-123">A digital-video instance should prepare for recording.</span></span> <span data-ttu-id="c25d9-124">Wenn die Anwendung keinen Speicherplatz reserviert hat, reserviert das Gerät den Speicherplatz mithilfe seiner Standardparameter.</span><span class="sxs-lookup"><span data-stu-id="c25d9-124">If the application has not reserved disk space, the device reserves the disk space using its default parameters.</span></span> <span data-ttu-id="c25d9-125">Die Anwendung kann dieses Flag weglassen, wenn die aktuelle Präsentations Quelle bereits die externe Eingabe ist.</span><span class="sxs-lookup"><span data-stu-id="c25d9-125">The application can omit this flag if the current presentation source is already the external input.</span></span> <span data-ttu-id="c25d9-126">(Dieses Flag hat keine Auswirkung auf die Auswahl der Präsentations Quelle.)</span><span class="sxs-lookup"><span data-stu-id="c25d9-126">(This flag has no effect on selecting the presentation source.)</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI \_ DGV-Hinweis \_ \_ noshow</span><span class="sxs-lookup"><span data-stu-id="c25d9-127"><span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>MCI\_DGV\_CUE\_NOSHOW</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-128">Eine Digital Video-Instanz sollte sich auf die Wiedergabe des Frames vorbereiten, der mit dem Befehl angegeben wurde, ohne ihn anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c25d9-128">A digital-video instance should prepare for playing the frame specified with the command without displaying it.</span></span> <span data-ttu-id="c25d9-129">Wenn dieses Flag angegeben wird, zeigt die Anzeige weiterhin das Bild im Frame Puffer an, auch wenn der entsprechende Frame nicht die aktuelle Position ist.</span><span class="sxs-lookup"><span data-stu-id="c25d9-129">When this flag is specified, the display continues to show the image in the frame buffer even though its corresponding frame is not the current position.</span></span> <span data-ttu-id="c25d9-130">Wenn der Frame Puffer z. b. das Bild aus Frame 7 enthält, zeigt das Gerät weiterhin Frame 7 an, wenn dieses Flag verwendet wird, um das Gerät an eine beliebige andere Position zu überweisen.</span><span class="sxs-lookup"><span data-stu-id="c25d9-130">For example, if the frame buffer contains the image from frame 7, the device continues to show frame 7 when this flag is used to cue the device to any other position.</span></span> <span data-ttu-id="c25d9-131">Mit einem nachfolgenden Hinweis Befehl ohne dieses Flag und ohne das Flag "MCI" wird \_ der aktuelle Frame angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c25d9-131">A subsequent cue command without this flag and without the MCI\_TO flag displays the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI- \_ DGV-Hinweis \_ \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c25d9-132"><span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>MCI\_DGV\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-133">Eine Digital Video-Instanz sollte sich auf die Wiedergabe vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="c25d9-133">A digital-video instance should prepare for playing.</span></span> <span data-ttu-id="c25d9-134">Wenn der Arbeitsbereich angehalten wird, findet keine Positionierung statt.</span><span class="sxs-lookup"><span data-stu-id="c25d9-134">If the workspace is paused, no positioning occurs.</span></span> <span data-ttu-id="c25d9-135">Wenn der Arbeitsbereich beendet wird, ändert sich die Position möglicherweise zu einem vorherigen Keyframe-Image.</span><span class="sxs-lookup"><span data-stu-id="c25d9-135">If the workspace is stopped, the position might change to a previous key-frame image.</span></span> <span data-ttu-id="c25d9-136">Die Anwendung kann dieses Flag weglassen, wenn die aktuelle Präsentations Quelle bereits der Arbeitsbereich ist.</span><span class="sxs-lookup"><span data-stu-id="c25d9-136">The application can omit this flag if the current presentation source is already the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="c25d9-137"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-138">Eine Arbeitsbereichs Position ist im **dwto** -Member der durch *lpcue* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="c25d9-138">A workspace position is included in the **dwTo** member of the structure identified by *lpCue*.</span></span> <span data-ttu-id="c25d9-139">Die den Positions Werten zugewiesenen Einheiten werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [ \_ MCI](mci-set.md) -Befehl festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c25d9-139">The units assigned to position values are specified using the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="c25d9-140">Dies entspricht der Suche nach einer Position, mit der Ausnahme, dass das Gerät nach dem Befehl angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="c25d9-140">This is equivalent to seeking to a position, except the device is paused after the command.</span></span>

</dd> </dl>

<span data-ttu-id="c25d9-141">Bei **Digitalvideo** -Geräten verweist der *lpcue* -Parameter auf eine [**MCI- \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="c25d9-141">For **digitalvideo** devices, the *lpCue* parameter points to an [**MCI\_DGV\_CUE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) structure.</span></span>

<span data-ttu-id="c25d9-142">Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="c25d9-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c25d9-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von</span><span class="sxs-lookup"><span data-stu-id="c25d9-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-144">Der **dwfrom** -Member der Struktur, auf die von *lpcue* verwiesen wird, enthält die im aktuellen Zeitformat angegebene Startposition.</span><span class="sxs-lookup"><span data-stu-id="c25d9-144">The **dwFrom** member of the structure pointed to by *lpCue* contains the starting location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="c25d9-145"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-146">Der **dwto** -Member der Struktur, auf die von *lpcue* verwiesen wird, enthält den im aktuellen Zeitformat angegebenen endspeicherort (Anhalten).</span><span class="sxs-lookup"><span data-stu-id="c25d9-146">The **dwTo** member of the structure pointed to by *lpCue* contains the ending (pausing) location specified in the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI- \_ VCR-Hinweis \_ \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="c25d9-147"><span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>MCI\_VCR\_CUE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-148">Vorbereiten der Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="c25d9-148">Prepare for recording.</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI- \_ VCR-Hinweis \_ \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c25d9-149"><span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>MCI\_VCR\_CUE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-150">Vorbereiten der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="c25d9-150">Prepare for playing.</span></span> <span data-ttu-id="c25d9-151">Wenn weder MCI \_ VCR-Hinweis \_ \_ Eingaben noch die MCI- \_ VCR-Hinweis \_ \_ Ausgabe angegeben ist, wird die MCI- \_ VCR-Hinweis \_ \_ Ausgabe angenommen.</span><span class="sxs-lookup"><span data-stu-id="c25d9-151">If neither MCI\_VCR\_CUE\_INPUT nor MCI\_VCR\_CUE\_OUTPUT is specified, MCI\_VCR\_CUE\_OUTPUT is assumed.</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI \_ VCR-Hinweis- \_ \_ Preroll</span><span class="sxs-lookup"><span data-stu-id="c25d9-152"><span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>MCI\_VCR\_CUE\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-153">Leiten Sie das Gerät an die aktuelle Position oder an die **dwfrom** -Position abzüglich der vorab Dauer der Vorabversion ab.</span><span class="sxs-lookup"><span data-stu-id="c25d9-153">Cue the device to the current position, or the **dwFrom** position, minus the preroll duration.</span></span> <span data-ttu-id="c25d9-154">Dadurch kann sich das Gerät vor dem Wechsel in den Daten Satz-oder Wiedergabemodus vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="c25d9-154">This will allow the device to prepare itself before entering record or playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI- \_ VCR-Hinweis \_ \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="c25d9-155"><span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>MCI\_VCR\_CUE\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-156">Die Richtung des nächsten Wiedergabe-oder Daten Satz Befehls ist umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="c25d9-156">The direction of the next play or record command is reverse.</span></span>

</dd> </dl>

<span data-ttu-id="c25d9-157">Wenn Sie die Wiedergabe mit dem MCI-Hinweis \_ Befehl mit dem MCI- \_ VCR-Flag- \_ \_ ausgabeflag verwenden, können Sie die MCI-Verwendung abbrechen, \_ indem Sie den [MCI- \_ Wiedergabe](mci-play.md) Befehl mit MCI \_ von, MCI \_ an oder MCI \_ VCR \_ Play Reverse ausgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="c25d9-157">When cueing for playback by using the MCI\_CUE command with the MCI\_VCR\_CUE\_OUTPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_PLAY](mci-play.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_PLAY\_REVERSE.</span></span>

<span data-ttu-id="c25d9-158">Wenn Sie die Aufzeichnung mit dem MCI- \_ Hinweis mit dem MCI \_ VCR-Flag Eingabe Kennzeichen durcharbeiten \_ \_ , können Sie den MCI-Hinweis abbrechen, \_ indem Sie den [MCI- \_ Eintrag](mci-record.md) Befehl mit MCI \_ from, MCI \_ to oder MCI \_ VCR \_ Record \_ Initialize ausgeben.</span><span class="sxs-lookup"><span data-stu-id="c25d9-158">When cueing for recording by using MCI\_CUE with the MCI\_VCR\_CUE\_INPUT flag, you can cancel MCI\_CUE by issuing the [MCI\_RECORD](mci-record.md) command with MCI\_FROM, MCI\_TO, or MCI\_VCR\_RECORD\_INITIALIZE.</span></span>

<span data-ttu-id="c25d9-159">Bei **VCR** -Geräten verweist der *lpcue* -Parameter auf eine [**MCI- \_ VCR \_ \_**](mci-vcr-cue-parms.md) -Endpunkt-Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="c25d9-159">For **vcr** devices, the *lpCue* parameter points to an [**MCI\_VCR\_CUE\_PARMS**](mci-vcr-cue-parms.md) structure.</span></span>

<span data-ttu-id="c25d9-160">Die folgenden zusätzlichen Flags werden mit dem **waveaudiogerätetyp** verwendet:</span><span class="sxs-lookup"><span data-stu-id="c25d9-160">The following additional flags are used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c25d9-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI- \_ Wave- \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="c25d9-161"><span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>MCI\_WAVE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-162">Ein Waveform-Audioeingabegerät sollte gecutzt werden.</span><span class="sxs-lookup"><span data-stu-id="c25d9-162">A waveform-audio input device should be cued.</span></span>

</dd> <dt>

<span data-ttu-id="c25d9-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI- \_ Wave- \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c25d9-163"><span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>MCI\_WAVE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="c25d9-164">Ein Waveform-Audioausgabegerät sollte gecutzt werden.</span><span class="sxs-lookup"><span data-stu-id="c25d9-164">A waveform-audio output device should be cued.</span></span> <span data-ttu-id="c25d9-165">Dies ist das Standardflag, wenn kein Flag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c25d9-165">This is the default flag if a flag is not specified.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c25d9-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c25d9-166">Requirements</span></span>



| <span data-ttu-id="c25d9-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c25d9-167">Requirement</span></span> | <span data-ttu-id="c25d9-168">Wert</span><span class="sxs-lookup"><span data-stu-id="c25d9-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c25d9-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c25d9-169">Minimum supported client</span></span><br/> | <span data-ttu-id="c25d9-170">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c25d9-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c25d9-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c25d9-171">Minimum supported server</span></span><br/> | <span data-ttu-id="c25d9-172">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c25d9-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c25d9-173">Header</span><span class="sxs-lookup"><span data-stu-id="c25d9-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="c25d9-174"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c25d9-174"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c25d9-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c25d9-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c25d9-176">MCI</span><span class="sxs-lookup"><span data-stu-id="c25d9-176">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c25d9-177">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="c25d9-177">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

