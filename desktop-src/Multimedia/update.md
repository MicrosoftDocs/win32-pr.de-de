---
title: Befehl "Aktualisieren"
description: Der Update-Befehl zeichnet den aktuellen Frame in den angegebenen Gerätekontext (DC). Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- Update Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518962"
---
# <a name="update-command"></a><span data-ttu-id="27778-105">Befehl "Aktualisieren"</span><span class="sxs-lookup"><span data-stu-id="27778-105">update command</span></span>

<span data-ttu-id="27778-106">Der Update-Befehl zeichnet den aktuellen Frame in den angegebenen Gerätekontext (DC).</span><span class="sxs-lookup"><span data-stu-id="27778-106">The update command repaints the current frame into the specified device context (DC).</span></span> <span data-ttu-id="27778-107">Dieser Befehl wird von Digital-Video-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="27778-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="27778-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="27778-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="27778-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="27778-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27778-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="27778-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="27778-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="27778-111">Identifier of an MCI device.</span></span> <span data-ttu-id="27778-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="27778-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="27778-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszhdc*</span><span class="sxs-lookup"><span data-stu-id="27778-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span></span>
</dt> <dd>

<span data-ttu-id="27778-114">Handle eines DC.</span><span class="sxs-lookup"><span data-stu-id="27778-114">Handle of a DC.</span></span> <span data-ttu-id="27778-115">In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Update** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="27778-115">The following table lists device types that recognize the **update** command and the flags used by each type.</span></span>



| <span data-ttu-id="27778-116">Wert</span><span class="sxs-lookup"><span data-stu-id="27778-116">Value</span></span>        | <span data-ttu-id="27778-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="27778-117">Meaning</span></span>                       | <span data-ttu-id="27778-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="27778-118">Meaning</span></span>         |
|--------------|-------------------------------|-----------------|
| <span data-ttu-id="27778-119">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="27778-119">digitalvideo</span></span> | <span data-ttu-id="27778-120">HDC *hdc* HDC *bei* *Rect*</span><span class="sxs-lookup"><span data-stu-id="27778-120">hdc *hdc* hdc *hdc* at *rect*</span></span> | <span data-ttu-id="27778-121">HDC *hdc* zeichnen</span><span class="sxs-lookup"><span data-stu-id="27778-121">paint hdc *hdc*</span></span> |



 

<span data-ttu-id="27778-122">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszhdc** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="27778-122">The following table lists the flags that can be specified in the **lpszHDC** parameter and their meanings.</span></span>



| <span data-ttu-id="27778-123">Wert</span><span class="sxs-lookup"><span data-stu-id="27778-123">Value</span></span>               | <span data-ttu-id="27778-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="27778-124">Meaning</span></span>                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27778-125">HDC- *hdc*</span><span class="sxs-lookup"><span data-stu-id="27778-125">hdc *hdc*</span></span>           | <span data-ttu-id="27778-126">Gibt das Handle des zu zeichnenden Domänen Controllers an.</span><span class="sxs-lookup"><span data-stu-id="27778-126">Specifies the handle of the DC to paint.</span></span>                                                               |
| <span data-ttu-id="27778-127">HDC- *hdc* bei *Rect*</span><span class="sxs-lookup"><span data-stu-id="27778-127">hdc *hdc* at *rect*</span></span> | <span data-ttu-id="27778-128">Gibt das Clippingrechteck relativ zum Client Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="27778-128">Specifies the clipping rectangle relative to the client rectangle.</span></span>                                     |
| <span data-ttu-id="27778-129">HDC *hdc* zeichnen</span><span class="sxs-lookup"><span data-stu-id="27778-129">paint hdc *hdc*</span></span>     | <span data-ttu-id="27778-130">Zeichnet den DC, wenn die Anwendung eine [**WM \_**](/windows/desktop/gdi/wm-paint) -Zeichnungs Nachricht empfängt, die für einen Domänen Controller gedacht ist.</span><span class="sxs-lookup"><span data-stu-id="27778-130">Paints the DC when the application receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message intended for a DC.</span></span> |



 

<span data-ttu-id="27778-131">Um das Handle des DC anzugeben, verwenden Sie die Zeichenfolge "HDC", gefolgt von einer ASCII-Darstellung des Handles.</span><span class="sxs-lookup"><span data-stu-id="27778-131">To specify the handle of the DC, use the string "hdc" followed by an ASCII representation of the handle.</span></span> <span data-ttu-id="27778-132">Das Rechteck wird als **x1 y1 x2 Y2** angegeben.</span><span class="sxs-lookup"><span data-stu-id="27778-132">The rectangle is specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="27778-133">Die Koordinaten **x1 y1** geben die linke obere Ecke des Rechtecks an, und die Koordinaten **x2 Y2** geben die Breite und Höhe an.</span><span class="sxs-lookup"><span data-stu-id="27778-133">The coordinates **X1 Y1** specify the upper left corner of the rectangle, and the coordinates **X2 Y2** specify the width and height.</span></span>

</dd> <dt>

<span data-ttu-id="27778-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="27778-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="27778-135">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="27778-135">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="27778-136">Für Digital Video-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="27778-136">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="27778-137">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="27778-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27778-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27778-138">Return Value</span></span>

<span data-ttu-id="27778-139">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="27778-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="27778-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27778-140">Examples</span></span>

<span data-ttu-id="27778-141">Der folgende Befehl aktualisiert das gesamte Anzeige Fenster, das vom "Movie"-Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27778-141">The following command updates the entire display window used by the "movie" device.</span></span> <span data-ttu-id="27778-142">Die Zahl 203 ist ein Handle für einen Domänen Controller, der von der [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="27778-142">The number 203 is a handle to a DC obtained from the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span>

``` syntax
update movie hdc 203
```

## <a name="requirements"></a><span data-ttu-id="27778-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27778-143">Requirements</span></span>



| <span data-ttu-id="27778-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27778-144">Requirement</span></span> | <span data-ttu-id="27778-145">Wert</span><span class="sxs-lookup"><span data-stu-id="27778-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="27778-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27778-146">Minimum supported client</span></span><br/> | <span data-ttu-id="27778-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27778-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="27778-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27778-148">Minimum supported server</span></span><br/> | <span data-ttu-id="27778-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27778-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="27778-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27778-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27778-151">MCI</span><span class="sxs-lookup"><span data-stu-id="27778-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="27778-152">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="27778-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

