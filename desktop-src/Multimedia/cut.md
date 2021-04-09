---
title: Befehl Ausschneiden
description: Mit dem Befehl "Ausschneiden" werden Daten aus dem Arbeitsbereich entfernt und in die Zwischenablage kopiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- Befehl "Ausschneiden" Windows Multimedia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956975"
---
# <a name="cut-command"></a><span data-ttu-id="a3fec-105">Befehl Ausschneiden</span><span class="sxs-lookup"><span data-stu-id="a3fec-105">cut command</span></span>

<span data-ttu-id="a3fec-106">Mit dem Befehl "Ausschneiden" werden Daten aus dem Arbeitsbereich entfernt und in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="a3fec-106">The cut command removes data from the workspace and copies it to the clipboard.</span></span> <span data-ttu-id="a3fec-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="a3fec-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="a3fec-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="a3fec-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a3fec-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3fec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3fec-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="a3fec-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a3fec-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="a3fec-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a3fec-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a3fec-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a3fec-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszitem*</span><span class="sxs-lookup"><span data-stu-id="a3fec-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="a3fec-114">Eines der folgenden Flags, das das auszuschneide Ende Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a3fec-114">One of the following flags identifying the item to cut.</span></span>



| <span data-ttu-id="a3fec-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a3fec-115">Value</span></span>                 | <span data-ttu-id="a3fec-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a3fec-116">Meaning</span></span>                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3fec-117">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="a3fec-117">at *rectangle*</span></span>        | <span data-ttu-id="a3fec-118">Gibt den Teil jedes Frame Ausschnitts an.</span><span class="sxs-lookup"><span data-stu-id="a3fec-118">Specifies the portion of each frame cut.</span></span> <span data-ttu-id="a3fec-119">Wenn der Wert nicht weggelassen wird, wird standardmäßig der gesamte Frame verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3fec-119">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="a3fec-120">Wenn dieses Element angegeben wird, werden Rahmen nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a3fec-120">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="a3fec-121">Stattdessen wird der Bereich innerhalb des Rechtecks schwarz.</span><span class="sxs-lookup"><span data-stu-id="a3fec-121">Instead the area inside the rectangle becomes black.</span></span>                                       |
| <span data-ttu-id="a3fec-122">Audiostream- *Stream*</span><span class="sxs-lookup"><span data-stu-id="a3fec-122">audio stream *stream*</span></span> | <span data-ttu-id="a3fec-123">Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="a3fec-123">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="a3fec-124">Wenn Sie dieses Flag verwenden und auch Video ausschneiden möchten, müssen Sie auch das Flag "Videostream" verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3fec-124">If you use this flag and also want to cut video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="a3fec-125">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams ausgeschnitten.)</span><span class="sxs-lookup"><span data-stu-id="a3fec-125">(If neither flag is specified, all audio and video streams are cut.)</span></span> |
| <span data-ttu-id="a3fec-126">von *Position*</span><span class="sxs-lookup"><span data-stu-id="a3fec-126">from *position*</span></span>       | <span data-ttu-id="a3fec-127">Gibt den Anfang des Bereichs Ausschnitts an.</span><span class="sxs-lookup"><span data-stu-id="a3fec-127">Specifies the start of the range cut.</span></span> <span data-ttu-id="a3fec-128">Wenn der Wert nicht weggelassen wird, wird standardmäßig die aktuelle Position verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3fec-128">If omitted, it defaults to the current position.</span></span>                                                                                                                                                |
| <span data-ttu-id="a3fec-129">an *Position*</span><span class="sxs-lookup"><span data-stu-id="a3fec-129">to *position*</span></span>         | <span data-ttu-id="a3fec-130">Gibt das Ende des Bereichs Ausschnitts an.</span><span class="sxs-lookup"><span data-stu-id="a3fec-130">Specifies the end of the range cut.</span></span> <span data-ttu-id="a3fec-131">Der Ton-und Videodaten Ausschnitt ist an dieser Position exklusiv.</span><span class="sxs-lookup"><span data-stu-id="a3fec-131">The audio and video data cut are exclusive of this position.</span></span> <span data-ttu-id="a3fec-132">Wenn der Wert ausgelassen wird, wird standardmäßig das Ende des Arbeitsbereichs verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3fec-132">If omitted it defaults to the end of the workspace.</span></span>                                                                                  |
| <span data-ttu-id="a3fec-133">*videostreamstream*</span><span class="sxs-lookup"><span data-stu-id="a3fec-133">video stream *stream*</span></span> | <span data-ttu-id="a3fec-134">Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="a3fec-134">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="a3fec-135">Wenn Sie dieses Flag verwenden und auch das Audiodaten ausschneiden möchten, müssen Sie auch das Flag "Audiostream" verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3fec-135">If you use this flag and also want to cut audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="a3fec-136">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams ausgeschnitten.)</span><span class="sxs-lookup"><span data-stu-id="a3fec-136">(If neither flag is specified, all audio and video streams are cut.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="a3fec-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="a3fec-137"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a3fec-138">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="a3fec-138">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="a3fec-139">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a3fec-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3fec-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3fec-140">Return Value</span></span>

<span data-ttu-id="a3fec-141">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="a3fec-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3fec-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3fec-142">Remarks</span></span>

<span data-ttu-id="a3fec-143">Die Änderung wird nur dann permanent, wenn die Daten explizit gespeichert werden. die Wiedergabe verhält sich jedoch so, als ob die Daten entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="a3fec-143">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3fec-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3fec-144">Requirements</span></span>



| <span data-ttu-id="a3fec-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3fec-145">Requirement</span></span> | <span data-ttu-id="a3fec-146">Wert</span><span class="sxs-lookup"><span data-stu-id="a3fec-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a3fec-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3fec-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a3fec-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3fec-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a3fec-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3fec-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a3fec-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3fec-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a3fec-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3fec-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3fec-152">MCI</span><span class="sxs-lookup"><span data-stu-id="a3fec-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a3fec-153">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="a3fec-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

