---
title: Schritt Befehl
description: Der Schritt Befehl führt Sie durch die Schritte zum Wiedergeben eines oder mehrerer Frames vor oder nach vorne. Die Standardaktion besteht darin, einen Frame vorwärts zu Stufen. Videodisk-Geräte Digital Video, VCR und CAV-Format erkennen diesen Befehl.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- Schritt Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476584"
---
# <a name="step-command"></a><span data-ttu-id="fac85-106">Schritt Befehl</span><span class="sxs-lookup"><span data-stu-id="fac85-106">step command</span></span>

<span data-ttu-id="fac85-107">Der Schritt Befehl führt Sie durch die Schritte zum Wiedergeben eines oder mehrerer Frames vor oder nach vorne.</span><span class="sxs-lookup"><span data-stu-id="fac85-107">The step command steps the play one or more frames forward or reverse.</span></span> <span data-ttu-id="fac85-108">Die Standardaktion besteht darin, einen Frame vorwärts zu Stufen.</span><span class="sxs-lookup"><span data-stu-id="fac85-108">The default action is to step forward one frame.</span></span> <span data-ttu-id="fac85-109">Videodisk-Geräte Digital Video, VCR und CAV-Format erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="fac85-109">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="fac85-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="fac85-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="fac85-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fac85-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac85-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="fac85-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="fac85-113">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="fac85-113">Identifier of an MCI device.</span></span> <span data-ttu-id="fac85-114">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="fac85-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="fac85-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszstepflags*</span><span class="sxs-lookup"><span data-stu-id="fac85-115"><span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fac85-116">Eines oder beide der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="fac85-116">One or both of the following flags.</span></span>



| <span data-ttu-id="fac85-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fac85-117">Value</span></span>       | <span data-ttu-id="fac85-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fac85-118">Meaning</span></span>                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac85-119">nach *Frames*</span><span class="sxs-lookup"><span data-stu-id="fac85-119">by *frames*</span></span> | <span data-ttu-id="fac85-120">Gibt die Anzahl der zu schrifenden Rahmen an.</span><span class="sxs-lookup"><span data-stu-id="fac85-120">Indicates the number of frames to step.</span></span> <span data-ttu-id="fac85-121">Wenn Sie einen negativen *Rahmen* Wert angeben, können Sie das Flag "Reverse" nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="fac85-121">If you specify a negative *frames* value, you cannot specify the "reverse" flag.</span></span> |
| <span data-ttu-id="fac85-122">reverse</span><span class="sxs-lookup"><span data-stu-id="fac85-122">reverse</span></span>     | <span data-ttu-id="fac85-123">Ändern Sie die Frames in umgekehrter Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="fac85-123">Step the frames in reverse.</span></span>                                                                                              |



 

</dd> <dt>

<span data-ttu-id="fac85-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="fac85-124"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fac85-125">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="fac85-125">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="fac85-126">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fac85-126">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="fac85-127">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fac85-127">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac85-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fac85-128">Return Value</span></span>

<span data-ttu-id="fac85-129">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="fac85-129">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac85-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fac85-130">Requirements</span></span>



| <span data-ttu-id="fac85-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fac85-131">Requirement</span></span> | <span data-ttu-id="fac85-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fac85-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fac85-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fac85-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fac85-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fac85-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fac85-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fac85-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fac85-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fac85-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fac85-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fac85-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac85-138">MCI</span><span class="sxs-lookup"><span data-stu-id="fac85-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fac85-139">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="fac85-139">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

