---
title: MCI_SETTUNER Befehl (MMSYSTEM. h)
description: Der MCI \_ settuner-Befehl legt den aktuellen Channel auf dem Tuner fest. VCR-Geräte erkennen diesen Befehl.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- MCI_SETTUNER Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040985"
---
# <a name="mci_settuner-command"></a><span data-ttu-id="c165e-105">MCI \_ settuner-Befehl</span><span class="sxs-lookup"><span data-stu-id="c165e-105">MCI\_SETTUNER command</span></span>

<span data-ttu-id="c165e-106">Der MCI \_ settuner-Befehl legt den aktuellen Channel auf dem Tuner fest.</span><span class="sxs-lookup"><span data-stu-id="c165e-106">The MCI\_SETTUNER command sets the current channel on the tuner.</span></span> <span data-ttu-id="c165e-107">VCR-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="c165e-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="c165e-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="c165e-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
);
```



## <a name="parameters"></a><span data-ttu-id="c165e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c165e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c165e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="c165e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c165e-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="c165e-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c165e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c165e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c165e-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="c165e-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="c165e-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c165e-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c165e-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpsettuner*</span><span class="sxs-lookup"><span data-stu-id="c165e-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span></span>
</dt> <dd>

<span data-ttu-id="c165e-116">Zeiger auf eine [**MCI \_ VCR \_ settuner \_**](mci-vcr-settuner-parms.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c165e-116">Pointer to an [**MCI\_VCR\_SETTUNER\_PARMS**](mci-vcr-settuner-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c165e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c165e-117">Return Value</span></span>

<span data-ttu-id="c165e-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c165e-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c165e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c165e-119">Remarks</span></span>

<span data-ttu-id="c165e-120">Die folgenden zusätzlichen Flags gelten für VCR-Geräte:</span><span class="sxs-lookup"><span data-stu-id="c165e-120">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="c165e-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI \_ VCR \_ settuner- \_ Kanal</span><span class="sxs-lookup"><span data-stu-id="c165e-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI\_VCR\_SETTUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="c165e-122">Der **dwchannel** -Member der-Struktur, die von *lpsettuner* identifiziert wird, enthält die neue Kanalnummer.</span><span class="sxs-lookup"><span data-stu-id="c165e-122">The **dwChannel** member of the structure identified by *lpSetTuner* contains the new channel number.</span></span>

</dd> <dt>

<span data-ttu-id="c165e-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI \_ VCR \_ settuner- \_ Kanal \_ nach unten</span><span class="sxs-lookup"><span data-stu-id="c165e-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="c165e-124">Verringert den tunkanchannel.</span><span class="sxs-lookup"><span data-stu-id="c165e-124">Decrements the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="c165e-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI \_ VCR \_ settuner- \_ Channel- \_ Suche \_ nach unten</span><span class="sxs-lookup"><span data-stu-id="c165e-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="c165e-126">Sucht nach einem gültigen Kanal in umgekehrter Richtung.</span><span class="sxs-lookup"><span data-stu-id="c165e-126">Searches for a valid channel in the reverse direction.</span></span>

</dd> <dt>

<span data-ttu-id="c165e-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI \_ VCR \_ settuner- \_ Kanal \_ Suche \_</span><span class="sxs-lookup"><span data-stu-id="c165e-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_UP</span></span>
</dt> <dd>

<span data-ttu-id="c165e-128">Sucht in Vorwärtsrichtung nach einem gültigen Kanal.</span><span class="sxs-lookup"><span data-stu-id="c165e-128">Searches for a valid channel in the forward direction.</span></span>

</dd> <dt>

<span data-ttu-id="c165e-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI \_ VCR \_ settuner- \_ Kanal \_ aufwärts</span><span class="sxs-lookup"><span data-stu-id="c165e-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_UP</span></span>
</dt> <dd>

<span data-ttu-id="c165e-130">Inkremente den tunkanchannel.</span><span class="sxs-lookup"><span data-stu-id="c165e-130">Increments the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="c165e-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI \_ VCR- \_ settuner- \_ Nummer</span><span class="sxs-lookup"><span data-stu-id="c165e-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI\_VCR\_SETTUNER\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="c165e-132">Der **dwnumber** -Member der Struktur, die von *lpsettuner* identifiziert wird, gibt an, welcher logische Tuner mit diesem Befehl beeinflusst werden soll.</span><span class="sxs-lookup"><span data-stu-id="c165e-132">The **dwNumber** member of the structure identified by *lpSetTuner* specifies which logical tuner to affect with this command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c165e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c165e-133">Requirements</span></span>



| <span data-ttu-id="c165e-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c165e-134">Requirement</span></span> | <span data-ttu-id="c165e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c165e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c165e-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c165e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c165e-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c165e-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c165e-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c165e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c165e-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c165e-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c165e-140">Header</span><span class="sxs-lookup"><span data-stu-id="c165e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c165e-141"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c165e-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c165e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c165e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c165e-143">MCI</span><span class="sxs-lookup"><span data-stu-id="c165e-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c165e-144">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="c165e-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

