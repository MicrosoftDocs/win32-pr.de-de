---
title: MCI_MARK Befehl (MMSYSTEM. h)
description: Mit dem Befehl MCI \_ Mark werden Markierungen aufgezeichnet oder gelöscht, die mit dem MCI-Such \_ Befehl für hoch Geschwindigkeits Suchvorgänge verwendet werden können. VCR-Geräte erkennen diesen Befehl.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- MCI_MARK Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040299"
---
# <a name="mci_mark-command"></a><span data-ttu-id="c9133-105">Befehl "MCI- \_ Markierung"</span><span class="sxs-lookup"><span data-stu-id="c9133-105">MCI\_MARK command</span></span>

<span data-ttu-id="c9133-106">Mit dem Befehl MCI \_ Mark werden Markierungen aufgezeichnet oder gelöscht, die mit dem MCI-Suchbefehl für hoch Geschwindigkeits [ \_ Suchvorgänge](mci-seek.md) verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c9133-106">The MCI\_MARK command records or erases marks that can be used with the [MCI\_SEEK](mci-seek.md) command for high-speed searches.</span></span> <span data-ttu-id="c9133-107">VCR-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="c9133-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="c9133-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="c9133-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
);
```



## <a name="parameters"></a><span data-ttu-id="c9133-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9133-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9133-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="c9133-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c9133-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="c9133-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c9133-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c9133-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c9133-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="c9133-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="c9133-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c9133-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9133-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpmark*</span><span class="sxs-lookup"><span data-stu-id="c9133-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span></span>
</dt> <dd>

<span data-ttu-id="c9133-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c9133-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="c9133-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="c9133-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9133-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9133-118">Return Value</span></span>

<span data-ttu-id="c9133-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c9133-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9133-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9133-120">Remarks</span></span>

<span data-ttu-id="c9133-121">Die folgenden zusätzlichen Flags gelten für VCR-Geräte:</span><span class="sxs-lookup"><span data-stu-id="c9133-121">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="c9133-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI- \_ VCR- \_ Markierung \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="c9133-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI\_VCR\_MARK\_ERASE</span></span>
</dt> <dd>

<span data-ttu-id="c9133-123">Löscht eine Markierung an der aktuellen Position, wenn eine Markierung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c9133-123">Erases a mark at the current position if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="c9133-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI- \_ VCR- \_ Markierung \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="c9133-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI\_VCR\_MARK\_WRITE</span></span>
</dt> <dd>

<span data-ttu-id="c9133-125">Schreibt eine Markierung an der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="c9133-125">Writes a mark at the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9133-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9133-126">Requirements</span></span>



| <span data-ttu-id="c9133-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9133-127">Requirement</span></span> | <span data-ttu-id="c9133-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c9133-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9133-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9133-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9133-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9133-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c9133-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9133-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9133-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9133-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c9133-133">Header</span><span class="sxs-lookup"><span data-stu-id="c9133-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9133-134"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9133-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9133-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9133-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9133-136">MCI</span><span class="sxs-lookup"><span data-stu-id="c9133-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c9133-137">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="c9133-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

