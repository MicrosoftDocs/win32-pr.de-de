---
title: Index Befehl
description: Der Index Befehl steuert die Bildschirm Anzeige eines VCR. VCR-Geräte erkennen diesen Befehl.
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- Index Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da652b1a7a48dffd9850c435345fcfcb11c2e674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957236"
---
# <a name="index-command"></a><span data-ttu-id="5f9d0-105">Index Befehl</span><span class="sxs-lookup"><span data-stu-id="5f9d0-105">index command</span></span>

<span data-ttu-id="5f9d0-106">Der Index Befehl steuert die Bildschirm Anzeige eines VCR.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-106">The index command controls a VCR's on-screen display.</span></span> <span data-ttu-id="5f9d0-107">VCR-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="5f9d0-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="5f9d0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f9d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f9d0-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="5f9d0-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5f9d0-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-111">Identifier of an MCI device.</span></span> <span data-ttu-id="5f9d0-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="5f9d0-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszindex*</span><span class="sxs-lookup"><span data-stu-id="5f9d0-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span></span>
</dt> <dd>

<span data-ttu-id="5f9d0-114">Eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-114">One of the following flags.</span></span>



| <span data-ttu-id="5f9d0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5f9d0-115">Value</span></span> | <span data-ttu-id="5f9d0-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5f9d0-116">Meaning</span></span>                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9d0-117">aus</span><span class="sxs-lookup"><span data-stu-id="5f9d0-117">off</span></span>   | <span data-ttu-id="5f9d0-118">Schaltet die Bildschirm Anzeige aus.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-118">Turns off the on-screen display.</span></span>                                                                                         |
| <span data-ttu-id="5f9d0-119">on</span><span class="sxs-lookup"><span data-stu-id="5f9d0-119">on</span></span>    | <span data-ttu-id="5f9d0-120">Schaltet die Bildschirm Anzeige.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-120">Turns on the on-screen display.</span></span> <span data-ttu-id="5f9d0-121">Das Element, das angezeigt werden soll, wird durch das Flag "index" des [Set](set.md) -Befehls angegeben.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-121">The item to be displayed is specified by the "index" flag of the [set](set.md) command.</span></span> |



 

</dd> <dt>

<span data-ttu-id="5f9d0-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="5f9d0-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5f9d0-123">Kann "wait", "notify" oder "Test" lauten.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-123">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="5f9d0-124">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5f9d0-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f9d0-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f9d0-125">Return Value</span></span>

<span data-ttu-id="5f9d0-126">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="5f9d0-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f9d0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f9d0-127">Requirements</span></span>



| <span data-ttu-id="5f9d0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f9d0-128">Requirement</span></span> | <span data-ttu-id="5f9d0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5f9d0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5f9d0-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f9d0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5f9d0-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f9d0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5f9d0-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f9d0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5f9d0-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f9d0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5f9d0-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f9d0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f9d0-135">MCI</span><span class="sxs-lookup"><span data-stu-id="5f9d0-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5f9d0-136">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="5f9d0-136">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="5f9d0-137">set</span><span class="sxs-lookup"><span data-stu-id="5f9d0-137">set</span></span>](set.md)
</dt> </dl>

 

