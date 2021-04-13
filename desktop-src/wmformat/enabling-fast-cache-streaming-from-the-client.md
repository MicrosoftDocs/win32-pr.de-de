---
title: Aktivieren von schnellem Cache Streaming vom Client
description: Aktivieren von schnellem Cache Streaming vom Client
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows Media-Format-SDK, Aktivieren von schnellem Cache Streaming
- Windows Media-Format-SDK, schnelles Cache Streaming
- Advanced Systems Format (ASF), Aktivieren von schnellem Cache Streaming
- ASF (Advanced Systems Format), Aktivieren von schnellem Cache Streaming
- Advanced Systems Format (ASF), schnelles Cache Streaming
- ASF (Advanced Systems Format), schnelles Cache Streaming
- Streams, Aktivieren von schnellem Cache Streaming
- Schnelles Cache Streaming, aktivieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389865"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a><span data-ttu-id="078f9-111">Aktivieren von schnellem Cache Streaming vom Client</span><span class="sxs-lookup"><span data-stu-id="078f9-111">Enabling Fast Cache Streaming from the Client</span></span>

<span data-ttu-id="078f9-112">Fast Cache ist eine Streamingtechnologie, bei der der-Server Inhalte in einer höheren Bitrate als die für die Wiedergabe benötigte Datenströme zustreamt.</span><span class="sxs-lookup"><span data-stu-id="078f9-112">Fast Cache is a streaming technology in which the server opportunistically streams content at a higher bit rate than what is needed for playback.</span></span>

<span data-ttu-id="078f9-113">Wenn die verfügbare Bandbreite höher ist als die Bitrate des Inhalts, werden schnelle Cache Datenströme mit höherer Geschwindigkeit gespeichert, und der Inhalt wird gepuffert.</span><span class="sxs-lookup"><span data-stu-id="078f9-113">If the available bandwidth is higher than the bit rate of the content, Fast Cache streams at the higher rate and buffers the content.</span></span> <span data-ttu-id="078f9-114">Dies trägt dazu bei, dass Unterbrechungen später reduziert werden, wenn das Netzwerk überlastet wird.</span><span class="sxs-lookup"><span data-stu-id="078f9-114">This helps to reduce interruptions later if the network becomes congested.</span></span> <span data-ttu-id="078f9-115">Wenn die Netzwerkbandbreite niedriger ist als die Bitrate des Inhalts, puffert der schnelle Cache einen Teil der Daten, bevor die Wiedergabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="078f9-115">If network bandwidth is lower than the bit rate of the content, Fast Cache buffers a portion of the data before playback starts.</span></span> <span data-ttu-id="078f9-116">Der schnelle Cache wird für unzuverlässige Netzwerke (z. b. drahtlose Netzwerke) oder Netzwerke empfohlen, die große Schwankungen des Netzwerkverkehrs, z. b. Kabelmodems, aufweisen.</span><span class="sxs-lookup"><span data-stu-id="078f9-116">Fast Cache is recommended for unreliable networks, such as wireless networks, or networks that experience large fluctuations in network traffic, such as cable modems.</span></span> <span data-ttu-id="078f9-117">Es wird auch für den Inhalt der Variable Bitrate (VBR) empfohlen.</span><span class="sxs-lookup"><span data-stu-id="078f9-117">It is also recommended for variable bit rate (VBR) content.</span></span> <span data-ttu-id="078f9-118">Die Bandbreitenanforderungen für VBR-Inhalte sind nicht konstant, und der Reader ermöglicht den Reader, den Datenstrom während der unteren Bitrate zu puffern.</span><span class="sxs-lookup"><span data-stu-id="078f9-118">The bandwidth requirements for VBR content are not constant, and Fast Cache enables the reader to buffer the stream during the lower-bit-rate portions.</span></span>

<span data-ttu-id="078f9-119">Schnelles Cache Streaming wird nur für Bedarfs gesteuerte Inhalte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="078f9-119">Fast Cache streaming is supported only for on-demand content.</span></span> <span data-ttu-id="078f9-120">Außerdem muss der Server so konfiguriert werden, dass er schnelles Cache Streaming verwendet.</span><span class="sxs-lookup"><span data-stu-id="078f9-120">In addition, the server must be configured to use Fast Cache streaming.</span></span>

<span data-ttu-id="078f9-121">Um den schnellen Cache im Reader-Objekt zu aktivieren, müssen Sie die Methoden [**IWMReaderNetworkConfig2:: setenablecontentcaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) und [**IWMReaderNetworkConfig2:: setenablefastcache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) mit dem Wert **true** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="078f9-121">To enable Fast Cache in the reader object, call the [**IWMReaderNetworkConfig2::SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) and [**IWMReaderNetworkConfig2::SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) methods with the value **TRUE**.</span></span> <span data-ttu-id="078f9-122">Die erste Methode ermöglicht dem Reader das Zwischenspeichern von Streaming-Inhalten.</span><span class="sxs-lookup"><span data-stu-id="078f9-122">The first method enables the reader to cache streamed content.</span></span> <span data-ttu-id="078f9-123">Die zweite Option ermöglicht insbesondere die Verwendung von schnellem Cache.</span><span class="sxs-lookup"><span data-stu-id="078f9-123">The second enables the use of Fast Cache in particular.</span></span>

<span data-ttu-id="078f9-124">Mit diesen Einstellungen aktiviert der Reader standardmäßig den schnellen Cache, wenn die Netzwerkbandbreite deutlich höher oder niedriger als die Bitrate des Inhalts ist und der Server diese unterstützt.</span><span class="sxs-lookup"><span data-stu-id="078f9-124">With these settings, the reader will activate Fast Cache by default if the network bandwidth is significantly higher or lower than the bit rate of the content, and if the server supports it.</span></span> <span data-ttu-id="078f9-125">Der Benutzer kann auch steuern, ob das Reader-Objekt einen schnellen Cache verwendet, indem er einen oder mehrere der folgenden modifiziererer zur URL hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="078f9-125">The user can also control whether the reader object uses Fast Cache by adding one or more of the following modifiers to the URL.</span></span>



| <span data-ttu-id="078f9-126">Modifizierer</span><span class="sxs-lookup"><span data-stu-id="078f9-126">Modifier</span></span>         | <span data-ttu-id="078f9-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="078f9-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="078f9-128">WMCache</span><span class="sxs-lookup"><span data-stu-id="078f9-128">WMCache</span></span>          | <span data-ttu-id="078f9-129">Wenn dieser Modifizierer vorhanden ist, deaktiviert der Wert ' 0 ' explizit den schnellen Cache, während der Wert ' 1 ' dies explizit ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="078f9-129">If this modifier is present, the value '0' explicitly disables Fast Cache, while the value '1' explicitly enables it.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="078f9-130">WMBitrate</span><span class="sxs-lookup"><span data-stu-id="078f9-130">WMBitrate</span></span>        | <span data-ttu-id="078f9-131">Dieser Modifizierer gibt die maximale Bitrate vom Server an.</span><span class="sxs-lookup"><span data-stu-id="078f9-131">This modifier specifies the maximum bit rate from the server.</span></span> <span data-ttu-id="078f9-132">Dieser Modifizierer kann verwendet werden, um den schnellen Cache auf eine bestimmte Bandbreitenbeschränkung zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="078f9-132">This modifier can be used to restrict Fast Cache to a certain bandwidth limit.</span></span> <span data-ttu-id="078f9-133">Dieser Modifizierer wird ignoriert, wenn eine explizite Verbindungs Bandbreite bereits mit einem [**callmreadernetworkconfig:: setconnectionbandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth)-Befehl festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="078f9-133">This modifier is ignored if an explicit connection bandwidth is already set with a call to [**IWMReaderNetworkConfig::SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span></span> |
| <span data-ttu-id="078f9-134">WMContentBitrate</span><span class="sxs-lookup"><span data-stu-id="078f9-134">WMContentBitrate</span></span> | <span data-ttu-id="078f9-135">Dieser Modifizierer gibt die Bitrate für den Inhalt an.</span><span class="sxs-lookup"><span data-stu-id="078f9-135">This modifier specifies the bit rate for the content.</span></span> <span data-ttu-id="078f9-136">Der Reader verwendet diesen Modifizierer, falls vorhanden, wenn er Datenströme aus einer MBR-Datei (Multiple Bitrate) auswählt.</span><span class="sxs-lookup"><span data-stu-id="078f9-136">The reader uses this modifier, if present, when it selects streams from a multiple bit rate (MBR) file.</span></span> <span data-ttu-id="078f9-137">Dies kann dazu führen, dass der Leser mit hoher Bitrate Inhalte über eine langsame Verbindung empfängt, was zu sehr langen Pufferzeiten und Verzögerungen führt.</span><span class="sxs-lookup"><span data-stu-id="078f9-137">This can cause the reader to receive high bit rate content over a slow connection, which results in very long buffering times and delays.</span></span>                                          |



 

<span data-ttu-id="078f9-138">Der Modifizierer WMCache = 1 erzwingt, dass der Reader schnelles Cache Streaming verwendet, unabhängig von der Netzwerkbandbreite oder der Bitrate des Inhalts und unabhängig von vorherigen Aufrufen von " **abtenablefastcache**".</span><span class="sxs-lookup"><span data-stu-id="078f9-138">The modifier WMCache=1 forces the reader to use Fast Cache streaming, regardless of the network bandwith or the bit rate of the content and regardless of any previous calls to **SetEnableFastCache**.</span></span> <span data-ttu-id="078f9-139">Allerdings wird die Einstellung **setenablecontentcaching** für den Reader nicht überschrieben. Außerdem wird die Serverkonfiguration nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="078f9-139">However, it does not override the **SetEnableContentCaching** setting on the reader; nor does it override the server configuration.</span></span>

<span data-ttu-id="078f9-140">URL-Modifizierer haben folgende Form:</span><span class="sxs-lookup"><span data-stu-id="078f9-140">URL modifiers have the following form:</span></span>

<span data-ttu-id="078f9-141">*URL*? *Modifizierer* = *Wert*</span><span class="sxs-lookup"><span data-stu-id="078f9-141">*url*?*modifier*=*value*</span></span>

<span data-ttu-id="078f9-142">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="078f9-142">For example:</span></span>

<span data-ttu-id="078f9-143">MMS://MyServer/MyVideo.WMV? WMCache = 1</span><span class="sxs-lookup"><span data-stu-id="078f9-143">mms://MyServer/MyVideo.wmv?WMCache=1</span></span>

<span data-ttu-id="078f9-144">Es können mehrere Modifizierer angegeben werden. Verwenden Sie ein kaufmännisches und-(&), um Sie zu trennen:</span><span class="sxs-lookup"><span data-stu-id="078f9-144">More than one modifier can specified; use an ampersand (&) to separate them:</span></span>

<span data-ttu-id="078f9-145">MMS://MyServer/MyVideo.WMV? WMCache = 1&WMContentBitrate = (56.000</span><span class="sxs-lookup"><span data-stu-id="078f9-145">mms://MyServer/MyVideo.wmv?WMCache=1&WMContentBitrate=56000</span></span>

 

 




