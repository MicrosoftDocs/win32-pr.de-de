---
title: MCI_UPDATE Befehl (MMSYSTEM. h)
description: Der Befehl "MCI- \_ Update" aktualisiert das Anzeige Rechteck. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105909"
---
# <a name="mci_update-command"></a><span data-ttu-id="4eb8a-105">Befehl "MCI- \_ Update"</span><span class="sxs-lookup"><span data-stu-id="4eb8a-105">MCI\_UPDATE command</span></span>

<span data-ttu-id="4eb8a-106">Der Befehl "MCI- \_ Update" aktualisiert das Anzeige Rechteck.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-106">The MCI\_UPDATE command updates the display rectangle.</span></span> <span data-ttu-id="4eb8a-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="4eb8a-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="4eb8a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4eb8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb8a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="4eb8a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4eb8a-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="4eb8a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4eb8a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4eb8a-113">**MCI \_ Benachrichtigen**, **MCI- \_ Wartezeit** oder, für Digital-Video-Geräte, **MCI- \_ Test**.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="4eb8a-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4eb8a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="4eb8a-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpdest*</span><span class="sxs-lookup"><span data-stu-id="4eb8a-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="4eb8a-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="4eb8a-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="4eb8a-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="4eb8a-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb8a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4eb8a-118">Return Value</span></span>

<span data-ttu-id="4eb8a-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb8a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4eb8a-120">Remarks</span></span>

<span data-ttu-id="4eb8a-121">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "Digitalvideo" verwendet:</span><span class="sxs-lookup"><span data-stu-id="4eb8a-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="4eb8a-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI- \_ DGV- \_ Update- \_ hdc</span><span class="sxs-lookup"><span data-stu-id="4eb8a-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI\_DGV\_UPDATE\_HDC</span></span>
</dt> <dd>

<span data-ttu-id="4eb8a-123">Das **hdc** -Mitglied der durch *lpdest* identifizierten Struktur enthält ein gültiges Fenster des Domänen Controllers, das gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-123">The **hDC** member of the structure identified by *lpDest* contains a valid window of the DC to paint.</span></span> <span data-ttu-id="4eb8a-124">Dieses Flag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-124">This flag is required.</span></span>

</dd> <dt>

<span data-ttu-id="4eb8a-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI- \_ DGV- \_ Rect</span><span class="sxs-lookup"><span data-stu-id="4eb8a-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="4eb8a-126">Der **RC** -Member der durch *lpunfreeze* identifizierten Struktur enthält ein gültiges Anzeige Rechteck.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-126">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="4eb8a-127">Das Rechteck gibt das Clippingrechteck relativ zum Client Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-127">The rectangle specifies the clipping rectangle relative to the client rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="4eb8a-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI \_ DGV- \_ Update \_ Paint</span><span class="sxs-lookup"><span data-stu-id="4eb8a-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI\_DGV\_UPDATE\_PAINT</span></span>
</dt> <dd>

<span data-ttu-id="4eb8a-129">Eine Anwendung verwendet dieses Flag, wenn Sie eine [**WM \_**](/windows/desktop/gdi/wm-paint) -Zeichnungs Nachricht empfängt, die für einen Anzeige-DC vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-129">An application uses this flag when it receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message that is intended for a display DC.</span></span> <span data-ttu-id="4eb8a-130">Ein Frame Puffer Gerät zeichnet in der Regel die Schlüsselfarbe.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-130">A frame-buffer device usually paints the key color.</span></span> <span data-ttu-id="4eb8a-131">Wenn das Anzeigegerät nicht über einen Frame Puffer verfügt, wird möglicherweise der Befehl MCI-Update ignoriert, \_ Wenn das **MCI DGV-Flag zum \_ \_ Zeichnen von \_ Paint** verwendet wird, da die Anzeige während des Wiedergabe Vorgangs neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-131">If the display device does not have a frame buffer, it might ignore the MCI\_UPDATE command when the **MCI\_DGV\_UPDATE\_PAINT** flag is used because the display will be repainted during the playback operation.</span></span>

</dd> </dl>

<span data-ttu-id="4eb8a-132">Für Digital Video-Geräte verweist der *lpdest* -Parameter auf eine [**MCI- \_ DGV- \_ Update \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) -Parameter-Struktur.</span><span class="sxs-lookup"><span data-stu-id="4eb8a-132">For digital-video devices, the *lpDest* parameter points to an [**MCI\_DGV\_UPDATE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb8a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4eb8a-133">Requirements</span></span>



| <span data-ttu-id="4eb8a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4eb8a-134">Requirement</span></span> | <span data-ttu-id="4eb8a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4eb8a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb8a-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4eb8a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb8a-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4eb8a-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4eb8a-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4eb8a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb8a-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4eb8a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4eb8a-140">Header</span><span class="sxs-lookup"><span data-stu-id="4eb8a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb8a-141"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4eb8a-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb8a-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eb8a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb8a-143">MCI</span><span class="sxs-lookup"><span data-stu-id="4eb8a-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4eb8a-144">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="4eb8a-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

