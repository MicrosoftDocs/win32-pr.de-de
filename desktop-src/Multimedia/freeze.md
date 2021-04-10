---
title: Freeze-Befehl
description: Der Freeze-Befehl friert Videoeingaben oder Video Ausgaben auf einem VCR oder deaktiviert die Video Beschaffung im Frame Puffer. Dieser Befehl wird von Digital Video, Video Overlay und VCR-Geräten erkannt.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- Freeze-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040080"
---
# <a name="freeze-command"></a><span data-ttu-id="fb4c2-105">Freeze-Befehl</span><span class="sxs-lookup"><span data-stu-id="fb4c2-105">freeze command</span></span>

<span data-ttu-id="fb4c2-106">Der Freeze-Befehl friert Videoeingaben oder Video Ausgaben auf einem VCR oder deaktiviert die Video Beschaffung im Frame Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-106">The freeze command freezes video input or video output on a VCR or disables video acquisition to the frame buffer.</span></span> <span data-ttu-id="fb4c2-107">Dieser Befehl wird von Digital Video, Video Overlay und VCR-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="fb4c2-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="fb4c2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb4c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb4c2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="fb4c2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="fb4c2-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="fb4c2-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="fb4c2-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszfrezeflags*</span><span class="sxs-lookup"><span data-stu-id="fb4c2-113"><span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fb4c2-114">Flag, das angibt, was fixiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-114">Flag that identifies what to freeze.</span></span> <span data-ttu-id="fb4c2-115">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Freeze** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-115">The following table lists device types that recognize the **freeze** command and the flags used by each type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb4c2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fb4c2-116">Value</span></span></th>
<th><span data-ttu-id="fb4c2-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fb4c2-117">Meaning</span></span></th>
<th><span data-ttu-id="fb4c2-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fb4c2-118">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb4c2-119">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="fb4c2-119">digitalvideo</span></span></td>
<td><span data-ttu-id="fb4c2-120">at- <em>Rechteck</em></span><span class="sxs-lookup"><span data-stu-id="fb4c2-120">at <em>rectangle</em></span></span></td>
<td><span data-ttu-id="fb4c2-121">außerhalb</span><span class="sxs-lookup"><span data-stu-id="fb4c2-121">outside</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb4c2-122">overlay</span><span class="sxs-lookup"><span data-stu-id="fb4c2-122">overlay</span></span></td>
<td><span data-ttu-id="fb4c2-123">at- <em>Rechteck</em></span><span class="sxs-lookup"><span data-stu-id="fb4c2-123">at <em>rectangle</em></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="fb4c2-124">VCR</span><span class="sxs-lookup"><span data-stu-id="fb4c2-124">vcr</span></span></td>
<td><ul>
<li><span data-ttu-id="fb4c2-125">Feld</span><span class="sxs-lookup"><span data-stu-id="fb4c2-125">field</span></span></li>
<li><span data-ttu-id="fb4c2-126">frame</span><span class="sxs-lookup"><span data-stu-id="fb4c2-126">frame</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fb4c2-127">input</span><span class="sxs-lookup"><span data-stu-id="fb4c2-127">input</span></span></li>
<li><span data-ttu-id="fb4c2-128">output</span><span class="sxs-lookup"><span data-stu-id="fb4c2-128">output</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fb4c2-129">In der folgenden Tabelle werden die Flags aufgelistet, die im *lpszfrezeflags* -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-129">The following table lists the flags that can be specified in the *lpszFreezeFlags* parameter and their meanings.</span></span>



| <span data-ttu-id="fb4c2-130">Wert</span><span class="sxs-lookup"><span data-stu-id="fb4c2-130">Value</span></span>          | <span data-ttu-id="fb4c2-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fb4c2-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4c2-132">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="fb4c2-132">at *rectangle*</span></span> | <span data-ttu-id="fb4c2-133">Gibt den Bereich an, der fixiert wird.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-133">Specifies the region that will be frozen.</span></span> <span data-ttu-id="fb4c2-134">Bei Video Überlagerungs Geräten wird die Video Erfassung in dieser Region deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-134">For video-overlay devices, this region will have video acquisition disabled.</span></span> <span data-ttu-id="fb4c2-135">Bei Digital Video-Geräten wird das Sperr Masken Bit für die Pixel innerhalb des Rechtecks aktiviert (es sei denn, das Flag "outside" ist angegeben).</span><span class="sxs-lookup"><span data-stu-id="fb4c2-135">For digital-video devices, the pixels within the rectangle will have their lock mask bit turned on (unless the "outside" flag is specified).</span></span> <span data-ttu-id="fb4c2-136">Das Rechteck ist relativ zum Video Puffer Ursprung und wird als *x1 y1 x2 Y2* angegeben.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-136">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="fb4c2-137">Die Koordinaten *x1 y1* geben die linke obere Ecke des Rechtecks an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-137">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="fb4c2-138">Feld</span><span class="sxs-lookup"><span data-stu-id="fb4c2-138">field</span></span>          | <span data-ttu-id="fb4c2-139">Friert das erste Feld ein.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-139">Freezes the first field.</span></span> <span data-ttu-id="fb4c2-140">Standardmäßig wird ein Feld angenommen (wenn weder ein Frame noch ein Feld angegeben ist).</span><span class="sxs-lookup"><span data-stu-id="fb4c2-140">Field is assumed by default (if neither frame nor field is specified).</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fb4c2-141">frame</span><span class="sxs-lookup"><span data-stu-id="fb4c2-141">frame</span></span>          | <span data-ttu-id="fb4c2-142">Friert den gesamten Frame und zeigt beide Felder an.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-142">Freezes the entire frame, displaying both fields.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="fb4c2-143">input</span><span class="sxs-lookup"><span data-stu-id="fb4c2-143">input</span></span>          | <span data-ttu-id="fb4c2-144">Friert den aktuellen Frame des Eingabe Bilds, unabhängig davon, ob er angehalten oder ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-144">Freezes the current frame of the input image, whether it is paused or running.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="fb4c2-145">output</span><span class="sxs-lookup"><span data-stu-id="fb4c2-145">output</span></span>         | <span data-ttu-id="fb4c2-146">Friert den aktuellen Frame der Ausgabe vom VCR.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-146">Freezes the current frame of the output from the VCR.</span></span> <span data-ttu-id="fb4c2-147">Wenn VCR beim Ausgeben von Freeze wiedergegeben wird, wird der aktuelle Frame eingefroren und das VCR angehalten.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-147">If the VCR is playing when freeze is issued, the current frame is frozen and the VCR is paused.</span></span> <span data-ttu-id="fb4c2-148">Wenn VCR angehalten wird, wenn dieser Befehl ausgegeben wird, wird der aktuelle Frame fixiert.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-148">If the VCR is paused when this command is issued, the current frame is frozen.</span></span> <span data-ttu-id="fb4c2-149">Das [fixierte](unfreeze.md) Bild verbleibt auf dem Ausgabegerät, bis ein Befehl zum Aufheben der Fixierung ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-149">The frozen image remains on the output device until an [unfreeze](unfreeze.md) command is issued.</span></span> <span data-ttu-id="fb4c2-150">Wenn weder "Input" noch "Output" angegeben ist, wird "Output" angenommen.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-150">If neither "input" nor "output" is specified, "output" is assumed.</span></span>                                                                                    |
| <span data-ttu-id="fb4c2-151">außerhalb</span><span class="sxs-lookup"><span data-stu-id="fb4c2-151">outside</span></span>        | <span data-ttu-id="fb4c2-152">Gibt an, dass der Bereich außerhalb des Bereichs, der mit dem Flag "at" angegeben wurde, eingefroren ist.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-152">Indicates that the area outside the region specified using the "at" flag is frozen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="fb4c2-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="fb4c2-153"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fb4c2-154">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-154">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="fb4c2-155">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-155">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="fb4c2-156">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fb4c2-156">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb4c2-157">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb4c2-157">Return Value</span></span>

<span data-ttu-id="fb4c2-158">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-158">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb4c2-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb4c2-159">Remarks</span></span>

<span data-ttu-id="fb4c2-160">Bei der Verwendung mit VCR-Geräten ist dieser Befehl für Frame Karten vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-160">When used with VCR devices, this command is intended for frame-grabbing cards.</span></span>

<span data-ttu-id="fb4c2-161">Verwenden Sie zum angeben irregulärer Erwerbs Regionen mit dem Flag "at" eine Reihe von Freeze-und [Fixierung aufheben](unfreeze.md) -Befehlen.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-161">To specify irregular acquisition regions with the "at" flag, use a series of freeze and [unfreeze](unfreeze.md) commands.</span></span> <span data-ttu-id="fb4c2-162">Einige Video Überlagerungs Geräte schränken die Komplexität des Erwerbs Bereichs ein.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-162">Some video-overlay devices limit the complexity of the acquisition region.</span></span>

<span data-ttu-id="fb4c2-163">Dieser Befehl wird nur unterstützt, wenn [ein Befehl zum Funktionsbefehl mit](capability.md) dem Flag "kann eingefroren" den Wert " **true**" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-163">This command is supported only if a call to the [capability](capability.md) command with the "can freeze" flag returns **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="fb4c2-164">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb4c2-164">Examples</span></span>

<span data-ttu-id="fb4c2-165">Der folgende Befehl deaktiviert die Video Erfassung in einem 100-Pixel-Quadrat in der oberen linken Ecke des Video Puffers.</span><span class="sxs-lookup"><span data-stu-id="fb4c2-165">The following command disables video acquisition in a 100-pixel square at the upper left corner of the video buffer.</span></span>

``` syntax
freeze vboard at 0 0 100 100
```

## <a name="requirements"></a><span data-ttu-id="fb4c2-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb4c2-166">Requirements</span></span>



| <span data-ttu-id="fb4c2-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb4c2-167">Requirement</span></span> | <span data-ttu-id="fb4c2-168">Wert</span><span class="sxs-lookup"><span data-stu-id="fb4c2-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fb4c2-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb4c2-169">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4c2-170">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb4c2-170">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fb4c2-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb4c2-171">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4c2-172">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb4c2-172">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fb4c2-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb4c2-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4c2-174">MCI</span><span class="sxs-lookup"><span data-stu-id="fb4c2-174">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fb4c2-175">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="fb4c2-175">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="fb4c2-176">capability</span><span class="sxs-lookup"><span data-stu-id="fb4c2-176">capability</span></span>](capability.md)
</dt> <dt>

[<span data-ttu-id="fb4c2-177">Fixierung aufheben</span><span class="sxs-lookup"><span data-stu-id="fb4c2-177">unfreeze</span></span>](unfreeze.md)
</dt> </dl>

 

