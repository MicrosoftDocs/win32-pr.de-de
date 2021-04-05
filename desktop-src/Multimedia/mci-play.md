---
title: MCI_PLAY Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Play signalisiert dem Gerät, mit dem Übertragen von Ausgabedaten zu beginnen. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- MCI_PLAY Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859310"
---
# <a name="mci_play-command"></a><span data-ttu-id="e51a0-105">MCI- \_ Wiedergabe Befehl</span><span class="sxs-lookup"><span data-stu-id="e51a0-105">MCI\_PLAY command</span></span>

<span data-ttu-id="e51a0-106">Der Befehl MCI \_ Play signalisiert dem Gerät, mit dem Übertragen von Ausgabedaten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e51a0-106">The MCI\_PLAY command signals the device to begin transmitting output data.</span></span> <span data-ttu-id="e51a0-107">CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="e51a0-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="e51a0-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="e51a0-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
);
```



## <a name="parameters"></a><span data-ttu-id="e51a0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e51a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e51a0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="e51a0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="e51a0-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="e51a0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-113">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="e51a0-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="e51a0-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e51a0-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpplay*</span><span class="sxs-lookup"><span data-stu-id="e51a0-115"><span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-116">Zeiger auf eine [**MCI- \_ Wiedergabe- \_ Parametern**](mci-play-parms.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e51a0-116">Pointer to an [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure.</span></span> <span data-ttu-id="e51a0-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="e51a0-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e51a0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e51a0-118">Return Value</span></span>

<span data-ttu-id="e51a0-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="e51a0-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e51a0-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e51a0-120">Remarks</span></span>

<span data-ttu-id="e51a0-121">Die folgenden zusätzlichen Flags gelten für alle Geräte, die die MCI-Wiedergabe unterstützen \_ :</span><span class="sxs-lookup"><span data-stu-id="e51a0-121">The following additional flags apply to all devices supporting MCI\_PLAY:</span></span>

<dl> <dt>

<span data-ttu-id="e51a0-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von</span><span class="sxs-lookup"><span data-stu-id="e51a0-122"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-123">Ein Start Speicherort ist im **dwfrom** -Member der von *lpplay* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="e51a0-123">A starting location is included in the **dwFrom** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="e51a0-124">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="e51a0-124">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="e51a0-125">Wenn MCI \_ from nicht angegeben wird, wird der Start Speicherort standardmäßig auf die aktuelle Position festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e51a0-125">If MCI\_FROM is not specified, the starting location defaults to the current position.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="e51a0-126"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-127">Eine Endposition ist im **dwto** -Member der von *lpplay* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="e51a0-127">An ending location is included in the **dwTo** member of the structure identified by *lpPlay*.</span></span> <span data-ttu-id="e51a0-128">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der MCI- \_ Menge angegeben.</span><span class="sxs-lookup"><span data-stu-id="e51a0-128">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span> <span data-ttu-id="e51a0-129">Wenn MCI \_ in nicht angegeben wird, wird die Endposition standardmäßig auf das Ende des Mediums festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e51a0-129">If MCI\_TO is not specified, the ending location defaults to the end of the media.</span></span>

</dd> </dl>

<span data-ttu-id="e51a0-130">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="e51a0-130">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="e51a0-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI \_ DGV- \_ Wiedergabe \_ Wiederholen</span><span class="sxs-lookup"><span data-stu-id="e51a0-131"><span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>MCI\_DGV\_PLAY\_REPEAT</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-132">Die Wiedergabe sollte am Anfang wieder gestartet werden, wenn das Ende des Inhalts erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="e51a0-132">Playback should start again at the beginning when the end of the content is reached.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI \_ DGV- \_ Wiedergabe \_ Rückgängigmachen</span><span class="sxs-lookup"><span data-stu-id="e51a0-133"><span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>MCI\_DGV\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-134">Wiedergabe sollte in umgekehrter Reihenfolge erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e51a0-134">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI- \_ MCIAVI- \_ Wiedergabe \_ Fenster</span><span class="sxs-lookup"><span data-stu-id="e51a0-135"><span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>MCI\_MCIAVI\_PLAY\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-136">Die Wiedergabe sollte in dem Fenster erfolgen, das einer Geräte Instanz zugeordnet ist (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="e51a0-136">Playback should occur in the window associated with a device instance (the default).</span></span> <span data-ttu-id="e51a0-137">(Dieses Flag ist für MCIAVI spezifisch. DRV.)</span><span class="sxs-lookup"><span data-stu-id="e51a0-137">(This flag is specific to MCIAVI.DRV.)</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI- \_ MCIAVI \_ Play \_ Fullscreen</span><span class="sxs-lookup"><span data-stu-id="e51a0-138"><span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>MCI\_MCIAVI\_PLAY\_FULLSCREEN</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-139">Bei der Wiedergabe sollte eine voll Bild Anzeige verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e51a0-139">Playback should use a full-screen display.</span></span> <span data-ttu-id="e51a0-140">Verwenden Sie dieses Flag nur bei der Wiedergabe von komprimierten oder 8-Bit-Dateien.</span><span class="sxs-lookup"><span data-stu-id="e51a0-140">Use this flag only when playing compressed or 8-bit files.</span></span>

</dd> </dl>

<span data-ttu-id="e51a0-141">Für Digital Video-Geräte verweist *lpplay* auf eine [**MCI- \_ DGV \_ - \_ Wiedergabe**](/previous-versions//dd743396(v=vs.85)) Elementstruktur.</span><span class="sxs-lookup"><span data-stu-id="e51a0-141">For digital-video devices, *lpPlay* points to an [**MCI\_DGV\_PLAY\_PARMS**](/previous-versions//dd743396(v=vs.85)) structure.</span></span>

<span data-ttu-id="e51a0-142">Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="e51a0-142">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="e51a0-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI \_ VCR- \_ Wiedergabe \_ bei</span><span class="sxs-lookup"><span data-stu-id="e51a0-143"><span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>MCI\_VCR\_PLAY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-144">Der **dwat** -Member der-Struktur, die von *lpplay* identifiziert wird, enthält einen Zeitpunkt, zu dem der gesamte Befehl beginnt, oder, wenn das Gerät über die Position des Geräts erreicht wird, die durch den [MCI \_](mci-cue.md) -Hinweis Befehl angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e51a0-144">The **dwAt** member of the structure identified by *lpPlay* contains a time when the entire command begins, or if the device is cued, when the device reaches the from position given by the [MCI\_CUE](mci-cue.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI \_ VCR- \_ Wiedergabe \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="e51a0-145"><span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>MCI\_VCR\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-146">Wiedergabe sollte in umgekehrter Reihenfolge erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e51a0-146">Playback should occur in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI- \_ VCR- \_ Wiedergabe Überprüfung \_</span><span class="sxs-lookup"><span data-stu-id="e51a0-147"><span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>MCI\_VCR\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-148">Die Wiedergabe sollte so schnell wie möglich sein, während die Videoausgabe erhalten bleibt.</span><span class="sxs-lookup"><span data-stu-id="e51a0-148">Playback should be as fast as possible while maintaining video output.</span></span>

</dd> </dl>

<span data-ttu-id="e51a0-149">Bei VCR-Geräten verweist *lpplay* auf eine [**MCI- \_ VCR-Wiedergabe- \_ \_ Parametern**](mci-vcr-play-parms.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e51a0-149">For VCR devices, *lpPlay* points to an [**MCI\_VCR\_PLAY\_PARMS**](mci-vcr-play-parms.md) structure.</span></span>

<span data-ttu-id="e51a0-150">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp " **Videodisk** " verwendet:</span><span class="sxs-lookup"><span data-stu-id="e51a0-150">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="e51a0-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI- \_ VD- \_ Wiedergabe \_ schnell</span><span class="sxs-lookup"><span data-stu-id="e51a0-151"><span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>MCI\_VD\_PLAY\_FAST</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-152">Spielen Sie schnell.</span><span class="sxs-lookup"><span data-stu-id="e51a0-152">Play fast.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI-VD-wieder \_ \_ Gabe \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="e51a0-153"><span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>MCI\_VD\_PLAY\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-154">Wiedergabe in umgekehrter Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="e51a0-154">Play in reverse.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI- \_ VD- \_ Wiedergabe \_ Scan</span><span class="sxs-lookup"><span data-stu-id="e51a0-155"><span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>MCI\_VD\_PLAY\_SCAN</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-156">Schnelles Scannen.</span><span class="sxs-lookup"><span data-stu-id="e51a0-156">Scan quickly.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI-VD-wieder \_ \_ Gabe \_ langsam</span><span class="sxs-lookup"><span data-stu-id="e51a0-157"><span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>MCI\_VD\_PLAY\_SLOW</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-158">Spielen Sie langsam.</span><span class="sxs-lookup"><span data-stu-id="e51a0-158">Play slowly.</span></span>

</dd> <dt>

<span data-ttu-id="e51a0-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI- \_ VD- \_ Wiedergabe \_ Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="e51a0-159"><span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>MCI\_VD\_PLAY\_SPEED</span></span>
</dt> <dd>

<span data-ttu-id="e51a0-160">Die Wiedergabegeschwindigkeit ist im **dwspeed** -Member in der von *lpplay* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="e51a0-160">The play speed is included in the **dwSpeed** member in the structure identified by *lpPlay*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e51a0-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e51a0-161">Requirements</span></span>



| <span data-ttu-id="e51a0-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e51a0-162">Requirement</span></span> | <span data-ttu-id="e51a0-163">Wert</span><span class="sxs-lookup"><span data-stu-id="e51a0-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51a0-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e51a0-164">Minimum supported client</span></span><br/> | <span data-ttu-id="e51a0-165">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e51a0-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e51a0-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e51a0-166">Minimum supported server</span></span><br/> | <span data-ttu-id="e51a0-167">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e51a0-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e51a0-168">Header</span><span class="sxs-lookup"><span data-stu-id="e51a0-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="e51a0-169"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e51a0-169"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e51a0-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e51a0-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e51a0-171">MCI</span><span class="sxs-lookup"><span data-stu-id="e51a0-171">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e51a0-172">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="e51a0-172">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

