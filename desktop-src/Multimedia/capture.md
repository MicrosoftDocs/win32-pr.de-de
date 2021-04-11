---
title: Aufzeichnungs Befehl
description: Mit dem Aufzeichnungs Befehl wird der Inhalt des Frame Puffers kopiert und in der angegebenen Datei gespeichert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- Erfassungs Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105920"
---
# <a name="capture-command"></a><span data-ttu-id="946bc-105">Aufzeichnungs Befehl</span><span class="sxs-lookup"><span data-stu-id="946bc-105">capture command</span></span>

<span data-ttu-id="946bc-106">Mit dem Aufzeichnungs Befehl wird der Inhalt des Frame Puffers kopiert und in der angegebenen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="946bc-106">The capture command copies the contents of the frame buffer and stores it in the specified file.</span></span> <span data-ttu-id="946bc-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="946bc-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="946bc-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="946bc-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="946bc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="946bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="946bc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="946bc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="946bc-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="946bc-111">Identifier of an MCI device.</span></span> <span data-ttu-id="946bc-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="946bc-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="946bc-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszcapture*</span><span class="sxs-lookup"><span data-stu-id="946bc-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span></span>
</dt> <dd>

<span data-ttu-id="946bc-114">Mindestens eines der folgenden Flags:</span><span class="sxs-lookup"><span data-stu-id="946bc-114">One or more of the following flags:</span></span>



| <span data-ttu-id="946bc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="946bc-115">Value</span></span>          | <span data-ttu-id="946bc-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="946bc-116">Meaning</span></span>                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946bc-117">als *Pfadname*</span><span class="sxs-lookup"><span data-stu-id="946bc-117">as *pathname*</span></span>  | <span data-ttu-id="946bc-118">Gibt den Zielpfad und den Dateinamen für das erfasste Abbild an.</span><span class="sxs-lookup"><span data-stu-id="946bc-118">Specifies the destination path and filename for the captured image.</span></span> <span data-ttu-id="946bc-119">Dieses Flag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="946bc-119">This flag is required.</span></span>                                                                                                                                                                |
| <span data-ttu-id="946bc-120">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="946bc-120">at *rectangle*</span></span> | <span data-ttu-id="946bc-121">Gibt den rechteckigen Bereich innerhalb des Frame Puffers an, den das Gerät anlegt und auf dem Datenträger speichert.</span><span class="sxs-lookup"><span data-stu-id="946bc-121">Specifies the rectangular region within the frame buffer that the device crops and saves to disk.</span></span> <span data-ttu-id="946bc-122">Wenn der Wert nicht angegeben wird, wird für den zugeschnittenen Bereich standardmäßig das Rechteck verwendet, das für den vorherigen Befehl "Quelle" für diese Geräte Instanz [festgelegt wurde](put.md)</span><span class="sxs-lookup"><span data-stu-id="946bc-122">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [put](put.md) "source" command for this device instance.</span></span> |



 

</dd> <dt>

<span data-ttu-id="946bc-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="946bc-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="946bc-124">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="946bc-124">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="946bc-125">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="946bc-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="946bc-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="946bc-126">Return Value</span></span>

<span data-ttu-id="946bc-127">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="946bc-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="946bc-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="946bc-128">Remarks</span></span>

<span data-ttu-id="946bc-129">Bei diesem Befehl tritt möglicherweise ein Fehler auf, wenn das Gerät gerade ein Bewegungsvideo wieder gibt oder ein anderer ressourcenintensiver Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="946bc-129">This command might fail if the device is currently playing motion video or executing some other resource-intensive operation.</span></span> <span data-ttu-id="946bc-130">Wenn der Frame Puffer in Echtzeit aktualisiert wird, wird die Aktualisierung vorübergehend angehalten, sodass ein Abbild erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="946bc-130">If the frame buffer is being updated in real time, the updating momentarily pauses so that a complete image is captured.</span></span> <span data-ttu-id="946bc-131">Wenn das Gerät die Aktualisierung anhält, kann es einen visuellen oder hörbaren Effekt geben.</span><span class="sxs-lookup"><span data-stu-id="946bc-131">If the device pauses the updating, there might be a visual or audible effect.</span></span> <span data-ttu-id="946bc-132">Wenn das Dateiformat, der Komprimierungs Algorithmus und die Qualitäts Ebenen nicht festgelegt wurden, werden die Standardwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="946bc-132">If the file format, compression algorithm, and quality levels have not been set, their defaults are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="946bc-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="946bc-133">Requirements</span></span>



| <span data-ttu-id="946bc-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="946bc-134">Requirement</span></span> | <span data-ttu-id="946bc-135">Wert</span><span class="sxs-lookup"><span data-stu-id="946bc-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="946bc-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="946bc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="946bc-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="946bc-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="946bc-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="946bc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="946bc-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="946bc-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="946bc-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="946bc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946bc-141">MCI</span><span class="sxs-lookup"><span data-stu-id="946bc-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="946bc-142">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="946bc-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="946bc-143">stellte</span><span class="sxs-lookup"><span data-stu-id="946bc-143">put</span></span>](put.md)
</dt> </dl>

 

