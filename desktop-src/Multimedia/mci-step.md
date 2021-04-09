---
title: MCI_STEP Befehl (MMSYSTEM. h)
description: Der MCI- \_ Schritt Befehl führt den Player um einen oder mehrere Frames. Videodisk-Geräte Digital Video, VCR und CAV-Format erkennen diesen Befehl.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- MCI_STEP Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102846"
---
# <a name="mci_step-command"></a><span data-ttu-id="be500-105">Befehl "MCI- \_ Schritt"</span><span class="sxs-lookup"><span data-stu-id="be500-105">MCI\_STEP command</span></span>

<span data-ttu-id="be500-106">Der MCI- \_ Schritt Befehl führt den Player um einen oder mehrere Frames.</span><span class="sxs-lookup"><span data-stu-id="be500-106">The MCI\_STEP command steps the player one or more frames.</span></span> <span data-ttu-id="be500-107">Videodisk-Geräte Digital Video, VCR und CAV-Format erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="be500-107">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="be500-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="be500-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
);
```



## <a name="parameters"></a><span data-ttu-id="be500-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="be500-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be500-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="be500-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="be500-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="be500-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="be500-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="be500-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="be500-113">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="be500-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="be500-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="be500-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="be500-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpstep*</span><span class="sxs-lookup"><span data-stu-id="be500-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span></span>
</dt> <dd>

<span data-ttu-id="be500-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="be500-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="be500-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="be500-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be500-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be500-118">Return Value</span></span>

<span data-ttu-id="be500-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="be500-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="be500-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be500-120">Remarks</span></span>

<span data-ttu-id="be500-121">Dieser Befehl unterstützt Geräte, die " **true** " zurückgeben, für das MCI \_ getdevcaps- \_ Video Kennzeichen \_ des Befehls [MCI \_ getdevcaps](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="be500-121">This command supports devices that return **TRUE** to the MCI\_GETDEVCAPS\_HAS\_VIDEO flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

<span data-ttu-id="be500-122">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="be500-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="be500-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI- \_ DGV- \_ Schritt \_ Rahmen</span><span class="sxs-lookup"><span data-stu-id="be500-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI\_DGV\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="be500-124">Der **dwframes** -Member der durch *lpstep* identifizierten-Struktur gibt die Anzahl der Frames an, die vor dem Anzeigen eines anderen Bilds fortgesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="be500-124">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="be500-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI- \_ DGV- \_ Schritt \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="be500-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI\_DGV\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="be500-126">Schritte in umgekehrter Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="be500-126">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="be500-127">Bei Digital-Video-Geräten verweist der *lpstep* -Parameter auf eine [**MCI- \_ DGV \_ \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="be500-127">For digital-video devices, the *lpStep* parameter points to an [**MCI\_DGV\_STEP\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) structure.</span></span>

<span data-ttu-id="be500-128">Die folgenden zusätzlichen Flags werden für den **VCR** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="be500-128">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="be500-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI- \_ VCR- \_ Schritt \_ Rahmen</span><span class="sxs-lookup"><span data-stu-id="be500-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI\_VCR\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="be500-130">Der **dwframes** -Member der durch *lpstep* identifizierten-Struktur gibt die Anzahl der Frames an, die vor dem Anzeigen eines anderen Bilds fortgesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="be500-130">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="be500-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI- \_ VCR- \_ Schritt \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="be500-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI\_VCR\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="be500-132">Schritte in umgekehrter Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="be500-132">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="be500-133">Bei VCR-Geräten verweist der *lpstep* -Parameter auf eine [**MCI- \_ VCR- \_ Schritt \_**](mci-vcr-step-parms.md) -Parameter-Struktur.</span><span class="sxs-lookup"><span data-stu-id="be500-133">For VCR devices, the *lpStep* parameter points to an [**MCI\_VCR\_STEP\_PARMS**](mci-vcr-step-parms.md) structure.</span></span>

<span data-ttu-id="be500-134">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp " **Videodisk** " verwendet:</span><span class="sxs-lookup"><span data-stu-id="be500-134">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="be500-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI- \_ VD- \_ Schritt- \_ Frames</span><span class="sxs-lookup"><span data-stu-id="be500-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI\_VD\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="be500-136">Der **dwframes** -Member der-Struktur, die von *lpstep* identifiziert wird, gibt die Anzahl der zu schrifenden Rahmen an.</span><span class="sxs-lookup"><span data-stu-id="be500-136">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to step.</span></span>

</dd> <dt>

<span data-ttu-id="be500-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI- \_ VD- \_ Schritt \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="be500-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI\_VD\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="be500-138">Schritte in umgekehrter Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="be500-138">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="be500-139">Bei Videodisk-Geräten verweist der *lpstep* -Parameter auf eine MCI-Schritt-für- [**\_ \_ Schritt \_**](mci-vd-step-parms.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="be500-139">For videodisc devices, the *lpStep* parameter points to an [**MCI\_VD\_STEP\_PARMS**](mci-vd-step-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="be500-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be500-140">Requirements</span></span>



| <span data-ttu-id="be500-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be500-141">Requirement</span></span> | <span data-ttu-id="be500-142">Wert</span><span class="sxs-lookup"><span data-stu-id="be500-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be500-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be500-143">Minimum supported client</span></span><br/> | <span data-ttu-id="be500-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be500-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be500-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be500-145">Minimum supported server</span></span><br/> | <span data-ttu-id="be500-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be500-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="be500-147">Header</span><span class="sxs-lookup"><span data-stu-id="be500-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="be500-148"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be500-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be500-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be500-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be500-150">MCI</span><span class="sxs-lookup"><span data-stu-id="be500-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="be500-151">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="be500-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

