---
title: MCI_CUT Befehl (MMSYSTEM. h)
description: Mit dem MCI \_ -Befehl "Ausschneiden" werden Daten aus der Datei entfernt und in die Zwischenablage kopiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- MCI_CUT Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956778"
---
# <a name="mci_cut-command"></a><span data-ttu-id="b90ae-105">MCI- \_ Befehl zum Ausschneiden</span><span class="sxs-lookup"><span data-stu-id="b90ae-105">MCI\_CUT command</span></span>

<span data-ttu-id="b90ae-106">Mit dem MCI \_ -Befehl "Ausschneiden" werden Daten aus der Datei entfernt und in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="b90ae-106">The MCI\_CUT command removes data from the file and copies it to the clipboard.</span></span> <span data-ttu-id="b90ae-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="b90ae-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="b90ae-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="b90ae-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
);
```



## <a name="parameters"></a><span data-ttu-id="b90ae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b90ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b90ae-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="b90ae-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b90ae-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="b90ae-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b90ae-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b90ae-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b90ae-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="b90ae-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="b90ae-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b90ae-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b90ae-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpcut*</span><span class="sxs-lookup"><span data-stu-id="b90ae-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span></span>
</dt> <dd>

<span data-ttu-id="b90ae-116">Zeiger auf eine [**MCI \_ DGV- \_ Ausschneide- \_ Parametern**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b90ae-116">Pointer to an [**MCI\_DGV\_CUT\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b90ae-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b90ae-117">Return Value</span></span>

<span data-ttu-id="b90ae-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="b90ae-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b90ae-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b90ae-119">Remarks</span></span>

<span data-ttu-id="b90ae-120">Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:</span><span class="sxs-lookup"><span data-stu-id="b90ae-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="b90ae-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI \_ DGV- \_ Ausschneiden \_ um</span><span class="sxs-lookup"><span data-stu-id="b90ae-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI\_DGV\_CUT\_AT</span></span>
</dt> <dd>

<span data-ttu-id="b90ae-122">Ein Rechteck ist im **RC** -Member der-Struktur enthalten, die von *lpcut* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b90ae-122">A rectangle is included in the **rc** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="b90ae-123">Das Rechteck gibt den Teil jedes Frames an, der abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="b90ae-123">The rectangle specifies the portion of each frame to cut.</span></span> <span data-ttu-id="b90ae-124">Wenn das Flag weggelassen wird, schneidet die MCI- \_ Ausschneide den gesamten Frame ab.</span><span class="sxs-lookup"><span data-stu-id="b90ae-124">If the flag is omitted, MCI\_CUT cuts the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="b90ae-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI \_ DGV \_ \_ -Audiodatenstrom Ausschneiden \_</span><span class="sxs-lookup"><span data-stu-id="b90ae-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI\_DGV\_CUT\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="b90ae-126">Eine audiostreamnummer ist im **dwaudiostream** -Member der durch *lpcut* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="b90ae-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="b90ae-127">Wenn Sie dieses Flag verwenden und auch Video ausschneiden möchten, müssen Sie auch das Flag MCI \_ DGV \_ - \_ Videodaten Strom verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="b90ae-127">If you use this flag and also want to cut video, you must also use the MCI\_DGV\_CUT\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="b90ae-128">(Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams ausgeschnitten.)</span><span class="sxs-lookup"><span data-stu-id="b90ae-128">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="b90ae-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI \_ DGV- \_ Ausschneide \_ Video Daten \_ Strom</span><span class="sxs-lookup"><span data-stu-id="b90ae-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI\_DGV\_CUT\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="b90ae-130">Im **dwvideostream** -Member der durch *lpcut* identifizierten Struktur ist eine Video Strom Nummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="b90ae-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="b90ae-131">Wenn Sie dieses Flag verwenden und auch das Audioelement ausschneiden möchten, müssen Sie auch das Flag MCI \_ DGV \_ \_ - \_ Audiodatenstrom verwenden.</span><span class="sxs-lookup"><span data-stu-id="b90ae-131">If you use this flag and also want to cut audio, you must also use the MCI\_DGV\_CUT\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="b90ae-132">(Wenn keines der Flags angegeben wird, werden Daten aus allen Audio-und Videostreams ausgeschnitten.)</span><span class="sxs-lookup"><span data-stu-id="b90ae-132">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="b90ae-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ von</span><span class="sxs-lookup"><span data-stu-id="b90ae-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="b90ae-134">Ein Start Speicherort ist im **dwfrom** -Member der durch *lpcut* identifizierten-Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="b90ae-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="b90ae-135">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="b90ae-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="b90ae-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="b90ae-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="b90ae-137">Eine Endposition ist im **dwto** -Member der durch *lpcut* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="b90ae-137">An ending location is included in the **dwTo** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="b90ae-138">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ \_ Format Flag zum Festlegen \_ der Uhrzeit der MCI- \_ Menge angegeben.</span><span class="sxs-lookup"><span data-stu-id="b90ae-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b90ae-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b90ae-139">Requirements</span></span>



| <span data-ttu-id="b90ae-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b90ae-140">Requirement</span></span> | <span data-ttu-id="b90ae-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b90ae-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b90ae-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b90ae-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b90ae-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b90ae-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b90ae-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b90ae-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b90ae-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b90ae-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b90ae-146">Header</span><span class="sxs-lookup"><span data-stu-id="b90ae-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b90ae-147"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b90ae-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b90ae-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b90ae-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90ae-149">MCI</span><span class="sxs-lookup"><span data-stu-id="b90ae-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b90ae-150">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="b90ae-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

