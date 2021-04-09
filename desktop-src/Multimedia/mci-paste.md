---
title: MCI_PASTE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl zum Einfügen fügt Daten aus der Zwischenablage in eine Datei ein. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- MCI_PASTE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739825"
---
# <a name="mci_paste-command"></a><span data-ttu-id="30dcc-105">MCI- \_ Befehl "Einfügen"</span><span class="sxs-lookup"><span data-stu-id="30dcc-105">MCI\_PASTE command</span></span>

<span data-ttu-id="30dcc-106">Der MCI- \_ Befehl zum Einfügen fügt Daten aus der Zwischenablage in eine Datei ein.</span><span class="sxs-lookup"><span data-stu-id="30dcc-106">The MCI\_PASTE command pastes data from the clipboard into a file.</span></span> <span data-ttu-id="30dcc-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="30dcc-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="30dcc-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="30dcc-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
);
```



## <a name="parameters"></a><span data-ttu-id="30dcc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30dcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30dcc-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="30dcc-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="30dcc-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="30dcc-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="30dcc-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="30dcc-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="30dcc-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="30dcc-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="30dcc-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="30dcc-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="30dcc-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lppaste*</span><span class="sxs-lookup"><span data-stu-id="30dcc-115"><span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*</span></span>
</dt> <dd>

<span data-ttu-id="30dcc-116">Zeiger auf eine [**MCI \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) -Struktur zum Einfügen von Parametern.</span><span class="sxs-lookup"><span data-stu-id="30dcc-116">Pointer to an [**MCI\_ DGV\_ PASTE\_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30dcc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30dcc-117">Return Value</span></span>

<span data-ttu-id="30dcc-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="30dcc-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="30dcc-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30dcc-119">Remarks</span></span>

<span data-ttu-id="30dcc-120">Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:</span><span class="sxs-lookup"><span data-stu-id="30dcc-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="30dcc-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI \_ DGV \_ Einfügen \_ bei</span><span class="sxs-lookup"><span data-stu-id="30dcc-121"><span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI\_DGV\_PASTE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="30dcc-122">In den **RC** -Member der durch *lppaste* identifizierten Struktur ist ein Rechteck enthalten.</span><span class="sxs-lookup"><span data-stu-id="30dcc-122">A rectangle is included in the **rc** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="30dcc-123">Die ersten beiden Werte des Rechtecks geben den Punkt im Frame an, an dem die Zwischenablage Informationen platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30dcc-123">The first two values of the rectangle specify the point within the frame to place the clipboard information.</span></span> <span data-ttu-id="30dcc-124">Wenn die Höhe und Breite des Rechtecks ungleich NULL sind, werden die Inhalte der Zwischenablage auf diese Dimensionen skaliert, wenn Sie im Frame eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="30dcc-124">If the rectangle height and width are nonzero, the clipboard contents are scaled to those dimensions when they are pasted in the frame.</span></span> <span data-ttu-id="30dcc-125">Wenn das-Flag weggelassen wird, wird der MCI-Wert \_ standardmäßig in das gesamte Frame Rechteck eingefügt.</span><span class="sxs-lookup"><span data-stu-id="30dcc-125">If the flag is omitted, MCI\_PASTE defaults to the entire frame rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="30dcc-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ \_ - \_ Audiodatenstrom einfügen</span><span class="sxs-lookup"><span data-stu-id="30dcc-126"><span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI\_DGV\_PASTE\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="30dcc-127">Im **dwaudiostream** -Member der durch *lppaste* identifizierten Struktur ist eine audiostreamnummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="30dcc-127">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="30dcc-128">Wenn nur ein Audiostream in der Zwischenablage vorhanden ist, werden die Audiodaten in den vorgesehenen Stream eingefügt.</span><span class="sxs-lookup"><span data-stu-id="30dcc-128">If only one audio stream exists on the clipboard, the audio data is pasted into the designated stream.</span></span> <span data-ttu-id="30dcc-129">Wenn mehr als ein Audiostream in der Zwischenablage vorhanden ist, gibt der Stream die Startnummer für die Datenstrom Sequenzen an.</span><span class="sxs-lookup"><span data-stu-id="30dcc-129">If more than one audio stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="30dcc-130">Wenn Sie dieses Flag verwenden und Video einfügen möchten, müssen Sie auch das Flag MCI \_ DGV- \_ Videodaten \_ Strom einfügen verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="30dcc-130">If you use this flag and also want to paste video, you must also use the MCI\_DGV\_PASTE\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="30dcc-131">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams beginnend mit dem ersten Audiostream und Videostream eingefügt.</span><span class="sxs-lookup"><span data-stu-id="30dcc-131">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="30dcc-132">Jeder eingefügte Stream behält seine ursprüngliche Datenstrom Nummer bei.)</span><span class="sxs-lookup"><span data-stu-id="30dcc-132">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="30dcc-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>Einfügen von MCI \_ DGV \_ Einfügen \_</span><span class="sxs-lookup"><span data-stu-id="30dcc-133"><span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI\_DGV\_PASTE\_INSERT</span></span>
</dt> <dd>

<span data-ttu-id="30dcc-134">Zwischenablage Daten sollten in den vorhandenen Arbeitsbereich an der Position eingefügt werden, die durch das zu flagende MCI angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="30dcc-134">Clipboard data should be inserted in the existing workspace at the position specified by the MCI\_TO flag.</span></span> <span data-ttu-id="30dcc-135">Alle vorhandenen Daten nach der Einfügemarke werden in den Arbeitsbereich verschoben, um Platz zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="30dcc-135">Any existing data after the insertion point is moved in the workspace to make room.</span></span> <span data-ttu-id="30dcc-136">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="30dcc-136">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="30dcc-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI- \_ DGV- \_ Einfüge \_ Überschreibung</span><span class="sxs-lookup"><span data-stu-id="30dcc-137"><span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI\_DGV\_PASTE\_OVERWRITE</span></span>
</dt> <dd>

<span data-ttu-id="30dcc-138">Zwischenablage Daten sollten die bereits im Arbeitsbereich vorhandenen Daten ersetzen.</span><span class="sxs-lookup"><span data-stu-id="30dcc-138">Clipboard data should replace data already present in the workspace.</span></span> <span data-ttu-id="30dcc-139">Die Arbeitsbereichs Daten werden nach der Einfügemarke ersetzt.</span><span class="sxs-lookup"><span data-stu-id="30dcc-139">The workspace data replaced follows the insertion point.</span></span>

</dd> <dt>

<span data-ttu-id="30dcc-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI \_ DGV \_ - \_ Video Daten \_ Strom einfügen</span><span class="sxs-lookup"><span data-stu-id="30dcc-140"><span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>MCI\_DGV\_PASTE\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="30dcc-141">Im **dwvideostream** -Member der durch *lppaste* identifizierten Struktur ist eine Video Strom Nummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="30dcc-141">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="30dcc-142">Wenn nur ein Videostream in der Zwischenablage vorhanden ist, werden die Videodaten in den vorgesehenen Stream eingefügt.</span><span class="sxs-lookup"><span data-stu-id="30dcc-142">If only one video stream exists on the clipboard, the video data is pasted into the designated stream.</span></span> <span data-ttu-id="30dcc-143">Wenn mehr als ein Videostream in der Zwischenablage vorhanden ist, gibt der Stream die Startnummer für die Datenstrom Sequenzen an.</span><span class="sxs-lookup"><span data-stu-id="30dcc-143">If more than one video stream exists on the clipboard, the stream indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="30dcc-144">Wenn Sie dieses Flag verwenden und auch Audiodaten einfügen möchten, müssen Sie auch das Flag MCI \_ DGV \_ \_ -Audiodatenstrom einfügen verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="30dcc-144">If you use this flag and also want to paste audio, you must also use the MCI\_DGV\_PASTE\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="30dcc-145">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams beginnend mit dem ersten Audiostream und Videostream eingefügt.</span><span class="sxs-lookup"><span data-stu-id="30dcc-145">(If neither flag is specified, all audio and video streams are pasted starting with the first audio and video stream.</span></span> <span data-ttu-id="30dcc-146">Jeder eingefügte Stream behält seine ursprüngliche Datenstrom Nummer bei.)</span><span class="sxs-lookup"><span data-stu-id="30dcc-146">Each pasted stream retains its original stream number.)</span></span>

</dd> <dt>

<span data-ttu-id="30dcc-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="30dcc-147"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="30dcc-148">Ein Positionswert ist im **dwto** -Member der durch *lppaste* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="30dcc-148">A position value is included in the **dwTo** member of the structure identified by *lpPaste*.</span></span> <span data-ttu-id="30dcc-149">Der Positionswert gibt die Position an, an der mit dem Einfügen von Daten in den Arbeitsbereich begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="30dcc-149">The position value specifies the position to begin pasting data into the workspace.</span></span> <span data-ttu-id="30dcc-150">Wenn dieses Flag weggelassen wird, wird die Position standardmäßig auf die aktuelle Position eingestellt.</span><span class="sxs-lookup"><span data-stu-id="30dcc-150">If this flag is omitted, the position defaults to the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30dcc-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30dcc-151">Requirements</span></span>



| <span data-ttu-id="30dcc-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30dcc-152">Requirement</span></span> | <span data-ttu-id="30dcc-153">Wert</span><span class="sxs-lookup"><span data-stu-id="30dcc-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30dcc-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30dcc-154">Minimum supported client</span></span><br/> | <span data-ttu-id="30dcc-155">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30dcc-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="30dcc-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30dcc-156">Minimum supported server</span></span><br/> | <span data-ttu-id="30dcc-157">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30dcc-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="30dcc-158">Header</span><span class="sxs-lookup"><span data-stu-id="30dcc-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="30dcc-159"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30dcc-159"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30dcc-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30dcc-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30dcc-161">MCI</span><span class="sxs-lookup"><span data-stu-id="30dcc-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="30dcc-162">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="30dcc-162">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

