---
title: DELETE-Befehl
description: Der DELETE-Befehl löscht ein Daten Segment aus einer Datei. Digital-Video-und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- DELETE-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859223"
---
# <a name="delete-command"></a><span data-ttu-id="5a249-105">DELETE-Befehl</span><span class="sxs-lookup"><span data-stu-id="5a249-105">delete command</span></span>

<span data-ttu-id="5a249-106">Der DELETE-Befehl löscht ein Daten Segment aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="5a249-106">The delete command deletes a data segment from a file.</span></span> <span data-ttu-id="5a249-107">Digital-Video-und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="5a249-107">Digital-video and waveform-audio devices recognize this command.</span></span>

<span data-ttu-id="5a249-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="5a249-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="5a249-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a249-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a249-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="5a249-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5a249-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="5a249-111">Identifier of an MCI device.</span></span> <span data-ttu-id="5a249-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5a249-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="5a249-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszposition*</span><span class="sxs-lookup"><span data-stu-id="5a249-113"><span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*</span></span>
</dt> <dd>

<span data-ttu-id="5a249-114">Flag, das ein zu löschende Daten Segment identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5a249-114">Flag that identifies a data segment to delete.</span></span> <span data-ttu-id="5a249-115">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Delete** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="5a249-115">The following table lists device types that recognize the **delete** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a249-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5a249-116">Value</span></span></th>
<th><span data-ttu-id="5a249-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5a249-117">Meaning</span></span></th>
<th><span data-ttu-id="5a249-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5a249-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a249-119">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="5a249-119">digitalvideo</span></span></td>
<td><ul>
<li><span data-ttu-id="5a249-120">at- <em>Rechteck</em></span><span class="sxs-lookup"><span data-stu-id="5a249-120">at <em>rectangle</em></span></span></li>
<li><span data-ttu-id="5a249-121">Audiostream- <em>Stream</em></span><span class="sxs-lookup"><span data-stu-id="5a249-121">audio stream <em>stream</em></span></span></li>
<li><span data-ttu-id="5a249-122">von <em>Position</em></span><span class="sxs-lookup"><span data-stu-id="5a249-122">from <em>position</em></span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5a249-123">an <em>Position</em></span><span class="sxs-lookup"><span data-stu-id="5a249-123">to <em>position</em></span></span></li>
<li><span data-ttu-id="5a249-124"><em>videostreamstream</em></span><span class="sxs-lookup"><span data-stu-id="5a249-124">video stream <em>stream</em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a249-125">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="5a249-125">waveaudio</span></span></td>
<td><span data-ttu-id="5a249-126">von <em>Position</em></span><span class="sxs-lookup"><span data-stu-id="5a249-126">from <em>position</em></span></span></td>
<td><span data-ttu-id="5a249-127">an <em>Position</em></span><span class="sxs-lookup"><span data-stu-id="5a249-127">to <em>position</em></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5a249-128">In der folgenden Tabelle werden die Flags aufgelistet, die im *lpszposition* -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="5a249-128">The following table lists the flags that can be specified in the *lpszPosition* parameter and their meanings.</span></span>



| <span data-ttu-id="5a249-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5a249-129">Value</span></span>                 | <span data-ttu-id="5a249-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5a249-130">Meaning</span></span>                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a249-131">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="5a249-131">at *rectangle*</span></span>        | <span data-ttu-id="5a249-132">Gibt den Teil jedes gelöschten Frames an.</span><span class="sxs-lookup"><span data-stu-id="5a249-132">Specifies the portion of each frame deleted.</span></span> <span data-ttu-id="5a249-133">Wenn der Wert nicht weggelassen wird, wird standardmäßig der gesamte Frame verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a249-133">If omitted, it defaults to the entire frame.</span></span> <span data-ttu-id="5a249-134">Wenn dieses Element angegeben wird, werden Rahmen nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5a249-134">When this item is specified, frames are not deleted.</span></span> <span data-ttu-id="5a249-135">Stattdessen wird der Bereich innerhalb des Rechtecks schwarz.</span><span class="sxs-lookup"><span data-stu-id="5a249-135">Instead the area inside the rectangle becomes black.</span></span>                                          |
| <span data-ttu-id="5a249-136">Audiostream- *Stream*</span><span class="sxs-lookup"><span data-stu-id="5a249-136">audio stream *stream*</span></span> | <span data-ttu-id="5a249-137">Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="5a249-137">Specifies the audio stream in the workspace affected by the command.</span></span> <span data-ttu-id="5a249-138">Wenn Sie dieses Flag verwenden und Video auch löschen möchten, müssen Sie auch das Flag "Videostream" verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a249-138">If you use this flag and also want to delete video, you must also use the "video stream" flag.</span></span> <span data-ttu-id="5a249-139">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams gelöscht.)</span><span class="sxs-lookup"><span data-stu-id="5a249-139">(If neither flag is specified, all audio and video streams are deleted.)</span></span> |
| <span data-ttu-id="5a249-140">von *Position*</span><span class="sxs-lookup"><span data-stu-id="5a249-140">from *position*</span></span>       | <span data-ttu-id="5a249-141">Gibt die Position an, an der der Löschvorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="5a249-141">Specifies the position at which deletion begins.</span></span> <span data-ttu-id="5a249-142">Wenn dieses Flag weggelassen wird, beginnt der Löschvorgang an der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="5a249-142">If this flag is omitted, the deletion begins at the current position.</span></span>                                                                                                                       |
| <span data-ttu-id="5a249-143">an *Position*</span><span class="sxs-lookup"><span data-stu-id="5a249-143">to *position*</span></span>         | <span data-ttu-id="5a249-144">Gibt die Position an, an der der Löschvorgang endet.</span><span class="sxs-lookup"><span data-stu-id="5a249-144">Specifies the position at which deletion ends.</span></span> <span data-ttu-id="5a249-145">Wenn dieses Flag weggelassen wird, wird der Löschvorgang bis zum Ende des Inhalts oder Arbeitsbereichs fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5a249-145">If this flag is omitted, the deletion continues to the end of the content or workspace.</span></span>                                                                                                       |
| <span data-ttu-id="5a249-146">*videostreamstream*</span><span class="sxs-lookup"><span data-stu-id="5a249-146">video stream *stream*</span></span> | <span data-ttu-id="5a249-147">Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="5a249-147">Specifies the video stream in the workspace affected by the command.</span></span> <span data-ttu-id="5a249-148">Wenn Sie dieses Flag verwenden und auch Audiodaten löschen möchten, müssen Sie auch das Flag "Audiostream" verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a249-148">If you use this flag and also want to delete audio, you must also use "audio stream" flag.</span></span> <span data-ttu-id="5a249-149">(Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams gelöscht.)</span><span class="sxs-lookup"><span data-stu-id="5a249-149">(If neither flag is specified, all audio and video streams are deleted.)</span></span>     |



 

</dd> <dt>

<span data-ttu-id="5a249-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="5a249-150"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5a249-151">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="5a249-151">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="5a249-152">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5a249-152">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="5a249-153">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5a249-153">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a249-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a249-154">Return Value</span></span>

<span data-ttu-id="5a249-155">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="5a249-155">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a249-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a249-156">Remarks</span></span>

<span data-ttu-id="5a249-157">Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen.</span><span class="sxs-lookup"><span data-stu-id="5a249-157">Before issuing any commands that use position values, you should set the desired time format by using the [set](set.md) command.</span></span>

## <a name="examples"></a><span data-ttu-id="5a249-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a249-158">Examples</span></span>

<span data-ttu-id="5a249-159">Der folgende Befehl löscht die Waveform-Audiodaten von 1 Millisekunde bis 900 Millisekunden (vorausgesetzt, das Uhrzeit Format ist auf Millisekunden festgelegt).</span><span class="sxs-lookup"><span data-stu-id="5a249-159">The following command deletes the waveform-audio data from 1 millisecond through 900 milliseconds (assuming the time format is set to milliseconds).</span></span>

``` syntax
delete mysound from 1 to 900
```

## <a name="requirements"></a><span data-ttu-id="5a249-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a249-160">Requirements</span></span>



| <span data-ttu-id="5a249-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a249-161">Requirement</span></span> | <span data-ttu-id="5a249-162">Wert</span><span class="sxs-lookup"><span data-stu-id="5a249-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5a249-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a249-163">Minimum supported client</span></span><br/> | <span data-ttu-id="5a249-164">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a249-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5a249-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a249-165">Minimum supported server</span></span><br/> | <span data-ttu-id="5a249-166">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a249-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5a249-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a249-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a249-168">MCI</span><span class="sxs-lookup"><span data-stu-id="5a249-168">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5a249-169">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="5a249-169">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="5a249-170">set</span><span class="sxs-lookup"><span data-stu-id="5a249-170">set</span></span>](set.md)
</dt> </dl>

 

