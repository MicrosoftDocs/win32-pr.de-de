---
title: MCI_COPY Befehl (MMSYSTEM. h)
description: Der MCI- \_ Kopier Befehl kopiert Daten in die Zwischenablage. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- MCI_COPY Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956528"
---
# <a name="mci_copy-command"></a><span data-ttu-id="d483c-105">MCI- \_ Kopier Befehl</span><span class="sxs-lookup"><span data-stu-id="d483c-105">MCI\_COPY command</span></span>

<span data-ttu-id="d483c-106">Der MCI- \_ Kopier Befehl kopiert Daten in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="d483c-106">The MCI\_COPY command copies data to the clipboard.</span></span> <span data-ttu-id="d483c-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="d483c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d483c-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="d483c-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
);
```



## <a name="parameters"></a><span data-ttu-id="d483c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d483c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d483c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="d483c-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d483c-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="d483c-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d483c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d483c-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d483c-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="d483c-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="d483c-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d483c-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d483c-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpcopy*</span><span class="sxs-lookup"><span data-stu-id="d483c-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span></span>
</dt> <dd>

<span data-ttu-id="d483c-116">Zeiger auf eine [**MCI \_ DGV \_ - \_ kopierparamemestruktur**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .</span><span class="sxs-lookup"><span data-stu-id="d483c-116">Pointer to an [**MCI\_DGV\_COPY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d483c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d483c-117">Return Value</span></span>

<span data-ttu-id="d483c-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="d483c-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d483c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d483c-119">Remarks</span></span>

<span data-ttu-id="d483c-120">Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:</span><span class="sxs-lookup"><span data-stu-id="d483c-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="d483c-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI \_ DGV- \_ Kopie \_ bei</span><span class="sxs-lookup"><span data-stu-id="d483c-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI\_DGV\_COPY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="d483c-122">Ein Rechteck ist im **RC** -Member der durch *lpcopy* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="d483c-122">A rectangle is included in the **rc** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="d483c-123">Das Rechteck gibt den Teil jedes Frames an, der kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d483c-123">The rectangle specifies the portion of each frame to copy.</span></span> <span data-ttu-id="d483c-124">Wenn das Flag weggelassen wird, kopiert MCI \_ Copy den gesamten Frame.</span><span class="sxs-lookup"><span data-stu-id="d483c-124">If the flag is omitted, MCI\_COPY copies the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="d483c-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI \_ DGV \_ \_ - \_ Audiodatenstrom kopieren</span><span class="sxs-lookup"><span data-stu-id="d483c-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI\_DGV\_COPY\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d483c-126">Im **dwaudiostream** -Member der durch *lpcopy* identifizierten Struktur ist eine audiostreamnummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="d483c-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="d483c-127">Wenn Sie dieses Flag verwenden und Videos auch kopieren möchten, müssen Sie auch das Flag MCI \_ DGV- \_ \_ \_ Videostream kopieren verwenden.</span><span class="sxs-lookup"><span data-stu-id="d483c-127">If you use this flag and also want to copy video, you must also use the MCI\_DGV\_COPY\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="d483c-128">(Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams kopiert.)</span><span class="sxs-lookup"><span data-stu-id="d483c-128">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="d483c-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI \_ DGV \_ - \_ \_ Videostream zum Kopieren</span><span class="sxs-lookup"><span data-stu-id="d483c-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI\_DGV\_COPY\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="d483c-130">Im **dwvideostream** -Member der durch *lpcopy* identifizierten Struktur ist eine Video Strom Nummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="d483c-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="d483c-131">Wenn Sie dieses Flag verwenden und auch Audiodaten kopieren möchten, müssen Sie auch das Flag MCI \_ DGV \_ \_ - \_ Audiodatenstrom verwenden.</span><span class="sxs-lookup"><span data-stu-id="d483c-131">If you use this flag and also want to copy audio, you must also use the MCI\_DGV\_COPY\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="d483c-132">(Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams kopiert.)</span><span class="sxs-lookup"><span data-stu-id="d483c-132">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="d483c-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von</span><span class="sxs-lookup"><span data-stu-id="d483c-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="d483c-134">Ein Start Speicherort ist im **dwfrom** -Member der durch *lpcopy* identifizierten-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="d483c-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="d483c-135">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="d483c-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="d483c-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="d483c-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="d483c-137">Eine Endposition ist im **dwto** -Member der durch *lpcopy* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="d483c-137">An ending location is included in the **dwTo** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="d483c-138">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls MCI \_ Set angegeben.</span><span class="sxs-lookup"><span data-stu-id="d483c-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the MCI\_SET command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d483c-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d483c-139">Requirements</span></span>



| <span data-ttu-id="d483c-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d483c-140">Requirement</span></span> | <span data-ttu-id="d483c-141">Wert</span><span class="sxs-lookup"><span data-stu-id="d483c-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d483c-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d483c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d483c-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d483c-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d483c-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d483c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d483c-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d483c-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d483c-146">Header</span><span class="sxs-lookup"><span data-stu-id="d483c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d483c-147"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d483c-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d483c-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d483c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d483c-149">MCI</span><span class="sxs-lookup"><span data-stu-id="d483c-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d483c-150">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="d483c-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

