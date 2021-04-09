---
title: Befehl "erkennen"
description: Der Befehl "erkennen" weist ein Gerät an, seine Palette im Anzeige Kontext des angezeigten Fensters auszuwählen und zu erkennen. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- Befehl "Windows Multimedia"
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957028"
---
# <a name="realize-command"></a><span data-ttu-id="9f622-105">Befehl "erkennen"</span><span class="sxs-lookup"><span data-stu-id="9f622-105">realize command</span></span>

<span data-ttu-id="9f622-106">Der Befehl "erkennen" weist ein Gerät an, seine Palette im Anzeige Kontext des angezeigten Fensters auszuwählen und zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="9f622-106">The realize command instructs a device to select and realize its palette into the display context of the displayed window.</span></span> <span data-ttu-id="9f622-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="9f622-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="9f622-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="9f622-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="9f622-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f622-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f622-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="9f622-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9f622-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f622-111">Identifier of an MCI device.</span></span> <span data-ttu-id="9f622-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9f622-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="9f622-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszpalette*</span><span class="sxs-lookup"><span data-stu-id="9f622-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span></span>
</dt> <dd>

<span data-ttu-id="9f622-114">Eines der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="9f622-114">One of the following flags.</span></span>



| <span data-ttu-id="9f622-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9f622-115">Value</span></span>      | <span data-ttu-id="9f622-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f622-116">Meaning</span></span>                                                                   |
|------------|---------------------------------------------------------------------------|
| <span data-ttu-id="9f622-117">background</span><span class="sxs-lookup"><span data-stu-id="9f622-117">background</span></span> | <span data-ttu-id="9f622-118">Erkennt die Palette als Hintergrund Palette.</span><span class="sxs-lookup"><span data-stu-id="9f622-118">Realizes the palette as a background palette.</span></span>                             |
| <span data-ttu-id="9f622-119">normal</span><span class="sxs-lookup"><span data-stu-id="9f622-119">normal</span></span>     | <span data-ttu-id="9f622-120">Erkennt die Palette für ein Fenster der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="9f622-120">Realizes the palette for a top-level window.</span></span> <span data-ttu-id="9f622-121">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9f622-121">This is the default setting.</span></span> |



 

</dd> <dt>

<span data-ttu-id="9f622-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="9f622-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9f622-123">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="9f622-123">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="9f622-124">Für Digital Video-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9f622-124">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="9f622-125">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9f622-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f622-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f622-126">Return Value</span></span>

<span data-ttu-id="9f622-127">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="9f622-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f622-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f622-128">Remarks</span></span>

<span data-ttu-id="9f622-129">Verwenden Sie diesen Befehl nur, wenn Ihre Anwendung ein Fenster Handle verwendet und eine **WM \_ querynewpallette** -oder **WM \_ palettechanged** -Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="9f622-129">Use this command only if your application uses a window handle and receives a **WM\_QUERYNEWPALLETTE** or **WM\_PALETTECHANGED** message.</span></span>

## <a name="examples"></a><span data-ttu-id="9f622-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f622-130">Examples</span></span>

<span data-ttu-id="9f622-131">Der folgende Befehl weist das Gerät "MyVideo" an, seine Palette zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="9f622-131">The following command tells the "myvideo" device to realize its palette.</span></span>

``` syntax
realize myvideo normal
```

## <a name="requirements"></a><span data-ttu-id="9f622-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f622-132">Requirements</span></span>



| <span data-ttu-id="9f622-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f622-133">Requirement</span></span> | <span data-ttu-id="9f622-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9f622-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9f622-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f622-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9f622-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f622-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9f622-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f622-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9f622-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f622-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9f622-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f622-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f622-140">MCI</span><span class="sxs-lookup"><span data-stu-id="9f622-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9f622-141">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="9f622-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

