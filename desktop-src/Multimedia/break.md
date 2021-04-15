---
title: Break-Befehl
description: Mit dem Break-Befehl wird ein Schlüssel angegeben, mit dem ein Befehl abgebrochen wird, der mithilfe von \ 0034; Wait \ 0034; aufgerufen wurde. ssen. Dieser Befehl ist ein MCI-Systembefehl. Sie wird direkt von MCI interpretiert.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- Umbruch Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478933"
---
# <a name="break-command"></a><span data-ttu-id="7acc0-105">Break-Befehl</span><span class="sxs-lookup"><span data-stu-id="7acc0-105">break command</span></span>

<span data-ttu-id="7acc0-106">Mit dem Break-Befehl wird ein Schlüssel angegeben, mit dem ein Befehl abgebrochen wird, der mit dem Flag "wait" aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7acc0-106">The break command specifies a key to abort a command that was invoked using the "wait" flag.</span></span> <span data-ttu-id="7acc0-107">Dieser Befehl ist ein MCI-Systembefehl. Sie wird direkt von MCI interpretiert.</span><span class="sxs-lookup"><span data-stu-id="7acc0-107">This command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="7acc0-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="7acc0-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="7acc0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7acc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7acc0-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="7acc0-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7acc0-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="7acc0-111">Identifier of an MCI device.</span></span> <span data-ttu-id="7acc0-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="7acc0-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="7acc0-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszvirtkey*</span><span class="sxs-lookup"><span data-stu-id="7acc0-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span></span>
</dt> <dd>

<span data-ttu-id="7acc0-114">Eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="7acc0-114">One of the following flags.</span></span>



| <span data-ttu-id="7acc0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7acc0-115">Value</span></span>                 | <span data-ttu-id="7acc0-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7acc0-116">Meaning</span></span>                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="7acc0-117">auf *virtuellem Schlüsselcode*</span><span class="sxs-lookup"><span data-stu-id="7acc0-117">on *virtual key code*</span></span> | <span data-ttu-id="7acc0-118">Gibt den Schlüssel an, der einen Befehl abbricht, der mit dem Flag "wait" gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="7acc0-118">Specifies the key that aborts a command that was started using the "wait" flag.</span></span> |
| <span data-ttu-id="7acc0-119">aus</span><span class="sxs-lookup"><span data-stu-id="7acc0-119">off</span></span>                   | <span data-ttu-id="7acc0-120">Deaktiviert die aktuelle Break-Taste.</span><span class="sxs-lookup"><span data-stu-id="7acc0-120">Disables the current break key.</span></span>                                                 |



 

</dd> <dt>

<span data-ttu-id="7acc0-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="7acc0-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7acc0-122">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="7acc0-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="7acc0-123">Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7acc0-123">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="7acc0-124">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7acc0-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7acc0-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7acc0-125">Return Value</span></span>

<span data-ttu-id="7acc0-126">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="7acc0-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7acc0-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7acc0-127">Remarks</span></span>

<span data-ttu-id="7acc0-128">Wenn die Break-Taste aktiviert ist und der Benutzer den Schlüssel drückt, der durch den im *lpszvirtkey* -Parameter angegebenen Code des virtuellen Schlüssels gekennzeichnet ist, gibt das Gerät die Steuerung an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="7acc0-128">When the break key is enabled and the user presses the key identified by the virtual-key code specified in the *lpszVirtKey* parameter, the device returns control to the application.</span></span> <span data-ttu-id="7acc0-129">Wenn möglich, wird die Ausführung des Befehls fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7acc0-129">If possible, the command continues execution.</span></span>

## <a name="examples"></a><span data-ttu-id="7acc0-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7acc0-130">Examples</span></span>

<span data-ttu-id="7acc0-131">Der folgende Befehl legt F2 als Break Key für das "mysound"-Gerät fest.</span><span class="sxs-lookup"><span data-stu-id="7acc0-131">The following command sets F2 as the break key for the "mysound" device.</span></span>

``` syntax
break mysound on 113
```

## <a name="requirements"></a><span data-ttu-id="7acc0-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7acc0-132">Requirements</span></span>



| <span data-ttu-id="7acc0-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7acc0-133">Requirement</span></span> | <span data-ttu-id="7acc0-134">Wert</span><span class="sxs-lookup"><span data-stu-id="7acc0-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7acc0-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7acc0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7acc0-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7acc0-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7acc0-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7acc0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7acc0-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7acc0-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7acc0-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7acc0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7acc0-140">MCI</span><span class="sxs-lookup"><span data-stu-id="7acc0-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7acc0-141">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="7acc0-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

