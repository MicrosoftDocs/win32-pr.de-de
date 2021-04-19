---
description: Seitenverhältnis Korrektur
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Seitenverhältnis Korrektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342561"
---
# <a name="aspect-ratio-correction"></a><span data-ttu-id="1fc38-103">Seitenverhältnis Korrektur</span><span class="sxs-lookup"><span data-stu-id="1fc38-103">Aspect Ratio Correction</span></span>

<span data-ttu-id="1fc38-104">Dieses Thema gilt für Windows XP Service Pack 2 oder höher.</span><span class="sxs-lookup"><span data-stu-id="1fc38-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="1fc38-105">Im Mischungs Modus wird das Video von VMR auf das richtige Seitenverhältnis fest.</span><span class="sxs-lookup"><span data-stu-id="1fc38-105">In mixing mode, the VMR sizes the video to the correct aspect ratio.</span></span> <span data-ttu-id="1fc38-106">(Ausnahme: siehe [nicht quadratische Vermischung](non-square-mixing.md).) Dies erfordert möglicherweise die Streckung des Videos, wenn das gewünschte Seitenverhältnis nicht mit dem physischen Seitenverhältnis des Bilds identisch ist.</span><span class="sxs-lookup"><span data-stu-id="1fc38-106">(Exception: See [Non-Square Mixing](non-square-mixing.md).) This may require stretching the video if the preferred aspect ratio is not the same as the image's physical aspect ratio.</span></span> <span data-ttu-id="1fc38-107">Das Format Digital Video (DV) lautet z. b. 720 x 480 Pixel (3:2), sollte jedoch mit einem 4:3-Seitenverhältnis angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1fc38-107">For example, digital video (DV) format is 720 x 480 pixels (3:2) but should be displayed at a 4:3 aspect ratio.</span></span>

<span data-ttu-id="1fc38-108">VMR unterstützt zwei verschiedene Verhaltensweisen für die Seitenverhältnis Korrektur:</span><span class="sxs-lookup"><span data-stu-id="1fc38-108">The VMR supports two different behaviors for aspect ratio correction:</span></span>

-   <span data-ttu-id="1fc38-109">Passen Sie die horizontale oder vertikale Größe an, damit das Bild immer gestreckt und nie verkleinert wird.</span><span class="sxs-lookup"><span data-stu-id="1fc38-109">Adjust either the horizontal or vertical size, so that the image is always stretched, never shrunk.</span></span> <span data-ttu-id="1fc38-110">Dies ist nun das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="1fc38-110">This is now the default behavior.</span></span>
-   <span data-ttu-id="1fc38-111">Passen Sie die horizontale Größe an, indem Sie das Video entweder Strecken oder verkleinern.</span><span class="sxs-lookup"><span data-stu-id="1fc38-111">Adjust the horizontal size, either stretching or shrinking the video.</span></span>

<span data-ttu-id="1fc38-112">Da das zweite Verhalten (nur horizontale Anpassung) das Verkleinern des Videos verursachen kann, kann das Ausgabe Bild weniger aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="1fc38-112">Because the second behavior (horizontal adjustment only) may entail shrinking the video, the output image may have less resolution.</span></span> <span data-ttu-id="1fc38-113">Aus diesem Grund wird das erste Verhalten bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="1fc38-113">For this reason, the first behavior is preferred.</span></span> <span data-ttu-id="1fc38-114">Beispielsweise erzeugt das Standardverhalten im Fall von 720 x 480-Video mit 4:3 Seitenverhältnis ein 720 x 550-Image, während die horizontale Anpassung ein kleineres 640 x 480-Image erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1fc38-114">For example, in the case of 720 x 480 video at 4:3 aspect ratio, the default behavior produces a 720 x 550 image, while horizontal adjustment produces a smaller 640 x 480 image.</span></span>

<span data-ttu-id="1fc38-115">**VMR-7**: um die Einstellung für die Seitenverhältnis Korrektur festzulegen, rufen Sie [**ivmrmixercontrol:: setmixingprefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect)auf.</span><span class="sxs-lookup"><span data-stu-id="1fc38-115">**VMR-7**: To set the aspect ratio correction preference, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span></span> <span data-ttu-id="1fc38-116">Legen Sie das Flag "aranpassxory" für "mixerpref" \_ auf das Standardverhalten fest, oder löschen Sie dieses Flag nur für die horizontale Anpassung.</span><span class="sxs-lookup"><span data-stu-id="1fc38-116">Set the MixerPref\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

<span data-ttu-id="1fc38-117">**VMR-9**: um die Einstellung für die Seitenverhältnis Korrektur festzulegen, rufen Sie [**IVMRMixerControl9:: setmixingprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs)auf.</span><span class="sxs-lookup"><span data-stu-id="1fc38-117">**VMR-9**: To set the aspect ratio correction preference, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span></span> <span data-ttu-id="1fc38-118">Legen Sie das \_ Flag "MixerPref9 aranpassxory" für das Standardverhalten fest, oder löschen Sie dieses Flag nur für die horizontale Anpassung.</span><span class="sxs-lookup"><span data-stu-id="1fc38-118">Set the MixerPref9\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fc38-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1fc38-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fc38-120">Verwenden des VMR-Mischungs Modus</span><span class="sxs-lookup"><span data-stu-id="1fc38-120">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



