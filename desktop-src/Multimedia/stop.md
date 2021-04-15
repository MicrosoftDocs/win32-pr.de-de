---
title: Befehl "Befehl"
description: Der Befehl "beenden" beendet die Wiedergabe oder Aufzeichnung. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- Befehl "Befehl" für Windows Multimedia
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391903"
---
# <a name="stop-command"></a><span data-ttu-id="bc699-105">Befehl "Befehl"</span><span class="sxs-lookup"><span data-stu-id="bc699-105">stop command</span></span>

<span data-ttu-id="bc699-106">Der Befehl "beenden" beendet die Wiedergabe oder Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="bc699-106">The stop command stops playback or recording.</span></span> <span data-ttu-id="bc699-107">CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="bc699-107">CD audio, digital-video, MIDI sequencer, videodisc, VCR, and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="bc699-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="bc699-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="bc699-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc699-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc699-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="bc699-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bc699-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="bc699-111">Identifier of an MCI device.</span></span> <span data-ttu-id="bc699-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="bc699-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="bc699-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszstopflags*</span><span class="sxs-lookup"><span data-stu-id="bc699-113"><span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bc699-114">Bei Digital-Video-Geräten kann es sich um das folgende Flag handeln:</span><span class="sxs-lookup"><span data-stu-id="bc699-114">For digital-video devices, it can be the following flag.</span></span>



| <span data-ttu-id="bc699-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bc699-115">Value</span></span> | <span data-ttu-id="bc699-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bc699-116">Meaning</span></span>                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc699-117">verfügen</span><span class="sxs-lookup"><span data-stu-id="bc699-117">hold</span></span>  | <span data-ttu-id="bc699-118">Verhindert das Freigeben von Ressourcen, die erforderlich sind, um ein Bild auf dem Bildschirm neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="bc699-118">Prevents the release of resources required to redraw a still image on the screen.</span></span> <span data-ttu-id="bc699-119">Der Frame Puffer bleibt für die Aktualisierung der Anzeige verfügbar, wenn beispielsweise das Fenster verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="bc699-119">The frame buffer remains available for use in updating the display when, for example, the window is moved.</span></span> |



 

</dd> <dt>

<span data-ttu-id="bc699-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="bc699-120"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bc699-121">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="bc699-121">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="bc699-122">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bc699-122">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="bc699-123">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bc699-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc699-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc699-124">Return Value</span></span>

<span data-ttu-id="bc699-125">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="bc699-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc699-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc699-126">Remarks</span></span>

<span data-ttu-id="bc699-127">Bei CD-Audiogeräten beendet der Befehl "beenden" die Wiedergabe und setzt die aktuelle Position des Titels auf NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="bc699-127">For CD audio devices, the stop command stops playback and resets the current track position to zero.</span></span>

## <a name="examples"></a><span data-ttu-id="bc699-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc699-128">Examples</span></span>

<span data-ttu-id="bc699-129">Der folgende Befehl beendet die Wiedergabe oder Aufzeichnung auf dem Gerät "mysound".</span><span class="sxs-lookup"><span data-stu-id="bc699-129">The following command stops playback or recording on the "mysound" device.</span></span>

``` syntax
stop mysound
```

## <a name="requirements"></a><span data-ttu-id="bc699-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc699-130">Requirements</span></span>



| <span data-ttu-id="bc699-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc699-131">Requirement</span></span> | <span data-ttu-id="bc699-132">Wert</span><span class="sxs-lookup"><span data-stu-id="bc699-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bc699-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc699-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bc699-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc699-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bc699-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc699-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bc699-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc699-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bc699-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc699-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc699-138">MCI</span><span class="sxs-lookup"><span data-stu-id="bc699-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bc699-139">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="bc699-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

