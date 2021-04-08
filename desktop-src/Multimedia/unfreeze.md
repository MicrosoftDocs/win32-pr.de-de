---
title: Befehl zum Einfrieren aufheben
description: Mit dem Befehl zum Aufheben der Fixierung wird die Video Erfassung im Frame Puffer wieder aktiviert, nachdem Sie durch den Freeze-Befehl deaktiviert wurde. Dieser Befehl wird von digitalen Video-, VCR-und Video Überlagerungs Geräten erkannt.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- Befehl zum Aufheben der Fixierung von Windows Multimedia
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743560"
---
# <a name="unfreeze-command"></a><span data-ttu-id="a303e-105">Befehl zum Einfrieren aufheben</span><span class="sxs-lookup"><span data-stu-id="a303e-105">unfreeze command</span></span>

<span data-ttu-id="a303e-106">Mit dem Befehl zum Aufheben der Fixierung wird die Video Erfassung im Frame Puffer wieder aktiviert, nachdem Sie durch den [Freeze](freeze.md) -Befehl deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="a303e-106">The unfreeze command reenables video acquisition to the frame buffer after it has been disabled by the [freeze](freeze.md) command.</span></span> <span data-ttu-id="a303e-107">Dieser Befehl wird von digitalen Video-, VCR-und Video Überlagerungs Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="a303e-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="a303e-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="a303e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a303e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a303e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a303e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="a303e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a303e-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="a303e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a303e-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a303e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a303e-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszunfreeze*</span><span class="sxs-lookup"><span data-stu-id="a303e-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="a303e-114">Flag zum erneuten Aktivieren der Video Erfassung für den Frame Puffer.</span><span class="sxs-lookup"><span data-stu-id="a303e-114">Flag for reenabling video acquisition to the frame buffer.</span></span> <span data-ttu-id="a303e-115">In der folgenden Tabelle sind die Gerätetypen aufgeführt **, die den Befehl zum** Aufheben der Fixierung und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="a303e-115">The following table lists device types that recognize the **unfreeze** command and the flags used by each type.</span></span>



| <span data-ttu-id="a303e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a303e-116">Value</span></span>        | <span data-ttu-id="a303e-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a303e-117">Meaning</span></span>        |
|--------------|----------------|
| <span data-ttu-id="a303e-118">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="a303e-118">digitalvideo</span></span> | <span data-ttu-id="a303e-119">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="a303e-119">at *rectangle*</span></span> |
| <span data-ttu-id="a303e-120">overlay</span><span class="sxs-lookup"><span data-stu-id="a303e-120">overlay</span></span>      | <span data-ttu-id="a303e-121">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="a303e-121">at *rectangle*</span></span> |
| <span data-ttu-id="a303e-122">VCR</span><span class="sxs-lookup"><span data-stu-id="a303e-122">vcr</span></span>          | <span data-ttu-id="a303e-123">Eingabe Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a303e-123">input output</span></span>   |



 

<span data-ttu-id="a303e-124">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszunfreeze** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="a303e-124">The following table lists the flags that can be specified in the **lpszUnfreeze** parameter and their meanings.</span></span>



| <span data-ttu-id="a303e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a303e-125">Value</span></span>          | <span data-ttu-id="a303e-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a303e-126">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a303e-127">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="a303e-127">at *rectangle*</span></span> | <span data-ttu-id="a303e-128">Gibt die Region an, in der die Video Beschaffung erneut aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="a303e-128">Specifies the region that will have video acquisition reenabled.</span></span> <span data-ttu-id="a303e-129">Das Rechteck ist relativ zum Video Puffer Ursprung und wird als *x1 y1 x2 Y2* angegeben.</span><span class="sxs-lookup"><span data-stu-id="a303e-129">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="a303e-130">Die Koordinaten *x1 y1* geben die linke obere Ecke des Rechtecks an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an.</span><span class="sxs-lookup"><span data-stu-id="a303e-130">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="a303e-131">input</span><span class="sxs-lookup"><span data-stu-id="a303e-131">input</span></span>          | <span data-ttu-id="a303e-132">Heben Sie die Fixierung des Eingabe Bilds auf.</span><span class="sxs-lookup"><span data-stu-id="a303e-132">Unfreeze the input image.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a303e-133">output</span><span class="sxs-lookup"><span data-stu-id="a303e-133">output</span></span>         | <span data-ttu-id="a303e-134">Entsperrung des Ausgabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="a303e-134">Unfreeze the output image.</span></span> <span data-ttu-id="a303e-135">Wenn weder "Input" noch "Output" angegeben wird, wird "Output" angenommen.</span><span class="sxs-lookup"><span data-stu-id="a303e-135">If neither "input" nor "output" is given, "output" is assumed.</span></span>                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="a303e-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="a303e-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a303e-137">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="a303e-137">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="a303e-138">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a303e-138">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="a303e-139">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a303e-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a303e-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a303e-140">Return Value</span></span>

<span data-ttu-id="a303e-141">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="a303e-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="a303e-142">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a303e-142">Examples</span></span>

<span data-ttu-id="a303e-143">Der folgende Befehl entfriert einen Bereich des Video Puffers.</span><span class="sxs-lookup"><span data-stu-id="a303e-143">The following command unfreezes a region of the video buffer.</span></span>

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a><span data-ttu-id="a303e-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a303e-144">Requirements</span></span>



| <span data-ttu-id="a303e-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a303e-145">Requirement</span></span> | <span data-ttu-id="a303e-146">Wert</span><span class="sxs-lookup"><span data-stu-id="a303e-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a303e-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a303e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a303e-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a303e-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a303e-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a303e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a303e-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a303e-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a303e-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a303e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a303e-152">MCI</span><span class="sxs-lookup"><span data-stu-id="a303e-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a303e-153">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="a303e-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="a303e-154">ge</span><span class="sxs-lookup"><span data-stu-id="a303e-154">freeze</span></span>](freeze.md)
</dt> </dl>

 

