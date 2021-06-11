---
description: Erfahren Sie mehr über Medienbeispiele in Microsoft Media Foundation. Ein Medienbeispiel ist ein Objekt, das eine sortierte Liste von null oder mehr Puffern enthält.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Medienbeispiele (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5d29b11fb6db316e3fbf6e33e24218ddbbf062
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989155"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="07603-104">Medienbeispiele (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="07603-104">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="07603-105">Ein Medienbeispiel ist ein Objekt, das eine sortierte Liste von null oder mehr Puffern enthält.</span><span class="sxs-lookup"><span data-stu-id="07603-105">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="07603-106">Medienbeispiele machen die [**INTERFACESSample-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07603-106">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="07603-107">Die Menge der in einem Beispiel enthaltenen Daten hängt von der Komponente ab, die das Beispiel erstellt, und vom Typ der Daten in den Puffern.</span><span class="sxs-lookup"><span data-stu-id="07603-107">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="07603-108">Für nicht komprimierte Videos enthält ein Beispiel in der Regel einen einzelnen Videoframe.</span><span class="sxs-lookup"><span data-stu-id="07603-108">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="07603-109">Bei unkomprimierten Audiodaten kann die Datenmenge variieren, aber in der Regel umfasst ein Audioframe nicht zwei Beispiele.</span><span class="sxs-lookup"><span data-stu-id="07603-109">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="07603-110">Für komprimierte Daten gelten diese Richtlinien möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="07603-110">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="07603-111">Ein einzelnes Beispiel kann aus Effizienzgründen mehrere Puffer enthalten.</span><span class="sxs-lookup"><span data-stu-id="07603-111">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="07603-112">Beispielsweise wird ein Videoframe in einer ASF-Datei häufig auf mehrere ASF-Pakete verteilt.</span><span class="sxs-lookup"><span data-stu-id="07603-112">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="07603-113">Die Medienquelle liest die Pakete möglicherweise in mehrere Puffer.</span><span class="sxs-lookup"><span data-stu-id="07603-113">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="07603-114">Anstatt jedes Fragment in einen Puffer zu kopieren, fügt die Quelle einfach alle Puffer in ein Beispiel ein.</span><span class="sxs-lookup"><span data-stu-id="07603-114">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="07603-115">Downstreamkomponenten können dann entscheiden, ob die kleineren Puffer in einen zusammenhängenden Puffer kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07603-115">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="07603-116">Wenn Sie eine Pipelinekomponente schreiben, sollten Sie im Allgemeinen davon ausgehen, dass jedes Beispiel mehrere Puffer enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="07603-116">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="07603-117">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="07603-117">This section contains the following topics.</span></span>



| <span data-ttu-id="07603-118">Thema</span><span class="sxs-lookup"><span data-stu-id="07603-118">Topic</span></span>                                                        | <span data-ttu-id="07603-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07603-119">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07603-120">Arbeiten mit Medienbeispielen</span><span class="sxs-lookup"><span data-stu-id="07603-120">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="07603-121">Beschreibt das allgemeine Verhalten von Medienbeispielen.</span><span class="sxs-lookup"><span data-stu-id="07603-121">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="07603-122">Videobeispiele</span><span class="sxs-lookup"><span data-stu-id="07603-122">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="07603-123">Beschreibt eine spezielle Implementierung von [**SPECIALIZEDSample,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) die für die Aufnahme von unkomprimierten Videoframes entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="07603-123">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="07603-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07603-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07603-125">Medienpuffer</span><span class="sxs-lookup"><span data-stu-id="07603-125">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="07603-126">Media Foundation Primitive</span><span class="sxs-lookup"><span data-stu-id="07603-126">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



