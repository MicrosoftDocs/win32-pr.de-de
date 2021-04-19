---
title: Signal Befehl
description: Der Signal-Befehl identifiziert eine angegebene Position im Arbeitsbereich, indem die Anwendung eine mm \_ mcisignal-Nachricht sendet. Dieser Befehl wird von Digital-Video-Geräten erkannt. MCIAVI unterstützt jeweils nur ein aktives Signal.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- Signal Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339977"
---
# <a name="signal-command"></a><span data-ttu-id="1efdf-106">Signal Befehl</span><span class="sxs-lookup"><span data-stu-id="1efdf-106">signal command</span></span>

<span data-ttu-id="1efdf-107">Der Signal-Befehl identifiziert eine angegebene Position im Arbeitsbereich, indem die Anwendung eine [mm \_ mcisignal](mm-mcisignal.md) -Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="1efdf-107">The signal command identifies a specified position in the workspace by sending the application an [MM\_MCISIGNAL](mm-mcisignal.md) message.</span></span> <span data-ttu-id="1efdf-108">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="1efdf-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="1efdf-109">MCIAVI unterstützt jeweils nur ein aktives Signal.</span><span class="sxs-lookup"><span data-stu-id="1efdf-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="1efdf-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="1efdf-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="1efdf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1efdf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1efdf-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="1efdf-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1efdf-113">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="1efdf-113">Identifier of an MCI device.</span></span> <span data-ttu-id="1efdf-114">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1efdf-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="1efdf-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszsignalflags*</span><span class="sxs-lookup"><span data-stu-id="1efdf-115"><span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1efdf-116">Eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="1efdf-116">One of the following flags.</span></span>



| <span data-ttu-id="1efdf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1efdf-117">Value</span></span>            | <span data-ttu-id="1efdf-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1efdf-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1efdf-119">an Position</span><span class="sxs-lookup"><span data-stu-id="1efdf-119">at position</span></span>      | <span data-ttu-id="1efdf-120">Gibt den Frame zum Aufrufen eines Signals an.</span><span class="sxs-lookup"><span data-stu-id="1efdf-120">Specifies the frame to invoke a signal.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1efdf-121">cancel</span><span class="sxs-lookup"><span data-stu-id="1efdf-121">cancel</span></span>           | <span data-ttu-id="1efdf-122">Entfernt Signale aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="1efdf-122">Removes signals from the workspace.</span></span> <span data-ttu-id="1efdf-123">Ein einzelnes Signal wird mit dem Flag "uservalue" angegeben.</span><span class="sxs-lookup"><span data-stu-id="1efdf-123">An individual signal is specified by using the "uservalue" flag.</span></span> <span data-ttu-id="1efdf-124">Wenn das Flag "uservalue" nicht mit "Abbrechen" angegeben wird, bricht das Gerät alle Signale ab.</span><span class="sxs-lookup"><span data-stu-id="1efdf-124">If the "uservalue" flag is not specified by using "cancel", the device cancels all signals.</span></span> <span data-ttu-id="1efdf-125">Das Flag "Abbrechen" ist nicht mit den Flags "at", "All" und "Return Position" kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1efdf-125">The "cancel" flag is incompatible with the "at", "every", and "return position" flags.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1efdf-126">Jedes *Intervall*</span><span class="sxs-lookup"><span data-stu-id="1efdf-126">every *interval*</span></span> | <span data-ttu-id="1efdf-127">Gibt den Zeitraum der Signale an.</span><span class="sxs-lookup"><span data-stu-id="1efdf-127">Specifies the period of the signals.</span></span> <span data-ttu-id="1efdf-128">Der *Intervall* Wert wird im aktuellen Zeitformat angegeben. Bei Verwendung mit der *Position*"an" werden Signale im gesamten Arbeitsbereich platziert, wobei eine Signal Markierung an der *Position* platziert wird.</span><span class="sxs-lookup"><span data-stu-id="1efdf-128">The *interval* value is specified in the current time format.If used with "at" *position*, signals are placed throughout the workspace with one signal mark placed at *position*.</span></span><br/> <span data-ttu-id="1efdf-129">Ohne das Flag "at" werden Signale im gesamten Arbeitsbereich mit einem Signal an der aktuellen Position platziert.</span><span class="sxs-lookup"><span data-stu-id="1efdf-129">Without the "at" flag, signals are placed throughout the workspace with one signal at the current position.</span></span><br/> <span data-ttu-id="1efdf-130">Wenn dieses Flag weggelassen wird, wird nur die durch das Flag "at" bezeichnete Position als markiert.</span><span class="sxs-lookup"><span data-stu-id="1efdf-130">If this flag is omitted, only the position indicated by the "at" flag is marked.</span></span><br/> <span data-ttu-id="1efdf-131">Wenn der *Intervall* Wert niedriger als die von einem Gerät unterstützte Mindestfrequenz ist, wird der Mindestwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="1efdf-131">If the *interval* value is less than the minimum frequency supported by a device, it will use its minimum value.</span></span><br/> |
| <span data-ttu-id="1efdf-132">Rückgabe Position</span><span class="sxs-lookup"><span data-stu-id="1efdf-132">return position</span></span>  | <span data-ttu-id="1efdf-133">Gibt an, dass das Gerät den Positionswert anstelle des Bezeichners "uservalue" in der Signalisierungs Nachricht senden soll.</span><span class="sxs-lookup"><span data-stu-id="1efdf-133">Indicates the device should send the position value instead of the "uservalue" identifier in the signaling message.</span></span> <span data-ttu-id="1efdf-134">Der Bezeichner "uservalue" kann weiterhin verwendet werden, um die Signal Markierungen abzubrechen oder neu zu definieren.</span><span class="sxs-lookup"><span data-stu-id="1efdf-134">The "uservalue" identifier can still be used to cancel or to redefine the signal marks.</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="1efdf-135">*ID* des Benutzer Werts</span><span class="sxs-lookup"><span data-stu-id="1efdf-135">uservalue *id*</span></span>   | <span data-ttu-id="1efdf-136">Gibt einen Bezeichner an, der mit der Signal Meldung zurückgemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="1efdf-136">Specifies an identifier that is reported back with the signaling message.</span></span> <span data-ttu-id="1efdf-137">Dieser Bezeichner fungiert als Bezeichner, der mit anderen **Signal** Befehlen verwendet werden kann, um auf diese **Signal** Einstellung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="1efdf-137">This identifier acts as an identifier that can be used with other **signal** commands to reference this **signal** setting.</span></span> <span data-ttu-id="1efdf-138">Wenn keine Angabe erfolgt, ist der Standardwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1efdf-138">If omitted, the default value is zero.</span></span>                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="1efdf-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="1efdf-139"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1efdf-140">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="1efdf-140">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="1efdf-141">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1efdf-141">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1efdf-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1efdf-142">Return Value</span></span>

<span data-ttu-id="1efdf-143">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="1efdf-143">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1efdf-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1efdf-144">Remarks</span></span>

<span data-ttu-id="1efdf-145">Das Fenster Handle, das für die Benachrichtigung über Befehls Vervollständigungs Meldungen verwendet wird, wird auch zur Signalisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1efdf-145">The window handle used for notification of command completion messages is also used for signaling.</span></span>

## <a name="requirements"></a><span data-ttu-id="1efdf-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1efdf-146">Requirements</span></span>



| <span data-ttu-id="1efdf-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1efdf-147">Requirement</span></span> | <span data-ttu-id="1efdf-148">Wert</span><span class="sxs-lookup"><span data-stu-id="1efdf-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1efdf-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1efdf-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1efdf-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1efdf-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1efdf-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1efdf-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1efdf-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1efdf-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1efdf-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1efdf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1efdf-154">MCI</span><span class="sxs-lookup"><span data-stu-id="1efdf-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1efdf-155">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="1efdf-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="1efdf-156">MM- \_ mcisignal</span><span class="sxs-lookup"><span data-stu-id="1efdf-156">MM\_MCISIGNAL</span></span>](mm-mcisignal.md)
</dt> </dl>

 

