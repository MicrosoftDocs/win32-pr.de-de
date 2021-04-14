---
title: MCI_STOP Befehl (MMSYSTEM. h)
description: Der MCI \_ -Befehl "beenden" beendet alle Wiedergabe-und Daten Satz Sequenzen, entlädt alle Wiedergabe Puffer und beendet die Anzeige von Videobildern. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- MCI_STOP Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea5f2acbe39b0be64ebc640ae31ceede7591c7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391967"
---
# <a name="mci_stop-command"></a><span data-ttu-id="dfeed-105">MCI- \_ Befehl zum Abbrechen</span><span class="sxs-lookup"><span data-stu-id="dfeed-105">MCI\_STOP command</span></span>

<span data-ttu-id="dfeed-106">Der MCI \_ -Befehl "beenden" beendet alle Wiedergabe-und Daten Satz Sequenzen, entlädt alle Wiedergabe Puffer und beendet die Anzeige von Videobildern.</span><span class="sxs-lookup"><span data-stu-id="dfeed-106">The MCI\_STOP command stops all play and record sequences, unloads all play buffers, and ceases display of video images.</span></span> <span data-ttu-id="dfeed-107">CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="dfeed-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="dfeed-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="dfeed-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
);
```



## <a name="parameters"></a><span data-ttu-id="dfeed-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfeed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfeed-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="dfeed-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="dfeed-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="dfeed-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="dfeed-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="dfeed-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="dfeed-113">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="dfeed-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="dfeed-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="dfeed-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfeed-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpstopps*</span><span class="sxs-lookup"><span data-stu-id="dfeed-115"><span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*</span></span>
</dt> <dd>

<span data-ttu-id="dfeed-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="dfeed-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="dfeed-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="dfeed-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfeed-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfeed-118">Return Value</span></span>

<span data-ttu-id="dfeed-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="dfeed-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfeed-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfeed-120">Remarks</span></span>

<span data-ttu-id="dfeed-121">Der Unterschied zwischen den MCI \_ -Stopps und den [MCI \_ ](mci-pause.md) -anhaltebefehlen hängt vom Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="dfeed-121">The difference between the MCI\_STOP and [MCI\_PAUSE](mci-pause.md) commands depends on the device.</span></span> <span data-ttu-id="dfeed-122">Wenn möglich, hält MCI anhalten \_ den Geräte Vorgang an, aber das Gerät kann sofort wieder aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="dfeed-122">If possible, MCI\_PAUSE suspends device operation but leaves the device ready to resume play immediately.</span></span>

<span data-ttu-id="dfeed-123">Für das CD-Audiogerät setzt MCI \_ die aktuelle Positionsposition auf NULL zurück. im Gegensatz dazu behält die [MCI- \_ Pause](mci-pause.md) die aktuelle Position des Titels bei und geht davon aus, dass die Wiedergabe des Geräts fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="dfeed-123">For the CD audio device, MCI\_STOP resets the current track position to zero; in contrast, [MCI\_PAUSE](mci-pause.md) maintains the current track position, anticipating that the device will resume playing.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfeed-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfeed-124">Requirements</span></span>



| <span data-ttu-id="dfeed-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfeed-125">Requirement</span></span> | <span data-ttu-id="dfeed-126">Wert</span><span class="sxs-lookup"><span data-stu-id="dfeed-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfeed-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfeed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dfeed-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfeed-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dfeed-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfeed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dfeed-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfeed-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dfeed-131">Header</span><span class="sxs-lookup"><span data-stu-id="dfeed-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfeed-132"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfeed-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfeed-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfeed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfeed-134">MCI</span><span class="sxs-lookup"><span data-stu-id="dfeed-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="dfeed-135">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="dfeed-135">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

