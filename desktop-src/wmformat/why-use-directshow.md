---
title: Gründe für die Verwendung von DirectShow
description: Gründe für die Verwendung von DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Hardware
- Windows Media-Format-SDK, Windows-Treibermodell (WDM)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Hardware
- ASF (Advanced Systems Format), Hardware
- Advanced Systems Format (ASF), Windows-Treibermodell (WDM)
- ASF (Advanced Systems Format), Windows-Treibermodell (WDM)
- DirectShow, Informationen
- DirectShow, Hardware
- DirectShow, Windows-Treibermodell (WDM)
- Windows-Treibermodell (WDM)
- WDM (Windows-Treibermodell)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710373"
---
# <a name="why-use-directshow"></a><span data-ttu-id="f9cde-117">Gründe für die Verwendung von DirectShow</span><span class="sxs-lookup"><span data-stu-id="f9cde-117">Why Use DirectShow?</span></span>

<span data-ttu-id="f9cde-118">Es gibt zwei Hauptgründe, warum eine Anwendung DirectShow anstelle des Windows Media Format SDK direkt verwenden kann: aus Gründen der Bedienung der DirectShow-streamingarchitektur und für den Zugriff auf die Hardware.</span><span class="sxs-lookup"><span data-stu-id="f9cde-118">There are two main reasons why an application might use DirectShow rather than the Windows Media Format SDK directly: for the convenience of the DirectShow streaming architecture, and for access to hardware.</span></span>

## <a name="convenience"></a><span data-ttu-id="f9cde-119">Komfort</span><span class="sxs-lookup"><span data-stu-id="f9cde-119">Convenience</span></span>

<span data-ttu-id="f9cde-120">Mit der DirectShow-streamingarchitektur werden nur einige Methodenaufrufe zum Abspielen von Windows Media Audio-oder Windows Media Video Dateien benötigt.</span><span class="sxs-lookup"><span data-stu-id="f9cde-120">With DirectShow streaming architecture, it takes only a few method calls to play Windows Media Audio or Windows Media Video files.</span></span> <span data-ttu-id="f9cde-121">Das Erstellen von Dateien wird ebenfalls vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f9cde-121">Creating files is also simplified.</span></span> <span data-ttu-id="f9cde-122">Sie geben einfach ein Profil mithilfe der **iconfigasfwriter** -Schnittstelle für den Filter an, und DirectShow lädt automatisch die erforderlichen Komponenten zum Rendern oder Schreiben der Streams und stellt die Mechanismen für die Übertragung und Synchronisierung des Datenflusses von Mediendaten bereit.</span><span class="sxs-lookup"><span data-stu-id="f9cde-122">You simply specify a profile using the **IConfigAsfWriter** interface on the filter, and DirectShow automatically loads the required components for rendering or writing the streams, and provides the mechanisms for transferring and synchronizing the flow of media data.</span></span> <span data-ttu-id="f9cde-123">DirectShow ist besonders nützlich, wenn Inhalte aus verschiedenen Formaten in das Windows Media-Format umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="f9cde-123">DirectShow is especially useful when converting content from varied formats into Windows Media Format.</span></span> <span data-ttu-id="f9cde-124">Sie können DirectShow-Filter Diagramme erstellen, die eine Vielzahl von Datei-und Komprimierungs Typen decodieren, und dann die decodierten Streams in den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter einblenden.</span><span class="sxs-lookup"><span data-stu-id="f9cde-124">You can create DirectShow filter graphs that decode a wide variety of file and compression types, and then feed the decoded streams into the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span> <span data-ttu-id="f9cde-125">Im Vergleich dazu funktioniert das uncompavitowmv-Beispiel in diesem SDK nur mit nicht komprimierten AVI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="f9cde-125">By comparison, the UncompAVItoWMV sample in this SDK works only with uncompressed AVI files.</span></span> <span data-ttu-id="f9cde-126">Textstreams und beliebige Datenströme können auch über DirectShow erstellt und/oder gerendert werden. Dies erfordert jedoch möglicherweise die Erstellung benutzerdefinierter DirectShow-Filter für die Verarbeitung dieser Streams.</span><span class="sxs-lookup"><span data-stu-id="f9cde-126">Text streams and arbitrary data streams can also be created and/or rendered through DirectShow, but this might require you to create custom DirectShow filters for processing those streams.</span></span>

## <a name="access-to-hardware"></a><span data-ttu-id="f9cde-127">Zugriff auf Hardware</span><span class="sxs-lookup"><span data-stu-id="f9cde-127">Access to Hardware</span></span>

<span data-ttu-id="f9cde-128">DirectShow ist die einzige Möglichkeit für den Anwendungscode, auf Windows-Treibermodell (WDM) – basierte Hardware Geräte wie 1394 DV-Kameras, TV-Tuners und USB-Webcams zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f9cde-128">DirectShow is the only way for application code to access Windows Driver Model (WDM)–based hardware devices such as 1394 DV cameras, TV tuners, and USB webcams.</span></span> <span data-ttu-id="f9cde-129">Wenn Ihre Anwendung Daten direkt von einem WDM-basierten Hardware Gerät erfassen und in das Windows Media-Format transcodieren muss und das Windows Media Encoder SDK nicht Ihren Anforderungen entspricht, ist DirectShow die einzige Alternative.</span><span class="sxs-lookup"><span data-stu-id="f9cde-129">If your application must capture data directly from a WDM-based hardware device and transcode it to Windows Media Format, and the Windows Media Encoder SDK does not suit your needs, then DirectShow is the only alternative.</span></span> <span data-ttu-id="f9cde-130">DirectShow kann auch für den Zugriff auf ältere Geräte auf der Grundlage von Video für Windows verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9cde-130">DirectShow can also be used to access legacy devices based on Video for Windows.</span></span>

 

 




