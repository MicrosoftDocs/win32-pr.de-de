---
title: Befehl "markieren"
description: Der Mark-Befehl steuert das Aufzeichnen und Löschen von Markierungen auf dem Videotape. VCR-Geräte erkennen diesen Befehl.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- Mark-Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570968af05424597a7fe2b59e86e0364694e0e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339960"
---
# <a name="mark-command"></a><span data-ttu-id="f0524-105">Befehl "markieren"</span><span class="sxs-lookup"><span data-stu-id="f0524-105">mark command</span></span>

<span data-ttu-id="f0524-106">Der Mark-Befehl steuert das Aufzeichnen und Löschen von Markierungen auf dem Videotape.</span><span class="sxs-lookup"><span data-stu-id="f0524-106">The mark command controls recording and erasing of marks on the videotape.</span></span> <span data-ttu-id="f0524-107">VCR-Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="f0524-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="f0524-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="f0524-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="f0524-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0524-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0524-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="f0524-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f0524-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="f0524-111">Identifier of an MCI device.</span></span> <span data-ttu-id="f0524-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f0524-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="f0524-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszmark*</span><span class="sxs-lookup"><span data-stu-id="f0524-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span></span>
</dt> <dd>

<span data-ttu-id="f0524-114">Eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="f0524-114">One of the following flags.</span></span>



| <span data-ttu-id="f0524-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f0524-115">Value</span></span> | <span data-ttu-id="f0524-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f0524-116">Meaning</span></span>                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0524-117">erase</span><span class="sxs-lookup"><span data-stu-id="f0524-117">erase</span></span> | <span data-ttu-id="f0524-118">Löscht eine Markierung an der aktuellen Position, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f0524-118">Erases a mark at the current position, if one exists.</span></span> <span data-ttu-id="f0524-119">Um eine Markierung zu löschen, suchen Sie zuerst nach der Markierung, und geben Sie dann den Befehl "Löschen" der Markierung aus.</span><span class="sxs-lookup"><span data-stu-id="f0524-119">To erase a mark, first seek to the mark and then issue the mark "erase" command.</span></span> |
| <span data-ttu-id="f0524-120">Schreiben</span><span class="sxs-lookup"><span data-stu-id="f0524-120">write</span></span> | <span data-ttu-id="f0524-121">Schreibt eine Markierung an der aktuellen Position.</span><span class="sxs-lookup"><span data-stu-id="f0524-121">Writes a mark at the current position.</span></span> <span data-ttu-id="f0524-122">Der VCR muss sich möglicherweise im Wiedergabe-oder Aufzeichnungsmodus befinden, damit dieser Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0524-122">The VCR might need to be in play or record mode for this command to succeed.</span></span>                    |



 

</dd> <dt>

<span data-ttu-id="f0524-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="f0524-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f0524-124">Kann "wait", "notify" oder "Test" lauten.</span><span class="sxs-lookup"><span data-stu-id="f0524-124">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="f0524-125">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f0524-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0524-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0524-126">Return Value</span></span>

<span data-ttu-id="f0524-127">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="f0524-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0524-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0524-128">Remarks</span></span>

<span data-ttu-id="f0524-129">Markierungen sind spezielle Signale, die in den Inhalt geschrieben werden, der von VCR bei hoch Geschwindigkeits suchen erkannt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0524-129">Marks are special signals written to the content that can be detected by the VCR during high-speed searches.</span></span> <span data-ttu-id="f0524-130">Marken sind VCR-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="f0524-130">Marks are VCR specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0524-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0524-131">Requirements</span></span>



| <span data-ttu-id="f0524-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0524-132">Requirement</span></span> | <span data-ttu-id="f0524-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f0524-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f0524-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0524-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f0524-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0524-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f0524-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0524-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f0524-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0524-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f0524-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0524-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0524-139">MCI</span><span class="sxs-lookup"><span data-stu-id="f0524-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f0524-140">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="f0524-140">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

