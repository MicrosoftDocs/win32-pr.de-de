---
title: Resume-Befehl
description: Der Resume-Befehl setzt die Wiedergabe oder Aufzeichnung auf einem Gerät fort, das mithilfe des Pause-Befehls angehalten wurde.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- Befehl "fortsetzen" Windows Multimedia
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f01fd96e2b25e191608c7c6abf70bfd842158d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338116"
---
# <a name="resume-command"></a><span data-ttu-id="b98f5-104">Resume-Befehl</span><span class="sxs-lookup"><span data-stu-id="b98f5-104">resume command</span></span>

<span data-ttu-id="b98f5-105">Der Resume-Befehl setzt die Wiedergabe oder Aufzeichnung auf einem Gerät fort, das mithilfe des [Pause](pause.md) -Befehls angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="b98f5-105">The resume command continues playing or recording on a device that has been paused using the [pause](pause.md) command.</span></span> <span data-ttu-id="b98f5-106">Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt.</span><span class="sxs-lookup"><span data-stu-id="b98f5-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="b98f5-107">Obwohl die Geräte von CD-Audiodaten, MIDI-Sequencer und Videodisc diesen Befehl ebenfalls erkennen, unterstützen die Gerätetreiber mcicda, mcitarq und mcipionr Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="b98f5-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="b98f5-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="b98f5-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="b98f5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b98f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b98f5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="b98f5-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b98f5-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="b98f5-111">Identifier of an MCI device.</span></span> <span data-ttu-id="b98f5-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="b98f5-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="b98f5-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="b98f5-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b98f5-114">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="b98f5-114">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="b98f5-115">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b98f5-115">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="b98f5-116">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b98f5-116">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b98f5-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b98f5-117">Return Value</span></span>

<span data-ttu-id="b98f5-118">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="b98f5-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="b98f5-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b98f5-119">Examples</span></span>

<span data-ttu-id="b98f5-120">Mit dem folgenden Befehl wird die Wiedergabe oder Aufzeichnung des "Newsound"-Geräts fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b98f5-120">The following command continues playing or recording the "newsound" device.</span></span>

``` syntax
resume newsound
```

## <a name="requirements"></a><span data-ttu-id="b98f5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b98f5-121">Requirements</span></span>



| <span data-ttu-id="b98f5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b98f5-122">Requirement</span></span> | <span data-ttu-id="b98f5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b98f5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b98f5-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b98f5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b98f5-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b98f5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b98f5-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b98f5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b98f5-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b98f5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b98f5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b98f5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b98f5-129">MCI</span><span class="sxs-lookup"><span data-stu-id="b98f5-129">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b98f5-130">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="b98f5-130">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="b98f5-131">pause</span><span class="sxs-lookup"><span data-stu-id="b98f5-131">pause</span></span>](pause.md)
</dt> </dl>

 

