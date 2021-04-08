---
title: Reserve Befehl
description: Der Reserve Befehl ordnet dem Arbeitsbereich der Geräte Instanz zusammenhängenden Speicherplatz zu. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- Reserve Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949441"
---
# <a name="reserve-command"></a><span data-ttu-id="84c2a-105">Reserve Befehl</span><span class="sxs-lookup"><span data-stu-id="84c2a-105">reserve command</span></span>

<span data-ttu-id="84c2a-106">Der Reserve Befehl ordnet dem Arbeitsbereich der Geräte Instanz zusammenhängenden Speicherplatz zu.</span><span class="sxs-lookup"><span data-stu-id="84c2a-106">The reserve command allocates contiguous disk space for the device instance's workspace.</span></span> <span data-ttu-id="84c2a-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="84c2a-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="84c2a-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="84c2a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="84c2a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="84c2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c2a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="84c2a-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="84c2a-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="84c2a-111">Identifier of an MCI device.</span></span> <span data-ttu-id="84c2a-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="84c2a-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="84c2a-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszreserve*</span><span class="sxs-lookup"><span data-stu-id="84c2a-113"><span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*</span></span>
</dt> <dd>

<span data-ttu-id="84c2a-114">Mindestens eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="84c2a-114">One or more of the following flags.</span></span>



| <span data-ttu-id="84c2a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="84c2a-115">Value</span></span>           | <span data-ttu-id="84c2a-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="84c2a-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c2a-117">in *Pfad*</span><span class="sxs-lookup"><span data-stu-id="84c2a-117">in *path*</span></span>       | <span data-ttu-id="84c2a-118">Gibt das Laufwerk und den Verzeichnispfad (aber nicht den Namen) einer temporären Datei an, die zum Speichern der aufgezeichneten Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84c2a-118">Specifies the drive and directory path (but not the name) of a temporary file used to hold recorded data.</span></span> <span data-ttu-id="84c2a-119">Der Name dieser Datei wird vom Gerät angegeben.</span><span class="sxs-lookup"><span data-stu-id="84c2a-119">The name of this file is specified by the device.</span></span> <span data-ttu-id="84c2a-120">Die temporäre Datei wird gelöscht, wenn das Gerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="84c2a-120">The temporary file is deleted when the device is closed.</span></span> <span data-ttu-id="84c2a-121">Wenn dieses Flag weggelassen wird, gibt das Gerät den Speicherort des Speicherplatzes an.</span><span class="sxs-lookup"><span data-stu-id="84c2a-121">If this flag is omitted, the device specifies the location of the disk space.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="84c2a-122">Größen *Dauer*</span><span class="sxs-lookup"><span data-stu-id="84c2a-122">size *duration*</span></span> | <span data-ttu-id="84c2a-123">Gibt die ungefähre Menge an Speicherplatz an, die im Arbeitsbereich reserviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="84c2a-123">Specifies the approximate amount of disk space to reserve in the workspace.</span></span> <span data-ttu-id="84c2a-124">Der *Duration* -Wert wird im aktuellen Zeitformat angegeben.</span><span class="sxs-lookup"><span data-stu-id="84c2a-124">The *duration* value is specified in the current time format.</span></span> <span data-ttu-id="84c2a-125">Das Gerät basiert auf der Schätzung des erforderlichen Speicherplatzes auf den folgenden Parametern: der angeforderten Zeit, dem Dateiformat, dem Video-und Audiokomprimierungs Algorithmus und den gültigen Komprimierungs Qualitätswerten.</span><span class="sxs-lookup"><span data-stu-id="84c2a-125">The device bases its estimate of the required disk space on the following parameters: the requested time, the file format, the video and audio compression algorithm, and the compression quality values in effect.</span></span> <span data-ttu-id="84c2a-126">Wenn [setvideo](setvideo.md) "Record" den Wert "Off" hat, ist der Speicherplatz nur für Audiodaten reserviert.</span><span class="sxs-lookup"><span data-stu-id="84c2a-126">If [setvideo](setvideo.md) "record" is "off", then space is reserved only for audio.</span></span> <span data-ttu-id="84c2a-127">Wenn [setaudiodaten](setaudio.md) "Record" den Wert "Off" hat, ist der Speicherplatz nur für Videos reserviert.</span><span class="sxs-lookup"><span data-stu-id="84c2a-127">If [setaudio](setaudio.md) "record" is "off", then space is reserved only for video.</span></span> <span data-ttu-id="84c2a-128">Wenn beide "Off" oder " *Duration* " gleich 0 (null) sind, ist kein Speicherplatz reserviert, und der vorhandene reservierte Speicherplatz wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="84c2a-128">If both are "off", or if *duration* is zero, then no space is reserved and any existing reserved space is deallocated.</span></span> <span data-ttu-id="84c2a-129">Wenn dieses Flag ausgelassen wird, verwendet das Gerät einen Geräte definierten Standardwert.</span><span class="sxs-lookup"><span data-stu-id="84c2a-129">If this flag is omitted, the device will use a device-defined default.</span></span> |



 

</dd> <dt>

<span data-ttu-id="84c2a-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="84c2a-130"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="84c2a-131">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="84c2a-131">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="84c2a-132">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="84c2a-132">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c2a-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84c2a-133">Return Value</span></span>

<span data-ttu-id="84c2a-134">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="84c2a-134">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84c2a-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84c2a-135">Remarks</span></span>

<span data-ttu-id="84c2a-136">Bei Bedarf verwenden nachfolgende [Daten Satz](record.md) -oder [Speicher](save.md) Befehle den von diesem Befehl reservierten Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="84c2a-136">If needed, subsequent [record](record.md) or [save](save.md) commands use the space reserved by this command.</span></span> <span data-ttu-id="84c2a-137">Wenn der Arbeitsbereich nicht gespeicherte Daten enthält, gehen die Daten verloren.</span><span class="sxs-lookup"><span data-stu-id="84c2a-137">If the workspace contains unsaved data, the data is lost.</span></span> <span data-ttu-id="84c2a-138">Einige Geräte erfordern keine Reservierung und ignorieren Sie.</span><span class="sxs-lookup"><span data-stu-id="84c2a-138">Some devices do not require reserve and ignore it.</span></span> <span data-ttu-id="84c2a-139">Wenn der Speicherplatz vor dem Aufzeichnen nicht reserviert ist, führt der Datensatz-Befehl eine implizite Reserve mit gerätespezifischen Standardflags aus.</span><span class="sxs-lookup"><span data-stu-id="84c2a-139">If disk space is not reserved prior to recording, the record command performs an implied reserve with device-specific default flags.</span></span> <span data-ttu-id="84c2a-140">Verwenden Sie einen expliziten Reserve Befehl, wenn Sie eine bessere Kontrolle darüber haben möchten, wann die Verzögerung für die Datenträger Zuordnung auftritt, und Steuern Sie, wie viel Speicherplatz zugewiesen ist, und Steuern Sie den Speicherort des Speicherplatzes.</span><span class="sxs-lookup"><span data-stu-id="84c2a-140">Use an explicit reserve command if you want better control of when the delay for disk allocation occurs, control of how much space is allocated, and control of where the disk space is allocated.</span></span> <span data-ttu-id="84c2a-141">Die Anwendung kann die Menge und den Speicherort des zuvor reservierten Speicherplatzes mit nachfolgenden Reserve Befehlen ändern.</span><span class="sxs-lookup"><span data-stu-id="84c2a-141">Your application can change the amount and location of previously reserved disk space with subsequent reserve commands.</span></span> <span data-ttu-id="84c2a-142">Der zugeordnete und noch nicht verwendete Speicherplatz wird nicht aufgehoben, bis alle aufgezeichneten Daten gespeichert oder die Geräte Instanz geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="84c2a-142">Any allocated and still unused disk space is not deallocated until any recorded data is saved, or until the device instance is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c2a-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84c2a-143">Requirements</span></span>



| <span data-ttu-id="84c2a-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84c2a-144">Requirement</span></span> | <span data-ttu-id="84c2a-145">Wert</span><span class="sxs-lookup"><span data-stu-id="84c2a-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="84c2a-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84c2a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="84c2a-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84c2a-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="84c2a-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84c2a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="84c2a-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84c2a-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="84c2a-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84c2a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c2a-151">MCI</span><span class="sxs-lookup"><span data-stu-id="84c2a-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="84c2a-152">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="84c2a-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="84c2a-153">record</span><span class="sxs-lookup"><span data-stu-id="84c2a-153">record</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="84c2a-154">Speichern</span><span class="sxs-lookup"><span data-stu-id="84c2a-154">save</span></span>](save.md)
</dt> <dt>

[<span data-ttu-id="84c2a-155">setaudiodatei</span><span class="sxs-lookup"><span data-stu-id="84c2a-155">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="84c2a-156">setvideo</span><span class="sxs-lookup"><span data-stu-id="84c2a-156">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

