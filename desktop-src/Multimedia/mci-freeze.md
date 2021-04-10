---
title: MCI_FREEZE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Freeze-Befehl friert die Bewegung auf der Anzeige. Dieser Befehl wird von Digital Video, Video Overlay und VCR-Geräten erkannt.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- MCI_FREEZE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040302"
---
# <a name="mci_freeze-command"></a><span data-ttu-id="0510d-105">MCI- \_ Freeze-Befehl</span><span class="sxs-lookup"><span data-stu-id="0510d-105">MCI\_FREEZE command</span></span>

<span data-ttu-id="0510d-106">Der MCI- \_ Freeze-Befehl friert die Bewegung auf der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="0510d-106">The MCI\_FREEZE command freezes motion on the display.</span></span> <span data-ttu-id="0510d-107">Dieser Befehl wird von Digital Video, Video Overlay und VCR-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="0510d-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="0510d-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="0510d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
);
```



## <a name="parameters"></a><span data-ttu-id="0510d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0510d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0510d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="0510d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0510d-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="0510d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="0510d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="0510d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0510d-113">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="0510d-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="0510d-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0510d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="0510d-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpfreeze*</span><span class="sxs-lookup"><span data-stu-id="0510d-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span></span>
</dt> <dd>

<span data-ttu-id="0510d-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="0510d-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="0510d-117">(Geräte mit zusätzlichen Parametern können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="0510d-117">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0510d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0510d-118">Return Value</span></span>

<span data-ttu-id="0510d-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="0510d-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0510d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0510d-120">Remarks</span></span>

<span data-ttu-id="0510d-121">Die folgenden zusätzlichen Flags werden vom **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="0510d-121">The following additional flags are used by the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="0510d-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI \_ DGV- \_ Sperrung \_ bei</span><span class="sxs-lookup"><span data-stu-id="0510d-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI\_DGV\_FREEZE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="0510d-123">Der **RC** -Member der durch *lpfreeze* identifizierten Struktur enthält ein gültiges Rechteck.</span><span class="sxs-lookup"><span data-stu-id="0510d-123">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="0510d-124">Das Rechteck gibt einen Bereich innerhalb des Frame Puffers an, für den das Sperr Masken Bit für jedes Pixel aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="0510d-124">The rectangle specifies a region within the frame buffer that will have the lock mask bit for each pixel turned on.</span></span> <span data-ttu-id="0510d-125">Die angegebenen Pixel werden erst aktualisiert, wenn das Sperr Masken Bit ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="0510d-125">The specified pixels will not be updated until their lock mask bit is turned off.</span></span> <span data-ttu-id="0510d-126">Wenn dieses Flag nicht angegeben wird, wird das Rechteck standardmäßig auf den gesamten Frame Puffer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0510d-126">If this flag is not specified, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="0510d-127">Dieses Flag wird nur unterstützt, wenn der [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl **true** zurückgibt, wenn das MCI \_ DGV- \_ Flag "getdevcaps-Lock" das \_ \_ Flag "</span><span class="sxs-lookup"><span data-stu-id="0510d-127">This flag is supported only if the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command returns **TRUE** for the MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK flag.</span></span>

</dd> <dt>

<span data-ttu-id="0510d-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI \_ DGV- \_ Sperrung \_ außerhalb</span><span class="sxs-lookup"><span data-stu-id="0510d-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI\_DGV\_FREEZE\_OUTSIDE</span></span>
</dt> <dd>

<span data-ttu-id="0510d-129">Der Bereich außerhalb der Region, der für das MCI DGV-Flag zum Fixieren bei festgelegt wurde, \_ \_ ist fixiert \_ .</span><span class="sxs-lookup"><span data-stu-id="0510d-129">The area outside the region specified for the MCI\_DGV\_FREEZE\_AT flag is frozen.</span></span>

</dd> </dl>

<span data-ttu-id="0510d-130">Bei Digital-Video-Geräten verweist der *lpfreeze* -Parameter auf eine [**MCI \_ DGV- \_ \_ sparstrukturstruktur**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="0510d-130">For digital-video devices, the *lpFreeze* parameter points to an [**MCI\_DGV\_FREEZE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="0510d-131">Die folgenden zusätzlichen Flags werden vom **VCR** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="0510d-131">The following additional flags are used by the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="0510d-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI \_ VCR-Sperr \_ \_ Feld</span><span class="sxs-lookup"><span data-stu-id="0510d-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI\_VCR\_FREEZE\_FIELD</span></span>
</dt> <dd>

<span data-ttu-id="0510d-133">Fixiert nur einen Member des aktuellen Frames.</span><span class="sxs-lookup"><span data-stu-id="0510d-133">Freeze only one member of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="0510d-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI \_ VCR- \_ Freeze- \_ Frame</span><span class="sxs-lookup"><span data-stu-id="0510d-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI\_VCR\_FREEZE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="0510d-135">Fixiert beide Felder des aktuellen Frames.</span><span class="sxs-lookup"><span data-stu-id="0510d-135">Freeze both fields of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="0510d-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI \_ VCR- \_ Freeze- \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="0510d-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI\_VCR\_FREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="0510d-137">Fixiert den aktuellen Frame auf dem Bildschirm (wird für die Aufzeichnung verwendet).</span><span class="sxs-lookup"><span data-stu-id="0510d-137">Freeze the current frame on the screen (used for recording).</span></span>

</dd> <dt>

<span data-ttu-id="0510d-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI \_ VCR- \_ Freeze- \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="0510d-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI\_VCR\_FREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="0510d-139">Fixieren Sie den aktuellen Frame aus der VCR (verwendet mit Frame Erfassung).</span><span class="sxs-lookup"><span data-stu-id="0510d-139">Freeze the current frame from the VCR (used with frame capture).</span></span>

</dd> </dl>

<span data-ttu-id="0510d-140">Bei VCR-Geräten verweist der *lpfreeze* -Parameter auf eine [**generische MCI \_ \_**](mci-generic-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="0510d-140">For VCR devices, the *lpFreeze* parameter points to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

<span data-ttu-id="0510d-141">Das folgende zusätzliche Flag wird vom **überlagerungsgerätetyp** verwendet:</span><span class="sxs-lookup"><span data-stu-id="0510d-141">The following additional flag is used by the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="0510d-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="0510d-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="0510d-143">Der **RC** -Member der durch *lpfreeze* identifizierten Struktur enthält ein gültiges Rechteck.</span><span class="sxs-lookup"><span data-stu-id="0510d-143">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="0510d-144">Wenn dieses Flag nicht angegeben wird, fixiert der Gerätetreiber den gesamten Frame.</span><span class="sxs-lookup"><span data-stu-id="0510d-144">If this flag is not specified, the device driver will freeze the entire frame.</span></span>

</dd> </dl>

<span data-ttu-id="0510d-145">Bei Video Überlagerungs Geräten zeigt der *lpfreeze* -Parameter auf eine MCI-Struktur mit [**\_ OVLY \_ Rect- \_ para**](mci-ovly-rect-parms.md) Metern.</span><span class="sxs-lookup"><span data-stu-id="0510d-145">For video-overlay devices, the *lpFreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0510d-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0510d-146">Requirements</span></span>



| <span data-ttu-id="0510d-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0510d-147">Requirement</span></span> | <span data-ttu-id="0510d-148">Wert</span><span class="sxs-lookup"><span data-stu-id="0510d-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0510d-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0510d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0510d-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0510d-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0510d-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0510d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0510d-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0510d-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0510d-153">Header</span><span class="sxs-lookup"><span data-stu-id="0510d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="0510d-154"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0510d-154"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0510d-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0510d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0510d-156">MCI</span><span class="sxs-lookup"><span data-stu-id="0510d-156">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0510d-157">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="0510d-157">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

