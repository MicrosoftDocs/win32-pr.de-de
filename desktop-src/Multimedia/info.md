---
title: Info-Befehl
description: Der Befehl "Info" Ruft eine Hardware Beschreibung von einem Gerät ab. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- Info-Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392153"
---
# <a name="info-command"></a><span data-ttu-id="5c26b-105">Info-Befehl</span><span class="sxs-lookup"><span data-stu-id="5c26b-105">info command</span></span>

<span data-ttu-id="5c26b-106">Der Befehl "Info" Ruft eine Hardware Beschreibung von einem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="5c26b-106">The info command retrieves a hardware description from a device.</span></span> <span data-ttu-id="5c26b-107">Dieser Befehl wird von allen MCI-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="5c26b-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="5c26b-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="5c26b-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="5c26b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c26b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c26b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="5c26b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5c26b-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="5c26b-111">Identifier of an MCI device.</span></span> <span data-ttu-id="5c26b-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5c26b-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="5c26b-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszinfotype*</span><span class="sxs-lookup"><span data-stu-id="5c26b-113"><span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*</span></span>
</dt> <dd>

<span data-ttu-id="5c26b-114">Flag, das den Typ der erforderlichen Informationen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5c26b-114">Flag that identifies the type of information required.</span></span> <span data-ttu-id="5c26b-115">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Info** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="5c26b-115">The following table lists device types that recognize the **info** command and the flags used by each type.</span></span>



| <span data-ttu-id="5c26b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5c26b-116">Value</span></span>        | <span data-ttu-id="5c26b-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5c26b-117">Meaning</span></span>                                                             | <span data-ttu-id="5c26b-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5c26b-118">Meaning</span></span>                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="5c26b-119">CDAudio</span><span class="sxs-lookup"><span data-stu-id="5c26b-119">cdaudio</span></span>      | <span data-ttu-id="5c26b-120">Informationen identityinfo UPC</span><span class="sxs-lookup"><span data-stu-id="5c26b-120">info identityinfo upc</span></span>                                               | <span data-ttu-id="5c26b-121">product</span><span class="sxs-lookup"><span data-stu-id="5c26b-121">product</span></span>                                             |
| <span data-ttu-id="5c26b-122">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="5c26b-122">digitalvideo</span></span> | <span data-ttu-id="5c26b-123">audioalgorithmaudioqualityfileproductimmer noch algorithmimmer Qualität</span><span class="sxs-lookup"><span data-stu-id="5c26b-123">audio algorithmaudio qualityfileproductstill algorithmstill quality</span></span> | <span data-ttu-id="5c26b-124">usageversionvideo algorithmvideo qualitywindow-Text</span><span class="sxs-lookup"><span data-stu-id="5c26b-124">usageversionvideo algorithmvideo qualitywindow text</span></span> |
| <span data-ttu-id="5c26b-125">overlay</span><span class="sxs-lookup"><span data-stu-id="5c26b-125">overlay</span></span>      | <span data-ttu-id="5c26b-126">file Product</span><span class="sxs-lookup"><span data-stu-id="5c26b-126">fileproduct</span></span>                                                         | <span data-ttu-id="5c26b-127">Fenster Text</span><span class="sxs-lookup"><span data-stu-id="5c26b-127">window text</span></span>                                         |
| <span data-ttu-id="5c26b-128">sequencer</span><span class="sxs-lookup"><span data-stu-id="5c26b-128">sequencer</span></span>    | <span data-ttu-id="5c26b-129">copyrightfile</span><span class="sxs-lookup"><span data-stu-id="5c26b-129">copyrightfile</span></span>                                                       | <span data-ttu-id="5c26b-130">nameproduct</span><span class="sxs-lookup"><span data-stu-id="5c26b-130">nameproduct</span></span>                                         |
| <span data-ttu-id="5c26b-131">VCR</span><span class="sxs-lookup"><span data-stu-id="5c26b-131">vcr</span></span>          | <span data-ttu-id="5c26b-132">product</span><span class="sxs-lookup"><span data-stu-id="5c26b-132">product</span></span>                                                             | <span data-ttu-id="5c26b-133">version</span><span class="sxs-lookup"><span data-stu-id="5c26b-133">version</span></span>                                             |
| <span data-ttu-id="5c26b-134">Videodisk</span><span class="sxs-lookup"><span data-stu-id="5c26b-134">videodisk</span></span>    | <span data-ttu-id="5c26b-135">product</span><span class="sxs-lookup"><span data-stu-id="5c26b-135">product</span></span>                                                             |                                                     |
| <span data-ttu-id="5c26b-136">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="5c26b-136">waveaudio</span></span>    | <span data-ttu-id="5c26b-137">FileInput</span><span class="sxs-lookup"><span data-stu-id="5c26b-137">fileinput</span></span>                                                           | <span data-ttu-id="5c26b-138">outputproduct</span><span class="sxs-lookup"><span data-stu-id="5c26b-138">outputproduct</span></span>                                       |



 

<span data-ttu-id="5c26b-139">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszinfotype** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="5c26b-139">The following table lists the flags that can be specified in the **lpszInfoType** parameter and their meanings.</span></span>



| <span data-ttu-id="5c26b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="5c26b-140">Value</span></span>           | <span data-ttu-id="5c26b-141">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5c26b-141">Meaning</span></span>                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c26b-142">audioalgorithmus</span><span class="sxs-lookup"><span data-stu-id="5c26b-142">audio algorithm</span></span> | <span data-ttu-id="5c26b-143">Gibt den Namen des aktuellen Audiokomprimierungs Algorithmus zurück.</span><span class="sxs-lookup"><span data-stu-id="5c26b-143">Returns the name of the current audio compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="5c26b-144">Audioqualität</span><span class="sxs-lookup"><span data-stu-id="5c26b-144">audio quality</span></span>   | <span data-ttu-id="5c26b-145">Gibt den Namen für den aktuellen audioqualitätsdeskriptor zurück.</span><span class="sxs-lookup"><span data-stu-id="5c26b-145">Returns the name for the current audio quality descriptor.</span></span> <span data-ttu-id="5c26b-146">Dadurch wird möglicherweise "unknown" zurückgegeben, wenn die Anwendung Parameter auf bestimmte Werte festgelegt hat, die nicht definierten Qualitäten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5c26b-146">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="5c26b-147">Copyright</span><span class="sxs-lookup"><span data-stu-id="5c26b-147">copyright</span></span>       | <span data-ttu-id="5c26b-148">Ruft den Urheberrechts Hinweis der MIDI-Datei aus dem Copyright-Meta-Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="5c26b-148">Retrieves the MIDI file copyright notice from the copyright meta event.</span></span>                                                                                                                            |
| <span data-ttu-id="5c26b-149">file</span><span class="sxs-lookup"><span data-stu-id="5c26b-149">file</span></span>            | <span data-ttu-id="5c26b-150">Ruft den Namen der Datei ab, die vom Verbund Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c26b-150">Retrieves the name of the file used by the compound device.</span></span> <span data-ttu-id="5c26b-151">Wenn das Gerät ohne eine Datei geöffnet wird und der [Load](load.md) -Befehl nicht verwendet wurde, wird eine NULL-Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c26b-151">If the device is opened without a file and the [load](load.md) command has not been used, a null string is returned.</span></span>                  |
| <span data-ttu-id="5c26b-152">Informations Identität</span><span class="sxs-lookup"><span data-stu-id="5c26b-152">info identity</span></span>   | <span data-ttu-id="5c26b-153">Erzeugt einen eindeutigen Bezeichner für die AudioCD, die derzeit in dem abgefragten Player geladen wird.</span><span class="sxs-lookup"><span data-stu-id="5c26b-153">Produces a unique identifier for the audio CD currently loaded in the player being queried.</span></span>                                                                                                        |
| <span data-ttu-id="5c26b-154">Info-UPC</span><span class="sxs-lookup"><span data-stu-id="5c26b-154">info upc</span></span>        | <span data-ttu-id="5c26b-155">Erzeugt den universellen Produkt Code (Universal Product Code, UPC), der auf einer AudioCD codiert ist.</span><span class="sxs-lookup"><span data-stu-id="5c26b-155">Produces the Universal Product Code (UPC) that is encoded on an audio CD.</span></span> <span data-ttu-id="5c26b-156">Der UPC ist eine Zeichenfolge mit Ziffern.</span><span class="sxs-lookup"><span data-stu-id="5c26b-156">The UPC is a string of digits.</span></span> <span data-ttu-id="5c26b-157">Sie ist möglicherweise nicht für alle CDs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c26b-157">It might not be available for all CDs.</span></span>                                                    |
| <span data-ttu-id="5c26b-158">input</span><span class="sxs-lookup"><span data-stu-id="5c26b-158">input</span></span>           | <span data-ttu-id="5c26b-159">Ruft die Beschreibung des aktuellen Eingabe Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="5c26b-159">Retrieves the description of the current input device.</span></span> <span data-ttu-id="5c26b-160">Gibt "None" zurück, wenn ein Eingabegerät nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5c26b-160">Returns "none" if an input device is not set.</span></span>                                                                                               |
| <span data-ttu-id="5c26b-161">name</span><span class="sxs-lookup"><span data-stu-id="5c26b-161">name</span></span>            | <span data-ttu-id="5c26b-162">Ruft den Sequenznamen aus dem Meta-Ereignis Sequence/Track Name ab.</span><span class="sxs-lookup"><span data-stu-id="5c26b-162">Retrieves the sequence name from the sequence/track name meta event.</span></span>                                                                                                                               |
| <span data-ttu-id="5c26b-163">output</span><span class="sxs-lookup"><span data-stu-id="5c26b-163">output</span></span>          | <span data-ttu-id="5c26b-164">Ruft die Beschreibung des aktuellen Ausgabegeräts ab.</span><span class="sxs-lookup"><span data-stu-id="5c26b-164">Retrieves the description of the current output device.</span></span> <span data-ttu-id="5c26b-165">Gibt "None" zurück, wenn kein Ausgabegerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5c26b-165">Returns "none" if an output device is not set.</span></span>                                                                                             |
| <span data-ttu-id="5c26b-166">product</span><span class="sxs-lookup"><span data-stu-id="5c26b-166">product</span></span>         | <span data-ttu-id="5c26b-167">Ruft eine Beschreibung des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="5c26b-167">Retrieves a description of the device.</span></span> <span data-ttu-id="5c26b-168">Diese Informationen enthalten häufig den Produktnamen und das Modell.</span><span class="sxs-lookup"><span data-stu-id="5c26b-168">This information often includes the product name and model.</span></span> <span data-ttu-id="5c26b-169">Die Länge der Zeichenfolge beträgt höchstens 31 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5c26b-169">The string length will be 31 characters or fewer.</span></span>                                               |
| <span data-ttu-id="5c26b-170">immer noch Algorithmus</span><span class="sxs-lookup"><span data-stu-id="5c26b-170">still algorithm</span></span> | <span data-ttu-id="5c26b-171">Gibt den Namen des aktuellen immer noch Bild Komprimierungs Algorithmus zurück.</span><span class="sxs-lookup"><span data-stu-id="5c26b-171">Returns the name of the current still image compression algorithm.</span></span>                                                                                                                                 |
| <span data-ttu-id="5c26b-172">immer noch Qualität</span><span class="sxs-lookup"><span data-stu-id="5c26b-172">still quality</span></span>   | <span data-ttu-id="5c26b-173">Gibt den Namen für den aktuellen immer noch Bild Qualitäts Deskriptor zurück.</span><span class="sxs-lookup"><span data-stu-id="5c26b-173">Returns the name for the current still image quality descriptor.</span></span> <span data-ttu-id="5c26b-174">Dadurch wird möglicherweise "unknown" zurückgegeben, wenn die Anwendung Parameter auf bestimmte Werte festgelegt hat, die nicht definierten Qualitäten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5c26b-174">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span> |
| <span data-ttu-id="5c26b-175">Nutzung</span><span class="sxs-lookup"><span data-stu-id="5c26b-175">usage</span></span>           | <span data-ttu-id="5c26b-176">Gibt eine Zeichenfolge zurück, in der Nutzungseinschränkungen beschrieben werden, die möglicherweise vom Besitzer der visuellen oder Audiodaten im Arbeitsbereich auferlegt werden.</span><span class="sxs-lookup"><span data-stu-id="5c26b-176">Returns a string describing usage restrictions that might be imposed by the owner of the visual or audio data in the workspace.</span></span>                                                                    |
| <span data-ttu-id="5c26b-177">version</span><span class="sxs-lookup"><span data-stu-id="5c26b-177">version</span></span>         | <span data-ttu-id="5c26b-178">Gibt die releaseebene des Gerätetreibers und der Hardware zurück.</span><span class="sxs-lookup"><span data-stu-id="5c26b-178">Returns the release level of the device driver and hardware.</span></span>                                                                                                                                       |
| <span data-ttu-id="5c26b-179">Video Algorithmus</span><span class="sxs-lookup"><span data-stu-id="5c26b-179">video algorithm</span></span> | <span data-ttu-id="5c26b-180">Gibt den Namen des aktuellen Video Komprimierungs Algorithmus zurück.</span><span class="sxs-lookup"><span data-stu-id="5c26b-180">Returns the name of the current video compression algorithm.</span></span>                                                                                                                                       |
| <span data-ttu-id="5c26b-181">Videoqualität</span><span class="sxs-lookup"><span data-stu-id="5c26b-181">video quality</span></span>   | <span data-ttu-id="5c26b-182">Gibt den Namen für den aktuellen Video Qualitäts Deskriptor zurück.</span><span class="sxs-lookup"><span data-stu-id="5c26b-182">Returns the name for the current video quality descriptor.</span></span> <span data-ttu-id="5c26b-183">Dadurch wird möglicherweise "unknown" zurückgegeben, wenn die Anwendung Parameter auf bestimmte Werte festgelegt hat, die nicht definierten Qualitäten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5c26b-183">This might return "unknown" if the application has set parameters to specific values that do not correspond to defined qualities.</span></span>       |
| <span data-ttu-id="5c26b-184">Fenster Text</span><span class="sxs-lookup"><span data-stu-id="5c26b-184">window text</span></span>     | <span data-ttu-id="5c26b-185">Ruft die Beschriftung des Fensters ab, das vom Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c26b-185">Retrieves the caption of the window used by the device.</span></span>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="5c26b-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="5c26b-186"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5c26b-187">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="5c26b-187">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="5c26b-188">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5c26b-188">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="5c26b-189">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5c26b-189">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c26b-190">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c26b-190">Return Value</span></span>

<span data-ttu-id="5c26b-191">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="5c26b-191">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="5c26b-192">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c26b-192">Examples</span></span>

<span data-ttu-id="5c26b-193">Der folgende Befehl ruft eine Beschreibung der Hardware ab, die dem Gerät "mysound" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5c26b-193">The following command retrieves a description of the hardware associated with the "mysound" device.</span></span>

``` syntax
info mysound product
```

## <a name="requirements"></a><span data-ttu-id="5c26b-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c26b-194">Requirements</span></span>



| <span data-ttu-id="5c26b-195">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c26b-195">Requirement</span></span> | <span data-ttu-id="5c26b-196">Wert</span><span class="sxs-lookup"><span data-stu-id="5c26b-196">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5c26b-197">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c26b-197">Minimum supported client</span></span><br/> | <span data-ttu-id="5c26b-198">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c26b-198">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5c26b-199">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c26b-199">Minimum supported server</span></span><br/> | <span data-ttu-id="5c26b-200">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c26b-200">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5c26b-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c26b-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c26b-202">MCI</span><span class="sxs-lookup"><span data-stu-id="5c26b-202">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5c26b-203">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="5c26b-203">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="5c26b-204">Laden</span><span class="sxs-lookup"><span data-stu-id="5c26b-204">load</span></span>](load.md)
</dt> </dl>

 

