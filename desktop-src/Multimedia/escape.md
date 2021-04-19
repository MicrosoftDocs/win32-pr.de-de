---
title: Befehl "Escape"
description: Der Befehl "Escape" sendet gerätespezifische Informationen an ein Gerät. Videodisk-Geräte erkennen diesen Befehl.
ms.assetid: 16e0e2b6-6d98-440a-86c1-eca8201ad61a
keywords:
- escapebefehl Windows Multimedia
topic_type:
- apiref
api_name:
- escape
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b04f7a2ef6c2e91adc9b24a044d0a7e941843f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339535"
---
# <a name="escape-command"></a><span data-ttu-id="a4559-105">Befehl "Escape"</span><span class="sxs-lookup"><span data-stu-id="a4559-105">escape command</span></span>

<span data-ttu-id="a4559-106">Der Befehl "Escape" sendet gerätespezifische Informationen an ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="a4559-106">The escape command sends device-specific information to a device.</span></span> <span data-ttu-id="a4559-107">Videodisk-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="a4559-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="a4559-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="a4559-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("escape %s %s %s"), 
  lpszDeviceID, 
  lpszEscape, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a4559-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4559-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4559-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="a4559-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a4559-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="a4559-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a4559-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a4559-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a4559-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszescape*</span><span class="sxs-lookup"><span data-stu-id="a4559-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span></span>
</dt> <dd>

<span data-ttu-id="a4559-114">Benutzerdefinierte Informationen, die an das Gerät gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a4559-114">Custom information to send to the device.</span></span>

</dd> <dt>

<span data-ttu-id="a4559-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="a4559-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a4559-116">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="a4559-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="a4559-117">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a4559-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4559-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4559-118">Return Value</span></span>

<span data-ttu-id="a4559-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="a4559-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="a4559-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4559-120">Examples</span></span>

<span data-ttu-id="a4559-121">Mit dem folgenden Befehl wird die Escapezeichenfolge "SA" an das Videodisk-Gerät gesendet.</span><span class="sxs-lookup"><span data-stu-id="a4559-121">The following command sends the escape string "SA" to the videodisc device.</span></span>

``` syntax
escape videodisc SA
```

## <a name="requirements"></a><span data-ttu-id="a4559-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4559-122">Requirements</span></span>



| <span data-ttu-id="a4559-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4559-123">Requirement</span></span> | <span data-ttu-id="a4559-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a4559-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a4559-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4559-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a4559-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4559-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a4559-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4559-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a4559-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4559-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a4559-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4559-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4559-130">MCI</span><span class="sxs-lookup"><span data-stu-id="a4559-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a4559-131">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="a4559-131">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

