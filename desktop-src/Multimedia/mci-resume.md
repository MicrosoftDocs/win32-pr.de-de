---
title: MCI_RESUME Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Resume bewirkt, dass ein angehaltene Gerät den angehaltenen Vorgang fortsetzt.
ms.assetid: 2df712c1-5005-4e89-a439-a651076bbb73
keywords:
- MCI_RESUME Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_RESUME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd83b6d753cd223235b8b11f2d4b0be4c828ec28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949536"
---
# <a name="mci_resume-command"></a><span data-ttu-id="ac5a3-104">Befehl "MCI \_ Resume"</span><span class="sxs-lookup"><span data-stu-id="ac5a3-104">MCI\_RESUME command</span></span>

<span data-ttu-id="ac5a3-105">Der Befehl MCI \_ Resume bewirkt, dass ein angehaltene Gerät den angehaltenen Vorgang fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="ac5a3-105">The MCI\_RESUME command causes a paused device to resume the paused operation.</span></span> <span data-ttu-id="ac5a3-106">Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.</span><span class="sxs-lookup"><span data-stu-id="ac5a3-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="ac5a3-107">Obwohl die Geräte von CD-Audiodaten, MIDI-Sequencer und Videodisc diesen Befehl ebenfalls erkennen, unterstützen die Gerätetreiber mcicda, mcitarq und mcipionr Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="ac5a3-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="ac5a3-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="ac5a3-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESUME, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpResume
);
```



## <a name="parameters"></a><span data-ttu-id="ac5a3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac5a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac5a3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="ac5a3-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ac5a3-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="ac5a3-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ac5a3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ac5a3-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ac5a3-113">MCI \_ -Benachrichtigung, MCI \_ -Wartezeit oder, für Digital Video-und VCR-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="ac5a3-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="ac5a3-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ac5a3-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac5a3-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lannahme*</span><span class="sxs-lookup"><span data-stu-id="ac5a3-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span></span>
</dt> <dd>

<span data-ttu-id="ac5a3-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ac5a3-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="ac5a3-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="ac5a3-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac5a3-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac5a3-118">Return Value</span></span>

<span data-ttu-id="ac5a3-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="ac5a3-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac5a3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac5a3-120">Remarks</span></span>

<span data-ttu-id="ac5a3-121">Dieser Befehl setzt die Wiedergabe und Aufzeichnung fort, ohne die aktuelle Position des Titels mit dem [MCI- \_ Play](mci-play.md) -oder [MCI- \_ Datensatz](mci-record.md)zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ac5a3-121">This command resumes playing and recording without changing the current track position set with [MCI\_PLAY](mci-play.md) or [MCI\_RECORD](mci-record.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac5a3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac5a3-122">Requirements</span></span>



| <span data-ttu-id="ac5a3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac5a3-123">Requirement</span></span> | <span data-ttu-id="ac5a3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ac5a3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5a3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac5a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ac5a3-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac5a3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ac5a3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac5a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ac5a3-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac5a3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ac5a3-129">Header</span><span class="sxs-lookup"><span data-stu-id="ac5a3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac5a3-130"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac5a3-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac5a3-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac5a3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac5a3-132">MCI</span><span class="sxs-lookup"><span data-stu-id="ac5a3-132">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ac5a3-133">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="ac5a3-133">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

