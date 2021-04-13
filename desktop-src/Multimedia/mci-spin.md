---
title: MCI_SPIN Befehl (MMSYSTEM. h)
description: Der Befehl "MCI \_ Spin" startet das Gerät nach oben oder unten. Videodisk-Geräte erkennen diesen Befehl.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- MCI_SPIN Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b154d9a2f54248ac6174e71a24d4afe74918d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391820"
---
# <a name="mci_spin-command"></a><span data-ttu-id="ceb0f-105">Befehl "MCI- \_ Spin"</span><span class="sxs-lookup"><span data-stu-id="ceb0f-105">MCI\_SPIN command</span></span>

<span data-ttu-id="ceb0f-106">Der Befehl "MCI \_ Spin" startet das Gerät nach oben oder unten.</span><span class="sxs-lookup"><span data-stu-id="ceb0f-106">The MCI\_SPIN command starts the device spinning up or down.</span></span> <span data-ttu-id="ceb0f-107">Videodisk-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="ceb0f-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="ceb0f-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="ceb0f-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
);
```



## <a name="parameters"></a><span data-ttu-id="ceb0f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ceb0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb0f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="ceb0f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ceb0f-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="ceb0f-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ceb0f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ceb0f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ceb0f-113">MCI- \_ Benachrichtigung oder MCI- \_ Wartezeit.</span><span class="sxs-lookup"><span data-stu-id="ceb0f-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="ceb0f-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ceb0f-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb0f-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpspin*</span><span class="sxs-lookup"><span data-stu-id="ceb0f-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span></span>
</dt> <dd>

<span data-ttu-id="ceb0f-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ceb0f-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="ceb0f-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="ceb0f-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceb0f-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ceb0f-118">Return Value</span></span>

<span data-ttu-id="ceb0f-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="ceb0f-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceb0f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ceb0f-120">Remarks</span></span>

<span data-ttu-id="ceb0f-121">Die folgenden zusätzlichen Flags gelten für Videodisk-Geräte:</span><span class="sxs-lookup"><span data-stu-id="ceb0f-121">The following additional flags apply to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="ceb0f-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI- \_ VD- \_ Spin- \_ Down</span><span class="sxs-lookup"><span data-stu-id="ceb0f-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI\_VD\_SPIN\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="ceb0f-123">Beendet das Drehen der CD.</span><span class="sxs-lookup"><span data-stu-id="ceb0f-123">Stops the disc spinning.</span></span>

</dd> <dt>

<span data-ttu-id="ceb0f-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI- \_ VD- \_ \_ Einrichtung</span><span class="sxs-lookup"><span data-stu-id="ceb0f-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI\_VD\_SPIN\_UP</span></span>
</dt> <dd>

<span data-ttu-id="ceb0f-125">Startet das Drehen der CD.</span><span class="sxs-lookup"><span data-stu-id="ceb0f-125">Starts the disc spinning.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ceb0f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ceb0f-126">Requirements</span></span>



| <span data-ttu-id="ceb0f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ceb0f-127">Requirement</span></span> | <span data-ttu-id="ceb0f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ceb0f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb0f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ceb0f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ceb0f-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ceb0f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ceb0f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ceb0f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ceb0f-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ceb0f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ceb0f-133">Header</span><span class="sxs-lookup"><span data-stu-id="ceb0f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceb0f-134"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ceb0f-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceb0f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ceb0f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb0f-136">MCI</span><span class="sxs-lookup"><span data-stu-id="ceb0f-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ceb0f-137">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="ceb0f-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

