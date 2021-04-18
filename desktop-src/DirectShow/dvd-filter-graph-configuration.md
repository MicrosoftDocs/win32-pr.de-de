---
description: Konfiguration des DVD-Filter Diagramms
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Konfiguration des DVD-Filter Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522403"
---
# <a name="dvd-filter-graph-configuration"></a><span data-ttu-id="2ecb7-103">Konfiguration des DVD-Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="2ecb7-103">DVD Filter Graph Configuration</span></span>

<span data-ttu-id="2ecb7-104">In diesem Abschnitt werden die verschiedenen Filter Diagramm Konfigurationen für die DVD-Wiedergabe in DirectShow beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-104">This section describes the various filter graph configurations for DVD playback in DirectShow.</span></span> <span data-ttu-id="2ecb7-105">Diese Diagramme werden hauptsächlich zur Referenz bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-105">These diagrams are provided mainly for reference.</span></span> <span data-ttu-id="2ecb7-106">Der DVD-Navigator erstellt das Diagramm. im Allgemeinen ist es nicht notwendig, die Details der Konfiguration des Diagramms zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-106">The DVD Navigator builds the graph, so in general it is not necessary to understand the details of how the graph is configured.</span></span> <span data-ttu-id="2ecb7-107">Weitere Informationen finden Sie unter [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="2ecb7-107">For more information, see [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).</span></span>

<span data-ttu-id="2ecb7-108">Die folgende Abbildung zeigt ein DVD-Filter Diagramm mit einem Software Decoder.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-108">The following illustration shows a DVD filter graph with a software decoder.</span></span>

![DVD-Filter Diagramm für Windows XP](images/dvd-graph-xp.png)

<span data-ttu-id="2ecb7-110">Wenn ein Hardware Decoder vorhanden ist, wird er normalerweise direkt mit der Grafikkarte von einem Videoport verbunden.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-110">When a hardware decoder is present, it is typically connected directly to the video card by a video port.</span></span> <span data-ttu-id="2ecb7-111">Dadurch können die decodierten Video Bits direkt an den Frame Puffer auf der Grafikkarte gesendet werden, ohne in den Host Speicher zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-111">This enables the decoded video bits to be sent directly to the frame buffer on the graphics card without passing into host memory.</span></span> <span data-ttu-id="2ecb7-112">Um diese direkte Verbindung unter früheren Versionen von Windows zu verwalten, unterstützt DirectShow DirectDraw Video Port Extensions (VPE) über eine Schnittstelle auf dem [Überlagerungs-Mischungs Filter](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2ecb7-112">To manage this direct connection on earlier versions of Windows, DirectShow supports DirectDraw Video Port Extensions (VPE) through an interface on the [Overlay Mixer Filter](overlay-mixer-filter.md).</span></span>

> [!Note]  
> <span data-ttu-id="2ecb7-113">Der Überlagerungs-Mixer ist nun veraltet.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-113">The Overlay Mixer is now deprecated.</span></span>

 

<span data-ttu-id="2ecb7-114">In Windows XP und höher kann ein Hardware Decoder eine Verbindung mit dem [Video Port-Manager](video-port-manager.md) -Filter herstellen.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-114">In Windows XP and later, a hardware decoder can connect to the [Video Port Manager](video-port-manager.md) filter.</span></span>

![DVD-Diagramm für Windows XP mit einem Hardware Decoder](images/dvd-hwgraph-xp.png)

<span data-ttu-id="2ecb7-116">In allen diesen Diagrammen ist der DVD-Navigator der Quell Filter. Er führt mehrere Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="2ecb7-116">In all these graphs, the DVD Navigator is the source filter; it performs several tasks:</span></span>

-   <span data-ttu-id="2ecb7-117">Liest die Navigations-und Videodaten von der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-117">Reads the navigation and video data from the disc.</span></span>
-   <span data-ttu-id="2ecb7-118">Demultiplexe der Video-, Audio-und Teil Bilddaten in separate Streams.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-118">Demultiplexes the video, audio, and subpicture data into separate streams.</span></span>
-   <span data-ttu-id="2ecb7-119">Pumpt die Streams zur weiteren Verarbeitung und zum endgültigen Rendering in das Diagramm.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-119">Pumps the streams into the graph for further processing and eventual rendering.</span></span>
-   <span data-ttu-id="2ecb7-120">Informiert ihre Anwendung über DVD-bezogene Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-120">Informs your application of DVD-related events.</span></span>

<span data-ttu-id="2ecb7-121">Im Audiostream stellt der DVD-Navigator eine Downstream-Verbindung mit einem Audiodecoder her, der eine Verbindung mit dem [DirectSound-rendererfilter](directsound-renderer-filter.md)herstellt, dem Standardaudiorenderer.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-121">On the audio stream, the DVD Navigator connects downstream to an audio decoder, which connects to the [DirectSound Renderer Filter](directsound-renderer-filter.md), the default audio renderer.</span></span> <span data-ttu-id="2ecb7-122">In den Video-und subbildstreams sind die downstreamfilter der Video Decoder von Drittanbietern und der Video Mischungs-Renderer (oder der [Überlagerungs-Mixer](overlay-mixer-filter.md)und der [Videorenderer](video-renderer-filter.md) bei Anwendungen mit kompatible).</span><span class="sxs-lookup"><span data-stu-id="2ecb7-122">On the video and subpicture streams, the downstream filters are the third-party video decoder, and the Video Mixing Renderer (or the [Overlay Mixer](overlay-mixer-filter.md), and the [Video Renderer](video-renderer-filter.md) on downlevel applications).</span></span> <span data-ttu-id="2ecb7-123">Wenn die Anwendung die von Closed unterteilten Daten in Zeile 21 behandelt, müssen Sie den Filter DirectShow Line 21 Decoder 2 dem Diagramm hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-123">If your application will handle line 21 closed-captioned data, you must add the DirectShow Line 21 Decoder 2 filter to the graph.</span></span> <span data-ttu-id="2ecb7-124">Dies umfasst einen einzelnen Methoden aufzurufen. der Filter wird automatisch verbunden.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-124">This involves a single method call; the filter will be connected automatically.</span></span>

<span data-ttu-id="2ecb7-125">Ihre Anwendung kommuniziert mit und steuert den DVD-Navigator über die benutzerdefinierten Schnittstellen, die der DVD-Navigator verfügbar macht: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)– die "Set"-Methoden – und [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)– die "Get"-Methoden.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-125">Your application communicates with and controls the DVD Navigator through the custom interfaces that the DVD Navigator exposes: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)—the "set" methods—and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)—the "get" methods.</span></span> <span data-ttu-id="2ecb7-126">Außerdem muss Sie mit dem Filter Graph-Manager (über [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) kommunizieren, um das Diagramm zu starten, zu starten und anderweitig zu steuern.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-126">It also must communicate with the filter graph manager (through [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) to stop, start, and otherwise control the graph.</span></span> <span data-ttu-id="2ecb7-127">Möglicherweise müssen Sie auch andere einzelne Filter steuern, z. b. den Überlagerungs Filter Filter zum Wechseln zwischen Fenster-und voll Bild Anzeige.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-127">You might also need to control other individual filters, such as the Overlay Mixer filter for switching between windowed and full-screen display.</span></span> <span data-ttu-id="2ecb7-128">Weitere Informationen finden Sie unter [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span><span class="sxs-lookup"><span data-stu-id="2ecb7-128">For more information, see [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span></span> <span data-ttu-id="2ecb7-129">Die genaue Konfiguration des Diagramms variiert abhängig davon, welche Art von MPEG-2-Decoder Sie installiert haben, ob Sie die von Closed beschrifteten Zeilen 21 und anderen Faktoren verarbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-129">The exact configuration of the graph will vary depending on what type of MPEG-2 decoder you have installed, whether you need to handle line 21 closed-captioned data, and other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ecb7-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2ecb7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ecb7-131">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="2ecb7-131">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



