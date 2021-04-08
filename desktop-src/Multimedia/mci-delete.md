---
title: MCI_DELETE Befehl (MMSYSTEM. h)
description: Mit dem MCI- \_ Befehl Delete werden Daten aus der Datei entfernt. Digital-Video-und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- MCI_DELETE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c1b9f81712c842e06085c323ca2110c8e06784
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956777"
---
# <a name="mci_delete-command"></a><span data-ttu-id="cadb2-105">Befehl "MCI \_ Delete"</span><span class="sxs-lookup"><span data-stu-id="cadb2-105">MCI\_DELETE command</span></span>

<span data-ttu-id="cadb2-106">Mit dem MCI- \_ Befehl Delete werden Daten aus der Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="cadb2-106">The MCI\_DELETE command removes data from the file.</span></span> <span data-ttu-id="cadb2-107">Digital-Video-und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="cadb2-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="cadb2-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="cadb2-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
);
```



## <a name="parameters"></a><span data-ttu-id="cadb2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cadb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cadb2-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="cadb2-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="cadb2-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="cadb2-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cadb2-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder, für Digital Video-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="cadb2-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="cadb2-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cadb2-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="cadb2-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpdelete*</span><span class="sxs-lookup"><span data-stu-id="cadb2-115"><span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="cadb2-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="cadb2-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="cadb2-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cadb2-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cadb2-118">Return Value</span></span>

<span data-ttu-id="cadb2-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="cadb2-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cadb2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cadb2-120">Remarks</span></span>

<span data-ttu-id="cadb2-121">Die folgenden Flags gelten für den **Digitalvideo** -Gerätetyp:</span><span class="sxs-lookup"><span data-stu-id="cadb2-121">The following flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="cadb2-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI \_ DGV \_ Delete \_ bei</span><span class="sxs-lookup"><span data-stu-id="cadb2-122"><span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>MCI\_DGV\_DELETE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-123">In den **RC** -Member der durch *lpdelete* identifizierten-Struktur ist ein Rechteck enthalten.</span><span class="sxs-lookup"><span data-stu-id="cadb2-123">A rectangle is included in the **rc** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="cadb2-124">Das Rechteck gibt den Teil jedes Frames an, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="cadb2-124">The rectangle specifies the portion of each frame to delete.</span></span> <span data-ttu-id="cadb2-125">Wenn dieses Flag verwendet wird, wird der Frame im Arbeitsbereich aufbewahrt, und der durch das Rechteck angegebene Bereich wird schwarz.</span><span class="sxs-lookup"><span data-stu-id="cadb2-125">When this flag is used, the frame is retained in the workspace and the area specified by the rectangle becomes black.</span></span> <span data-ttu-id="cadb2-126">Wenn das Flag weggelassen wird, wird der \_ gesamte Frame vom MCI-Löschvorgang standardmäßig gelöscht und der Frame aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="cadb2-126">If the flag is omitted, MCI\_DELETE defaults to the entire frame and removes the frame from the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="cadb2-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI \_ DGV \_ , \_ \_ Audiostream löschen</span><span class="sxs-lookup"><span data-stu-id="cadb2-127"><span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>MCI\_DGV\_DELETE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-128">Im **dwaudiostream** -Member der von *lpdelete* identifizierten Struktur ist eine audiostreamnummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="cadb2-128">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="cadb2-129">Wenn Sie dieses Flag verwenden und Video auch löschen möchten, müssen Sie auch das Flag MCI \_ DGV- \_ \_ \_ Videostream löschen verwenden.</span><span class="sxs-lookup"><span data-stu-id="cadb2-129">If you use this flag and also want to delete video, you must also use the MCI\_DGV\_DELETE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="cadb2-130">(Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams gelöscht.)</span><span class="sxs-lookup"><span data-stu-id="cadb2-130">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="cadb2-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI \_ DGV \_ - \_ \_ Videostream löschen</span><span class="sxs-lookup"><span data-stu-id="cadb2-131"><span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>MCI\_DGV\_DELETE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-132">Im **dwvideostream** -Member der von *lpdelete* identifizierten Struktur ist eine Video Strom Nummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="cadb2-132">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="cadb2-133">Wenn Sie dieses Flag verwenden und auch Audiodaten löschen möchten, müssen Sie auch das Flag MCI \_ DGV \_ Delete \_ \_ Audiostream verwenden.</span><span class="sxs-lookup"><span data-stu-id="cadb2-133">If you use this flag and also want to delete audio, you must also use the MCI\_DGV\_DELETE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="cadb2-134">(Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams gelöscht.)</span><span class="sxs-lookup"><span data-stu-id="cadb2-134">(If neither flag is specified, data from all audio and video streams is deleted.)</span></span>

</dd> <dt>

<span data-ttu-id="cadb2-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von</span><span class="sxs-lookup"><span data-stu-id="cadb2-135"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-136">Im **dwfrom** -Member der von *lpdelete* identifizierten-Struktur ist ein Start Speicherort enthalten.</span><span class="sxs-lookup"><span data-stu-id="cadb2-136">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="cadb2-137">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="cadb2-137">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="cadb2-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="cadb2-138"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-139">Eine Endposition ist im **dwto** -Member der durch *lpdelete* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="cadb2-139">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="cadb2-140">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der MCI- \_ Menge angegeben.</span><span class="sxs-lookup"><span data-stu-id="cadb2-140">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="cadb2-141">Bei Digital Video-Geräten verweist der *lpdelete* -Parameter auf eine [**MCI \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) -Struktur zum Löschen von Parametern.</span><span class="sxs-lookup"><span data-stu-id="cadb2-141">For digital-video devices, the *lpDelete* parameter points to an [**MCI\_DGV\_DELETE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) structure.</span></span>

<span data-ttu-id="cadb2-142">Die folgenden Flags gelten für den **waveaudiogerätetyp** :</span><span class="sxs-lookup"><span data-stu-id="cadb2-142">The following flags apply to the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="cadb2-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von</span><span class="sxs-lookup"><span data-stu-id="cadb2-143"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-144">Im **dwfrom** -Member der von *lpdelete* identifizierten-Struktur ist ein Start Speicherort enthalten.</span><span class="sxs-lookup"><span data-stu-id="cadb2-144">A starting location is included in the **dwFrom** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="cadb2-145">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der [MCI- \_ Menge](mci-set.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="cadb2-145">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of [MCI\_SET](mci-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="cadb2-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="cadb2-146"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="cadb2-147">Eine Endposition ist im **dwto** -Member der durch *lpdelete* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="cadb2-147">An ending location is included in the **dwTo** member of the structure identified by *lpDelete*.</span></span> <span data-ttu-id="cadb2-148">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der MCI- \_ Menge angegeben.</span><span class="sxs-lookup"><span data-stu-id="cadb2-148">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

<span data-ttu-id="cadb2-149">Bei Waveform-Audiogeräten zeigt der *lpdelete* -Parameter auf eine [**MCI- \_ Wave \_ Delete \_**](mci-wave-delete-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="cadb2-149">For waveform-audio devices, the *lpDelete* parameter points to an [**MCI\_WAVE\_DELETE\_PARMS**](mci-wave-delete-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cadb2-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cadb2-150">Requirements</span></span>



| <span data-ttu-id="cadb2-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cadb2-151">Requirement</span></span> | <span data-ttu-id="cadb2-152">Wert</span><span class="sxs-lookup"><span data-stu-id="cadb2-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cadb2-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cadb2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="cadb2-154">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cadb2-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cadb2-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cadb2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="cadb2-156">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cadb2-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cadb2-157">Header</span><span class="sxs-lookup"><span data-stu-id="cadb2-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="cadb2-158"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cadb2-158"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cadb2-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cadb2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cadb2-160">MCI</span><span class="sxs-lookup"><span data-stu-id="cadb2-160">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cadb2-161">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="cadb2-161">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

