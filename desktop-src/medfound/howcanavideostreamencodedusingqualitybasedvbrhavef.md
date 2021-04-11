---
description: Wie kann ein Videostream, der mit einem Qualitäts basierten VBR codiert ist, weniger Frames aufweisen als der ursprüngliche Stream?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: Wie kann ein Videostream, der mit einem Qualitäts basierten VBR codiert ist, weniger Frames aufweisen als der ursprüngliche Stream?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215573"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a><span data-ttu-id="d44c3-103">Wie kann ein Videostream, der mit einem Qualitäts basierten VBR codiert ist, weniger Frames aufweisen als der ursprüngliche Stream?</span><span class="sxs-lookup"><span data-stu-id="d44c3-103">How can a video stream encoded using quality-based VBR have fewer frames than the original stream?</span></span>

<span data-ttu-id="d44c3-104">Die Frame-Anzahl eines codierten Streams kann aus zwei Gründen niedriger sein als die Frame Anzahl der ursprünglichen: doppelte Frames und gelöschte Frames.</span><span class="sxs-lookup"><span data-stu-id="d44c3-104">The frame count of an encoded stream can be lower than the frame count of the original for one of two reasons: duplicate frames and dropped frames.</span></span>

<span data-ttu-id="d44c3-105">Der Encoder erzeugt normalerweise keine Frames, die exakte Duplikate des vorherigen Frames sind.</span><span class="sxs-lookup"><span data-stu-id="d44c3-105">The encoder does not normally produce frames that are exact duplicates of the previous frame.</span></span> <span data-ttu-id="d44c3-106">Wenn Sie ein Beispiel für jeden Frame benötigen (Dies ist z. b. für einige Container erforderlich), können Sie den Encoder so konfigurieren, dass "Dummy"-Frames erzeugt werden, indem Sie die Eigenschaft " [mfpkey \_ producedummyframes](mfpkey-producedummyframesproperty.md) " auf "Variant true" festlegen \_ .</span><span class="sxs-lookup"><span data-stu-id="d44c3-106">If you need to have a sample for every frame (this is required by some containers, for example), you can configure the encoder to produce "dummy" frames by setting the [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="d44c3-107">Der Encoder löscht Frames, wenn er nicht alle Frames codieren kann, ohne den Puffer zu überlaufen.</span><span class="sxs-lookup"><span data-stu-id="d44c3-107">The encoder drops frames when it cannot encode all of the frames without overflowing the buffer.</span></span> <span data-ttu-id="d44c3-108">Verworfene Frames beeinflussen die Qualität des Streams, doppelte Frames nicht.</span><span class="sxs-lookup"><span data-stu-id="d44c3-108">Dropped frames affect the quality of the stream, duplicate frames do not.</span></span>

<span data-ttu-id="d44c3-109">Sie können eine Frame-Statistik aus dem Encoder erhalten, um zu bestimmen, ob Frames gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="d44c3-109">You can get frame statistics from the encoder to determine whether frames have been dropped.</span></span> <span data-ttu-id="d44c3-110">Weitere Informationen finden Sie unter [erhalten von Codierungs Statistiken](gettingencodingstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="d44c3-110">For more information, see [Getting Encoding Statistics](gettingencodingstatistics.md).</span></span>

<span data-ttu-id="d44c3-111">In der Regel verfügen Qualitäts basierte VBR-Streams nur über weniger Frames als das ursprüngliche, wenn es doppelte Frames gibt (da die Bitrate nicht eingeschränkt ist).</span><span class="sxs-lookup"><span data-stu-id="d44c3-111">Typically, quality-based VBR streams will only have fewer frames than the original if there are duplicate frames (because the bit rate is not constrained).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d44c3-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d44c3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d44c3-113">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="d44c3-113">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



