---
title: Befehl Einfügen
description: Mit dem Befehl Einfügen wird der Inhalt der Zwischenablage in den Arbeitsbereich kopiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- Befehl zum Einfügen von Windows Multimedia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040294"
---
# <a name="paste-command"></a><span data-ttu-id="9ba8e-105">Befehl Einfügen</span><span class="sxs-lookup"><span data-stu-id="9ba8e-105">paste command</span></span>

<span data-ttu-id="9ba8e-106">Mit dem Befehl Einfügen wird der Inhalt der Zwischenablage in den Arbeitsbereich kopiert.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-106">The paste command copies the contents of the clipboard into the workspace.</span></span> <span data-ttu-id="9ba8e-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="9ba8e-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="9ba8e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ba8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba8e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="9ba8e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9ba8e-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="9ba8e-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="9ba8e-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszitem*</span><span class="sxs-lookup"><span data-stu-id="9ba8e-113"><span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*</span></span>
</dt> <dd>

<span data-ttu-id="9ba8e-114">Mindestens eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-114">One or more of the following flags.</span></span>



| <span data-ttu-id="9ba8e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9ba8e-115">Value</span></span>                 | <span data-ttu-id="9ba8e-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9ba8e-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba8e-117">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="9ba8e-117">at *rectangle*</span></span>        | <span data-ttu-id="9ba8e-118">Gibt den Speicherort innerhalb des Frames an, in den die Daten eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-118">Specifies the location within the frame where the data is pasted.</span></span> <span data-ttu-id="9ba8e-119">Die linke obere Ecke des *Rechtecks* entspricht der oberen linken Ecke der hinzugefügten Daten.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-119">The upper left corner of the *rectangle* corresponds to the upper left corner of the added data.</span></span> <span data-ttu-id="9ba8e-120">Wenn das Rechteck eine Größe ungleich 0 (null) aufweist, wird der Inhalt der Zwischenablage in diesen Dimensionen skaliert, wenn Sie in den Frame eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-120">If the rectangle has a nonzero size in X or Y, the contents of the clipboard are scaled in those dimensions when they are pasted into the frame.</span></span> <span data-ttu-id="9ba8e-121">Wenn der Wert nicht weggelassen wird, wird das *Rechteck* standardmäßig auf den gesamten Frame</span><span class="sxs-lookup"><span data-stu-id="9ba8e-121">If omitted, the *rectangle* defaults to the entire frame.</span></span> <span data-ttu-id="9ba8e-122">Wenn dieses Flag im Einfügemodus (Standardeinstellung) angegeben wird, wird jede Region außerhalb des Rechtecks mit einer voll Tonfarbe gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-122">If this flag is specified in "insert" mode (the default), any region outside the rectangle is painted a solid color.</span></span>                       |
| <span data-ttu-id="9ba8e-123">Audiostream- *Stream*</span><span class="sxs-lookup"><span data-stu-id="9ba8e-123">audio stream *stream*</span></span> | <span data-ttu-id="9ba8e-124">Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-124">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="9ba8e-125">Wenn nur ein Audiostream in der Zwischenablage vorhanden ist, werden die Audiodaten in den vorgesehenen *Stream* eingefügt.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-125">If only one audio stream exists on the clipboard, the audio data is pasted into the designated *stream*.</span></span> <span data-ttu-id="9ba8e-126">Wenn mehr als ein Audiostream in der Zwischenablage vorhanden ist, gibt der *Stream* die Startnummer für die Datenstrom Sequenzen an.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-126">If more than one audio stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="9ba8e-127">Wenn Sie dieses Flag verwenden und auch Videos einfügen möchten, müssen Sie auch das Flag "Videostream" verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-127">If you use this flag and also want to paste video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="9ba8e-128">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams eingefügt, und ihre ursprünglichen streamnummern werden beibehalten.)</span><span class="sxs-lookup"><span data-stu-id="9ba8e-128">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |
| <span data-ttu-id="9ba8e-129">insert</span><span class="sxs-lookup"><span data-stu-id="9ba8e-129">insert</span></span>                | <span data-ttu-id="9ba8e-130">Gibt an, dass die Daten in den Arbeitsbereich eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-130">Specifies that the data is inserted into the workspace.</span></span> <span data-ttu-id="9ba8e-131">Alle Daten nach der Einfügemarke werden im Arbeitsbereich vorwärts verschoben, um Platz zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-131">Any data after the insertion point is moved forward in the workspace to make room.</span></span> <span data-ttu-id="9ba8e-132">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-132">This is the default value.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="9ba8e-133">overwrite</span><span class="sxs-lookup"><span data-stu-id="9ba8e-133">overwrite</span></span>             | <span data-ttu-id="9ba8e-134">Gibt an, dass die Daten in den Arbeitsbereich kopiert werden, indem alle vorhandenen Daten nach der Einfügemarke geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-134">Specifies that the data is copied into the workspace by writing over any existing data after the insertion point.</span></span> <span data-ttu-id="9ba8e-135">Die Flags "Insert" und "Überschreibung" beeinflussen, ob Frames während des Einfügevorgangs zerstört oder verschoben werden, und nicht, wie die Daten in jedem Frame eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-135">The "insert" and "overwrite" flags affect whether frames are destroyed or moved during the paste operation, not how the data is pasted within each frame.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="9ba8e-136">an *Position*</span><span class="sxs-lookup"><span data-stu-id="9ba8e-136">to *position*</span></span>         | <span data-ttu-id="9ba8e-137">Gibt die Position im Arbeitsbereich an, an der die Daten eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-137">Specifies the position in the workspace at which the data is pasted.</span></span> <span data-ttu-id="9ba8e-138">Wenn der Wert nicht weggelassen wird, wird standardmäßig die aktuelle Position verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-138">If omitted, it defaults to the current position.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="9ba8e-139">*videostreamstream*</span><span class="sxs-lookup"><span data-stu-id="9ba8e-139">video stream *stream*</span></span> | <span data-ttu-id="9ba8e-140">Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-140">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="9ba8e-141">Wenn nur ein Videostream in der Zwischenablage vorhanden ist, werden die Videodaten in den vorgesehenen *Stream* eingefügt.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-141">If only one video stream exists on the clipboard, the video data is pasted into the designated *stream*.</span></span> <span data-ttu-id="9ba8e-142">Wenn mehr als ein Videostream in der Zwischenablage vorhanden ist, gibt der *Stream* die Startnummer für die Datenstrom Sequenzen an.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-142">If more than one video stream exists on the clipboard, the *stream* indicates the starting number for the stream sequences.</span></span> <span data-ttu-id="9ba8e-143">Wenn Sie dieses Flag verwenden und auch Audiodaten einfügen möchten, müssen Sie auch das Flag "Audiostream" verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-143">If you use this flag and also want to paste audio, you must also use the "audio stream" flag.</span></span> <span data-ttu-id="9ba8e-144">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams eingefügt, und ihre ursprünglichen streamnummern werden beibehalten.)</span><span class="sxs-lookup"><span data-stu-id="9ba8e-144">(If neither flag is specified, all audio and video streams are pasted and retain their original stream numbers.)</span></span> |



 

</dd> <dt>

<span data-ttu-id="9ba8e-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="9ba8e-145"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9ba8e-146">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-146">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="9ba8e-147">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9ba8e-147">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba8e-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ba8e-148">Return Value</span></span>

<span data-ttu-id="9ba8e-149">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-149">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ba8e-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ba8e-150">Remarks</span></span>

<span data-ttu-id="9ba8e-151">In den Daten, die aus der Zwischenablage kopiert wurden, sind keine Signale vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-151">No signals are present in the data copied from the clipboard.</span></span> <span data-ttu-id="9ba8e-152">Die Änderung wird nur dann permanent, wenn die Daten explizit gespeichert werden. die Wiedergabe verhält sich jedoch so, als ob die Daten hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-152">The change becomes permanent only when the data is explicitly saved; however, playback acts as if the data has been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba8e-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ba8e-153">Requirements</span></span>



| <span data-ttu-id="9ba8e-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ba8e-154">Requirement</span></span> | <span data-ttu-id="9ba8e-155">Wert</span><span class="sxs-lookup"><span data-stu-id="9ba8e-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9ba8e-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ba8e-156">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba8e-157">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba8e-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9ba8e-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ba8e-158">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba8e-159">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba8e-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9ba8e-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ba8e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba8e-161">MCI</span><span class="sxs-lookup"><span data-stu-id="9ba8e-161">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9ba8e-162">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="9ba8e-162">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

