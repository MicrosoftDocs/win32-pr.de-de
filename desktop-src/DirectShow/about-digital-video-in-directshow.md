---
description: Informationen zu digitalen Videos in DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Informationen zu digitalen Videos in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568028"
---
# <a name="about-digital-video-in-directshow"></a><span data-ttu-id="f672f-103">Informationen zu digitalen Videos in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f672f-103">About Digital Video in DirectShow</span></span>

<span data-ttu-id="f672f-104">Digitale Videos (DV) können von einer DV-Kamera aufgezeichnet, in einer Datei auf dem Computer des Benutzers gespeichert oder mithilfe eines Video Tape Recorder (VTR) auf einem Band gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f672f-104">Digital video (DV) can be captured from a DV camera, stored in a file on the user's computer, or stored on tape using a video tape recorder (VTR).</span></span> <span data-ttu-id="f672f-105">Folglich umfassen die Vorgänge, die eine Anwendung in einem DV-Stream ausführen kann, Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f672f-105">Thus, the operations that an application might perform on a DV stream include:</span></span>

-   <span data-ttu-id="f672f-106">Erfassen Sie Live Videos von einer DV-Kamera.</span><span class="sxs-lookup"><span data-stu-id="f672f-106">Capture live video from a DV camera.</span></span>
-   <span data-ttu-id="f672f-107">Übertragen von DV-Daten vom VTR-Band an den Computer.</span><span class="sxs-lookup"><span data-stu-id="f672f-107">Transmit DV data from VTR tape to the computer.</span></span>
-   <span data-ttu-id="f672f-108">Übertragen von DV-Daten vom Computer an den VTR.</span><span class="sxs-lookup"><span data-stu-id="f672f-108">Transmit DV data from the computer to the VTR.</span></span>
-   <span data-ttu-id="f672f-109">Lesen von DV-Daten aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="f672f-109">Read DV data from a file.</span></span>
-   <span data-ttu-id="f672f-110">Schreiben von DV-Daten in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="f672f-110">Write DV data to a file.</span></span>
-   <span data-ttu-id="f672f-111">Die Audiodatei und das Video in einem DV-Stream.</span><span class="sxs-lookup"><span data-stu-id="f672f-111">Render the audio and video in a DV stream.</span></span>

<span data-ttu-id="f672f-112">DirectShow stellt die folgenden DV-Filter bereit:</span><span class="sxs-lookup"><span data-stu-id="f672f-112">DirectShow provides the following DV filters:</span></span>

-   <span data-ttu-id="f672f-113">[Msdv-Treiber](msdv-driver.md)</span><span class="sxs-lookup"><span data-stu-id="f672f-113">[MSDV Driver](msdv-driver.md).</span></span> <span data-ttu-id="f672f-114">Der msdv-Treiber steuert ein DV-Gerät (z. b. einen Camcorder).</span><span class="sxs-lookup"><span data-stu-id="f672f-114">The MSDV driver controls a DV device, such as a camcorder.</span></span> <span data-ttu-id="f672f-115">Das Gerät weist möglicherweise eine Kamera-Untereinheit und eine VTR-Untereinheit auf. Msdv steuert beide Subeinheiten.</span><span class="sxs-lookup"><span data-stu-id="f672f-115">The device may have a camera subunit and a VTR subunit; MSDV controls both subunits.</span></span> <span data-ttu-id="f672f-116">Der msdv-Treiber wird in Anwendungen als DirectShow-Filter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f672f-116">The MSDV driver appears to applications as a DirectShow filter.</span></span>
-   <span data-ttu-id="f672f-117">[DV-Splitter](dv-splitter-filter.md) Filter.</span><span class="sxs-lookup"><span data-stu-id="f672f-117">[DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="f672f-118">DV-Frames enthalten Audiodateien und Videos im gleichen Frame.</span><span class="sxs-lookup"><span data-stu-id="f672f-118">DV frames contain audio and video in the same frame.</span></span> <span data-ttu-id="f672f-119">Der DV-Splitter Filter extrahiert die Audiodaten und gibt Sie als einen oder zwei Audiostreams aus.</span><span class="sxs-lookup"><span data-stu-id="f672f-119">The DV Splitter filter extracts the audio data and outputs it as one or two audio streams.</span></span> <span data-ttu-id="f672f-120">Die ursprünglichen Daten werden als separater DV-Videostream ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="f672f-120">It outputs the original data as a separate DV video stream.</span></span>
-   <span data-ttu-id="f672f-121">[DV-Video Decoder](dv-video-decoder-filter.md) -Filter.</span><span class="sxs-lookup"><span data-stu-id="f672f-121">[DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span> <span data-ttu-id="f672f-122">Decodiert DV-Video in unkomprimiertes Video.</span><span class="sxs-lookup"><span data-stu-id="f672f-122">Decodes DV video into uncompressed video.</span></span>
-   <span data-ttu-id="f672f-123">[DV-Video Encoder](dv-video-encoder-filter.md) -Filter.</span><span class="sxs-lookup"><span data-stu-id="f672f-123">[DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span> <span data-ttu-id="f672f-124">Codiert unkomprimiertes Video in DV-codiertes Video.</span><span class="sxs-lookup"><span data-stu-id="f672f-124">Encodes uncompressed video to DV-encoded video.</span></span>
-   <span data-ttu-id="f672f-125">[DV-Muxer](dv-muxer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f672f-125">[DV Muxer](dv-muxer-filter.md).</span></span> <span data-ttu-id="f672f-126">Kombiniert einen DV-Videostream mit einem oder zwei Audiostreams, um einen einzelnen verschachtelten DV-Stream zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f672f-126">Combines a DV video stream with one or two audio streams, to create a single interleaved DV stream.</span></span>

<span data-ttu-id="f672f-127">Der DV-Splitter und der DV-Video Decoder arbeiten zusammen.</span><span class="sxs-lookup"><span data-stu-id="f672f-127">The DV Splitter and DV Video Decoder work together.</span></span> <span data-ttu-id="f672f-128">Der Splitter nimmt den verschachtelten Stream und gibt separate Video-und DV-Videostreams aus.</span><span class="sxs-lookup"><span data-stu-id="f672f-128">The splitter takes the interleaved stream and outputs separate audio and DV video streams.</span></span> <span data-ttu-id="f672f-129">Der Decoder konvertiert das DV-Video in ein unkomprimiertes Video.</span><span class="sxs-lookup"><span data-stu-id="f672f-129">The decoder converts the DV video to uncompressed video.</span></span> <span data-ttu-id="f672f-130">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f672f-130">The following image illustrates this process.</span></span>

![DV-Splitter und DV-Decoder](images/dv-filters1.png)

<span data-ttu-id="f672f-132">Der DV-Video Encoder und der DV-Muxer umkehren den Prozess: der Encoder konvertiert unkomprimierte Videos in DV-Video, und das MUX kombiniert Audio-und DV-Videos, um einen einzelnen überlappenden Datenstrom zu erstellen, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f672f-132">The DV Video Encoder and the DV Muxer reverse the process: The encoder converts uncompressed video to DV video, and the mux combines audio and DV video to create a single interleaved stream, as shown in the following diagram.</span></span>

![DV-Encoder und DV-Muxer](images/dv-filters2.png)

## <a name="related-topics"></a><span data-ttu-id="f672f-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f672f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f672f-135">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="f672f-135">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



