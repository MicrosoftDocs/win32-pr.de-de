---
title: Dreh Befehl
description: Der Spin-Befehl beginnt mit dem Drehen einer CD oder hält das Drehen der CD an. Videodisk-Geräte erkennen diesen Befehl.
ms.assetid: 1fdf4d09-fafd-4245-ad92-397114d0f473
keywords:
- Dreh Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- spin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c25e25f5a44ad6e6c9562d05653ab25cb2950b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340595"
---
# <a name="spin-command"></a><span data-ttu-id="69635-105">Dreh Befehl</span><span class="sxs-lookup"><span data-stu-id="69635-105">spin command</span></span>

<span data-ttu-id="69635-106">Der Spin-Befehl beginnt mit dem Drehen einer CD oder hält das Drehen der CD an.</span><span class="sxs-lookup"><span data-stu-id="69635-106">The spin command starts spinning a disc or stops the disc from spinning.</span></span> <span data-ttu-id="69635-107">Videodisk-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="69635-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="69635-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="69635-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("spin %s %s %s"), 
  lpszDeviceID, 
  lpszUpDown, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="69635-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="69635-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69635-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="69635-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="69635-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="69635-111">Identifier of an MCI device.</span></span> <span data-ttu-id="69635-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="69635-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="69635-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszupdown*</span><span class="sxs-lookup"><span data-stu-id="69635-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span></span>
</dt> <dd>

<span data-ttu-id="69635-114">Eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="69635-114">One of the following flags.</span></span>



| <span data-ttu-id="69635-115">Wert</span><span class="sxs-lookup"><span data-stu-id="69635-115">Value</span></span> | <span data-ttu-id="69635-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="69635-116">Meaning</span></span>                       |
|-------|-------------------------------|
| <span data-ttu-id="69635-117">fahren</span><span class="sxs-lookup"><span data-stu-id="69635-117">down</span></span>  | <span data-ttu-id="69635-118">Hält das Drehen der Festplatte an.</span><span class="sxs-lookup"><span data-stu-id="69635-118">Stops the disc from spinning.</span></span> |
| <span data-ttu-id="69635-119">up</span><span class="sxs-lookup"><span data-stu-id="69635-119">up</span></span>    | <span data-ttu-id="69635-120">Startet das Drehen der CD.</span><span class="sxs-lookup"><span data-stu-id="69635-120">Starts spinning the disc.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="69635-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="69635-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="69635-122">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="69635-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="69635-123">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="69635-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69635-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69635-124">Return Value</span></span>

<span data-ttu-id="69635-125">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="69635-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="69635-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69635-126">Examples</span></span>

<span data-ttu-id="69635-127">Der folgende Befehl beginnt mit dem Drehen eines Videodisk-Geräts.</span><span class="sxs-lookup"><span data-stu-id="69635-127">The following command starts spinning a videodisc device.</span></span>

``` syntax
spin videodisc up
```

## <a name="requirements"></a><span data-ttu-id="69635-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69635-128">Requirements</span></span>



| <span data-ttu-id="69635-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69635-129">Requirement</span></span> | <span data-ttu-id="69635-130">Wert</span><span class="sxs-lookup"><span data-stu-id="69635-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="69635-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69635-131">Minimum supported client</span></span><br/> | <span data-ttu-id="69635-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69635-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="69635-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69635-133">Minimum supported server</span></span><br/> | <span data-ttu-id="69635-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69635-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="69635-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69635-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69635-136">MCI</span><span class="sxs-lookup"><span data-stu-id="69635-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="69635-137">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="69635-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

