---
title: settuner-Befehl
description: Der settuner-Befehl ändert den aktuellen Tuner oder die channeleinstellung des aktuellen Tuners. VCR-Geräte erkennen diesen Befehl.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- settuner-Befehl, Windows Multimedia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479368"
---
# <a name="settuner-command"></a><span data-ttu-id="6f890-105">settuner-Befehl</span><span class="sxs-lookup"><span data-stu-id="6f890-105">settuner command</span></span>

<span data-ttu-id="6f890-106">Der settuner-Befehl ändert den aktuellen Tuner oder die channeleinstellung des aktuellen Tuners.</span><span class="sxs-lookup"><span data-stu-id="6f890-106">The settuner command changes the current tuner or the channel setting of the current tuner.</span></span> <span data-ttu-id="6f890-107">VCR-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="6f890-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="6f890-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="6f890-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6f890-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f890-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f890-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="6f890-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6f890-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="6f890-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6f890-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="6f890-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6f890-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpsztuner*</span><span class="sxs-lookup"><span data-stu-id="6f890-113"><span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*</span></span>
</dt> <dd>

<span data-ttu-id="6f890-114">Eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="6f890-114">One of the following flags.</span></span>



| <span data-ttu-id="6f890-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6f890-115">Value</span></span>                            | <span data-ttu-id="6f890-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6f890-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f890-117">*kanalchannel*</span><span class="sxs-lookup"><span data-stu-id="6f890-117">channel *channel*</span></span>                | <span data-ttu-id="6f890-118">Legt den Tuner auf *Channel* fest.</span><span class="sxs-lookup"><span data-stu-id="6f890-118">Sets the tuner to *channel*.</span></span> <span data-ttu-id="6f890-119">Abhängig vom VCR ist es möglicherweise nicht möglich, den Kanal während der Aufzeichnung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6f890-119">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="6f890-120">Ein Kanal, der größer als der Höchstwert ist, legt den Tuner auf den maximalen Kanal fest.</span><span class="sxs-lookup"><span data-stu-id="6f890-120">A channel larger than the maximum sets the tuner to the maximum channel.</span></span>                                                                                                                    |
| <span data-ttu-id="6f890-121">Channel Seek-upchannel-Suche nach unten</span><span class="sxs-lookup"><span data-stu-id="6f890-121">channel seek upchannel seek down</span></span> | <span data-ttu-id="6f890-122">Sucht den nächsten Kanal mit einem gültigen Signal.</span><span class="sxs-lookup"><span data-stu-id="6f890-122">Seeks the next channel with a valid signal.</span></span> <span data-ttu-id="6f890-123">"Suchen" erhöht die Kanalnummer in der Suche.</span><span class="sxs-lookup"><span data-stu-id="6f890-123">"Seek up" increments the channel number in its search.</span></span> <span data-ttu-id="6f890-124">"Suchen" Dekremente die Kanalnummer in der Suche.</span><span class="sxs-lookup"><span data-stu-id="6f890-124">"Seek down" decrements the channel number in its search.</span></span> <span data-ttu-id="6f890-125">Der Tuner wird mit Channel 1 umschlossen, wenn die maximale Kanalnummer überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="6f890-125">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="6f890-126">Entsprechend umschließt der Tuner bei der Suche den maximalen Kanal.</span><span class="sxs-lookup"><span data-stu-id="6f890-126">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span> |
| <span data-ttu-id="6f890-127">Kanal-upchannel nach unten</span><span class="sxs-lookup"><span data-stu-id="6f890-127">channel upchannel down</span></span>           | <span data-ttu-id="6f890-128">Inkrement oder Dekrement für den tunkanchannel.</span><span class="sxs-lookup"><span data-stu-id="6f890-128">Increments or decrements the tuner channel.</span></span> <span data-ttu-id="6f890-129">Abhängig vom VCR ist es möglicherweise nicht möglich, den Kanal während der Aufzeichnung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6f890-129">You might not be able to change the channel while recording, depending on the VCR.</span></span> <span data-ttu-id="6f890-130">Der Tuner wird mit Channel 1 umschlossen, wenn die maximale Kanalnummer überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="6f890-130">The tuner wraps to channel 1 when the maximum channel number is exceeded.</span></span> <span data-ttu-id="6f890-131">Entsprechend umschließt der Tuner bei der Suche den maximalen Kanal.</span><span class="sxs-lookup"><span data-stu-id="6f890-131">Similarly, when seeking down, the tuner wraps to the maximum channel.</span></span>                              |
| <span data-ttu-id="6f890-132">Zahlen *Nummer*</span><span class="sxs-lookup"><span data-stu-id="6f890-132">number *number*</span></span>                  | <span data-ttu-id="6f890-133">Gibt den Tuner an, der vom settuner-Befehl beeinflusst werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f890-133">Specifies the tuner to be affected by the settuner command.</span></span> <span data-ttu-id="6f890-134">Wenn *Number* nicht angegeben wird, wird der Standardwert 1 angenommen.</span><span class="sxs-lookup"><span data-stu-id="6f890-134">If *number* is not given, the default value of 1 is assumed.</span></span>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="6f890-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="6f890-135"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6f890-136">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="6f890-136">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6f890-137">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6f890-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f890-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f890-138">Return Value</span></span>

<span data-ttu-id="6f890-139">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="6f890-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f890-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f890-140">Requirements</span></span>



| <span data-ttu-id="6f890-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f890-141">Requirement</span></span> | <span data-ttu-id="6f890-142">Wert</span><span class="sxs-lookup"><span data-stu-id="6f890-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6f890-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f890-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6f890-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f890-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6f890-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f890-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6f890-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f890-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6f890-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f890-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f890-148">MCI</span><span class="sxs-lookup"><span data-stu-id="6f890-148">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6f890-149">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="6f890-149">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

