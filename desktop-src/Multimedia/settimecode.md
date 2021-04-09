---
title: settimecode-Befehl
description: Der Befehl "settimecode" aktiviert oder deaktiviert die Zeit Code Aufzeichnung für einen VCR. VCR-Geräte erkennen diesen Befehl.
ms.assetid: 1b4b82e8-4f13-4bc9-afb0-796339cabb51
keywords:
- Befehl "settimecode" Windows Multimedia
topic_type:
- apiref
api_name:
- settimecode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32092e5af7c77cdc274491b20663218d39a1ec1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743904"
---
# <a name="settimecode-command"></a><span data-ttu-id="6a226-105">settimecode-Befehl</span><span class="sxs-lookup"><span data-stu-id="6a226-105">settimecode command</span></span>

<span data-ttu-id="6a226-106">Der Befehl "settimecode" aktiviert oder deaktiviert die Zeit Code Aufzeichnung für einen VCR.</span><span class="sxs-lookup"><span data-stu-id="6a226-106">The settimecode command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="6a226-107">VCR-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="6a226-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="6a226-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="6a226-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settimecode %s %s %s"), 
  lpszDeviceID,
  lpszTimecode, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="6a226-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a226-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a226-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="6a226-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6a226-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="6a226-111">Identifier of an MCI device.</span></span> <span data-ttu-id="6a226-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="6a226-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="6a226-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpsztimecode*</span><span class="sxs-lookup"><span data-stu-id="6a226-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span></span>
</dt> <dd>

<span data-ttu-id="6a226-114">Eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="6a226-114">One of the following flags.</span></span>



| <span data-ttu-id="6a226-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6a226-115">Value</span></span>      | <span data-ttu-id="6a226-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6a226-116">Meaning</span></span>                          |
|------------|----------------------------------|
| <span data-ttu-id="6a226-117">Aufzeichnen am</span><span class="sxs-lookup"><span data-stu-id="6a226-117">record on</span></span>  | <span data-ttu-id="6a226-118">Legt fest, dass der VCR Timecode aufzeichnen soll.</span><span class="sxs-lookup"><span data-stu-id="6a226-118">Sets the VCR to record timecode.</span></span> |
| <span data-ttu-id="6a226-119">Datensatz aus</span><span class="sxs-lookup"><span data-stu-id="6a226-119">record off</span></span> | <span data-ttu-id="6a226-120">Deaktiviert die Zeit Code Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="6a226-120">Disables timecode recording.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="6a226-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="6a226-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6a226-122">Kann "wait", "notify", "Test" oder eine Kombination daraus sein.</span><span class="sxs-lookup"><span data-stu-id="6a226-122">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="6a226-123">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6a226-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a226-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a226-124">Return Value</span></span>

<span data-ttu-id="6a226-125">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="6a226-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a226-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a226-126">Requirements</span></span>



| <span data-ttu-id="6a226-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a226-127">Requirement</span></span> | <span data-ttu-id="6a226-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6a226-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6a226-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a226-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6a226-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a226-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6a226-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a226-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6a226-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a226-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6a226-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a226-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a226-134">MCI</span><span class="sxs-lookup"><span data-stu-id="6a226-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6a226-135">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="6a226-135">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

