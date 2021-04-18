---
title: MCI_REALIZE Befehl (MMSYSTEM. h)
description: Der MCI- \_ Befehl "überprüfen" bewirkt, dass die Palette eines Grafik Geräts in einem Gerätekontext (DC) erkannt wird. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- MCI_REALIZE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339145"
---
# <a name="mci_realize-command"></a><span data-ttu-id="75881-105">Befehl "MCI- \_ Umsetzung"</span><span class="sxs-lookup"><span data-stu-id="75881-105">MCI\_REALIZE command</span></span>

<span data-ttu-id="75881-106">Der MCI- \_ Befehl "überprüfen" bewirkt, dass die Palette eines Grafik Geräts in einem Gerätekontext (DC) erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="75881-106">The MCI\_REALIZE command causes a graphic device to realize its palette into a device context (DC).</span></span> <span data-ttu-id="75881-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="75881-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="75881-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="75881-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
);
```



## <a name="parameters"></a><span data-ttu-id="75881-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="75881-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75881-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="75881-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="75881-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="75881-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="75881-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="75881-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="75881-113">**MCI \_ Benachrichtigen**, **MCI- \_ Wartezeit** oder, für Digital-Video-Geräte, **MCI- \_ Test**.</span><span class="sxs-lookup"><span data-stu-id="75881-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="75881-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="75881-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="75881-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lprealize*</span><span class="sxs-lookup"><span data-stu-id="75881-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span></span>
</dt> <dd>

<span data-ttu-id="75881-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="75881-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="75881-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="75881-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75881-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75881-118">Return Value</span></span>

<span data-ttu-id="75881-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="75881-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="75881-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75881-120">Remarks</span></span>

<span data-ttu-id="75881-121">Sie sollten diesen Befehl verwenden, wenn die Anwendung die [**WM- \_ querynewpalette**](/windows/desktop/gdi/wm-querynewpalette) -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="75881-121">You should use this command when your application receives the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message.</span></span>

<span data-ttu-id="75881-122">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "Digitalvideo" verwendet:</span><span class="sxs-lookup"><span data-stu-id="75881-122">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="75881-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ realisiert \_ bkgd</span><span class="sxs-lookup"><span data-stu-id="75881-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI\_DGV\_REALIZE\_BKGD</span></span>
</dt> <dd>

<span data-ttu-id="75881-124">Erkennt die Palette als Hintergrund Palette.</span><span class="sxs-lookup"><span data-stu-id="75881-124">Realizes the palette as a background palette.</span></span>

</dd> <dt>

<span data-ttu-id="75881-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI \_ DGV-Integritäts \_ \_ Norm</span><span class="sxs-lookup"><span data-stu-id="75881-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI\_DGV\_REALIZE\_NORM</span></span>
</dt> <dd>

<span data-ttu-id="75881-126">Erkennt die Palette normal.</span><span class="sxs-lookup"><span data-stu-id="75881-126">Realizes the palette normally.</span></span> <span data-ttu-id="75881-127">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="75881-127">This is the default.</span></span>

</dd> </dl>

<span data-ttu-id="75881-128">Für Digital Video-Geräte verweist der *lprealize* -Parameter auf eine **MCI-Struktur zum \_ realisieren von \_ para** Metern.</span><span class="sxs-lookup"><span data-stu-id="75881-128">For digital-video devices, the *lpRealize* parameter points to an **MCI\_REALIZE\_PARMS** structure.</span></span> <span data-ttu-id="75881-129">Weitere Informationen finden Sie in den Kommentaren in der [**\_ generischen \_ MCI**](mci-generic-parms.md) -Struktur von Parametern.</span><span class="sxs-lookup"><span data-stu-id="75881-129">For more information, see comments in the [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="75881-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75881-130">Requirements</span></span>



| <span data-ttu-id="75881-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75881-131">Requirement</span></span> | <span data-ttu-id="75881-132">Wert</span><span class="sxs-lookup"><span data-stu-id="75881-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75881-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75881-133">Minimum supported client</span></span><br/> | <span data-ttu-id="75881-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75881-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="75881-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75881-135">Minimum supported server</span></span><br/> | <span data-ttu-id="75881-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75881-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="75881-137">Header</span><span class="sxs-lookup"><span data-stu-id="75881-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="75881-138"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75881-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75881-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75881-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75881-140">MCI</span><span class="sxs-lookup"><span data-stu-id="75881-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="75881-141">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="75881-141">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

