---
description: Medien Beispiele
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Medien Beispiele (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e10df770f0edcdcb329cf8d2bda3d3dc46acbf6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961169"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="26ca8-103">Medien Beispiele (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="26ca8-103">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="26ca8-104">Ein Medien Beispiel ist ein Objekt, das eine geordnete Liste von 0 (null) oder mehr Puffern enthält.</span><span class="sxs-lookup"><span data-stu-id="26ca8-104">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="26ca8-105">In Medien Beispielen wird die [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="26ca8-105">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="26ca8-106">Die Datenmenge, die in einem Beispiel enthalten ist, hängt von der Komponente ab, die das Beispiel erstellt, und von der Art der Daten in den Puffern.</span><span class="sxs-lookup"><span data-stu-id="26ca8-106">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="26ca8-107">Für nicht komprimierte Videos enthält ein Beispiel normalerweise einen einzelnen Videoframe.</span><span class="sxs-lookup"><span data-stu-id="26ca8-107">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="26ca8-108">Für nicht komprimierte Audiodaten kann die Datenmenge variieren, aber in der Regel umfasst ein audioframe nicht zwei Beispiele.</span><span class="sxs-lookup"><span data-stu-id="26ca8-108">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="26ca8-109">Bei komprimierten Daten werden diese Richtlinien möglicherweise nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="26ca8-109">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="26ca8-110">Eine einzelne Stichprobe kann aus Gründen der Effizienz mehrere Puffer enthalten.</span><span class="sxs-lookup"><span data-stu-id="26ca8-110">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="26ca8-111">Beispielsweise wird in einer ASF-Datei ein videaframe häufig zwischen mehreren ASF-Paketen verteilt.</span><span class="sxs-lookup"><span data-stu-id="26ca8-111">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="26ca8-112">Die Medienquelle liest die Pakete möglicherweise in mehrere Puffer.</span><span class="sxs-lookup"><span data-stu-id="26ca8-112">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="26ca8-113">Anstatt jedes Fragment in einen Puffer zu kopieren, platziert die Quelle einfach alle Puffer in eine Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="26ca8-113">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="26ca8-114">Downstreamkomponenten können dann entscheiden, ob die kleineren Puffer in einen zusammenhängenden Puffer kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="26ca8-114">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="26ca8-115">Wenn Sie eine Pipeline Komponente schreiben, sollten Sie in der Regel davon ausgehen, dass jede Stichprobe mehr als einen Puffer enthalten könnte.</span><span class="sxs-lookup"><span data-stu-id="26ca8-115">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="26ca8-116">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="26ca8-116">This section contains the following topics.</span></span>



| <span data-ttu-id="26ca8-117">Thema</span><span class="sxs-lookup"><span data-stu-id="26ca8-117">Topic</span></span>                                                        | <span data-ttu-id="26ca8-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26ca8-118">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26ca8-119">Arbeiten mit Medien Beispielen</span><span class="sxs-lookup"><span data-stu-id="26ca8-119">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="26ca8-120">Beschreibt das allgemeine Verhalten von Medien Beispielen.</span><span class="sxs-lookup"><span data-stu-id="26ca8-120">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="26ca8-121">Video Beispiele</span><span class="sxs-lookup"><span data-stu-id="26ca8-121">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="26ca8-122">Beschreibt eine spezialisierte Implementierung von [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , die für die Aufnahme nicht komprimierter Video Frames konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="26ca8-122">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="26ca8-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26ca8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ca8-124">Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="26ca8-124">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="26ca8-125">Media Foundation primitiver</span><span class="sxs-lookup"><span data-stu-id="26ca8-125">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



