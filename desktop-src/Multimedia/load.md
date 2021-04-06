---
title: Befehl "Laden"
description: Der Load-Befehl lädt eine Datei in einem gerätespezifischen Format. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- Befehl "Laden" Windows Multimedia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742496"
---
# <a name="load-command"></a><span data-ttu-id="2c67b-105">Befehl "Laden"</span><span class="sxs-lookup"><span data-stu-id="2c67b-105">load command</span></span>

<span data-ttu-id="2c67b-106">Der Load-Befehl lädt eine Datei in einem gerätespezifischen Format.</span><span class="sxs-lookup"><span data-stu-id="2c67b-106">The load command loads a file in a device-specific format.</span></span> <span data-ttu-id="2c67b-107">Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="2c67b-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="2c67b-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="2c67b-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="2c67b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c67b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c67b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="2c67b-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2c67b-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="2c67b-111">Identifier of an MCI device.</span></span> <span data-ttu-id="2c67b-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2c67b-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="2c67b-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszfilepos*</span><span class="sxs-lookup"><span data-stu-id="2c67b-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="2c67b-114">Der zu ladende Pfad und Dateiname.</span><span class="sxs-lookup"><span data-stu-id="2c67b-114">Path and filename to load.</span></span> <span data-ttu-id="2c67b-115">Bei Video Überlagerungs Geräten kann dies auch ein Ziel Rechteck für die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c67b-115">For video-overlay devices, this can also include a target rectangle for the data.</span></span> <span data-ttu-id="2c67b-116">Geben Sie zum Angeben eines Ziel Rechtecks "at" gefolgt von **x1 y1 x2 Y2** an, wobei **x1 y1** die obere linke Ecke des Rechtecks angeben und **x2 Y2** die Breite und Höhe angeben.</span><span class="sxs-lookup"><span data-stu-id="2c67b-116">To specify a target rectangle, specify "at" followed by **X1 Y1 X2 Y2**, where **X1 Y1** specify the upper left corner of the rectangle, and **X2 Y2** specify the width and height.</span></span> <span data-ttu-id="2c67b-117">Das Rechteck ist relativ zum Video Puffer Ursprung.</span><span class="sxs-lookup"><span data-stu-id="2c67b-117">The rectangle is relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="2c67b-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="2c67b-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2c67b-119">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="2c67b-119">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="2c67b-120">Für Digital Video-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c67b-120">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="2c67b-121">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2c67b-121">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c67b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c67b-122">Return Value</span></span>

<span data-ttu-id="2c67b-123">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="2c67b-123">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c67b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c67b-124">Remarks</span></span>

<span data-ttu-id="2c67b-125">Das "vidboard"-Gerät sendet eine Benachrichtigungs Meldung, wenn der Ladevorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2c67b-125">The "vidboard" device sends a notification message when the loading is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="2c67b-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c67b-126">Examples</span></span>

<span data-ttu-id="2c67b-127">Mit dem folgenden Befehl wird eine Datei in das "vidboard"-Gerät geladen.</span><span class="sxs-lookup"><span data-stu-id="2c67b-127">The following command loads a file into the "vidboard" device.</span></span>

``` syntax
load vidboard c:\vid\fish.vid notify
```

## <a name="requirements"></a><span data-ttu-id="2c67b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c67b-128">Requirements</span></span>



| <span data-ttu-id="2c67b-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c67b-129">Requirement</span></span> | <span data-ttu-id="2c67b-130">Wert</span><span class="sxs-lookup"><span data-stu-id="2c67b-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2c67b-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c67b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2c67b-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c67b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2c67b-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c67b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2c67b-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c67b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2c67b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c67b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c67b-136">MCI</span><span class="sxs-lookup"><span data-stu-id="2c67b-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2c67b-137">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="2c67b-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

