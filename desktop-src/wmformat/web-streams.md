---
title: Webstreams
description: Webstreams
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows Media-Format-SDK, Webstreams
- Advanced Systems Format (ASF), Webstreams
- ASF (Advanced Systems Format), Webstreams
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Webstreams, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036891"
---
# <a name="web-streams"></a><span data-ttu-id="3cddf-110">Webstreams</span><span class="sxs-lookup"><span data-stu-id="3cddf-110">Web Streams</span></span>

<span data-ttu-id="3cddf-111">Ein Webstream ist wie ein Dateistream, in dem er Datendateien enthält.</span><span class="sxs-lookup"><span data-stu-id="3cddf-111">A Web stream is like a file stream in that it contains data files.</span></span> <span data-ttu-id="3cddf-112">In einem Webstream sind diese Dateien in der Regel HTML-Seiten und zugehörige Grafiken im GIF-oder JPEG-Format.</span><span class="sxs-lookup"><span data-stu-id="3cddf-112">In a Web stream, these files are typically HTML pages and associated graphics in GIF or JPEG format.</span></span>

<span data-ttu-id="3cddf-113">Webstreams können besonders nützlich für ASF-Dateien sein, die als Präsentationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3cddf-113">Web streams can be particularly useful for ASF files that are used as presentations.</span></span> <span data-ttu-id="3cddf-114">Vor der Unterstützung von Webstreams hätten Präsentationen URLs in Skript Datenströmen innerhalb einer Datei, damit eine Webseite zu einem vordefinierten Zeitpunkt geladen wird.</span><span class="sxs-lookup"><span data-stu-id="3cddf-114">Prior to the support of Web streams, presentations would have URLs in script streams within a file so that a Web page would load at a predetermined time.</span></span> <span data-ttu-id="3cddf-115">Die Schwierigkeit bestand darin, dass die Netzwerk Überlastung Verzögerungen verursachen könnte und eine schlechte Anzeige der Anzeige Leistung zur Folge hat.</span><span class="sxs-lookup"><span data-stu-id="3cddf-115">The difficulty was that network congestion could cause delays and create a poor viewing experience.</span></span>

<span data-ttu-id="3cddf-116">Bei Webstreams können die Bestandteile von Webseiten in der ASF-Datei als Datenstrom enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3cddf-116">With Web streams, the constituent parts of Web pages can be included in the ASF file as a stream.</span></span> <span data-ttu-id="3cddf-117">Wenn die Dateien empfangen werden, können Sie zwischengespeichert werden, sodass, wenn der Befehl zum Anzeigen (oder Rendering) einer URL zugestellt wird, sofort ein Browser darauf zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="3cddf-117">As the files are received, they can be cached so that, when the command to display (or render) a URL is delivered, they can be instantly accessed by a browser.</span></span> <span data-ttu-id="3cddf-118">Dies ermöglicht eine reibungslose, konsistente Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="3cddf-118">This enables smooth, consistent playback.</span></span> <span data-ttu-id="3cddf-119">Der Rendering-Befehl wird im Webstream selbst übermittelt, nicht als Skript Befehl in einem separaten Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="3cddf-119">The render command is delivered in the Web stream itself, not as a script command in a separate stream.</span></span>

<span data-ttu-id="3cddf-120">Es wird empfohlen, dass Webstreams, die mithilfe des SDK der Windows Media-Serie 9 oder höher erstellt wurden, die Versionsnummer 1 erhalten.</span><span class="sxs-lookup"><span data-stu-id="3cddf-120">It is recommended that Web streams created by using the Windows Media Format 9 Series SDK, or later be given the version number 1.</span></span> <span data-ttu-id="3cddf-121">Dieser Wert wird in der [**WMT- \_ Webstream- \_ Format**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) Struktur im **wversion** -Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="3cddf-121">This value is specified in the [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure in the **wVersion** member.</span></span> <span data-ttu-id="3cddf-122">Das SDK selbst führt keine Aktion aus, um diese Version zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="3cddf-122">The SDK itself does nothing to enforce this version.</span></span>

> [!Note]  
> <span data-ttu-id="3cddf-123">Beim Herstellen einer Verbindung mit Live Broadcast Datenströmen, die über Webstreams verfügen, kann der Benutzer möglicherweise einen Rendering-Befehl erhalten, bevor sich die angegebene Datei tatsächlich im lokalen Cache befindet.</span><span class="sxs-lookup"><span data-stu-id="3cddf-123">When connecting to live broadcast streams that have Web streams, it is possible that the user may receive a render command before the specified file is actually in the local cache.</span></span> <span data-ttu-id="3cddf-124">Wenn die Anwendung diese Bedingung nicht erfüllt, wird im Browser der Fehler "Seite nicht gefunden" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3cddf-124">Unless your application handles this condition, the browser will display a "Page not found" error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3cddf-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cddf-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cddf-126">**Beliebige Streams**</span><span class="sxs-lookup"><span data-stu-id="3cddf-126">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="3cddf-127">**Konfigurieren von Webstreams**</span><span class="sxs-lookup"><span data-stu-id="3cddf-127">**Configuring Web Streams**</span></span>](configuring-web-streams.md)
</dt> </dl>

 

 




