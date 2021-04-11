---
title: Put-Befehl
description: Der Put-Befehl definiert den Bereich des Quell Bilds und des Zielfensters, das für die Anzeige verwendet wird. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- Put-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105705"
---
# <a name="put-command"></a><span data-ttu-id="d10cf-105">Put-Befehl</span><span class="sxs-lookup"><span data-stu-id="d10cf-105">put command</span></span>

<span data-ttu-id="d10cf-106">Der Put-Befehl definiert den Bereich des Quell Bilds und des Zielfensters, das für die Anzeige verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d10cf-106">The put command defines the area of the source image and destination window used for display.</span></span> <span data-ttu-id="d10cf-107">Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="d10cf-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="d10cf-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.</span><span class="sxs-lookup"><span data-stu-id="d10cf-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d10cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d10cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d10cf-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*</span><span class="sxs-lookup"><span data-stu-id="d10cf-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d10cf-111">Der Bezeichner eines MCI-Geräts.</span><span class="sxs-lookup"><span data-stu-id="d10cf-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d10cf-112">Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d10cf-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d10cf-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszregions*</span><span class="sxs-lookup"><span data-stu-id="d10cf-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span></span>
</dt> <dd>

<span data-ttu-id="d10cf-114">Flag zum Definieren des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="d10cf-114">Flag for defining the area.</span></span> <span data-ttu-id="d10cf-115">In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den Put-Befehl und die von den einzelnen Typen verwendeten Flags erkennen.</span><span class="sxs-lookup"><span data-stu-id="d10cf-115">The following table lists device types that recognize the put command and the flags used by each type.</span></span>



| <span data-ttu-id="d10cf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d10cf-116">Value</span></span>        | <span data-ttu-id="d10cf-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d10cf-117">Meaning</span></span>                                                                                      | <span data-ttu-id="d10cf-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d10cf-118">Meaning</span></span>                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10cf-119">Digitalvideo</span><span class="sxs-lookup"><span data-stu-id="d10cf-119">digitalvideo</span></span> | <span data-ttu-id="d10cf-120">Zielziel bei *rechtedem Frame Rahmen* bei *Rechteck Quell Quelle* bei *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-120">destination destination at *rectangle* frame frame at *rectangle* source source at *rectangle*</span></span> | <span data-ttu-id="d10cf-121">Video *Video* in *Rechteck Fenster im* Fenster Client Fenster Client *im Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-121">video video at *rectangle* window window at *rectangle* window client window client at *rectangle*</span></span> |
| <span data-ttu-id="d10cf-122">overlay</span><span class="sxs-lookup"><span data-stu-id="d10cf-122">overlay</span></span>      | <span data-ttu-id="d10cf-123">Zielziel bei *Rechteck Rahmen Rahmen* bei *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-123">destination destination at *rectangle* frame frame at *rectangle*</span></span>                             | <span data-ttu-id="d10cf-124">Quell Quelle bei *Rechteck* Video Video bei *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-124">source source at *rectangle* video video at *rectangle*</span></span>                                           |



 

<span data-ttu-id="d10cf-125">In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszregions** -Parameter und deren Bedeutung angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="d10cf-125">The following table lists the flags that can be specified in the **lpszRegions** parameter and their meanings.</span></span>



| <span data-ttu-id="d10cf-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d10cf-126">Value</span></span>                        | <span data-ttu-id="d10cf-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d10cf-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10cf-128">destination</span><span class="sxs-lookup"><span data-stu-id="d10cf-128">destination</span></span>                  | <span data-ttu-id="d10cf-129">Wählt den gesamten Client Bereich des Zielfensters aus, um die Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d10cf-129">Selects the entire client area of the destination window to display the data.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d10cf-130">Ziel bei *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-130">destination at *rectangle*</span></span>   | <span data-ttu-id="d10cf-131">Wählt einen Teil des Client Bereichs des Zielfensters aus, in dem das Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d10cf-131">Selects a portion of the client area of the destination window used to display the image.</span></span> <span data-ttu-id="d10cf-132">Wenn ein Bereich des Anzeige Fensters angegeben wird und das Gerät die Streckung unterstützt, wird das Quellbild auf den Ziel Offset und-Block gestreckt.</span><span class="sxs-lookup"><span data-stu-id="d10cf-132">When an area of the display window is specified and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                     |
| <span data-ttu-id="d10cf-133">frame</span><span class="sxs-lookup"><span data-stu-id="d10cf-133">frame</span></span>                        | <span data-ttu-id="d10cf-134">Wählt den gesamten Frame Puffer zum Empfangen der eingehenden Videobilder aus.</span><span class="sxs-lookup"><span data-stu-id="d10cf-134">Selects the entire frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d10cf-135">Rahmen bei *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-135">frame at *rectangle*</span></span>         | <span data-ttu-id="d10cf-136">Wählt einen Teil des Frame Puffers zum Empfangen der eingehenden Videobilder aus.</span><span class="sxs-lookup"><span data-stu-id="d10cf-136">Selects a portion of the frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d10cf-137">source</span><span class="sxs-lookup"><span data-stu-id="d10cf-137">source</span></span>                       | <span data-ttu-id="d10cf-138">Wählt das gesamte Bild aus, das im Zielfenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d10cf-138">Selects the entire image for display in the destination window.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d10cf-139">Quelle beim *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-139">source at *rectangle*</span></span>        | <span data-ttu-id="d10cf-140">Wählt einen Teil des Bilds aus, der im Zielfenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d10cf-140">Selects a portion of the image to display in the destination window.</span></span> <span data-ttu-id="d10cf-141">Wenn ein Bereich des Quell Bilds angegeben wird und das Gerät die Streckung unterstützt, wird das Quell Abbild auf den Ziel Offset und-Block gestreckt.</span><span class="sxs-lookup"><span data-stu-id="d10cf-141">When an area of the source image is specified, and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                                           |
| <span data-ttu-id="d10cf-142">video</span><span class="sxs-lookup"><span data-stu-id="d10cf-142">video</span></span>                        | <span data-ttu-id="d10cf-143">Wählt das gesamte eingehende Videobild aus, das im Frame Puffer erfasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="d10cf-143">Selects the entire incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d10cf-144">Video mit *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-144">video at *rectangle*</span></span>         | <span data-ttu-id="d10cf-145">Wählt einen Teil des eingehenden Video Bilds aus, der im Frame Puffer erfasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="d10cf-145">Selects a portion of the incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d10cf-146">Fenster</span><span class="sxs-lookup"><span data-stu-id="d10cf-146">window</span></span>                       | <span data-ttu-id="d10cf-147">Stellt die anfängliche Fenstergröße auf der Anzeige wieder her.</span><span class="sxs-lookup"><span data-stu-id="d10cf-147">Restores the initial window size on the display.</span></span> <span data-ttu-id="d10cf-148">Mit diesem Befehl wird auch das-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d10cf-148">This command also displays the window.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d10cf-149">Fenster mit *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-149">window at *rectangle*</span></span>        | <span data-ttu-id="d10cf-150">Ändert die Größe und Position des Anzeige Fensters.</span><span class="sxs-lookup"><span data-stu-id="d10cf-150">Changes the size and location of the display window.</span></span> <span data-ttu-id="d10cf-151">Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Anzeige Fensters (normalerweise der Desktop), wenn das Flag "Style Child" für den Befehl " [Öffnen](open.md) " verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d10cf-151">The specified rectangle is relative to the parent window of the display window (usually the desktop) if the "style child" flag has been used for the [open](open.md) command.</span></span> <span data-ttu-id="d10cf-152">Um die Position des Fensters zu ändern, ohne die Höhe oder Breite zu ändern, geben Sie 0 für Höhe und Breite an.</span><span class="sxs-lookup"><span data-stu-id="d10cf-152">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span> |
| <span data-ttu-id="d10cf-153">Fenster Client</span><span class="sxs-lookup"><span data-stu-id="d10cf-153">window client</span></span>                | <span data-ttu-id="d10cf-154">Stellt den Client Bereich des Fensters wieder her.</span><span class="sxs-lookup"><span data-stu-id="d10cf-154">Restores the client area of the window.</span></span>                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d10cf-155">Fenster Client bei *Rechteck*</span><span class="sxs-lookup"><span data-stu-id="d10cf-155">window client at *rectangle*</span></span> | <span data-ttu-id="d10cf-156">Ändert die Größe und Position des Client Bereichs des Fensters.</span><span class="sxs-lookup"><span data-stu-id="d10cf-156">Changes the size and location of the client area of the window.</span></span> <span data-ttu-id="d10cf-157">Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Client Fensters.</span><span class="sxs-lookup"><span data-stu-id="d10cf-157">The specified rectangle is relative to the parent window of the client window.</span></span> <span data-ttu-id="d10cf-158">Um die Position des Fensters zu ändern, ohne die Höhe oder Breite zu ändern, geben Sie 0 für Höhe und Breite an.</span><span class="sxs-lookup"><span data-stu-id="d10cf-158">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span>                                                                                      |



 

<span data-ttu-id="d10cf-159">Wenn ein Flag ein Rechteck enthält, sind die Rechteck Koordinaten relativ zum Fenster Ursprung oder dem Bild Ursprung, wenn dies erforderlich ist, und werden als **x1 y1 x2 Y2** angegeben.</span><span class="sxs-lookup"><span data-stu-id="d10cf-159">When a flag includes a rectangle, the rectangle coordinates are relative to the window origin or the image origin, as appropriate, and are specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="d10cf-160">Die Koordinaten **X1Y1** geben die linke obere Ecke an, und die Koordinaten **X2Y2** geben die Breite und Höhe des Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="d10cf-160">The coordinates **X1Y1** specify the upper left corner, and the coordinates **X2Y2** specify the width and height of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d10cf-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*</span><span class="sxs-lookup"><span data-stu-id="d10cf-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d10cf-162">Kann "wait", "notify" oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="d10cf-162">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="d10cf-163">Für Digital Video-Geräte kann auch "Test" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d10cf-163">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="d10cf-164">Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d10cf-164">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d10cf-165">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d10cf-165">Return Value</span></span>

<span data-ttu-id="d10cf-166">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="d10cf-166">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d10cf-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d10cf-167">Remarks</span></span>

<span data-ttu-id="d10cf-168">Der Put-Befehl definiert bei der Arbeit mit Video Überlagerungs Geräten mindestens eine der folgenden Rechtecke:</span><span class="sxs-lookup"><span data-stu-id="d10cf-168">The put command defines one or more of the following rectangles when working with video-overlay devices:</span></span>

-   <span data-ttu-id="d10cf-169">Das Video Rechteck definiert den Bereich des zu erfassenden eingehenden Video Bilds.</span><span class="sxs-lookup"><span data-stu-id="d10cf-169">The video rectangle defines the region of the incoming video image to capture.</span></span>
-   <span data-ttu-id="d10cf-170">Das Rahmen Rechteck definiert den Bereich des Frame Puffers, der das eingehende Video Bild empfängt.</span><span class="sxs-lookup"><span data-stu-id="d10cf-170">The frame rectangle defines the region of the frame buffer that receives the incoming video image.</span></span>
-   <span data-ttu-id="d10cf-171">Das Quell Rechteck definiert, welcher Bereich des Frame Puffers in das Ziel Rechteck kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="d10cf-171">The source rectangle defines which region of the frame buffer is copied to the destination rectangle.</span></span>
-   <span data-ttu-id="d10cf-172">Das Ziel Rechteck definiert den Bereich des Client Bereichs des Anzeige Fensters, der das Video Bild empfängt.</span><span class="sxs-lookup"><span data-stu-id="d10cf-172">The destination rectangle defines the region of the display window client area that receives the video image.</span></span>

<span data-ttu-id="d10cf-173">Das Video Rechteck ist mit dem Frame Rechteck identisch, ebenso wie das Quell Rechteck mit dem Ziel Rechteck verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d10cf-173">The video rectangle is related to the frame rectangle in the same way the source rectangle is related to the destination rectangle.</span></span> <span data-ttu-id="d10cf-174">Die Streckung kann vom Video Rechteck bis zum Frame Rechteck und vom Quell Rechteck bis zum Ziel Rechteck erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d10cf-174">Stretching can occur from the video rectangle to the frame rectangle and from the source rectangle to the destination rectangle.</span></span> <span data-ttu-id="d10cf-175">Nicht alle Geräte unterstützen die Streckung, und die Streckung muss aktiviert sein (mit dem [Set](set.md) -Befehl).</span><span class="sxs-lookup"><span data-stu-id="d10cf-175">Not all devices support stretching, and stretching must be enabled (by using the [set](set.md) command).</span></span>

<span data-ttu-id="d10cf-176">Mit dem folgenden Befehl werden drei Bereiche für das Video, den Frame und die Quelle definiert.</span><span class="sxs-lookup"><span data-stu-id="d10cf-176">The following command defines three regions for the video, frame, and source.</span></span>

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

<span data-ttu-id="d10cf-177">Die Regionen in diesem Beispiel werden wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="d10cf-177">The regions in this example are defined as follows:</span></span>

-   <span data-ttu-id="d10cf-178">Ein Bereich von 200 bis 200 Pixel der eingehenden Videodaten, beginnend bei einem Ursprung 120 Pixel von der oberen linken Ecke, wird im Frame Puffer aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d10cf-178">A 200- by 200-pixel region of the incoming video data, starting at an origin 120 pixels from the upper left corner, will be captured to the frame buffer.</span></span>
-   <span data-ttu-id="d10cf-179">Die Videodaten werden in einem Bereich von 200 bis 200 Pixel in der oberen linken Ecke des Frame Puffers platziert.</span><span class="sxs-lookup"><span data-stu-id="d10cf-179">The video data will be placed in a 200- by 200-pixel region at the upper left corner of the frame buffer.</span></span>
-   <span data-ttu-id="d10cf-180">Übertragungen werden vom Bereich 200 bis 200 Pixel in der linken oberen Ecke des Frame Puffers zum Zielfenster durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d10cf-180">Transfers are made from the 200- by 200-pixel region at the upper left corner of the frame buffer to the destination window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10cf-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d10cf-181">Requirements</span></span>



| <span data-ttu-id="d10cf-182">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d10cf-182">Requirement</span></span> | <span data-ttu-id="d10cf-183">Wert</span><span class="sxs-lookup"><span data-stu-id="d10cf-183">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d10cf-184">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d10cf-184">Minimum supported client</span></span><br/> | <span data-ttu-id="d10cf-185">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d10cf-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d10cf-186">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d10cf-186">Minimum supported server</span></span><br/> | <span data-ttu-id="d10cf-187">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d10cf-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d10cf-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d10cf-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10cf-189">MCI</span><span class="sxs-lookup"><span data-stu-id="d10cf-189">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d10cf-190">MCI-Befehls Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="d10cf-190">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d10cf-191">open</span><span class="sxs-lookup"><span data-stu-id="d10cf-191">open</span></span>](open.md)
</dt> <dt>

[<span data-ttu-id="d10cf-192">set</span><span class="sxs-lookup"><span data-stu-id="d10cf-192">set</span></span>](set.md)
</dt> </dl>

 

