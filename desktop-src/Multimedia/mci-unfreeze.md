---
title: MCI_UNFREEZE Befehl (MMSYSTEM. h)
description: Der MCI-Befehl zum Aufheben der Fixierung \_ stellt die Bewegung in einem Bereich des Video Puffers wieder her, der mit dem Befehl MCI Freeze eingefroren ist \_ . Dieser Befehl wird von digitalen Video-, VCR-und Video Überlagerungs Geräten erkannt.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- MCI_UNFREEZE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105914"
---
# <a name="mci_unfreeze-command"></a><span data-ttu-id="33893-105">MCI-Befehl zum Einfrieren der Fixierung \_</span><span class="sxs-lookup"><span data-stu-id="33893-105">MCI\_UNFREEZE command</span></span>

<span data-ttu-id="33893-106">Der MCI-Befehl zum Aufheben der Fixierung \_ stellt die Bewegung in einem Bereich des Video Puffers wieder her, der mit dem Befehl [MCI \_ Freeze](mci-freeze.md) eingefroren ist.</span><span class="sxs-lookup"><span data-stu-id="33893-106">The MCI\_UNFREEZE command restores motion to an area of the video buffer frozen with the [MCI\_FREEZE](mci-freeze.md) command.</span></span> <span data-ttu-id="33893-107">Dieser Befehl wird von digitalen Video-, VCR-und Video Überlagerungs Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="33893-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="33893-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="33893-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
);
```



## <a name="parameters"></a><span data-ttu-id="33893-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="33893-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33893-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="33893-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="33893-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="33893-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="33893-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="33893-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="33893-113">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="33893-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="33893-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="33893-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="33893-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpunfreeze*</span><span class="sxs-lookup"><span data-stu-id="33893-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="33893-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="33893-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="33893-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="33893-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33893-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33893-118">Return Value</span></span>

<span data-ttu-id="33893-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="33893-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="33893-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33893-120">Remarks</span></span>

<span data-ttu-id="33893-121">Das folgende zusätzliche Flag wird mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="33893-121">The following additional flag is used with the **digitalvideo** device type:</span></span>

<span data-ttu-id="33893-122">MCI- \_ DGV- \_ Rect</span><span class="sxs-lookup"><span data-stu-id="33893-122">MCI\_DGV\_RECT</span></span>

<span data-ttu-id="33893-123">Der **RC** -Member der durch *lpunfreeze* identifizierten Struktur enthält ein gültiges Anzeige Rechteck.</span><span class="sxs-lookup"><span data-stu-id="33893-123">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="33893-124">Das Rechteck gibt einen Bereich innerhalb des Frame Puffers an, dessen Pixel das Sperr Masken Bit deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="33893-124">The rectangle specifies a region within the frame buffer whose pixels should have their lock mask bit turned off.</span></span> <span data-ttu-id="33893-125">Rechteckige Bereiche werden wie für den Befehl [MCI \_ Put](mci-put.md) beschrieben angegeben.</span><span class="sxs-lookup"><span data-stu-id="33893-125">Rectangular regions are specified as described for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="33893-126">Wenn der Wert ausgelassen wird, wird das Rechteck standardmäßig auf den gesamten Frame Puffer eingestellt.</span><span class="sxs-lookup"><span data-stu-id="33893-126">If omitted, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="33893-127">Mithilfe einer Sequenz von Freeze-und Fixierung aufheben-Befehlen mit unterschiedlichen Rechtecke können beliebige Muster von Sperr Masken Bits beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="33893-127">By using a sequence of freeze and unfreeze commands with different rectangles, arbitrary patterns of lock mask bits can be described.</span></span>

<span data-ttu-id="33893-128">Für Digital Video-Geräte zeigt der *lpunfreeze* -Parameter auf eine **MCI \_ DGV \_ \_** -Struktur zum Aufheben der Fixierung von Parametern.</span><span class="sxs-lookup"><span data-stu-id="33893-128">For digital-video devices, the *lpUnfreeze* parameter points to an **MCI\_DGV\_UNFREEZE\_PARMS** structure.</span></span> <span data-ttu-id="33893-129">Weitere Informationen finden Sie in den Kommentaren für die [**MCI-DGV-Struktur " \_ \_ Rect- \_ Parser**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) ".</span><span class="sxs-lookup"><span data-stu-id="33893-129">For more information, see the comments for the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="33893-130">Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="33893-130">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="33893-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI \_ VCR- \_ einfrierende \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="33893-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI\_VCR\_UNFREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="33893-132">Entsperrung der Eingabe.</span><span class="sxs-lookup"><span data-stu-id="33893-132">Unfreeze the input.</span></span>

</dd> <dt>

<span data-ttu-id="33893-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI \_ VCR- \_ Ausgabe wird eingefroren \_</span><span class="sxs-lookup"><span data-stu-id="33893-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI\_VCR\_UNFREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="33893-134">Heben Sie die Fixierung der Ausgabe auf.</span><span class="sxs-lookup"><span data-stu-id="33893-134">Unfreeze the output.</span></span>

</dd> </dl>

<span data-ttu-id="33893-135">Das folgende zusätzliche Flag wird mit dem **Überlagerungs** Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="33893-135">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="33893-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="33893-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="33893-137">Der **RC** -Member der durch *lpunfreeze* identifizierten Struktur enthält ein gültiges Anzeige Rechteck.</span><span class="sxs-lookup"><span data-stu-id="33893-137">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="33893-138">Dies ist ein erforderlicher Parameter.</span><span class="sxs-lookup"><span data-stu-id="33893-138">This is a required parameter.</span></span>

</dd> </dl>

<span data-ttu-id="33893-139">Bei Video Überlagerungs Geräten zeigt der *lpunfreeze* -Parameter auf eine MCI-Struktur mit [**\_ OVLY \_ Rect- \_ para**](mci-ovly-rect-parms.md) Metern.</span><span class="sxs-lookup"><span data-stu-id="33893-139">For video-overlay devices, the *lpUnfreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="33893-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33893-140">Requirements</span></span>



| <span data-ttu-id="33893-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33893-141">Requirement</span></span> | <span data-ttu-id="33893-142">Wert</span><span class="sxs-lookup"><span data-stu-id="33893-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33893-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33893-143">Minimum supported client</span></span><br/> | <span data-ttu-id="33893-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33893-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="33893-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33893-145">Minimum supported server</span></span><br/> | <span data-ttu-id="33893-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33893-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="33893-147">Header</span><span class="sxs-lookup"><span data-stu-id="33893-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="33893-148"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33893-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33893-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33893-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33893-150">MCI</span><span class="sxs-lookup"><span data-stu-id="33893-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="33893-151">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="33893-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

