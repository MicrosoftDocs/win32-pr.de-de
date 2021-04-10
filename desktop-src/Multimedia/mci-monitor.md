---
title: MCI_MONITOR Befehl (MMSYSTEM. h)
description: Der MCI- \_ Monitor-Befehl gibt die Präsentations Quelle an. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- MCI_MONITOR Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956776"
---
# <a name="mci_monitor-command"></a><span data-ttu-id="7b41d-105">MCI- \_ Monitor (Befehl)</span><span class="sxs-lookup"><span data-stu-id="7b41d-105">MCI\_MONITOR command</span></span>

<span data-ttu-id="7b41d-106">Der MCI- \_ Monitor-Befehl gibt die Präsentations Quelle an.</span><span class="sxs-lookup"><span data-stu-id="7b41d-106">The MCI\_MONITOR command specifies the presentation source.</span></span> <span data-ttu-id="7b41d-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="7b41d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="7b41d-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="7b41d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="7b41d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b41d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b41d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="7b41d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7b41d-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="7b41d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="7b41d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7b41d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7b41d-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="7b41d-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="7b41d-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7b41d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b41d-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpmonitor*</span><span class="sxs-lookup"><span data-stu-id="7b41d-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="7b41d-116">Zeiger auf eine [**MCI- \_ DGV- \_ Monitor \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7b41d-116">Pointer to an [**MCI\_DGV\_MONITOR\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b41d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b41d-117">Return Value</span></span>

<span data-ttu-id="7b41d-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="7b41d-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b41d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b41d-119">Remarks</span></span>

<span data-ttu-id="7b41d-120">Die folgenden zusätzlichen Flags gelten für Digital-Video-Geräte:</span><span class="sxs-lookup"><span data-stu-id="7b41d-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="7b41d-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI- \_ DGV- \_ Monitor \_ Methode</span><span class="sxs-lookup"><span data-stu-id="7b41d-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI\_DGV\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="7b41d-122">Eine-Konstante, die angibt, dass die Überwachungsmethode im **dwmethod** -Member der von *lpmonitor* identifizierten Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7b41d-122">A constant indicating the method of monitoring is included in the **dwMethod** member of the structure identified by *lpMonitor*.</span></span>

<span data-ttu-id="7b41d-123">Wenn das Eingabe Kennzeichen für das MCI- \_ DGV- \_ Monitor \_ im **dwsource** -Member verwendet wird, wählt dies die Überwachungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="7b41d-123">When the MCI\_DGV\_MONITOR\_INPUT flag is used in the **dwSource** member, this selects the method of monitoring.</span></span> <span data-ttu-id="7b41d-124">In der Regel haben unterschiedliche Überwachungsmethoden andere Auswirkungen auf die Verwendung der Hardware.</span><span class="sxs-lookup"><span data-stu-id="7b41d-124">Typically, different monitoring methods have different implications on how the hardware is used.</span></span> <span data-ttu-id="7b41d-125">Die Standard Überwachungsmethode wird vom Gerät ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="7b41d-125">The default monitoring method is selected by the device.</span></span>

</dd> <dt>

<span data-ttu-id="7b41d-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI- \_ DGV- \_ Monitor \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="7b41d-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI\_DGV\_MONITOR\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="7b41d-127">Eine-Konstante, die angibt, dass die Monitor Quelle im **dwsource** -Member der von *lpmonitor* identifizierten Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7b41d-127">A constant indicating the monitor source is included in the **dwSource** member of the structure identified by *lpMonitor*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b41d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b41d-128">Requirements</span></span>



| <span data-ttu-id="7b41d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b41d-129">Requirement</span></span> | <span data-ttu-id="7b41d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7b41d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b41d-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b41d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7b41d-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b41d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7b41d-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b41d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7b41d-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b41d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7b41d-135">Header</span><span class="sxs-lookup"><span data-stu-id="7b41d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b41d-136"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b41d-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b41d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b41d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b41d-138">MCI</span><span class="sxs-lookup"><span data-stu-id="7b41d-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7b41d-139">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="7b41d-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

