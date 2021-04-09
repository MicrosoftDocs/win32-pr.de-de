---
title: Befehl "Where"
description: Der WHERE-Befehl ruft das Rechteck ab, das den Quell-oder Zielbereich angibt. Dieses Rechteck wurde mit dem Put-Befehl angegeben. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- Where-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957026"
---
# <a name="where-command"></a><span data-ttu-id="d09c3-106">Befehl "Where"</span><span class="sxs-lookup"><span data-stu-id="d09c3-106">where command</span></span>

<span data-ttu-id="d09c3-107">Der WHERE-Befehl ruft das Rechteck ab, das den Quell-oder Zielbereich angibt.</span><span class="sxs-lookup"><span data-stu-id="d09c3-107">The where command retrieves the rectangle specifying the source or destination area.</span></span> <span data-ttu-id="d09c3-108">Dieses Rechteck wurde mit dem [Put](put.md) -Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="d09c3-108">This rectangle was specified using the [put](put.md) command.</span></span> <span data-ttu-id="d09c3-109">Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="d09c3-109">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="d09c3-110">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="d09c3-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d09c3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d09c3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d09c3-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="d09c3-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d09c3-113">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="d09c3-113">Identifier of an MCI device.</span></span> <span data-ttu-id="d09c3-114">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d09c3-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d09c3-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszrequestrect*</span><span class="sxs-lookup"><span data-stu-id="d09c3-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span></span>
</dt> <dd>

<span data-ttu-id="d09c3-116">Flag, das das Rechteck identifiziert, dessen Dimensionen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d09c3-116">Flag that identifies the rectangle whose dimensions are retrieved.</span></span> <span data-ttu-id="d09c3-117">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Where** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="d09c3-117">The following table lists device types that recognize the **where** command and the flags used by each type.</span></span>



| <span data-ttu-id="d09c3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d09c3-118">Value</span></span>        | <span data-ttu-id="d09c3-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d09c3-119">Meaning</span></span>                                                       | <span data-ttu-id="d09c3-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d09c3-120">Meaning</span></span>                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="d09c3-121">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="d09c3-121">digitalvideo</span></span> | <span data-ttu-id="d09c3-122">destinationdestination [**Max**](max.md)frameframe maxsource</span><span class="sxs-lookup"><span data-stu-id="d09c3-122">destinationdestination [**max**](max.md)frameframe maxsource</span></span> | <span data-ttu-id="d09c3-123">Quelle maxvideovideo maxwindowwindow Max</span><span class="sxs-lookup"><span data-stu-id="d09c3-123">source maxvideovideo maxwindowwindow max</span></span> |
| <span data-ttu-id="d09c3-124">overlay</span><span class="sxs-lookup"><span data-stu-id="d09c3-124">overlay</span></span>      | <span data-ttu-id="d09c3-125">destinationframe</span><span class="sxs-lookup"><span data-stu-id="d09c3-125">destinationframe</span></span>                                              | <span data-ttu-id="d09c3-126">sourcevideo</span><span class="sxs-lookup"><span data-stu-id="d09c3-126">sourcevideo</span></span>                              |



 

<span data-ttu-id="d09c3-127">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszrequestrect** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="d09c3-127">The following table lists the flags that can be specified in the **lpszRequestRect** parameter and their meanings.</span></span>



| <span data-ttu-id="d09c3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d09c3-128">Value</span></span>                          | <span data-ttu-id="d09c3-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d09c3-129">Meaning</span></span>                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d09c3-130">destination</span><span class="sxs-lookup"><span data-stu-id="d09c3-130">destination</span></span>                    | <span data-ttu-id="d09c3-131">Ruft den Ziel Offset und-Block ab.</span><span class="sxs-lookup"><span data-stu-id="d09c3-131">Retrieves the destination offset and extent.</span></span> <span data-ttu-id="d09c3-132">Bei Video Überlagerungs Geräten definiert das Ziel Rechteck den Bereich des Client Bereichs Anzeige Fenster, in dem die Bilddaten aus dem Frame Puffer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d09c3-132">For video-overlay devices, the destination rectangle defines the area of the display window client area that displays the image data from the frame buffer.</span></span>                                                                                             |
| <span data-ttu-id="d09c3-133">[ **Max** . Ziel](max.md)</span><span class="sxs-lookup"><span data-stu-id="d09c3-133">destination [**max**](max.md)</span></span> | <span data-ttu-id="d09c3-134">Ruft die aktuelle Größe des Client Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="d09c3-134">Retrieves the current size of the client rectangle.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d09c3-135">frame</span><span class="sxs-lookup"><span data-stu-id="d09c3-135">frame</span></span>                          | <span data-ttu-id="d09c3-136">Ruft den Offset und den Umfang des Frame Puffer Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="d09c3-136">Retrieves the offset and extent of the frame buffer rectangle.</span></span> <span data-ttu-id="d09c3-137">Das Rahmen Puffer Rechteck definiert den Bereich des Frame Puffers, der eingehende Videodaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="d09c3-137">The frame buffer rectangle defines the area of the frame buffer that receives incoming video data.</span></span> <span data-ttu-id="d09c3-138">Bilder aus dem Rechteck "Video" werden in diesen Bereich skaliert.</span><span class="sxs-lookup"><span data-stu-id="d09c3-138">Images from the "video" rectangle are scaled into this region.</span></span>                                                                     |
| <span data-ttu-id="d09c3-139">[ **Max** . Frame](max.md)</span><span class="sxs-lookup"><span data-stu-id="d09c3-139">frame [**max**](max.md)</span></span>       | <span data-ttu-id="d09c3-140">Gibt die maximale Größe des Frame Puffers zurück.</span><span class="sxs-lookup"><span data-stu-id="d09c3-140">Returns the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d09c3-141">source</span><span class="sxs-lookup"><span data-stu-id="d09c3-141">source</span></span>                         | <span data-ttu-id="d09c3-142">Ruft den Quell Offset und den Wertebereich ab.</span><span class="sxs-lookup"><span data-stu-id="d09c3-142">Retrieves the source offset and extent.</span></span> <span data-ttu-id="d09c3-143">Bei Video Überlagerungs Geräten definiert das Quell Rechteck den Bereich des Frame Puffers, der im Zielfenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d09c3-143">For video-overlay devices, the source rectangle defines the region of the frame buffer that is displayed in the destination window.</span></span> <span data-ttu-id="d09c3-144">Das Gerät verwendet dieses Rechteck zum Zuschneiden des Bilds, bevor es gestreckt wird, um das Ziel Rechteck auf der Anzeige anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d09c3-144">The device uses this rectangle to crop the image before it is stretched to fit the destination rectangle on the display.</span></span> |
| <span data-ttu-id="d09c3-145">[ **Maximale** Quelldatei](max.md)</span><span class="sxs-lookup"><span data-stu-id="d09c3-145">source [**max**](max.md)</span></span>      | <span data-ttu-id="d09c3-146">Ruft die maximale Größe des Frame Puffers ab.</span><span class="sxs-lookup"><span data-stu-id="d09c3-146">Retrieves the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d09c3-147">video</span><span class="sxs-lookup"><span data-stu-id="d09c3-147">video</span></span>                          | <span data-ttu-id="d09c3-148">Ruft den Offset und den Umfang des Video Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="d09c3-148">Retrieves the offset and extent of the video rectangle.</span></span> <span data-ttu-id="d09c3-149">Das Video Rechteck definiert den Bereich der eingehenden Videodaten, die an den Frame Puffer übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="d09c3-149">The video rectangle defines the region of the incoming video data that is transferred to the frame buffer.</span></span>                                                                                                                                   |
| <span data-ttu-id="d09c3-150">[ **Maximales** Video](max.md)</span><span class="sxs-lookup"><span data-stu-id="d09c3-150">video [**max**](max.md)</span></span>       | <span data-ttu-id="d09c3-151">Gibt die maximale Größe der Eingabe zurück.</span><span class="sxs-lookup"><span data-stu-id="d09c3-151">Returns the maximum size of the input.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d09c3-152">Fenster</span><span class="sxs-lookup"><span data-stu-id="d09c3-152">window</span></span>                         | <span data-ttu-id="d09c3-153">Ruft die aktuelle Größe und Position des Anzeige Fensterrahmens ab.</span><span class="sxs-lookup"><span data-stu-id="d09c3-153">Retrieves the current size and position of the display-window frame.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="d09c3-154">[ **Max** . Fenster](max.md)</span><span class="sxs-lookup"><span data-stu-id="d09c3-154">window [**max**](max.md)</span></span>      | <span data-ttu-id="d09c3-155">Ruft die Größe der gesamten Anzeige ab.</span><span class="sxs-lookup"><span data-stu-id="d09c3-155">Retrieves the size of the entire display.</span></span>                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="d09c3-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="d09c3-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d09c3-157">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="d09c3-157">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="d09c3-158">Für Digital Video-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d09c3-158">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="d09c3-159">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d09c3-159">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d09c3-160">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d09c3-160">Return Value</span></span>

<span data-ttu-id="d09c3-161">Gibt ein Rechteck im *lpszreturnstring* -Parameter der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="d09c3-161">Returns a rectangle in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="d09c3-162">Das Rechteck beschreibt den Bereich, der im *lpszrequestrect* -Parameter dieses Befehls angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d09c3-162">The rectangle describes the area specified in the *lpszRequestRect* parameter of this command.</span></span> <span data-ttu-id="d09c3-163">Das Rechteck wird als *x1 y1 x2 Y2* angegeben.</span><span class="sxs-lookup"><span data-stu-id="d09c3-163">The rectangle is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="d09c3-164">Die Koordinaten *x1 y1* geben die linke obere Ecke des Rechtecks an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an.</span><span class="sxs-lookup"><span data-stu-id="d09c3-164">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span>

## <a name="examples"></a><span data-ttu-id="d09c3-165">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d09c3-165">Examples</span></span>

<span data-ttu-id="d09c3-166">Der folgende Befehl gibt das Anzeige Rechteck des "Movie"-Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="d09c3-166">The following command returns the display rectangle of the "movie" device.</span></span>

``` syntax
where movie destination
```

## <a name="requirements"></a><span data-ttu-id="d09c3-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d09c3-167">Requirements</span></span>



| <span data-ttu-id="d09c3-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d09c3-168">Requirement</span></span> | <span data-ttu-id="d09c3-169">Wert</span><span class="sxs-lookup"><span data-stu-id="d09c3-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d09c3-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d09c3-170">Minimum supported client</span></span><br/> | <span data-ttu-id="d09c3-171">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d09c3-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d09c3-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d09c3-172">Minimum supported server</span></span><br/> | <span data-ttu-id="d09c3-173">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d09c3-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d09c3-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d09c3-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09c3-175">MCI</span><span class="sxs-lookup"><span data-stu-id="d09c3-175">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d09c3-176">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="d09c3-176">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d09c3-177">stellte</span><span class="sxs-lookup"><span data-stu-id="d09c3-177">put</span></span>](put.md)
</dt> </dl>

 

