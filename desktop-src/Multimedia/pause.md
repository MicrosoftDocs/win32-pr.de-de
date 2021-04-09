---
title: Befehl "anhalten"
description: Der Pause-Befehl hält Wiedergabe oder Aufzeichnung an.
ms.assetid: 8fa1a40d-fdb1-4c9f-a8db-9dd6a0d83b87
keywords:
- Befehl "Pause" Windows Multimedia
topic_type:
- apiref
api_name:
- pause
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25957defa4db514ce84f2e013dcc3751e21779b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859305"
---
# <a name="pause-command"></a><span data-ttu-id="39405-104">Befehl "anhalten"</span><span class="sxs-lookup"><span data-stu-id="39405-104">pause command</span></span>

<span data-ttu-id="39405-105">Der Pause-Befehl hält Wiedergabe oder Aufzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="39405-105">The pause command pauses playing or recording.</span></span> <span data-ttu-id="39405-106">Die meisten Treiber behalten die aktuelle Position bei und setzen schließlich die Wiedergabe oder Aufzeichnung an dieser Position fort.</span><span class="sxs-lookup"><span data-stu-id="39405-106">Most drivers retain the current position and eventually resume playback or recording at this position.</span></span> <span data-ttu-id="39405-107">CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="39405-107">CD audio, digital-video, MIDI sequencer, VCR, videodisc, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="39405-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="39405-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("pause %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="39405-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="39405-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39405-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="39405-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="39405-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="39405-111">Identifier of an MCI device.</span></span> <span data-ttu-id="39405-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="39405-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="39405-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="39405-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="39405-114">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="39405-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="39405-115">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="39405-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="39405-116">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="39405-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39405-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39405-117">Return Value</span></span>

<span data-ttu-id="39405-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="39405-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="39405-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39405-119">Remarks</span></span>

<span data-ttu-id="39405-120">Bei den Treibern mcicda, mciseq und mcipionr funktioniert der Befehl Pause genauso wie der Befehl zum [stoppen](stop.md) .</span><span class="sxs-lookup"><span data-stu-id="39405-120">With the MCICDA, MCISEQ, and MCIPIONR drivers, the pause command works the same as the [stop](stop.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="39405-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39405-121">Examples</span></span>

<span data-ttu-id="39405-122">Der folgende Befehl hält das Gerät "mysound" an.</span><span class="sxs-lookup"><span data-stu-id="39405-122">The following command pauses the "mysound" device.</span></span>

``` syntax
pause mysound
```

## <a name="requirements"></a><span data-ttu-id="39405-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39405-123">Requirements</span></span>



| <span data-ttu-id="39405-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39405-124">Requirement</span></span> | <span data-ttu-id="39405-125">Wert</span><span class="sxs-lookup"><span data-stu-id="39405-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="39405-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39405-126">Minimum supported client</span></span><br/> | <span data-ttu-id="39405-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39405-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39405-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39405-128">Minimum supported server</span></span><br/> | <span data-ttu-id="39405-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39405-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="39405-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39405-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39405-131">MCI</span><span class="sxs-lookup"><span data-stu-id="39405-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="39405-132">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="39405-132">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="39405-133">stop</span><span class="sxs-lookup"><span data-stu-id="39405-133">stop</span></span>](stop.md)
</dt> </dl>

 

