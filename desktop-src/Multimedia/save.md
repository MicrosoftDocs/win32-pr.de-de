---
title: Befehl "Speichern"
description: Mit dem Befehl "Speichern" wird eine MCI-Datei gespeichert. Video-Overlay-und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, unterstützen die MCIAVI-und mciseq-Treiber dies nicht.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- Befehl "Speichern" Windows Multimedia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339537"
---
# <a name="save-command"></a><span data-ttu-id="89985-106">Befehl "Speichern"</span><span class="sxs-lookup"><span data-stu-id="89985-106">save command</span></span>

<span data-ttu-id="89985-107">Mit dem Befehl "Speichern" wird eine MCI-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="89985-107">The save command saves an MCI file.</span></span> <span data-ttu-id="89985-108">Video-Overlay-und Waveform-Audiogeräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="89985-108">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="89985-109">Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, unterstützen die MCIAVI-und mciseq-Treiber dies nicht.</span><span class="sxs-lookup"><span data-stu-id="89985-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not support it.</span></span>

<span data-ttu-id="89985-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="89985-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="89985-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="89985-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89985-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="89985-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="89985-113">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="89985-113">Identifier of an MCI device.</span></span> <span data-ttu-id="89985-114">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="89985-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="89985-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszfilename*</span><span class="sxs-lookup"><span data-stu-id="89985-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span></span>
</dt> <dd>

<span data-ttu-id="89985-116">Flag, das den Namen der zu speichernden Datei und optional zusätzliche Flags angibt, die den Speichervorgang verändern.</span><span class="sxs-lookup"><span data-stu-id="89985-116">Flag specifying the name of the file being saved and, optionally, additional flags modifying the save operation.</span></span> <span data-ttu-id="89985-117">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Save** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="89985-117">The following table lists device types that recognize the **save** command and the flags used by each type.</span></span>



| <span data-ttu-id="89985-118">Wert</span><span class="sxs-lookup"><span data-stu-id="89985-118">Value</span></span>        | <span data-ttu-id="89985-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="89985-119">Meaning</span></span>              | <span data-ttu-id="89985-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="89985-120">Meaning</span></span>               |
|--------------|----------------------|-----------------------|
| <span data-ttu-id="89985-121">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="89985-121">digitalvideo</span></span> | <span data-ttu-id="89985-122">beim *Rechteck* Abbrechen</span><span class="sxs-lookup"><span data-stu-id="89985-122">abort at *rectangle*</span></span> | <span data-ttu-id="89985-123">*Dateiname* keepreserve</span><span class="sxs-lookup"><span data-stu-id="89985-123">*filename* keepreserve</span></span> |
| <span data-ttu-id="89985-124">overlay</span><span class="sxs-lookup"><span data-stu-id="89985-124">overlay</span></span>      | <span data-ttu-id="89985-125">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="89985-125">at *rectangle*</span></span>       | <span data-ttu-id="89985-126">*filename*</span><span class="sxs-lookup"><span data-stu-id="89985-126">*filename*</span></span>            |
| <span data-ttu-id="89985-127">sequencer</span><span class="sxs-lookup"><span data-stu-id="89985-127">sequencer</span></span>    | <span data-ttu-id="89985-128">*filename*</span><span class="sxs-lookup"><span data-stu-id="89985-128">*filename*</span></span>           |                       |
| <span data-ttu-id="89985-129">waveaudiodatei</span><span class="sxs-lookup"><span data-stu-id="89985-129">waveaudio</span></span>    | <span data-ttu-id="89985-130">*filename*</span><span class="sxs-lookup"><span data-stu-id="89985-130">*filename*</span></span>           |                       |



 

<span data-ttu-id="89985-131">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszfilename** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="89985-131">The following table lists the flags that can be specified in the **lpszFilename** parameter and their meanings.</span></span>



| <span data-ttu-id="89985-132">Wert</span><span class="sxs-lookup"><span data-stu-id="89985-132">Value</span></span>          | <span data-ttu-id="89985-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="89985-133">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89985-134">abort</span><span class="sxs-lookup"><span data-stu-id="89985-134">abort</span></span>          | <span data-ttu-id="89985-135">Beendet einen aktuell ausgeführten **Speicher** Vorgang.</span><span class="sxs-lookup"><span data-stu-id="89985-135">Stops a **save** operation in progress.</span></span> <span data-ttu-id="89985-136">Wenn diese Option verwendet wird, muss dies das einzige vorhandene Element sein.</span><span class="sxs-lookup"><span data-stu-id="89985-136">If used, this must be the only item present.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="89985-137">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="89985-137">at *rectangle*</span></span> | <span data-ttu-id="89985-138">Gibt ein Rechteck relativ zum Frame Puffer Ursprung an.</span><span class="sxs-lookup"><span data-stu-id="89985-138">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="89985-139">Das *Rechteck* wird als *x1 y1 x2 Y2* angegeben.</span><span class="sxs-lookup"><span data-stu-id="89985-139">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="89985-140">Die Koordinaten *x1 y1* geben die linke obere Ecke an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an. Für Digital Video-Geräte wird der [Erfassungs](capture.md) Befehl verwendet, um den Inhalt des Frame Puffers aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="89985-140">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.For digital-video devices, the [capture](capture.md) command is used to capture the contents of the frame buffer.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="89985-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="89985-141">*filename*</span></span>     | <span data-ttu-id="89985-142">Gibt den Dateinamen an, der der Datendatei zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="89985-142">Specifies the filename to assign to the data file.</span></span> <span data-ttu-id="89985-143">Wenn kein Pfad angegeben ist, wird die Datei auf dem Datenträger und im Verzeichnis abgelegt, das zuvor im expliziten oder impliziten [Reserve](reserve.md) Befehl angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="89985-143">If a path is not specified, the file will be placed on the disk and in the directory previously specified on the explicit or implicit [reserve](reserve.md) command.</span></span> <span data-ttu-id="89985-144">Wenn **Reserve** nicht ausgestellt wurde, sind das Standard Laufwerk und das Standardverzeichnis diejenigen, die der Aufgabe der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="89985-144">If **reserve** has not been issued, the default drive and directory are those associated with the application's task.</span></span> <span data-ttu-id="89985-145">Wenn ein Pfad angegeben ist, muss sich das Gerät möglicherweise auf dem Laufwerk befinden, das von der expliziten oder impliziten **Reserve** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="89985-145">If a path is specified, the device might require it to be on the disk drive specified by the explicit or implicit **reserve**.</span></span> <span data-ttu-id="89985-146">Dieses Flag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="89985-146">This flag is required.</span></span> |
| <span data-ttu-id="89985-147">keepreserve</span><span class="sxs-lookup"><span data-stu-id="89985-147">keepreserve</span></span>    | <span data-ttu-id="89985-148">Gibt an, dass nicht verwendeter Speicherplatz, der vom ursprünglichen **Reserve** Befehl übrig geblieben ist, nicht aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="89985-148">Specifies that unused disk space left over from the original **reserve** command is not deallocated.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="89985-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="89985-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="89985-150">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="89985-150">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="89985-151">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="89985-151">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="89985-152">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="89985-152">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89985-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89985-153">Return Value</span></span>

<span data-ttu-id="89985-154">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="89985-154">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="89985-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89985-155">Remarks</span></span>

<span data-ttu-id="89985-156">Die *filename* -Variable ist erforderlich, wenn das Gerät mithilfe des "neuen" Geräte Bezeichners geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="89985-156">The *filename* variable is required if the device was opened using the "new" device identifier.</span></span>

## <a name="examples"></a><span data-ttu-id="89985-157">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89985-157">Examples</span></span>

<span data-ttu-id="89985-158">Der folgende Befehl speichert den gesamten Video Puffer in einer Datei namens vcapfile. TGA.</span><span class="sxs-lookup"><span data-stu-id="89985-158">The following command saves the entire video buffer to a file named VCAPFILE.TGA.</span></span>

``` syntax
save vboard c:\vcap\vcapfile.tga
```

## <a name="requirements"></a><span data-ttu-id="89985-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89985-159">Requirements</span></span>



| <span data-ttu-id="89985-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89985-160">Requirement</span></span> | <span data-ttu-id="89985-161">Wert</span><span class="sxs-lookup"><span data-stu-id="89985-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="89985-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89985-162">Minimum supported client</span></span><br/> | <span data-ttu-id="89985-163">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89985-163">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89985-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89985-164">Minimum supported server</span></span><br/> | <span data-ttu-id="89985-165">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89985-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="89985-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89985-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89985-167">MCI</span><span class="sxs-lookup"><span data-stu-id="89985-167">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="89985-168">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="89985-168">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="89985-169">einver</span><span class="sxs-lookup"><span data-stu-id="89985-169">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="89985-170">Reserve</span><span class="sxs-lookup"><span data-stu-id="89985-170">reserve</span></span>](reserve.md)
</dt> </dl>

 

