---
title: Qualitäts Befehl
description: Der Qualitäts Befehl definiert eine benutzerdefinierte Qualitätsstufe für Audiodaten, Video-oder Bild Datenkomprimierung. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- Qualitäts Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344493"
---
# <a name="quality-command"></a><span data-ttu-id="d180c-105">Qualitäts Befehl</span><span class="sxs-lookup"><span data-stu-id="d180c-105">quality command</span></span>

<span data-ttu-id="d180c-106">Der Qualitäts Befehl definiert eine benutzerdefinierte Qualitätsstufe für Audiodaten, Video-oder Bild Datenkomprimierung.</span><span class="sxs-lookup"><span data-stu-id="d180c-106">The quality command defines a custom quality level for either audio, video or still image data compression.</span></span> <span data-ttu-id="d180c-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="d180c-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d180c-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="d180c-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d180c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d180c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d180c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="d180c-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d180c-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="d180c-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d180c-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d180c-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d180c-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszquality*</span><span class="sxs-lookup"><span data-stu-id="d180c-113"><span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*</span></span>
</dt> <dd>

<span data-ttu-id="d180c-114">Mindestens eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="d180c-114">One or more of the following flags.</span></span> <span data-ttu-id="d180c-115">(Eines der drei Flags "Audio", "immer noch" und "Video" muss vorhanden sein.)</span><span class="sxs-lookup"><span data-stu-id="d180c-115">(One of the three flags "audio", "still", and "video" must be present.)</span></span>



| <span data-ttu-id="d180c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d180c-116">Value</span></span>                 | <span data-ttu-id="d180c-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d180c-117">Meaning</span></span>                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d180c-118">*algorithmusalgorithmus*</span><span class="sxs-lookup"><span data-stu-id="d180c-118">algorithm *algorithm*</span></span> | <span data-ttu-id="d180c-119">Ordnet die Qualitätsstufe dem angegebenen *Algorithmus* zu.</span><span class="sxs-lookup"><span data-stu-id="d180c-119">Associates the quality level with the specified *algorithm*.</span></span> <span data-ttu-id="d180c-120">Dieser *Algorithmus* muss vom Gerät unterstützt werden und mit dem verwendeten Flag "Audiodatei", "immer noch" oder "Video" kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="d180c-120">This *algorithm* must be supported by the device and be compatible with the "audio", "still", or "video" flag that is used.</span></span> <span data-ttu-id="d180c-121">Wenn der Wert nicht weggelassen wird, wird der aktuelle Algorithmus verwendet.</span><span class="sxs-lookup"><span data-stu-id="d180c-121">If omitted, the current algorithm is used.</span></span> |
| <span data-ttu-id="d180c-122">*audioname*</span><span class="sxs-lookup"><span data-stu-id="d180c-122">audio *name*</span></span>          | <span data-ttu-id="d180c-123">Gibt an, dass dieser Befehl eine Audioqualität angibt, die mit dem *Namen* identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="d180c-123">Indicates this command specifies an "audio" quality level identified with *name*.</span></span>                                                                                                                                                   |
| <span data-ttu-id="d180c-124">Dialog (dialog)</span><span class="sxs-lookup"><span data-stu-id="d180c-124">dialog</span></span>                | <span data-ttu-id="d180c-125">Fordert an, dass das Gerät ein Dialogfeld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d180c-125">Requests that the device display a dialog box.</span></span> <span data-ttu-id="d180c-126">Dieses Dialogfeld enthält algorithmusspezifische Felder, die intern vom Gerät verwendet werden, um die Struktur zu erstellen, die eine bestimmte Qualitätsstufe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d180c-126">This dialog box has algorithm-specific fields that are used internally by the device to create the structure describing a specific quality level.</span></span>                                    |
| <span data-ttu-id="d180c-127">Handle *handle*</span><span class="sxs-lookup"><span data-stu-id="d180c-127">handle *handle*</span></span>       | <span data-ttu-id="d180c-128">Gibt ein *handle* für eine-Struktur an, die algorithmische spezifische Daten enthält, die eine bestimmte Qualitätsstufe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d180c-128">Specifies a *handle* to a structure that contains algorithmic-specific data describing a specific quality level.</span></span> <span data-ttu-id="d180c-129">Die Strukturen für die Daten, auf die von diesem Handle verwiesen wird, sind gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="d180c-129">The structures for the data referenced by this handle are device specific.</span></span>                                         |
| <span data-ttu-id="d180c-130">immer noch *Name*</span><span class="sxs-lookup"><span data-stu-id="d180c-130">still *name*</span></span>          | <span data-ttu-id="d180c-131">Gibt an, dass der Befehl eine "immer noch"-Qualitätsstufe angibt, die mit dem *Namen*</span><span class="sxs-lookup"><span data-stu-id="d180c-131">Indicates the command specifies a "still" quality level identified with *name.*</span></span>                                                                                                                                                     |
| <span data-ttu-id="d180c-132">*videoname*</span><span class="sxs-lookup"><span data-stu-id="d180c-132">video *name*</span></span>          | <span data-ttu-id="d180c-133">Gibt an, dass der Befehl eine mit dem *Namen* identifizierte "Video"-Qualitätsstufe angibt.</span><span class="sxs-lookup"><span data-stu-id="d180c-133">Indicates the command specifies a "video" quality level identified with *name*.</span></span>                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="d180c-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="d180c-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d180c-135">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="d180c-135">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="d180c-136">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d180c-136">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d180c-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d180c-137">Return Value</span></span>

<span data-ttu-id="d180c-138">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="d180c-138">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d180c-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d180c-139">Remarks</span></span>

<span data-ttu-id="d180c-140">Dieser Befehl definiert einen Zeichen folgen Namen für den Qualitätsgrad, der dann im [setvideo](setvideo.md) -"Quality"-, setvideo-"immer Qualität"-oder [SetAudio"](setaudio.md) Quality"-Befehl verwendet werden kann, um ihn als Aktuelles Video, noch immer oder als audiokomprimierungsqualitätsstufe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d180c-140">This command defines a string name for the quality level, which can then be used in a [setvideo](setvideo.md) "quality", setvideo "still quality", or [setaudio](setaudio.md) "quality" command to establish it as the current video, still, or audio-compression quality level.</span></span>

## <a name="requirements"></a><span data-ttu-id="d180c-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d180c-141">Requirements</span></span>



| <span data-ttu-id="d180c-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d180c-142">Requirement</span></span> | <span data-ttu-id="d180c-143">Wert</span><span class="sxs-lookup"><span data-stu-id="d180c-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d180c-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d180c-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d180c-145">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d180c-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d180c-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d180c-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d180c-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d180c-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d180c-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d180c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d180c-149">MCI</span><span class="sxs-lookup"><span data-stu-id="d180c-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d180c-150">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="d180c-150">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d180c-151">setaudiodatei</span><span class="sxs-lookup"><span data-stu-id="d180c-151">setaudio</span></span>](setaudio.md)
</dt> <dt>

[<span data-ttu-id="d180c-152">setvideo</span><span class="sxs-lookup"><span data-stu-id="d180c-152">setvideo</span></span>](setvideo.md)
</dt> </dl>

 

