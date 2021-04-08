---
title: Befehl "Konfigurieren"
description: Der Befehl konfigurieren zeigt ein Dialogfeld an, das zum Konfigurieren des Geräts verwendet wird. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 17d99992-f432-4b8a-ae98-2a70637c29c3
keywords:
- Konfigurieren des Befehls Windows Multimedia
topic_type:
- apiref
api_name:
- configure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f131159d389577e3c717e5630633bb46558d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739840"
---
# <a name="configure-command"></a><span data-ttu-id="5d7dd-105">Befehl "Konfigurieren"</span><span class="sxs-lookup"><span data-stu-id="5d7dd-105">configure command</span></span>

<span data-ttu-id="5d7dd-106">Der Befehl konfigurieren zeigt ein Dialogfeld an, das zum Konfigurieren des Geräts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d7dd-106">The configure command displays a dialog box used to configure the device.</span></span> <span data-ttu-id="5d7dd-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="5d7dd-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="5d7dd-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="5d7dd-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("configure %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="5d7dd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d7dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d7dd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="5d7dd-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5d7dd-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="5d7dd-111">Identifier of an MCI device.</span></span> <span data-ttu-id="5d7dd-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5d7dd-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="5d7dd-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="5d7dd-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5d7dd-114">Kann "wait", "notify" oder "Test" lauten.</span><span class="sxs-lookup"><span data-stu-id="5d7dd-114">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="5d7dd-115">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5d7dd-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d7dd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d7dd-116">Return Value</span></span>

<span data-ttu-id="5d7dd-117">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="5d7dd-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7dd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d7dd-118">Requirements</span></span>



| <span data-ttu-id="5d7dd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d7dd-119">Requirement</span></span> | <span data-ttu-id="5d7dd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5d7dd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5d7dd-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d7dd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7dd-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d7dd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5d7dd-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d7dd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7dd-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d7dd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5d7dd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d7dd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7dd-126">MCI</span><span class="sxs-lookup"><span data-stu-id="5d7dd-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5d7dd-127">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="5d7dd-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

