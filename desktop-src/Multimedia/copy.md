---
title: Befehl "Kopieren"
description: Der Kopier Befehl kopiert Daten in die Zwischenablage. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- Kopier Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740497"
---
# <a name="copy-command"></a><span data-ttu-id="69bc4-105">Befehl "Kopieren"</span><span class="sxs-lookup"><span data-stu-id="69bc4-105">copy command</span></span>

<span data-ttu-id="69bc4-106">Der Kopier Befehl kopiert Daten in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="69bc4-106">The copy command copies data to the clipboard.</span></span> <span data-ttu-id="69bc4-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="69bc4-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="69bc4-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="69bc4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="69bc4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="69bc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69bc4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="69bc4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="69bc4-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="69bc4-111">Identifier of an MCI device.</span></span> <span data-ttu-id="69bc4-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="69bc4-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="69bc4-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszitem*</span><span class="sxs-lookup"><span data-stu-id="69bc4-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="69bc4-114">Eines der folgenden Flags, das das zu kopierende Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="69bc4-114">One of the following flags identifying the item to copy.</span></span>



| <span data-ttu-id="69bc4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="69bc4-115">Value</span></span>                 | <span data-ttu-id="69bc4-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="69bc4-116">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bc4-117">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="69bc4-117">at *rectangle*</span></span>        | <span data-ttu-id="69bc4-118">Gibt den Teil jedes Frames an, der kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="69bc4-118">Specifies the portion of each frame that will be copied.</span></span> <span data-ttu-id="69bc4-119">Wenn keine Angabe erfolgt, ist die Standardeinstellung der gesamte Frame.</span><span class="sxs-lookup"><span data-stu-id="69bc4-119">If omitted, the default setting is the entire frame.</span></span>                                                                                                                             |
| <span data-ttu-id="69bc4-120">Audiostream- *Stream*</span><span class="sxs-lookup"><span data-stu-id="69bc4-120">audio stream *stream*</span></span> | <span data-ttu-id="69bc4-121">Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="69bc4-121">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="69bc4-122">Wenn Sie dieses Flag verwenden und Video auch kopieren möchten, müssen Sie auch das Flag "Videostream" verwenden.</span><span class="sxs-lookup"><span data-stu-id="69bc4-122">If you use this flag and also want to copy video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="69bc4-123">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams kopiert.)</span><span class="sxs-lookup"><span data-stu-id="69bc4-123">(If neither flag is specified, all audio and video streams are copied.)</span></span> |
| <span data-ttu-id="69bc4-124">von *Position*</span><span class="sxs-lookup"><span data-stu-id="69bc4-124">from *position*</span></span>       | <span data-ttu-id="69bc4-125">Gibt den Anfang des kopierten Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="69bc4-125">Specifies the start of the range copied.</span></span> <span data-ttu-id="69bc4-126">Wenn keine Angabe erfolgt, ist die Standardeinstellung die aktuelle Position.</span><span class="sxs-lookup"><span data-stu-id="69bc4-126">If omitted, the default setting is the current position.</span></span>                                                                                                                                         |
| <span data-ttu-id="69bc4-127">an *Position*</span><span class="sxs-lookup"><span data-stu-id="69bc4-127">to *position*</span></span>         | <span data-ttu-id="69bc4-128">Gibt das Ende des kopierten Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="69bc4-128">Specifies the end of the range copied.</span></span> <span data-ttu-id="69bc4-129">Die kopierten Audiodaten und Videodaten sind an dieser Position exklusiv.</span><span class="sxs-lookup"><span data-stu-id="69bc4-129">The audio and video data copied are exclusive of this position.</span></span> <span data-ttu-id="69bc4-130">Wenn keine Angabe erfolgt, ist die Standardeinstellung das Ende des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="69bc4-130">If omitted, the default setting is the end of the workspace.</span></span>                                                                       |
| <span data-ttu-id="69bc4-131">*videostreamstream*</span><span class="sxs-lookup"><span data-stu-id="69bc4-131">video stream *stream*</span></span> | <span data-ttu-id="69bc4-132">Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="69bc4-132">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="69bc4-133">Wenn Sie dieses Flag verwenden und auch Audiodaten kopieren möchten, müssen Sie auch das Flag "Audiostream" verwenden.</span><span class="sxs-lookup"><span data-stu-id="69bc4-133">If you use this flag and also want to copy audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="69bc4-134">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams kopiert.)</span><span class="sxs-lookup"><span data-stu-id="69bc4-134">(If neither flag is specified, all audio and video streams are copied.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="69bc4-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="69bc4-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="69bc4-136">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="69bc4-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="69bc4-137">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="69bc4-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69bc4-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69bc4-138">Return Value</span></span>

<span data-ttu-id="69bc4-139">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="69bc4-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="69bc4-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69bc4-140">Requirements</span></span>



| <span data-ttu-id="69bc4-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69bc4-141">Requirement</span></span> | <span data-ttu-id="69bc4-142">Wert</span><span class="sxs-lookup"><span data-stu-id="69bc4-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="69bc4-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69bc4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="69bc4-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69bc4-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="69bc4-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69bc4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="69bc4-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69bc4-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="69bc4-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69bc4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bc4-148">MCI</span><span class="sxs-lookup"><span data-stu-id="69bc4-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="69bc4-149">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="69bc4-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

