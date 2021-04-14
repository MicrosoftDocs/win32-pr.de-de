---
title: MCI_SIGNAL Befehl (MMSYSTEM. h)
description: Mit dem Befehl MCI- \_ Signal wird eine angegebene Position im Arbeitsbereich festgelegt. Dieser Befehl wird von Digital-Video-Geräten erkannt. MCIAVI unterstützt jeweils nur ein aktives Signal.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- MCI_SIGNAL Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391821"
---
# <a name="mci_signal-command"></a><span data-ttu-id="a01a0-106">Befehl "MCI- \_ Signal"</span><span class="sxs-lookup"><span data-stu-id="a01a0-106">MCI\_SIGNAL command</span></span>

<span data-ttu-id="a01a0-107">Mit dem Befehl MCI- \_ Signal wird eine angegebene Position im Arbeitsbereich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a01a0-107">The MCI\_SIGNAL command sets a specified position in the workspace.</span></span> <span data-ttu-id="a01a0-108">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="a01a0-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="a01a0-109">MCIAVI unterstützt jeweils nur ein aktives Signal.</span><span class="sxs-lookup"><span data-stu-id="a01a0-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="a01a0-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="a01a0-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
);
```



## <a name="parameters"></a><span data-ttu-id="a01a0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a01a0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a01a0-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="a01a0-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a01a0-113">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="a01a0-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a01a0-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a01a0-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a01a0-115">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="a01a0-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="a01a0-116">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a01a0-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a01a0-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpsignal*</span><span class="sxs-lookup"><span data-stu-id="a01a0-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span></span>
</dt> <dd>

<span data-ttu-id="a01a0-118">Zeiger auf eine [**MCI- \_ DGV- \_ Signal \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a01a0-118">Pointer to an [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a01a0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a01a0-119">Return Value</span></span>

<span data-ttu-id="a01a0-120">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="a01a0-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a01a0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a01a0-121">Remarks</span></span>

<span data-ttu-id="a01a0-122">Das Fenster, dessen Handle Sie im **dwcallback** -Member der [**MCI- \_ DGV- \_ Signal- \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) -Struktur angeben, empfängt die mm \_ mcisignal-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a01a0-122">The window whose handle you specify in the **dwCallback** member of the [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure receives the MM\_MCISIGNAL message.</span></span>

<span data-ttu-id="a01a0-123">Die folgenden Flags gelten für Digital-Video-Geräte:</span><span class="sxs-lookup"><span data-stu-id="a01a0-123">The following flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="a01a0-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI \_ DGV- \_ Signal \_ bei</span><span class="sxs-lookup"><span data-stu-id="a01a0-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI\_DGV\_SIGNAL\_AT</span></span>
</dt> <dd>

<span data-ttu-id="a01a0-125">Eine Signal Position ist im **dwposition** -Member der durch *lpsignal* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="a01a0-125">A signal position is included in the **dwPosition** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="a01a0-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI- \_ DGV- \_ Signal \_ Abbruch</span><span class="sxs-lookup"><span data-stu-id="a01a0-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI\_DGV\_SIGNAL\_CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="a01a0-127">Entfernt die Signal Position, die durch den dem MCI- \_ DGV- \_ Signal userval zugeordneten Wert angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="a01a0-127">Removes the signal position specified by the value associated with MCI\_DGV\_SIGNAL\_USERVAL.</span></span>

</dd> <dt>

<span data-ttu-id="a01a0-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI- \_ DGV- \_ Signal \_ alle</span><span class="sxs-lookup"><span data-stu-id="a01a0-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI\_DGV\_SIGNAL\_EVERY</span></span>
</dt> <dd>

<span data-ttu-id="a01a0-129">Ein Signal Zeitraum-Wert ist im **dwperiod** -Member der durch *lpsignal* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="a01a0-129">A signal-period value is included in the **dwPeriod** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="a01a0-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI- \_ DGV- \_ Signal \_ Position</span><span class="sxs-lookup"><span data-stu-id="a01a0-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI\_DGV\_SIGNAL\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="a01a0-131">Das Gerät sendet den Positionswert nicht mit dem vom Benutzer angegebenen Wert, sondern mit der Windows-Meldung.</span><span class="sxs-lookup"><span data-stu-id="a01a0-131">The device will send the position value with the Windows message instead of the user-specified value.</span></span>

</dd> <dt>

<span data-ttu-id="a01a0-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI \_ DGV- \_ Signal \_ userval</span><span class="sxs-lookup"><span data-stu-id="a01a0-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI\_DGV\_SIGNAL\_USERVAL</span></span>
</dt> <dd>

<span data-ttu-id="a01a0-133">Ein Datenwert ist im **dwuserparamem** -Member der durch *lpsignal* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="a01a0-133">A data value is included in the **dwUserParm** member of the structure identified by *lpSignal*.</span></span> <span data-ttu-id="a01a0-134">Der Datenwert, der dieser Anforderung zugeordnet ist, wird mit der Windows-Meldung zurückgemeldet.</span><span class="sxs-lookup"><span data-stu-id="a01a0-134">The data value associated with this request is reported back with the Windows message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a01a0-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a01a0-135">Requirements</span></span>



| <span data-ttu-id="a01a0-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a01a0-136">Requirement</span></span> | <span data-ttu-id="a01a0-137">Wert</span><span class="sxs-lookup"><span data-stu-id="a01a0-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01a0-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a01a0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a01a0-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a01a0-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a01a0-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a01a0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a01a0-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a01a0-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a01a0-142">Header</span><span class="sxs-lookup"><span data-stu-id="a01a0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a01a0-143"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a01a0-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a01a0-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a01a0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a01a0-145">MCI</span><span class="sxs-lookup"><span data-stu-id="a01a0-145">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a01a0-146">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="a01a0-146">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

