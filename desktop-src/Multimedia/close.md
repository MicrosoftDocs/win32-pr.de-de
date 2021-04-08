---
title: Befehl "Schließen" (corecrt \_ IO. h)
description: Der Close-Befehl schließt das Gerät oder die Datei und alle zugehörigen Ressourcen. MCI entlädt ein Gerät, wenn alle Instanzen des Geräts oder alle Dateien geschlossen sind. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- Befehl "Schließen" Windows Multimedia
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949758"
---
# <a name="close-command"></a><span data-ttu-id="fd28a-106">Befehl "Schließen"</span><span class="sxs-lookup"><span data-stu-id="fd28a-106">close command</span></span>

<span data-ttu-id="fd28a-107">Der Close-Befehl schließt das Gerät oder die Datei und alle zugehörigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="fd28a-107">The close command closes the device or file and any associated resources.</span></span> <span data-ttu-id="fd28a-108">MCI entlädt ein Gerät, wenn alle Instanzen des Geräts oder alle Dateien geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="fd28a-108">MCI unloads a device when all instances of the device or all files are closed.</span></span> <span data-ttu-id="fd28a-109">Dieser Befehl wird von allen MCI-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="fd28a-109">All MCI devices recognize this command.</span></span>

<span data-ttu-id="fd28a-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="fd28a-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="fd28a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd28a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd28a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="fd28a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="fd28a-113">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="fd28a-113">Identifier of an MCI device.</span></span> <span data-ttu-id="fd28a-114">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="fd28a-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="fd28a-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="fd28a-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fd28a-116">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="fd28a-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="fd28a-117">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fd28a-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd28a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd28a-118">Return Value</span></span>

<span data-ttu-id="fd28a-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="fd28a-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd28a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd28a-120">Remarks</span></span>

<span data-ttu-id="fd28a-121">Wenn Sie alle von Ihrer Anwendung geöffneten Geräte schließen möchten, geben Sie den "All"-Geräte Bezeichner für den *lpszdebug* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="fd28a-121">To close all devices opened by your application, specify the "all" device identifier for the *lpszDeviceID* parameter.</span></span>

<span data-ttu-id="fd28a-122">Durch das Schließen des **CDAudio** -Geräts wird die Audiowiedergabe beendet.</span><span class="sxs-lookup"><span data-stu-id="fd28a-122">Closing the **cdaudio** device stops audio playback.</span></span>

<span data-ttu-id="fd28a-123">**Windows 2000/XP:** Wenn das **CDAudio** -Gerät abgespielt wird, führt das Schließen des **CDAudio** -Geräts nicht dazu, dass die Audiowiedergabe beendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd28a-123">**Windows 2000/XP:** If the **cdaudio** device is playing, closing the **cdaudio** device does not cause the audio to stop playing.</span></span> <span data-ttu-id="fd28a-124">Senden Sie zuerst den Befehl " [Abbrechen](stop.md) ".</span><span class="sxs-lookup"><span data-stu-id="fd28a-124">Send the [stop](stop.md) command first.</span></span>

## <a name="examples"></a><span data-ttu-id="fd28a-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd28a-125">Examples</span></span>

<span data-ttu-id="fd28a-126">Mit dem folgenden Befehl wird das Gerät "mysound" geschlossen.</span><span class="sxs-lookup"><span data-stu-id="fd28a-126">The following command closes the "mysound" device.</span></span>

``` syntax
close mysound
```

## <a name="requirements"></a><span data-ttu-id="fd28a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd28a-127">Requirements</span></span>



| <span data-ttu-id="fd28a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd28a-128">Requirement</span></span> | <span data-ttu-id="fd28a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="fd28a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd28a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd28a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fd28a-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd28a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fd28a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd28a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fd28a-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd28a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fd28a-134">Header</span><span class="sxs-lookup"><span data-stu-id="fd28a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd28a-135"><dt>Corecrt \_ IO. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd28a-135"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd28a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd28a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd28a-137">MCI</span><span class="sxs-lookup"><span data-stu-id="fd28a-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fd28a-138">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="fd28a-138">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

