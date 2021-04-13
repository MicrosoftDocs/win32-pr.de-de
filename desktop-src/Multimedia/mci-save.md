---
title: MCI_SAVE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl Save speichert die aktuelle Datei.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- MCI_SAVE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475693"
---
# <a name="mci_save-command"></a><span data-ttu-id="aa89b-104">Befehl zum Speichern von MCI \_</span><span class="sxs-lookup"><span data-stu-id="aa89b-104">MCI\_SAVE command</span></span>

<span data-ttu-id="aa89b-105">Der MCI- \_ Befehl Save speichert die aktuelle Datei.</span><span class="sxs-lookup"><span data-stu-id="aa89b-105">The MCI\_SAVE command saves the current file.</span></span> <span data-ttu-id="aa89b-106">Geräte, die Dateien ändern, sollten die ursprüngliche Kopie erst zerstören, wenn Sie die Speicher Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="aa89b-106">Devices that modify files should not destroy the original copy until they receive the save message.</span></span> <span data-ttu-id="aa89b-107">Video-Overlay-und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="aa89b-107">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="aa89b-108">Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI-und mciseq-Treiber Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="aa89b-108">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not implement it.</span></span>

<span data-ttu-id="aa89b-109">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="aa89b-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
);
```



## <a name="parameters"></a><span data-ttu-id="aa89b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa89b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa89b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="aa89b-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="aa89b-112">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="aa89b-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="aa89b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="aa89b-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="aa89b-114">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="aa89b-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="aa89b-115">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="aa89b-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa89b-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpsave*</span><span class="sxs-lookup"><span data-stu-id="aa89b-116"><span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*</span></span>
</dt> <dd>

<span data-ttu-id="aa89b-117">Zeiger auf eine [**MCI-Struktur zum \_ Speichern von \_ Parametern**](mci-save-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="aa89b-117">Pointer to an [**MCI\_SAVE\_PARMS**](mci-save-parms.md) structure.</span></span> <span data-ttu-id="aa89b-118">(Geräte mit zusätzlichen Parametern können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="aa89b-118">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa89b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa89b-119">Return Value</span></span>

<span data-ttu-id="aa89b-120">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="aa89b-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa89b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa89b-121">Remarks</span></span>

<span data-ttu-id="aa89b-122">Dieser Befehl wird von Geräten unterstützt, die " **true** " zurückgeben, wenn Sie den [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl mit dem MCI \_ getdevcaps- \_ Flag " \_ Save Save" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="aa89b-122">This command is supported by devices that return **TRUE** when you call the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command with the MCI\_GETDEVCAPS\_CAN\_SAVE flag.</span></span>

<span data-ttu-id="aa89b-123">Das folgende zusätzliche Flag gilt für alle Geräte, die [MCI- \_ Speicher](/windows)unterstützen:</span><span class="sxs-lookup"><span data-stu-id="aa89b-123">The following additional flag applies to all devices supporting [MCI\_SAVE](/windows):</span></span>

<dl> <dt>

<span data-ttu-id="aa89b-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI \_ - \_ Datei speichern</span><span class="sxs-lookup"><span data-stu-id="aa89b-124"><span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>MCI\_SAVE\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="aa89b-125">Der **lpFileName** -Member der durch *lpsave* identifizierten Struktur enthält eine Adresse eines Puffers, der den Ziel Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="aa89b-125">The **lpfilename** member of the structure identified by *lpSave* contains an address of a buffer containing the destination filename.</span></span>

</dd> </dl>

<span data-ttu-id="aa89b-126">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="aa89b-126">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="aa89b-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI- \_ DGV- \_ Rect</span><span class="sxs-lookup"><span data-stu-id="aa89b-127"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="aa89b-128">Der **RC** -Member der durch *lpsave* identifizierten Struktur enthält ein gültiges Rechteck.</span><span class="sxs-lookup"><span data-stu-id="aa89b-128">The **rc** member of the structure identified by *lpSave* contains a valid rectangle.</span></span> <span data-ttu-id="aa89b-129">Das Rechteck gibt einen Bereich des Frame Puffers an, der in der angegebenen Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="aa89b-129">The rectangle specifies a region of the frame buffer that will be saved to the specified file.</span></span> <span data-ttu-id="aa89b-130">Das erste Koordinaten paar gibt die linke obere Ecke des Rechtecks an. Das zweite paar gibt die Breite und Höhe an.</span><span class="sxs-lookup"><span data-stu-id="aa89b-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="aa89b-131">Digital Video-Geräte müssen den [MCI- \_ Erfassungs](mci-capture.md) Befehl verwenden, um den Inhalt des Frame Puffers aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="aa89b-131">Digital-video devices must use the [MCI\_CAPTURE](mci-capture.md) command to capture the contents of the frame buffer.</span></span> <span data-ttu-id="aa89b-132">(Video Überlagerungs Geräte sollten auch MCI \_ verwenden Erfassen.) Dieses Flag ist aus Gründen der Kompatibilität mit dem vorhandenen MCI-Video-Overlay-Befehlssatz.</span><span class="sxs-lookup"><span data-stu-id="aa89b-132">(Video-overlay devices should also use MCI\_CAPTURE.) This flag is for compatibility with the existing MCI video-overlay command set.</span></span>

</dd> <dt>

<span data-ttu-id="aa89b-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI- \_ DGV- \_ Speicher \_ Abbruch</span><span class="sxs-lookup"><span data-stu-id="aa89b-133"><span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>MCI\_DGV\_SAVE\_ABORT</span></span>
</dt> <dd>

<span data-ttu-id="aa89b-134">Beendet einen aktuell ausgeführten Speichervorgang.</span><span class="sxs-lookup"><span data-stu-id="aa89b-134">Stops a save operation in progress.</span></span> <span data-ttu-id="aa89b-135">Dies muss das einzige Flag sein, das vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aa89b-135">This must be the only flag present.</span></span>

</dd> <dt>

<span data-ttu-id="aa89b-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ Save \_ keepreserve</span><span class="sxs-lookup"><span data-stu-id="aa89b-136"><span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI\_DGV\_SAVE\_KEEPRESERVE</span></span>
</dt> <dd>

<span data-ttu-id="aa89b-137">Nicht verwendeter Speicherplatz aus dem ursprünglichen [MCI- \_ Reserve](mci-reserve.md) Befehl wird nicht aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="aa89b-137">Unused disk space left over from the original [MCI\_RESERVE](mci-reserve.md) command is not deallocated.</span></span>

</dd> </dl>

<span data-ttu-id="aa89b-138">Für Digital Video-Geräte zeigt der *lpsave* -Parameter auf eine [**MCI \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) -Struktur zum Speichern von Parametern.</span><span class="sxs-lookup"><span data-stu-id="aa89b-138">For digital-video devices, the *lpSave* parameter points to an [**MCI\_DGV\_SAVE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) structure.</span></span>

<span data-ttu-id="aa89b-139">Das folgende zusätzliche Flag wird mit dem **Überlagerungs** Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="aa89b-139">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="aa89b-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="aa89b-140"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="aa89b-141">Der **RC** -Member der durch *lpsave* identifizierten Struktur enthält ein gültiges Anzeige Rechteck, das den Bereich des zu speichernden Video Puffers angibt.</span><span class="sxs-lookup"><span data-stu-id="aa89b-141">The **rc** member of the structure identified by *lpSave* contains a valid display rectangle indicating the area of the video buffer to save.</span></span>

</dd> </dl>

<span data-ttu-id="aa89b-142">Bei Video Überlagerungs Geräten verweist der *lpsave* -Parameter auf eine [**MCI- \_ OVLY- \_ Speicher \_**](/previous-versions//dd743447(v=vs.85)) Struktur.</span><span class="sxs-lookup"><span data-stu-id="aa89b-142">For video-overlay devices, the *lpSave* parameter points to an [**MCI\_OVLY\_SAVE\_PARMS**](/previous-versions//dd743447(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa89b-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa89b-143">Requirements</span></span>



| <span data-ttu-id="aa89b-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa89b-144">Requirement</span></span> | <span data-ttu-id="aa89b-145">Wert</span><span class="sxs-lookup"><span data-stu-id="aa89b-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa89b-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa89b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="aa89b-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa89b-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aa89b-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa89b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="aa89b-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa89b-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aa89b-150">Header</span><span class="sxs-lookup"><span data-stu-id="aa89b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa89b-151"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa89b-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa89b-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa89b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa89b-153">MCI</span><span class="sxs-lookup"><span data-stu-id="aa89b-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="aa89b-154">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="aa89b-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

