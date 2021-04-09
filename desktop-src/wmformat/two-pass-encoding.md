---
title: Two-Pass Codierung
description: Two-Pass Codierung
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media-Format-SDK, Two-Pass-Codierung
- Windows Media-Format-SDK, 2-Pass-Codierung
- Codecs, Two-Pass-Codierung
- Codecs, 2-Pass-Codierung
- zwei-Pass-Codierung, Informationen
- '2: Codierung, Informationen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036722"
---
# <a name="two-pass-encoding"></a><span data-ttu-id="b70d8-109">Two-Pass Codierung</span><span class="sxs-lookup"><span data-stu-id="b70d8-109">Two-Pass Encoding</span></span>

<span data-ttu-id="b70d8-110">Die zwei-Pass-Codierung ist eine Codierungsmethode, die mit einigen Codecs verfügbar ist, z. b. Windows Media Video 9-Codec</span><span class="sxs-lookup"><span data-stu-id="b70d8-110">Two-pass encoding is an encoding method available with some codecs, like the Windows Media Video 9 codec.</span></span> <span data-ttu-id="b70d8-111">Wenn Sie die zwei-Pass-Codierung verwenden, verarbeitet der Codec alle Beispiele für den Stream zweimal.</span><span class="sxs-lookup"><span data-stu-id="b70d8-111">When you use two-pass encoding, the codec processes all of the samples for the stream twice.</span></span> <span data-ttu-id="b70d8-112">Beim ersten Durchlauf sammelt der Codec Informationen zum Inhalt des Streams.</span><span class="sxs-lookup"><span data-stu-id="b70d8-112">On the first pass, the codec gathers information about the content of the stream.</span></span> <span data-ttu-id="b70d8-113">Beim zweiten Durchlauf verwendet der Codec die Informationen, die beim ersten Durchlauf gesammelt werden, um den Codierungsprozess für den Datenstrom zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="b70d8-113">On the second pass, the codec uses the information gathered on the first pass to optimize the encoding process for the stream.</span></span>

<span data-ttu-id="b70d8-114">Im konstanten Bitrate-Codierungs Modus sind Dateien, die in zwei Durchläufen codiert sind, im Allgemeinen effizienter als Dateien, die in einem einzelnen Durchlauf codiert sind.</span><span class="sxs-lookup"><span data-stu-id="b70d8-114">In the Constant Bit Rate encoding mode, files that are encoded in two passes are generally more efficient than files encoded in a single pass.</span></span> <span data-ttu-id="b70d8-115">Bei der Qualitäts basierten VBR, bei der es sich um einen Durchlauf handelt, wird eine konsistentere Qualität erzielt als bei einem Bitrate-basierten VBR, der zwei Pass ist.</span><span class="sxs-lookup"><span data-stu-id="b70d8-115">Quality-based VBR, which is one pass, produces more consistent quality than bit-rate-based VBR, which is two-pass.</span></span>

<span data-ttu-id="b70d8-116">Sie können keine zwei-Pass-Codierung für Livestreams verwenden.</span><span class="sxs-lookup"><span data-stu-id="b70d8-116">You cannot use two-pass encoding on live streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b70d8-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b70d8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b70d8-118">**Codec-Features**</span><span class="sxs-lookup"><span data-stu-id="b70d8-118">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="b70d8-119">**Verwenden von Two-Pass Codierung**</span><span class="sxs-lookup"><span data-stu-id="b70d8-119">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




