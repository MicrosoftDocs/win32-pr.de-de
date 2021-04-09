---
title: MCI_INDEX Befehl (MMSYSTEM. h)
description: Mit dem Befehl MCI \_ -Index wird die Bildschirm Anzeige ein-oder ausgeschaltet. VCR-Geräte erkennen diesen Befehl.
ms.assetid: c0f18f28-3578-4648-9b75-2d3ede68b3df
keywords:
- MCI_INDEX Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_INDEX
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e93890b8c3db1150bc7224b0fd8b6ee7475ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106203"
---
# <a name="mci_index-command"></a><span data-ttu-id="58631-105">Befehl "MCI- \_ Index"</span><span class="sxs-lookup"><span data-stu-id="58631-105">MCI\_INDEX command</span></span>

<span data-ttu-id="58631-106">Mit dem Befehl MCI \_ -Index wird die Bildschirm Anzeige ein-oder ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="58631-106">The MCI\_INDEX command turns the on-screen display on or off.</span></span> <span data-ttu-id="58631-107">VCR-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="58631-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="58631-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="58631-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INDEX, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpIndex
);
```



## <a name="parameters"></a><span data-ttu-id="58631-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="58631-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58631-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="58631-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="58631-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="58631-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="58631-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="58631-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="58631-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="58631-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="58631-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="58631-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="58631-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpindex*</span><span class="sxs-lookup"><span data-stu-id="58631-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span></span>
</dt> <dd>

<span data-ttu-id="58631-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="58631-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="58631-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="58631-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58631-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58631-118">Return Value</span></span>

<span data-ttu-id="58631-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="58631-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="58631-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58631-120">Remarks</span></span>

<span data-ttu-id="58631-121">Die Informationen, die in der Bildschirm Anzeige angezeigt werden, werden vom MCI \_ VCR \_ Set \_ Index-Flag im [MCI \_ ](mci-set.md) -Befehl Set gesteuert.</span><span class="sxs-lookup"><span data-stu-id="58631-121">The information presented in the on-screen display is controlled by the MCI\_VCR\_SET\_INDEX flag in the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="58631-122">Die folgenden zusätzlichen Flags gelten für VCR-Geräte:</span><span class="sxs-lookup"><span data-stu-id="58631-122">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="58631-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="58631-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="58631-124">Schaltet die Bildschirm Anzeige aus.</span><span class="sxs-lookup"><span data-stu-id="58631-124">Turns on-screen display off.</span></span>

</dd> <dt>

<span data-ttu-id="58631-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf</span><span class="sxs-lookup"><span data-stu-id="58631-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="58631-126">Schaltet die Anzeige auf dem Bildschirm ein.</span><span class="sxs-lookup"><span data-stu-id="58631-126">Turns on-screen display on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58631-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58631-127">Requirements</span></span>



| <span data-ttu-id="58631-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58631-128">Requirement</span></span> | <span data-ttu-id="58631-129">Wert</span><span class="sxs-lookup"><span data-stu-id="58631-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58631-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58631-130">Minimum supported client</span></span><br/> | <span data-ttu-id="58631-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58631-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="58631-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58631-132">Minimum supported server</span></span><br/> | <span data-ttu-id="58631-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58631-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="58631-134">Header</span><span class="sxs-lookup"><span data-stu-id="58631-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="58631-135"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58631-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58631-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58631-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58631-137">MCI</span><span class="sxs-lookup"><span data-stu-id="58631-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="58631-138">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="58631-138">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

