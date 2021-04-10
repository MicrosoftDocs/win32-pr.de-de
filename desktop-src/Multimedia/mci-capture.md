---
title: MCI_CAPTURE Befehl (MMSYSTEM. h)
description: Der MCI \_ -Aufzeichnungs Befehl erfasst den Inhalt des Frame Puffers und speichert ihn in einer angegebenen Datei. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- MCI_CAPTURE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956779"
---
# <a name="mci_capture-command"></a><span data-ttu-id="26e52-105">MCI- \_ Aufzeichnungs Befehl</span><span class="sxs-lookup"><span data-stu-id="26e52-105">MCI\_CAPTURE command</span></span>

<span data-ttu-id="26e52-106">Der MCI \_ -Aufzeichnungs Befehl erfasst den Inhalt des Frame Puffers und speichert ihn in einer angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="26e52-106">The MCI\_CAPTURE command captures the contents of the frame buffer and stores it in a specified file.</span></span> <span data-ttu-id="26e52-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="26e52-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="26e52-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="26e52-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a><span data-ttu-id="26e52-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="26e52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e52-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="26e52-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="26e52-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="26e52-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="26e52-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="26e52-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="26e52-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="26e52-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="26e52-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="26e52-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="26e52-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpcapture*</span><span class="sxs-lookup"><span data-stu-id="26e52-115"><span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*</span></span>
</dt> <dd>

<span data-ttu-id="26e52-116">Zeiger auf eine [**MCI- \_ DGV- \_ Erfassungs \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) Struktur.</span><span class="sxs-lookup"><span data-stu-id="26e52-116">Pointer to an [**MCI\_DGV\_CAPTURE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e52-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26e52-117">Return Value</span></span>

<span data-ttu-id="26e52-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="26e52-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="26e52-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26e52-119">Remarks</span></span>

<span data-ttu-id="26e52-120">Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:</span><span class="sxs-lookup"><span data-stu-id="26e52-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="26e52-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI- \_ DGV- \_ Erfassung \_ als</span><span class="sxs-lookup"><span data-stu-id="26e52-121"><span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI\_DGV\_CAPTURE\_AS</span></span>
</dt> <dd>

<span data-ttu-id="26e52-122">Der **lpstrinfilename** -Member der durch *lpcapture* identifizierten Struktur enthält die Adresse eines Puffers, der den Zielpfad und den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="26e52-122">The **lpstrFileName** member of the structure identified by *lpCapture* contains an address of a buffer specifying the destination path and filename.</span></span> <span data-ttu-id="26e52-123">(Dieses Flag ist erforderlich.)</span><span class="sxs-lookup"><span data-stu-id="26e52-123">(This flag is required.)</span></span>

</dd> <dt>

<span data-ttu-id="26e52-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI \_ DGV- \_ Erfassung \_ unter</span><span class="sxs-lookup"><span data-stu-id="26e52-124"><span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>MCI\_DGV\_CAPTURE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="26e52-125">Der **RC** -Member der durch *lpcapture* identifizierten Struktur enthält ein gültiges Rechteck.</span><span class="sxs-lookup"><span data-stu-id="26e52-125">The **rc** member of the structure identified by *lpCapture* contains a valid rectangle.</span></span> <span data-ttu-id="26e52-126">Das Rechteck gibt den rechteckigen Bereich innerhalb des Frame Puffers an, der abgeschnitten und auf dem Datenträger gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="26e52-126">The rectangle specifies the rectangular region within the frame buffer that is cropped and saved to disk.</span></span> <span data-ttu-id="26e52-127">Wenn der Wert nicht angegeben wird, wird der zugeschnittenen Bereich standardmäßig auf das Rechteck festgelegt oder standardmäßig auf einen vorherigen [MCI \_ Put](mci-put.md) -Befehl festgelegt, der den Quellbereich für diese Instanz des Gerätetreibers angibt.</span><span class="sxs-lookup"><span data-stu-id="26e52-127">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [MCI\_PUT](mci-put.md) command that specifies the source area for this instance of the device driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26e52-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26e52-128">Requirements</span></span>



| <span data-ttu-id="26e52-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26e52-129">Requirement</span></span> | <span data-ttu-id="26e52-130">Wert</span><span class="sxs-lookup"><span data-stu-id="26e52-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26e52-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26e52-131">Minimum supported client</span></span><br/> | <span data-ttu-id="26e52-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26e52-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="26e52-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26e52-133">Minimum supported server</span></span><br/> | <span data-ttu-id="26e52-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26e52-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="26e52-135">Header</span><span class="sxs-lookup"><span data-stu-id="26e52-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="26e52-136"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26e52-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e52-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26e52-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e52-138">MCI</span><span class="sxs-lookup"><span data-stu-id="26e52-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="26e52-139">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="26e52-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

