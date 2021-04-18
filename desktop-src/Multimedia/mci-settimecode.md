---
title: MCI_SETTIMECODE Befehl (MMSYSTEM. h)
description: Der Befehl "MCI \_ settimecode" aktiviert oder deaktiviert die Zeit Code Aufzeichnung für einen VCR. VCR-Geräte erkennen diesen Befehl.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- MCI_SETTIMECODE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344273"
---
# <a name="mci_settimecode-command"></a><span data-ttu-id="061e6-105">Befehl "MCI \_ settimecode"</span><span class="sxs-lookup"><span data-stu-id="061e6-105">MCI\_SETTIMECODE command</span></span>

<span data-ttu-id="061e6-106">Der Befehl "MCI \_ settimecode" aktiviert oder deaktiviert die Zeit Code Aufzeichnung für einen VCR.</span><span class="sxs-lookup"><span data-stu-id="061e6-106">The MCI\_SETTIMECODE command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="061e6-107">VCR-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="061e6-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="061e6-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="061e6-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
);
```



## <a name="parameters"></a><span data-ttu-id="061e6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="061e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="061e6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="061e6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="061e6-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="061e6-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="061e6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="061e6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="061e6-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="061e6-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="061e6-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="061e6-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="061e6-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpsettimecode*</span><span class="sxs-lookup"><span data-stu-id="061e6-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="061e6-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="061e6-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="061e6-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="061e6-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="061e6-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="061e6-118">Return Value</span></span>

<span data-ttu-id="061e6-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="061e6-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="061e6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="061e6-120">Remarks</span></span>

<span data-ttu-id="061e6-121">Das folgende zusätzliche Flag gilt für VCR-Geräte:</span><span class="sxs-lookup"><span data-stu-id="061e6-121">The following additional flag applies to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="061e6-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>MCI- \_ VCR- \_ settimecode- \_ Datensatz</span><span class="sxs-lookup"><span data-stu-id="061e6-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>MCI\_VCR\_SETTIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="061e6-123">Legt die Aufzeichnung von Zeitcode Track auf ein oder aus fest.</span><span class="sxs-lookup"><span data-stu-id="061e6-123">Sets the timecode track recording to on or off.</span></span> <span data-ttu-id="061e6-124">Dieses Flag wird in Kombination mit einem der folgenden zusätzlichen Flags verwendet:</span><span class="sxs-lookup"><span data-stu-id="061e6-124">This flag is used in combination with one of the following additional flags:</span></span>

</dd> <dt>

<span data-ttu-id="061e6-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf</span><span class="sxs-lookup"><span data-stu-id="061e6-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="061e6-126">Zeit Code Aufzeichnung in.</span><span class="sxs-lookup"><span data-stu-id="061e6-126">Timecode recording on.</span></span>

</dd> <dt>

<span data-ttu-id="061e6-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="061e6-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="061e6-128">Zeit Code Aufzeichnung aus.</span><span class="sxs-lookup"><span data-stu-id="061e6-128">Timecode recording off.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="061e6-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="061e6-129">Requirements</span></span>



| <span data-ttu-id="061e6-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="061e6-130">Requirement</span></span> | <span data-ttu-id="061e6-131">Wert</span><span class="sxs-lookup"><span data-stu-id="061e6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="061e6-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="061e6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="061e6-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="061e6-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="061e6-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="061e6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="061e6-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="061e6-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="061e6-136">Header</span><span class="sxs-lookup"><span data-stu-id="061e6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="061e6-137"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="061e6-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="061e6-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="061e6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061e6-139">MCI</span><span class="sxs-lookup"><span data-stu-id="061e6-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="061e6-140">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="061e6-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

