---
description: Texturen werden in der unteren rechten Ecke immer linear von (0,0, 0,0) an der oberen linken Ecke bis (1,0, 1,0) adressiert, wie in der folgenden Abbildung dargestellt.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Bilineare Textur Filterung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393186"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a><span data-ttu-id="9269e-103">Bilineare Textur Filterung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9269e-103">Bilinear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="9269e-104">Texturen werden in der unteren rechten Ecke immer linear von (0,0, 0,0) an der oberen linken Ecke bis (1,0, 1,0) adressiert, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9269e-104">Textures are always linearly addressed from (0.0, 0.0) at the top-left corner to (1.0, 1.0) at the bottom-right corner, as shown in the following illustration.</span></span>

![Abbildung der 4X4-Textur mit voll Tonfarben](images/bilinear-fig7a.png)

<span data-ttu-id="9269e-106">Texturen werden in der Regel so dargestellt, als würden Sie aus voll Tonfarben bestehen, aber es ist eigentlich korrekter, dass Sie sich auf die gleiche Weise wie die Raster Darstellung vorstellen können: jede Textzelle wird in der Mitte einer Raster Zelle definiert, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9269e-106">Textures are usually represented as if they were composed of solid blocks of color, but it's actually more correct to think of textures the same way you should think of the raster display: Each texel is defined at the exact center of a grid cell, as shown in the following illustration.</span></span>

![Abbildung der 4X4-Textur mit texeln, die in der Mitte der Rasterzellen definiert sind](images/bilinear-fig7b.png)

<span data-ttu-id="9269e-108">Wenn Sie den Textur Sampler bei UV-Koordinaten (0,375, 0,375) für die Farbe der Textur Anfragen, erhalten Sie rot (255, 0,0).</span><span class="sxs-lookup"><span data-stu-id="9269e-108">If you ask the texture sampler for this texture's color at UV coordinates (0.375, 0.375) you'll get solid red (255, 0, 0).</span></span> <span data-ttu-id="9269e-109">Das ist ideal, da der exakte Mittelpunkt der roten Textzelle sich bei UV (0,375, 0,375) befindet.</span><span class="sxs-lookup"><span data-stu-id="9269e-109">That makes perfect sense because the exact center of the red texel cell is at UV (0.375, 0.375).</span></span> <span data-ttu-id="9269e-110">Was geschieht, wenn Sie den Sampler um die Farbe der Textur bei UV (0,25, 0,25) bitten?</span><span class="sxs-lookup"><span data-stu-id="9269e-110">What if you ask the sampler for the texture's color at UV (0.25, 0.25)?</span></span> <span data-ttu-id="9269e-111">Das ist nicht ganz einfach, da der Punkt bei UV (0,25, 0,25) in der exakten Ecke von vier texeln liegt.</span><span class="sxs-lookup"><span data-stu-id="9269e-111">That's not quite as easy, because the point at UV (0.25, 0.25) lies at the exact corner of 4 texels.</span></span>

<span data-ttu-id="9269e-112">Das einfachste Schema besteht darin, dass der Sampler einfach die Farbe des nächsten Texten zurückgibt. Dies wird als Punkt Filterung bezeichnet (siehe [Sampling des nächsten Punkts (Direct3D 9)](nearest-point-sampling.md)) und ist in der Regel aufgrund von grainen-oder grobe-Ergebnissen nicht erwünscht.</span><span class="sxs-lookup"><span data-stu-id="9269e-112">The simplest scheme is simply to have the sampler return the color of the closest texel; this is called Point filtering (see [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md)), and is usually undesirable due to grainy or blocky results.</span></span> <span data-ttu-id="9269e-113">Point-Sampling unsere Textur bei UV (0,25, 0,25) zeigt ein weiteres Problem mit dem nächstgelegenen filtern: Es gibt vier texeln, die vom Stichproben Punkt entfernt werden, sodass es keine einzelnen nächsten texellen gibt.</span><span class="sxs-lookup"><span data-stu-id="9269e-113">Point-sampling our texture at UV (0.25, 0.25) shows another subtle problem with nearest-point filtering: there are four texels equidistant from the sampling point, so there's no single nearest texel.</span></span> <span data-ttu-id="9269e-114">Eines dieser vier texeln wird als die zurückgegebene Farbe ausgewählt. die Auswahl hängt jedoch davon ab, wie die Koordinate gerundet wird. Dies kann zu Tränen enden Artefakten führen (Weitere Informationen finden Sie im Nearest-Point Sampling-Artikel im SDK).</span><span class="sxs-lookup"><span data-stu-id="9269e-114">One of those four texels will be chosen as the returned color, but the selection depends on how the coordinate is rounded, which may introduce tearing artifacts (see the Nearest-Point Sampling article in the SDK).</span></span>

<span data-ttu-id="9269e-115">Ein etwas genaueres und allgemeineres Filter Schema besteht darin, den gewichteten Durchschnitt der 4 texeln zu berechnen, die dem Stichproben Punkt am nächsten sind. Dies wird als bilineare Filterung bezeichnet, und die zusätzlichen berechnungskosten sind normalerweise unerheblich, da diese Routine in moderner Grafikhardware implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9269e-115">A slightly more accurate and more common filtering scheme is to calculate the weighted average of the 4 texels closest to the sampling point; this is called Bilinear filtering, and the extra computational cost is usually negligible because this routine is implemented in modern graphics hardware.</span></span> <span data-ttu-id="9269e-116">Im folgenden finden Sie die Farben, die wir mit der bilinearen Filterung für einige verschiedene Beispiel Punkte erhalten:</span><span class="sxs-lookup"><span data-stu-id="9269e-116">Here are the colors we get at a few different sample points using bilinear filtering:</span></span>


```
UV: (0.5, 0.5)
```



<span data-ttu-id="9269e-117">Dieser Punkt befindet sich an der exakten Grenze zwischen rot, grün, blau und weißen texeln.</span><span class="sxs-lookup"><span data-stu-id="9269e-117">This point is at the exact border between red, green, blue, and white texels.</span></span> <span data-ttu-id="9269e-118">Die Farbe, die der Sampler zurückgibt, ist grau:</span><span class="sxs-lookup"><span data-stu-id="9269e-118">The color the sampler returns is gray:</span></span>


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



<span data-ttu-id="9269e-119">Dieser Punkt befindet sich im Mittelpunkt des Rahmens zwischen roten und grünen texeln.</span><span class="sxs-lookup"><span data-stu-id="9269e-119">This point is at the midpoint of the border between red and green texels.</span></span> <span data-ttu-id="9269e-120">Die Farbe, die der Sampler zurückgibt, ist gelb grau (Beachten Sie, dass die Beiträge der blauen und weißen texeln auf 0 skaliert werden):</span><span class="sxs-lookup"><span data-stu-id="9269e-120">The color the sampler returns is yellow-gray (note that the contributions of the blue and white texels are scaled to 0):</span></span>


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



<span data-ttu-id="9269e-121">Dies ist die Adresse des roten texms, bei dem es sich um die zurückgegebene Farbe handelt (alle anderen texeln in der Filter Berechnung werden auf 0 gewichtet):</span><span class="sxs-lookup"><span data-stu-id="9269e-121">This is the address of the red texel, which is the returned color (all other texels in the filtering calculation are weighted to 0):</span></span>


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



<span data-ttu-id="9269e-122">Vergleichen Sie diese Berechnungen mit der folgenden Abbildung, die zeigt, was geschieht, wenn die Berechnung der bilinearen Filterung an jeder Textur Adresse in der 4 x 4-Textur ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9269e-122">Compare these calculations against the following illustration, which shows what happens if the bilinear filtering calculation is performed at every texture address across the 4x4 texture.</span></span>

![Abbildung der 4X4-Textur mit bilinearer Filterung, die bei jeder Textur Adresse ausgeführt wird](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a><span data-ttu-id="9269e-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9269e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9269e-125">Textur Filterung</span><span class="sxs-lookup"><span data-stu-id="9269e-125">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 



