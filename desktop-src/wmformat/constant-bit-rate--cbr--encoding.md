---
title: Codierung mit konstanter Bitrate (CBR)
description: Codierung mit konstanter Bitrate (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media-Format-SDK, CBR-Codierung
- Windows Media-Format-SDK, Konstante Bitrate (CBR)
- Codecs, CBR-Codierung
- Codecs, Konstante Bitrate (CBR)
- Konstante Bitrate (CBR)
- CBR (Konstante Bitrate)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388658"
---
# <a name="constant-bit-rate-cbr-encoding"></a><span data-ttu-id="e36e3-109">Codierung mit konstanter Bitrate (CBR)</span><span class="sxs-lookup"><span data-stu-id="e36e3-109">Constant Bit Rate (CBR) Encoding</span></span>

<span data-ttu-id="e36e3-110">Bei der Codierung mit konstanter Bitrate (CBR) handelt es sich um die Standard Codierungsmethode mit dem Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="e36e3-110">Constant bit rate (CBR) encoding is the default method of encoding with the Windows Media Format SDK.</span></span> <span data-ttu-id="e36e3-111">Wenn Sie die CBR-Codierung verwenden, geben Sie die Zielbitrate für einen Datenstrom an, und der Codec verwendet die erforderliche Komprimierung, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="e36e3-111">When using CBR encoding, you specify the target bit rate for a stream, and the codec uses whatever amount of compression is necessary to achieve it.</span></span>

<span data-ttu-id="e36e3-112">Bei der CBR-Codierung sind die Bitrate und die Größe des codierten Streams vor der Codierung bekannt.</span><span class="sxs-lookup"><span data-stu-id="e36e3-112">With CBR encoding the bit rate and size of the encoded stream are known prior to encoding.</span></span> <span data-ttu-id="e36e3-113">Wenn Sie z. b. einen dreiminütigen Titel bei 32.000 Bits pro Sekunde codieren, wissen Sie, dass die Dateigröße ungefähr 704 Kilobyte beträgt (32.000 Bit/s = 180 Sekunden/8 Bits pro Byte/1.024).</span><span class="sxs-lookup"><span data-stu-id="e36e3-113">For example, if you are encoding a three minute song at 32,000 bits per second, you know that the file size will be about 704 kilobytes (32,000 bps x 180 seconds / 8 bits per byte / 1,024).</span></span> <span data-ttu-id="e36e3-114">Sie wissen auch, dass die Bandbreite, die zum Streamen des codierten Inhalts erforderlich ist, ungefähr 32.000 Bits pro Sekunde beträgt.</span><span class="sxs-lookup"><span data-stu-id="e36e3-114">You also know that the bandwidth required to stream the encoded content is about 32,000 bits per second.</span></span>

<span data-ttu-id="e36e3-115">Bei der Codierung mit eingeschränkter Variablen Bitrate (im folgenden Abschnitt beschrieben) können Sie auch die Bitrate vor der Codierung ermitteln. da die Rate jedoch variabel ist, kann die resultierende Datei nicht so effizient wie eine im CBR-Modus codierte Datei gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="e36e3-115">Constrained variable bit rate encoding (described in the following section) also enables you to know the bit rate prior to encoding, but since the rate is variable, the resulting file cannot be streamed as efficiently as a file encoded in CBR mode.</span></span> <span data-ttu-id="e36e3-116">Mit CBR bleibt die Bitrate im Lauf der Zeit immer in der Nähe der durchschnittlichen oder Zielbitrate, und die Menge an Variation kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e36e3-116">With CBR, the bit rate over time always remains close to the average or target bit rate, and the amount of variation can be specified.</span></span>

<span data-ttu-id="e36e3-117">Der Nachteil der CBR-Codierung besteht darin, dass die Qualität des codierten Inhalts nicht konstant ist.</span><span class="sxs-lookup"><span data-stu-id="e36e3-117">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="e36e3-118">Da es schwieriger ist, Inhalte zu komprimieren, sind Teile eines CBR-Streams von geringerer Qualität als andere.</span><span class="sxs-lookup"><span data-stu-id="e36e3-118">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="e36e3-119">Ein typischer Film hat z. b. einige Szenen, die relativ statisch sind, und einige Szenen, die vollständig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e36e3-119">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="e36e3-120">Wenn Sie einen Film mit CBR codieren, sind die Szenen, die statisch und somit einfach zu codieren sind, von höherer Qualität als die Aktions Szenen, die eine effiziente Codierung wesentlich erschweren.</span><span class="sxs-lookup"><span data-stu-id="e36e3-120">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which are much more difficult to encode efficiently.</span></span>

<span data-ttu-id="e36e3-121">Die CBR-Codierung kann auch zu inkonsistenter Qualität von einer Datei zu einer anderen führen.</span><span class="sxs-lookup"><span data-stu-id="e36e3-121">CBR encoding can also result in inconsistent quality from one file to another.</span></span> <span data-ttu-id="e36e3-122">Wenn Sie CBR verwenden, um mehrere Lieder verschiedener Genres mit derselben Bitrate zu codieren, werden Sie möglicherweise einen gewissen Unterschied in der Qualität feststellen.</span><span class="sxs-lookup"><span data-stu-id="e36e3-122">If you use CBR to encode several songs of different genres at the same bit rate, you may notice some difference in quality between them.</span></span>

<span data-ttu-id="e36e3-123">Im Allgemeinen sind Variationen der Qualität einer CBR-Datei in niedrigeren Bitraten deutlicher ausgeprägt.</span><span class="sxs-lookup"><span data-stu-id="e36e3-123">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="e36e3-124">Bei höheren Bitraten variiert die Qualität einer CBR-codierten Datei weiterhin, aber die Qualitätsprobleme sind für den Benutzer weniger bemerkbar.</span><span class="sxs-lookup"><span data-stu-id="e36e3-124">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="e36e3-125">Wenn Sie die CBR-Codierung verwenden, sollten Sie die Bandbreite so hoch festlegen, dass Sie das Liefer Szenario zulässt.</span><span class="sxs-lookup"><span data-stu-id="e36e3-125">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e36e3-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e36e3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e36e3-127">**Auswählen einer Codierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="e36e3-127">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="e36e3-128">**Codec-Features**</span><span class="sxs-lookup"><span data-stu-id="e36e3-128">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="e36e3-129">**Codierung der Variablen Bitrate (VBR)**</span><span class="sxs-lookup"><span data-stu-id="e36e3-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




