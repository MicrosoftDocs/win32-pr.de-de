---
title: MCI_PAUSE Befehl (MMSYSTEM. h)
description: Der MCI- \_ anhaltebefehl hält die aktuelle Aktion an. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: c4d0b0a2-cd7b-4641-a318-eb4b4e88b70f
keywords:
- MCI_PAUSE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_PAUSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076397ca9ab770d6f9c23cc5b64853bdd2f07ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739824"
---
# <a name="mci_pause-command"></a><span data-ttu-id="cb09b-105">MCI-Befehl "anhalten" \_</span><span class="sxs-lookup"><span data-stu-id="cb09b-105">MCI\_PAUSE command</span></span>

<span data-ttu-id="cb09b-106">Der MCI- \_ anhaltebefehl hält die aktuelle Aktion an.</span><span class="sxs-lookup"><span data-stu-id="cb09b-106">The MCI\_PAUSE command pauses the current action.</span></span> <span data-ttu-id="cb09b-107">CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="cb09b-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="cb09b-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="cb09b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PAUSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpPause
);
```



## <a name="parameters"></a><span data-ttu-id="cb09b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb09b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb09b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="cb09b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="cb09b-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="cb09b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="cb09b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="cb09b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="cb09b-113">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="cb09b-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="cb09b-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cb09b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb09b-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lppause*</span><span class="sxs-lookup"><span data-stu-id="cb09b-115"><span id="lpPause"></span><span id="lppause"></span><span id="LPPAUSE"></span>*lpPause*</span></span>
</dt> <dd>

<span data-ttu-id="cb09b-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="cb09b-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="cb09b-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="cb09b-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb09b-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb09b-118">Return Value</span></span>

<span data-ttu-id="cb09b-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="cb09b-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb09b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb09b-120">Remarks</span></span>

<span data-ttu-id="cb09b-121">Der Unterschied zwischen den [MCI- \_ Stopps](mci-stop.md) und den MCI-anhaltebefehlen \_ hängt vom Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="cb09b-121">The difference between the [MCI\_STOP](mci-stop.md) and MCI\_PAUSE commands depends on the device.</span></span> <span data-ttu-id="cb09b-122">Wenn möglich, hält MCI anhalten \_ den Geräte Vorgang an, aber das Gerät kann sofort wieder aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="cb09b-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span> <span data-ttu-id="cb09b-123">Bei den mcicda-, mciseq-und mcipionr-Treibern funktioniert der MCI- \_ anhaltebefehl genauso wie der Befehl zum Stoppen von MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="cb09b-123">With the MCICDA, MCISEQ, and MCIPIONR drivers, the MCI\_PAUSE command works the same as the MCI\_STOP command.</span></span>

<span data-ttu-id="cb09b-124">Für Digital Video-Geräte zeigt der *lppause* -Parameter auf eine [**MCI \_ DGV \_ - \_ Pause**](/previous-versions//dd743395(v=vs.85)) -Parameter-Struktur.</span><span class="sxs-lookup"><span data-stu-id="cb09b-124">For digital-video devices, the *lpPause* parameter points to an [**MCI\_DGV\_PAUSE\_PARMS**](/previous-versions//dd743395(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb09b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb09b-125">Requirements</span></span>



| <span data-ttu-id="cb09b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb09b-126">Requirement</span></span> | <span data-ttu-id="cb09b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cb09b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb09b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb09b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cb09b-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb09b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cb09b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb09b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cb09b-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb09b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cb09b-132">Header</span><span class="sxs-lookup"><span data-stu-id="cb09b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb09b-133"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb09b-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb09b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb09b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb09b-135">MCI</span><span class="sxs-lookup"><span data-stu-id="cb09b-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cb09b-136">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="cb09b-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

