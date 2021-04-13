---
title: Netzwerk Objekt
description: Das Netzwerk Objekt stellt Eigenschaften und Methoden bereit, die für den Zugriff auf Statistiken in Bezug auf die Qualität einer Netzwerkverbindung und zum angeben und Abrufen der Netzwerk Proxy Einstellungen verwendet werden.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Windows-Media Player für Netzwerk Objekte
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104389372"
---
# <a name="network-object"></a><span data-ttu-id="0aac3-104">Netzwerk Objekt</span><span class="sxs-lookup"><span data-stu-id="0aac3-104">Network Object</span></span>

<span data-ttu-id="0aac3-105">Das **Netzwerk** Objekt stellt Eigenschaften und Methoden bereit, die für den Zugriff auf Statistiken in Bezug auf die Qualität einer Netzwerkverbindung und zum angeben und Abrufen der Netzwerk Proxy Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0aac3-105">The **Network** object provides properties and methods used to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="0aac3-106">Das **Netzwerk** Objekt unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0aac3-106">The **Network** object supports the following properties.</span></span>



| <span data-ttu-id="0aac3-107">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0aac3-107">Property</span></span>                                           | <span data-ttu-id="0aac3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aac3-108">Description</span></span>                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0aac3-109">Bandbreite</span><span class="sxs-lookup"><span data-stu-id="0aac3-109">bandWidth</span></span>](network-bandwidth.md)                 | <span data-ttu-id="0aac3-110">Ruft die aktuelle Bandbreite des Medien Elements ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-110">Retrieves the current bandwidth of the media item.</span></span>                                          |
| [<span data-ttu-id="0aac3-111">Bitrate</span><span class="sxs-lookup"><span data-stu-id="0aac3-111">bitRate</span></span>](network-bitrate.md)                     | <span data-ttu-id="0aac3-112">Ruft die aktuelle Bitrate ab, die empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="0aac3-112">Retrieves the current bit rate being received.</span></span>                                              |
| [<span data-ttu-id="0aac3-113">bufferingcount</span><span class="sxs-lookup"><span data-stu-id="0aac3-113">bufferingCount</span></span>](network-bufferingcount.md)       | <span data-ttu-id="0aac3-114">Ruft ab, wie oft die Pufferung während der Wiedergabe aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="0aac3-114">Retrieves the number of times buffering occurred during playback.</span></span>                           |
| [<span data-ttu-id="0aac3-115">Pufferungs</span><span class="sxs-lookup"><span data-stu-id="0aac3-115">bufferingProgress</span></span>](network-bufferingprogress.md) | <span data-ttu-id="0aac3-116">Ruft den Prozentsatz der abgeschlossenen Pufferung ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-116">Retrieves the percentage of buffering completed.</span></span>                                            |
| [<span data-ttu-id="0aac3-117">BufferingTime</span><span class="sxs-lookup"><span data-stu-id="0aac3-117">bufferingTime</span></span>](network-bufferingtime.md)         | <span data-ttu-id="0aac3-118">Gibt den Puffer Zeitraum in Millisekunden vor Beginn der Wiedergabe an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-118">Specifies or retrieves the amount of buffering time in milliseconds before playback begins.</span></span> |
| [<span data-ttu-id="0aac3-119">Download Fortschritt</span><span class="sxs-lookup"><span data-stu-id="0aac3-119">downloadProgress</span></span>](network-downloadprogress.md)   | <span data-ttu-id="0aac3-120">Ruft den Prozentsatz des abgeschlossenen Downloads ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-120">Retrieves the percentage of download completed.</span></span>                                             |
| [<span data-ttu-id="0aac3-121">encodframerate</span><span class="sxs-lookup"><span data-stu-id="0aac3-121">encodedFrameRate</span></span>](network-encodedframerate.md)   | <span data-ttu-id="0aac3-122">Ruft die vom Inhalts Autor angegebene Video Frame Rate ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-122">Retrieves the video frame rate specified by the content author.</span></span>                             |
| [<span data-ttu-id="0aac3-123">Framerate</span><span class="sxs-lookup"><span data-stu-id="0aac3-123">frameRate</span></span>](network-framerate.md)                 | <span data-ttu-id="0aac3-124">Ruft die aktuelle Video Frame Rate ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-124">Retrieves the current video frame rate.</span></span>                                                     |
| [<span data-ttu-id="0aac3-125">framesskipped</span><span class="sxs-lookup"><span data-stu-id="0aac3-125">framesSkipped</span></span>](network-framesskipped.md)         | <span data-ttu-id="0aac3-126">Ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.</span><span class="sxs-lookup"><span data-stu-id="0aac3-126">Retrieves the total number of frames skipped during playback.</span></span>                               |
| [<span data-ttu-id="0aac3-127">lostpakete</span><span class="sxs-lookup"><span data-stu-id="0aac3-127">lostPackets</span></span>](network-lostpackets.md)             | <span data-ttu-id="0aac3-128">Ruft die Anzahl der verlorenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-128">Retrieves the number of packets lost.</span></span>                                                       |
| [<span data-ttu-id="0aac3-129">maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="0aac3-129">maxBandwidth</span></span>](network-maxbandwidth.md)           | <span data-ttu-id="0aac3-130">Gibt die maximal zulässige Bandbreite an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-130">Specifies or retrieves the maximum allowed bandwidth.</span></span>                                       |
| [<span data-ttu-id="0aac3-131">maxbitrate</span><span class="sxs-lookup"><span data-stu-id="0aac3-131">maxBitRate</span></span>](network-maxbitrate.md)               | <span data-ttu-id="0aac3-132">Ruft die maximal mögliche Video Bitrate ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-132">Retrieves the maximum possible video bit rate.</span></span>                                              |
| [<span data-ttu-id="0aac3-133">receivedpakete</span><span class="sxs-lookup"><span data-stu-id="0aac3-133">receivedPackets</span></span>](network-receivedpackets.md)     | <span data-ttu-id="0aac3-134">Ruft die Anzahl der empfangenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-134">Retrieves the number of packets received.</span></span>                                                   |
| [<span data-ttu-id="0aac3-135">"receptionquality"</span><span class="sxs-lookup"><span data-stu-id="0aac3-135">receptionQuality</span></span>](network-receptionquality.md)   | <span data-ttu-id="0aac3-136">Ruft den Prozentsatz der in den letzten 30 Sekunden empfangenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-136">Retrieves the percentage of packets received in the last 30 seconds.</span></span>                        |
| [<span data-ttu-id="0aac3-137">wiederherstellbare Pakete</span><span class="sxs-lookup"><span data-stu-id="0aac3-137">recoveredPackets</span></span>](network-recoveredpackets.md)   | <span data-ttu-id="0aac3-138">Ruft die Anzahl der wiederhergestellten Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-138">Retrieves the number of recovered packets.</span></span>                                                  |
| [<span data-ttu-id="0aac3-139">sourceprotocol</span><span class="sxs-lookup"><span data-stu-id="0aac3-139">sourceProtocol</span></span>](network-sourceprotocol.md)       | <span data-ttu-id="0aac3-140">Ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0aac3-140">Retrieves the source protocol used to receive data.</span></span>                                         |



 

<span data-ttu-id="0aac3-141">Das- **Netzwerk** Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="0aac3-141">The **Network** object supports the following methods.</span></span>



| <span data-ttu-id="0aac3-142">Methode</span><span class="sxs-lookup"><span data-stu-id="0aac3-142">Method</span></span>                                                       | <span data-ttu-id="0aac3-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aac3-143">Description</span></span>                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0aac3-144">getproxybypassforlocal</span><span class="sxs-lookup"><span data-stu-id="0aac3-144">getProxyBypassForLocal</span></span>](network-getproxybypassforlocal.md) | <span data-ttu-id="0aac3-145">Ruft einen Wert ab, der angibt, ob der Proxy Server umgangen werden soll, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="0aac3-145">Retrieves a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="0aac3-146">getproxyexceptionlist</span><span class="sxs-lookup"><span data-stu-id="0aac3-146">getProxyExceptionList</span></span>](network-getproxyexceptionlist.md)   | <span data-ttu-id="0aac3-147">Ruft die Proxy Ausnahmeliste ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-147">Retrieves the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="0aac3-148">getproxyname</span><span class="sxs-lookup"><span data-stu-id="0aac3-148">getProxyName</span></span>](network-getproxyname.md)                     | <span data-ttu-id="0aac3-149">Ruft den Namen des zu verwendenden Proxy Servers ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-149">Retrieves the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="0aac3-150">getproxyport</span><span class="sxs-lookup"><span data-stu-id="0aac3-150">getProxyPort</span></span>](network-getproxyport.md)                     | <span data-ttu-id="0aac3-151">Ruft den zu verwendenden ProxyPort ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-151">Retrieves the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="0aac3-152">getproxysettings</span><span class="sxs-lookup"><span data-stu-id="0aac3-152">getProxySettings</span></span>](network-getproxysettings.md)             | <span data-ttu-id="0aac3-153">Ruft die Proxy Einstellung für ein bestimmtes Protokoll ab.</span><span class="sxs-lookup"><span data-stu-id="0aac3-153">Retrieves the proxy setting for a given protocol.</span></span>                                                                    |
| [<span data-ttu-id="0aac3-154">setproxybypassforlocal</span><span class="sxs-lookup"><span data-stu-id="0aac3-154">setProxyBypassForLocal</span></span>](network-setproxybypassforlocal.md) | <span data-ttu-id="0aac3-155">Gibt einen Wert an, der angibt, ob der Proxy Server umgangen werden soll, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="0aac3-155">Specifies a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="0aac3-156">setproxyexceptionlist</span><span class="sxs-lookup"><span data-stu-id="0aac3-156">setProxyExceptionList</span></span>](network-setproxyexceptionlist.md)   | <span data-ttu-id="0aac3-157">Gibt die Proxy Ausnahmeliste an.</span><span class="sxs-lookup"><span data-stu-id="0aac3-157">Specifies the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="0aac3-158">setproxyname</span><span class="sxs-lookup"><span data-stu-id="0aac3-158">setProxyName</span></span>](network-setproxyname.md)                     | <span data-ttu-id="0aac3-159">Gibt den Namen des zu verwendenden Proxy Servers an.</span><span class="sxs-lookup"><span data-stu-id="0aac3-159">Specifies the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="0aac3-160">setproxyport</span><span class="sxs-lookup"><span data-stu-id="0aac3-160">setProxyPort</span></span>](network-setproxyport.md)                     | <span data-ttu-id="0aac3-161">Gibt den zu verwendenden ProxyPort an.</span><span class="sxs-lookup"><span data-stu-id="0aac3-161">Specifies the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="0aac3-162">setProxySettings</span><span class="sxs-lookup"><span data-stu-id="0aac3-162">setProxySettings</span></span>](network-setproxysettings.md)             | <span data-ttu-id="0aac3-163">Gibt die Proxy Einstellung für ein bestimmtes Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="0aac3-163">Specifies the proxy setting for a given protocol.</span></span>                                                                    |



 

<span data-ttu-id="0aac3-164">Der Zugriff auf das **Netzwerk** Objekt erfolgt über die folgende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0aac3-164">The **Network** object is accessed through the following property.</span></span>



| <span data-ttu-id="0aac3-165">Object</span><span class="sxs-lookup"><span data-stu-id="0aac3-165">Object</span></span>                      | <span data-ttu-id="0aac3-166">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0aac3-166">Property</span></span>                      |
|-----------------------------|-------------------------------|
| [<span data-ttu-id="0aac3-167">Player</span><span class="sxs-lookup"><span data-stu-id="0aac3-167">Player</span></span>](player-object.md) | [<span data-ttu-id="0aac3-168">network</span><span class="sxs-lookup"><span data-stu-id="0aac3-168">network</span></span>](player-network.md) |



 

## <a name="see-also"></a><span data-ttu-id="0aac3-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0aac3-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aac3-170">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="0aac3-170">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




