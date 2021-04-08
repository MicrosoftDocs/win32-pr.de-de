---
title: Restore-Befehl
description: Der Restore-Befehl kopiert ein Bild aus einer Datei in den Frame Puffer. Dies ist das Gegenteil des Aufzeichnungs Befehls. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- Restore-Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d7f0f236b26e3e73807b32485442d597e93d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949442"
---
# <a name="restore-command"></a><span data-ttu-id="13e81-106">Restore-Befehl</span><span class="sxs-lookup"><span data-stu-id="13e81-106">restore command</span></span>

<span data-ttu-id="13e81-107">Der Restore-Befehl kopiert ein Bild aus einer Datei in den Frame Puffer.</span><span class="sxs-lookup"><span data-stu-id="13e81-107">The restore command copies a still image from a file to the frame buffer.</span></span> <span data-ttu-id="13e81-108">Dies ist das Gegenteil des [Aufzeichnungs](capture.md) Befehls.</span><span class="sxs-lookup"><span data-stu-id="13e81-108">This is the reverse of the [capture](capture.md) command.</span></span> <span data-ttu-id="13e81-109">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="13e81-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="13e81-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="13e81-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="13e81-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="13e81-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e81-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="13e81-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="13e81-113">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="13e81-113">Identifier of an MCI device.</span></span> <span data-ttu-id="13e81-114">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="13e81-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="13e81-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszrestore*</span><span class="sxs-lookup"><span data-stu-id="13e81-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span></span>
</dt> <dd>

<span data-ttu-id="13e81-116">Mindestens eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="13e81-116">One or more of the following flags.</span></span>



| <span data-ttu-id="13e81-117">Wert</span><span class="sxs-lookup"><span data-stu-id="13e81-117">Value</span></span>           | <span data-ttu-id="13e81-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="13e81-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e81-119">at- *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="13e81-119">at *rectangle*</span></span>  | <span data-ttu-id="13e81-120">Gibt ein Rechteck relativ zum Frame Puffer Ursprung an.</span><span class="sxs-lookup"><span data-stu-id="13e81-120">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="13e81-121">Das *Rechteck* wird als *x1 y1 x2 Y2* angegeben.</span><span class="sxs-lookup"><span data-stu-id="13e81-121">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="13e81-122">Die Koordinaten *x1 y1* geben die linke obere Ecke an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an. Wenn dieses Flag nicht verwendet wird, wird das Bild in die linke obere Ecke des Frame Puffers kopiert.</span><span class="sxs-lookup"><span data-stu-id="13e81-122">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.If this flag is not used, the image is copied to the upper left corner of the frame buffer.</span></span><br/> |
| <span data-ttu-id="13e81-123">*Dateiname*</span><span class="sxs-lookup"><span data-stu-id="13e81-123">from *filename*</span></span> | <span data-ttu-id="13e81-124">Gibt den Namen des zu Rückruf Bilds an.</span><span class="sxs-lookup"><span data-stu-id="13e81-124">Specifies the image filename to recall.</span></span> <span data-ttu-id="13e81-125">Dieses Flag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13e81-125">This flag is required.</span></span>                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="13e81-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="13e81-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="13e81-127">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="13e81-127">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="13e81-128">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="13e81-128">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e81-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13e81-129">Return Value</span></span>

<span data-ttu-id="13e81-130">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="13e81-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e81-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13e81-131">Remarks</span></span>

<span data-ttu-id="13e81-132">Geräte können eine Vielzahl von Bildformaten erkennen. eine Windows-geräteunabhängige Bitmap wird immer erkannt.</span><span class="sxs-lookup"><span data-stu-id="13e81-132">Devices can recognize a variety of image formats; a Windows device-independent bitmap is always recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e81-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13e81-133">Requirements</span></span>



| <span data-ttu-id="13e81-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13e81-134">Requirement</span></span> | <span data-ttu-id="13e81-135">Wert</span><span class="sxs-lookup"><span data-stu-id="13e81-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="13e81-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13e81-136">Minimum supported client</span></span><br/> | <span data-ttu-id="13e81-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13e81-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="13e81-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13e81-138">Minimum supported server</span></span><br/> | <span data-ttu-id="13e81-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13e81-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="13e81-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13e81-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e81-141">MCI</span><span class="sxs-lookup"><span data-stu-id="13e81-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="13e81-142">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="13e81-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="13e81-143">einver</span><span class="sxs-lookup"><span data-stu-id="13e81-143">capture</span></span>](capture.md)
</dt> </dl>

 

