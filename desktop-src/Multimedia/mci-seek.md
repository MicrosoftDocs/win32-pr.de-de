---
title: MCI_SEEK Befehl (MMSYSTEM. h)
description: Der MCI \_ Seek-Befehl ändert die aktuelle Position im Inhalt so schnell wie möglich.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- MCI_SEEK Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040297"
---
# <a name="mci_seek-command"></a><span data-ttu-id="c898a-104">Befehl "MCI- \_ Suche"</span><span class="sxs-lookup"><span data-stu-id="c898a-104">MCI\_SEEK command</span></span>

<span data-ttu-id="c898a-105">Der MCI \_ Seek-Befehl ändert die aktuelle Position im Inhalt so schnell wie möglich.</span><span class="sxs-lookup"><span data-stu-id="c898a-105">The MCI\_SEEK command changes the current position in the content as quickly as possible.</span></span> <span data-ttu-id="c898a-106">Die Video-und Audioausgabe sind während der Suche deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c898a-106">Video and audio output are disabled during the seek.</span></span> <span data-ttu-id="c898a-107">Nachdem die Suche beendet wurde, wird das Gerät beendet.</span><span class="sxs-lookup"><span data-stu-id="c898a-107">After the seek is complete, the device is stopped.</span></span> <span data-ttu-id="c898a-108">CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="c898a-108">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="c898a-109">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="c898a-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
);
```



## <a name="parameters"></a><span data-ttu-id="c898a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c898a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c898a-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="c898a-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c898a-112">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="c898a-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c898a-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c898a-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c898a-114">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="c898a-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="c898a-115">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c898a-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c898a-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpseek*</span><span class="sxs-lookup"><span data-stu-id="c898a-116"><span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*</span></span>
</dt> <dd>

<span data-ttu-id="c898a-117">Zeiger auf eine [**MCI \_ - \_ Such**](mci-seek-parms.md) Elementstruktur.</span><span class="sxs-lookup"><span data-stu-id="c898a-117">Pointer to an [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="c898a-118">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="c898a-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c898a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c898a-119">Return Value</span></span>

<span data-ttu-id="c898a-120">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c898a-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c898a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c898a-121">Remarks</span></span>

<span data-ttu-id="c898a-122">Wenn eine Daten Stichprobengröße für ein Gerät größer als 1 Byte ist (z. b. mit Waveform-audiostereo-Daten), wechselt dieser Befehl zum Anfang des nächsten Beispiels, wenn eine angegebene Position nicht mit dem Anfang eines Beispiels übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c898a-122">If a data sample size for a device is larger than 1 byte (such as with waveform-audio stereo data), this command moves to the beginning of the nearest sample when a specified position does not coincide with the start of a sample.</span></span>

<span data-ttu-id="c898a-123">Die folgenden zusätzlichen Flags gelten für alle Geräte, die die MCI-Suche unterstützen \_ :</span><span class="sxs-lookup"><span data-stu-id="c898a-123">The following additional flags apply to all devices supporting MCI\_SEEK:</span></span>

<dl> <dt>

<span data-ttu-id="c898a-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI \_ - \_ Suche \_ am Ende</span><span class="sxs-lookup"><span data-stu-id="c898a-124"><span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI\_SEEK\_TO\_END</span></span>
</dt> <dd>

<span data-ttu-id="c898a-125">Suchen Sie nach dem Ende des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="c898a-125">Seek to the end of the content.</span></span>

</dd> <dt>

<span data-ttu-id="c898a-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI \_ - \_ Suche \_ starten</span><span class="sxs-lookup"><span data-stu-id="c898a-126"><span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI\_SEEK\_TO\_START</span></span>
</dt> <dd>

<span data-ttu-id="c898a-127">Suchen Sie am Anfang des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="c898a-127">Seek to the beginning of the content.</span></span>

</dd> <dt>

<span data-ttu-id="c898a-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ zu</span><span class="sxs-lookup"><span data-stu-id="c898a-128"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="c898a-129">Eine Position ist im **dwto** -Member der durch *lpseek* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="c898a-129">A position is included in the **dwTo** member of the structure identified by *lpSeek*.</span></span> <span data-ttu-id="c898a-130">Die Einheiten, die den Positions Werten zugewiesen sind, werden mit dem MCI- \_ Flag zum Festlegen \_ \_ des Zeit Formats des Befehls [MCI \_ Set](mci-set.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="c898a-130">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span> <span data-ttu-id="c898a-131">Verwenden Sie dieses Flag nicht mit der MCI- \_ Suche \_ , um zu \_ \_ starten oder \_ zu \_ starten.</span><span class="sxs-lookup"><span data-stu-id="c898a-131">Do not use this flag with MCI\_SEEK\_TO\_END or MCI\_SEEK\_TO\_START.</span></span>

</dd> </dl>

<span data-ttu-id="c898a-132">Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="c898a-132">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c898a-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI \_ VCR- \_ Suche \_ unter</span><span class="sxs-lookup"><span data-stu-id="c898a-133"><span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>MCI\_VCR\_SEEK\_AT</span></span>
</dt> <dd>

<span data-ttu-id="c898a-134">Der **dwat** -Member der-Struktur, die von *lpseek* identifiziert wird, enthält einen Zeitpunkt, zu dem der gesamte Befehl beginnt.</span><span class="sxs-lookup"><span data-stu-id="c898a-134">The **dwAt** member of the structure identified by *lpSeek* contains a time when the entire command begins.</span></span>

</dd> <dt>

<span data-ttu-id="c898a-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI- \_ VCR- \_ Such \_ Zeichen</span><span class="sxs-lookup"><span data-stu-id="c898a-135"><span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>MCI\_VCR\_SEEK\_MARK</span></span>
</dt> <dd>

<span data-ttu-id="c898a-136">Der **dwmark** -Member der durch *lpseek* identifizierten Struktur enthält die nummerierte Markierung, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c898a-136">The **dwMark** member of the structure identified by *lpSeek* contains the numbered mark to search for.</span></span>

</dd> <dt>

<span data-ttu-id="c898a-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI \_ VCR- \_ Suche \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="c898a-137"><span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>MCI\_VCR\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="c898a-138">Die Suchrichtung ist umgekehrt. Diese wird nur mit dem Flag "MCI \_ VCR- \_ \_ suchflag" verwendet.</span><span class="sxs-lookup"><span data-stu-id="c898a-138">Seek direction is reverse; this is used only with the MCI\_VCR\_SEEK\_MARK flag.</span></span>

</dd> </dl>

<span data-ttu-id="c898a-139">Bei VCR-Geräten verweist der *lpseek* -Parameter auf eine [**MCI- \_ VCR- \_ suchparameterstruktur \_**](mci-vcr-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c898a-139">For VCR devices, the *lpSeek* parameter points to an [**MCI\_VCR\_SEEK\_PARMS**](mci-vcr-seek-parms.md) structure.</span></span>

<span data-ttu-id="c898a-140">Das folgende zusätzliche Flag wird für den **Videodisk** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="c898a-140">The following additional flag is used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="c898a-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI- \_ VD- \_ Suche \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="c898a-141"><span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI\_VD\_SEEK\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="c898a-142">Die Suchrichtung ist umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="c898a-142">Seek direction is reverse.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c898a-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c898a-143">Requirements</span></span>



| <span data-ttu-id="c898a-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c898a-144">Requirement</span></span> | <span data-ttu-id="c898a-145">Wert</span><span class="sxs-lookup"><span data-stu-id="c898a-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c898a-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c898a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c898a-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c898a-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c898a-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c898a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c898a-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c898a-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c898a-150">Header</span><span class="sxs-lookup"><span data-stu-id="c898a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c898a-151"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c898a-151"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c898a-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c898a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c898a-153">MCI</span><span class="sxs-lookup"><span data-stu-id="c898a-153">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c898a-154">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="c898a-154">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

