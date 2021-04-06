---
title: MCI_RESTORE Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Restore kopiert eine Bitmap aus einer Datei in den Frame Puffer. Dieser Befehl wird von Digital-Video-Geräten erkannt. Dieser Befehl führt die umgekehrte Aktion des MCI- \_ Erfassungs Befehls aus.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- MCI_RESTORE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742809"
---
# <a name="mci_restore-command"></a><span data-ttu-id="14717-106">MCI- \_ Restore-Befehl</span><span class="sxs-lookup"><span data-stu-id="14717-106">MCI\_RESTORE command</span></span>

<span data-ttu-id="14717-107">Der Befehl MCI \_ Restore kopiert eine Bitmap aus einer Datei in den Frame Puffer.</span><span class="sxs-lookup"><span data-stu-id="14717-107">The MCI\_RESTORE command copies a bitmap from a file to the frame buffer.</span></span> <span data-ttu-id="14717-108">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="14717-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="14717-109">Dieser Befehl führt die umgekehrte Aktion des [MCI- \_ Erfassungs](mci-capture.md) Befehls aus.</span><span class="sxs-lookup"><span data-stu-id="14717-109">This command performs the opposite action of the [MCI\_CAPTURE](mci-capture.md) command.</span></span>

<span data-ttu-id="14717-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="14717-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
);
```



## <a name="parameters"></a><span data-ttu-id="14717-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="14717-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14717-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="14717-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="14717-113">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="14717-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="14717-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="14717-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="14717-115">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="14717-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="14717-116">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="14717-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="14717-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lprestore*</span><span class="sxs-lookup"><span data-stu-id="14717-117"><span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*</span></span>
</dt> <dd>

<span data-ttu-id="14717-118">Zeiger auf eine [**MCI \_ DGV \_ Restore \_ -paramemstruktur**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="14717-118">Pointer to an [**MCI\_DGV\_RESTORE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14717-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14717-119">Return Value</span></span>

<span data-ttu-id="14717-120">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="14717-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="14717-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14717-121">Remarks</span></span>

<span data-ttu-id="14717-122">Die-Implementierung kann eine Vielzahl von Bildformaten erkennen, aber eine Windows-geräteunabhängige Bitmap (DIB) wird immer akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="14717-122">The implementation can recognize a variety of image formats, but a Windows device-independent bitmap (DIB) is always accepted.</span></span>

<span data-ttu-id="14717-123">Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:</span><span class="sxs-lookup"><span data-stu-id="14717-123">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="14717-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI \_ DGV- \_ Wiederherstellung \_ von</span><span class="sxs-lookup"><span data-stu-id="14717-124"><span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>MCI\_DGV\_RESTORE\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="14717-125">Der **lpstrinfilename** -Member der durch *lprestore* identifizierten Struktur enthält eine Adresse eines Puffers, der den Quell Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="14717-125">The **lpstrFileName** member of the structure identified by *lpRestore* contains an address of a buffer containing the source filename.</span></span> <span data-ttu-id="14717-126">Der Dateiname ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="14717-126">The filename is required.</span></span>

</dd> <dt>

<span data-ttu-id="14717-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI \_ DGV- \_ Wiederherstellung \_ unter</span><span class="sxs-lookup"><span data-stu-id="14717-127"><span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>MCI\_DGV\_RESTORE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="14717-128">Der **RC** -Member der durch *lprestore* identifizierten Struktur enthält ein gültiges Rechteck.</span><span class="sxs-lookup"><span data-stu-id="14717-128">The **rc** member of the structure identified by *lpRestore* contains a valid rectangle.</span></span> <span data-ttu-id="14717-129">Das Rechteck gibt einen Bereich des Frame Puffers relativ zum Ursprung an.</span><span class="sxs-lookup"><span data-stu-id="14717-129">The rectangle specifies a region of the frame buffer relative to its origin.</span></span> <span data-ttu-id="14717-130">Das erste Koordinaten paar gibt die linke obere Ecke des Rechtecks an. Das zweite paar gibt die Breite und Höhe an.</span><span class="sxs-lookup"><span data-stu-id="14717-130">The first pair of coordinates specifies the upper left corner of the rectangle; the second pair specifies the width and height.</span></span> <span data-ttu-id="14717-131">Wenn dieses Flag nicht angegeben wird, wird das Bild in die linke obere Ecke des Frame Puffers kopiert.</span><span class="sxs-lookup"><span data-stu-id="14717-131">If this flag is not specified, the image is copied to the upper left corner of the frame buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14717-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14717-132">Requirements</span></span>



| <span data-ttu-id="14717-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14717-133">Requirement</span></span> | <span data-ttu-id="14717-134">Wert</span><span class="sxs-lookup"><span data-stu-id="14717-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14717-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14717-135">Minimum supported client</span></span><br/> | <span data-ttu-id="14717-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14717-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="14717-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14717-137">Minimum supported server</span></span><br/> | <span data-ttu-id="14717-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14717-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="14717-139">Header</span><span class="sxs-lookup"><span data-stu-id="14717-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="14717-140"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14717-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14717-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14717-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14717-142">MCI</span><span class="sxs-lookup"><span data-stu-id="14717-142">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="14717-143">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="14717-143">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

