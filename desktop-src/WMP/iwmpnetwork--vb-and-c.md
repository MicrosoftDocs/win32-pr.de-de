---
title: Iwmpnetwork (VB und C)-Schnittstelle (WMP. h)
description: Stellt Eigenschaften und Methoden für den Zugriff auf Statistiken in Bezug auf die Qualität einer Netzwerkverbindung sowie zum angeben und Abrufen der Netzwerk Proxy Einstellungen bereit. Die iwmpnetwork-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- Iwmpnetwork (VB und C) Interface Windows Media Player
- Iwmpnetwork (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364700"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a><span data-ttu-id="a263e-105">Iwmpnetwork (VB und c#)-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a263e-105">IWMPNetwork (VB and C#) interface</span></span>

<span data-ttu-id="a263e-106">Stellt Eigenschaften und Methoden für den Zugriff auf Statistiken in Bezug auf die Qualität einer Netzwerkverbindung sowie zum angeben und Abrufen der Netzwerk Proxy Einstellungen bereit.</span><span class="sxs-lookup"><span data-stu-id="a263e-106">Provides properties and methods to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="a263e-107">Die **iwmpnetwork** -Schnittstelle macht die folgenden Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a263e-107">The **IWMPNetwork** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="a263e-108">Member</span><span class="sxs-lookup"><span data-stu-id="a263e-108">Members</span></span>

<span data-ttu-id="a263e-109">Die **iwmpnetwork (VB und c#)** -Schnittstelle verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a263e-109">The **IWMPNetwork (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="a263e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="a263e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a263e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a263e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a263e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="a263e-112">Methods</span></span>

<span data-ttu-id="a263e-113">Die **iwmpnetwork (VB und c#)** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a263e-113">The **IWMPNetwork (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="a263e-114">Methode</span><span class="sxs-lookup"><span data-stu-id="a263e-114">Method</span></span>                                                                                           | <span data-ttu-id="a263e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a263e-115">Description</span></span>                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a263e-116">**getproxybypassforlocal**</span><span class="sxs-lookup"><span data-stu-id="a263e-116">**getProxyBypassForLocal**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | <span data-ttu-id="a263e-117">Gibt einen Wert zurück, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="a263e-117">Returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/> |
| [<span data-ttu-id="a263e-118">**getproxyexceptionlist**</span><span class="sxs-lookup"><span data-stu-id="a263e-118">**getProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="a263e-119">Gibt die Liste der Proxy Ausnahmen zurück.</span><span class="sxs-lookup"><span data-stu-id="a263e-119">Returns the proxy exception list.</span></span><br/>                                                                           |
| [<span data-ttu-id="a263e-120">**getproxyname**</span><span class="sxs-lookup"><span data-stu-id="a263e-120">**getProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | <span data-ttu-id="a263e-121">Gibt den Namen des verwendeten Proxy Servers zurück.</span><span class="sxs-lookup"><span data-stu-id="a263e-121">Returns the name of the proxy server being used.</span></span><br/>                                                            |
| [<span data-ttu-id="a263e-122">**getproxyport**</span><span class="sxs-lookup"><span data-stu-id="a263e-122">**getProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | <span data-ttu-id="a263e-123">Gibt den verwendeten ProxyPort zurück.</span><span class="sxs-lookup"><span data-stu-id="a263e-123">Returns the proxy port being used.</span></span><br/>                                                                          |
| [<span data-ttu-id="a263e-124">**getproxysettings**</span><span class="sxs-lookup"><span data-stu-id="a263e-124">**getProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | <span data-ttu-id="a263e-125">Gibt Informationen zu den Proxy Einstellungen für ein Protokoll zurück.</span><span class="sxs-lookup"><span data-stu-id="a263e-125">Returns information about the proxy settings for a protocol.</span></span><br/>                                                |
| [<span data-ttu-id="a263e-126">**setproxybypassforlocal**</span><span class="sxs-lookup"><span data-stu-id="a263e-126">**setProxyBypassForLocal**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | <span data-ttu-id="a263e-127">Gibt an, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="a263e-127">Specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span><br/>                  |
| [<span data-ttu-id="a263e-128">**setproxyexceptionlist**</span><span class="sxs-lookup"><span data-stu-id="a263e-128">**setProxyExceptionList**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | <span data-ttu-id="a263e-129">Gibt die Proxy Ausnahmeliste an.</span><span class="sxs-lookup"><span data-stu-id="a263e-129">Specifies the proxy exception list.</span></span><br/>                                                                         |
| [<span data-ttu-id="a263e-130">**setproxyname**</span><span class="sxs-lookup"><span data-stu-id="a263e-130">**setProxyName**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | <span data-ttu-id="a263e-131">Gibt den Namen des zu verwendenden Proxy Servers an.</span><span class="sxs-lookup"><span data-stu-id="a263e-131">Specifies the name of the proxy server to use.</span></span><br/>                                                              |
| [<span data-ttu-id="a263e-132">**setproxyport**</span><span class="sxs-lookup"><span data-stu-id="a263e-132">**setProxyPort**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | <span data-ttu-id="a263e-133">Gibt den zu verwendenden ProxyPort an.</span><span class="sxs-lookup"><span data-stu-id="a263e-133">Specifies the proxy port to use.</span></span><br/>                                                                            |
| [<span data-ttu-id="a263e-134">**setProxySettings**</span><span class="sxs-lookup"><span data-stu-id="a263e-134">**setProxySettings**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | <span data-ttu-id="a263e-135">Gibt die Proxy Einstellungen für ein Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="a263e-135">Specifies the proxy settings for a protocol.</span></span><br/>                                                                |



 

### <a name="properties"></a><span data-ttu-id="a263e-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a263e-136">Properties</span></span>

<span data-ttu-id="a263e-137">Die **iwmpnetwork (VB und c#)** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a263e-137">The **IWMPNetwork (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="a263e-138">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a263e-138">Property</span></span>                                                                                          | <span data-ttu-id="a263e-139">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="a263e-139">Access type</span></span>           | <span data-ttu-id="a263e-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a263e-140">Description</span></span>                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a263e-141">**Bandbreite**</span><span class="sxs-lookup"><span data-stu-id="a263e-141">**bandWidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | <span data-ttu-id="a263e-142">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-142">Read-only</span></span><br/>  | <span data-ttu-id="a263e-143">Ruft die aktuelle Bandbreite des Medien Elements ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-143">Gets the current bandwidth of the media item.</span></span><br/>                                     |
| [<span data-ttu-id="a263e-144">**Bitrate**</span><span class="sxs-lookup"><span data-stu-id="a263e-144">**bitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | <span data-ttu-id="a263e-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-145">Read-only</span></span><br/>  | <span data-ttu-id="a263e-146">Ruft die aktuelle Bitrate ab, die empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="a263e-146">Gets the current bit rate being received.</span></span><br/>                                         |
| [<span data-ttu-id="a263e-147">**bufferingcount**</span><span class="sxs-lookup"><span data-stu-id="a263e-147">**bufferingCount**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | <span data-ttu-id="a263e-148">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-148">Read-only</span></span><br/>  | <span data-ttu-id="a263e-149">Ruft ab, wie oft die Pufferung während der Wiedergabe aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a263e-149">Gets the number of times buffering occurred during playback.</span></span><br/>                      |
| [<span data-ttu-id="a263e-150">**Pufferungs**</span><span class="sxs-lookup"><span data-stu-id="a263e-150">**bufferingProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | <span data-ttu-id="a263e-151">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-151">Read-only</span></span><br/>  | <span data-ttu-id="a263e-152">Ruft den Prozentsatz der abgeschlossenen Pufferung ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-152">Gets the percentage of buffering completed.</span></span><br/>                                       |
| [<span data-ttu-id="a263e-153">**BufferingTime**</span><span class="sxs-lookup"><span data-stu-id="a263e-153">**bufferingTime**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | <span data-ttu-id="a263e-154">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a263e-154">Read/write</span></span><br/> | <span data-ttu-id="a263e-155">Ruft die Zeitspanne in Millisekunden ab, bevor die Wiedergabe beginnt, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="a263e-155">Gets or sets the amount of buffering time in milliseconds before playback begins.</span></span><br/> |
| [<span data-ttu-id="a263e-156">**Download Fortschritt**</span><span class="sxs-lookup"><span data-stu-id="a263e-156">**downloadProgress**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | <span data-ttu-id="a263e-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-157">Read-only</span></span><br/>  | <span data-ttu-id="a263e-158">Ruft den Prozentsatz des abgeschlossenen Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-158">Gets the percentage of downloading completed.</span></span><br/>                                     |
| [<span data-ttu-id="a263e-159">**encodframerate**</span><span class="sxs-lookup"><span data-stu-id="a263e-159">**encodedFrameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | <span data-ttu-id="a263e-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-160">Read-only</span></span><br/>  | <span data-ttu-id="a263e-161">Ruft die vom Inhalts Autor angegebene Video Frame Rate ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-161">Gets the video frame rate specified by the content author.</span></span><br/>                        |
| [<span data-ttu-id="a263e-162">**Framerate**</span><span class="sxs-lookup"><span data-stu-id="a263e-162">**frameRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | <span data-ttu-id="a263e-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-163">Read-only</span></span><br/>  | <span data-ttu-id="a263e-164">Ruft die aktuelle Video Frame Rate ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-164">Gets the current video frame rate.</span></span><br/>                                                |
| [<span data-ttu-id="a263e-165">**framesskipped**</span><span class="sxs-lookup"><span data-stu-id="a263e-165">**framesSkipped**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | <span data-ttu-id="a263e-166">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-166">Read-only</span></span><br/>  | <span data-ttu-id="a263e-167">Ruft die Gesamtanzahl der während der Wiedergabe übersprungenen Frames ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-167">Gets the total number of frames skipped during playback.</span></span><br/>                          |
| [<span data-ttu-id="a263e-168">**lostpakete**</span><span class="sxs-lookup"><span data-stu-id="a263e-168">**lostPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | <span data-ttu-id="a263e-169">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-169">Read-only</span></span><br/>  | <span data-ttu-id="a263e-170">Ruft die Anzahl der verlorenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-170">Gets the number of packets lost.</span></span><br/>                                                  |
| [<span data-ttu-id="a263e-171">**maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="a263e-171">**maxBandwidth**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | <span data-ttu-id="a263e-172">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a263e-172">Read/write</span></span><br/> | <span data-ttu-id="a263e-173">Ruft die maximal zulässige Bandbreite ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="a263e-173">Gets or sets the maximum allowed bandwidth.</span></span><br/>                                       |
| [<span data-ttu-id="a263e-174">**maxbitrate**</span><span class="sxs-lookup"><span data-stu-id="a263e-174">**maxBitRate**</span></span>](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | <span data-ttu-id="a263e-175">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-175">Read-only</span></span><br/>  | <span data-ttu-id="a263e-176">Ruft die maximal mögliche Video Bitrate ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-176">Gets the maximum possible video bit rate.</span></span><br/>                                         |
| [<span data-ttu-id="a263e-177">**receivedpakete**</span><span class="sxs-lookup"><span data-stu-id="a263e-177">**receivedPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | <span data-ttu-id="a263e-178">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-178">Read-only</span></span><br/>  | <span data-ttu-id="a263e-179">Ruft die Anzahl der empfangenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-179">Gets the number of packets received.</span></span><br/>                                              |
| [<span data-ttu-id="a263e-180">**"receptionquality"**</span><span class="sxs-lookup"><span data-stu-id="a263e-180">**receptionQuality**</span></span>](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | <span data-ttu-id="a263e-181">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-181">Read-only</span></span><br/>  | <span data-ttu-id="a263e-182">Ruft den Prozentsatz der in den letzten 30 Sekunden nicht verlorenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-182">Gets the percentage of packets not lost in the last 30 seconds.</span></span><br/>                   |
| [<span data-ttu-id="a263e-183">**wiederherstellbare Pakete**</span><span class="sxs-lookup"><span data-stu-id="a263e-183">**recoveredPackets**</span></span>](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | <span data-ttu-id="a263e-184">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-184">Read-only</span></span><br/>  | <span data-ttu-id="a263e-185">Ruft die Anzahl der wiederhergestellten Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="a263e-185">Gets the number of recovered packets.</span></span><br/>                                             |
| [<span data-ttu-id="a263e-186">**sourceprotocol**</span><span class="sxs-lookup"><span data-stu-id="a263e-186">**sourceProtocol**</span></span>](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | <span data-ttu-id="a263e-187">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a263e-187">Read-only</span></span><br/>  | <span data-ttu-id="a263e-188">Ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a263e-188">Gets the source protocol used to receive data.</span></span><br/>                                    |



 

<span data-ttu-id="a263e-189">Verwenden Sie die folgende Eigenschaft, um eine **iwmpnetwork** -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a263e-189">Get an **IWMPNetwork** interface by using the following property.</span></span>



| <span data-ttu-id="a263e-190">Object</span><span class="sxs-lookup"><span data-stu-id="a263e-190">Object</span></span>                                                                   | <span data-ttu-id="a263e-191">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a263e-191">Property</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="a263e-192">AxWindowsMediaPlayer-Objekt</span><span class="sxs-lookup"><span data-stu-id="a263e-192">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="a263e-193">**Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="a263e-193">**network**</span></span>](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="a263e-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a263e-194">Requirements</span></span>



| <span data-ttu-id="a263e-195">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a263e-195">Requirement</span></span> | <span data-ttu-id="a263e-196">Wert</span><span class="sxs-lookup"><span data-stu-id="a263e-196">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a263e-197">Header</span><span class="sxs-lookup"><span data-stu-id="a263e-197">Header</span></span><br/> | <dl> <span data-ttu-id="a263e-198"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a263e-198"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a263e-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a263e-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a263e-200">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="a263e-200">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





