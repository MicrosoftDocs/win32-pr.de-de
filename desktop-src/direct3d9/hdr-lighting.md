---
description: Beleuchtung in der realen Welt enthält einen sehr hohen dynamischen Bereich (HDR) von Leuchtkraft Werten.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: HDR-Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213801"
---
# <a name="hdr-lighting-direct3d-9"></a><span data-ttu-id="cb821-103">HDR-Beleuchtung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cb821-103">HDR Lighting (Direct3D 9)</span></span>

<span data-ttu-id="cb821-104">Beleuchtung in der realen Welt enthält einen sehr hohen dynamischen Bereich (HDR) von Leuchtkraft Werten.</span><span class="sxs-lookup"><span data-stu-id="cb821-104">Lighting in the real world contains a very high dynamic range (HDR) of luminance values.</span></span> <span data-ttu-id="cb821-105">Die reale Welt hat ungefähr 10 Aufträge des dynamischen Bereichs (Dr) für Glanzwerte, die auf das Spektrum von Dunkelheit und Helligkeit verteilt sind.</span><span class="sxs-lookup"><span data-stu-id="cb821-105">The real world has about 10 orders of dynamic range (DR) for luminance values spread across the spectrum of darkness to brightness.</span></span> <span data-ttu-id="cb821-106">Andererseits hat ein Computerbildschirm einen sehr begrenzten Anzeigebereich (oder Bereich von Leuchtkraft Werten): ungefähr zwei Aufträge des dynamischen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="cb821-106">On the other hand, a computer screen has a very limited display gamut (or range of luminance values): approximately two orders of dynamic range.</span></span> <span data-ttu-id="cb821-107">Die Herausforderung bei der Erstellung von HDR-gerenderten Images besteht darin, die realen HDR-Werte in den begrenzten Bereich eines Computerbildschirms zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="cb821-107">The challenge to producing HDR rendered images is to map the real world HDR values into the limited gamut of a computer screen.</span></span>

<span data-ttu-id="cb821-108">Die Tonzuordnung ist das Verfahren, das von DirectX zum Mapping von HDR-Informationen in einem eingeschränkteren Bereich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb821-108">Tone mapping is the technique used by DirectX for mapping HDR information into a more limited range.</span></span> <span data-ttu-id="cb821-109">Die auf CGI-Rendering angewendete Tonzuordnung kann die Menge der dargestellten Beleuchtungs Details erheblich verbessern, sodass Details in den dunkelsten Bereichen angezeigt werden, und der Kontrast in Bereichen, die so hell sind, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb821-109">Tone mapping applied to CGI rendering can dramatically improve the amount of lighting detail rendered, allowing details in the darkest areas to be seen, and providing contrast in areas that are so bright, they appear burned.</span></span> <span data-ttu-id="cb821-110">Die resultierenden Szenen werden mit deutlich ausführlicheren Beleuchtungs Details dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cb821-110">The resulting scenes render with far more visible lighting detail.</span></span>

<span data-ttu-id="cb821-111">[Hdrbeleuchtungs Sample](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) ist ein SDK-Beispiel, das die HDR-Beleuchtung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="cb821-111">[HDRLighting Sample](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) is a SDK sample that demonstrates HDR lighting.</span></span>

## <a name="tone-mapping"></a><span data-ttu-id="cb821-112">Ton Zuordnung</span><span class="sxs-lookup"><span data-stu-id="cb821-112">Tone Mapping</span></span>

<span data-ttu-id="cb821-113">Die Tone-Zuordnung simuliert in der Regel optische Phänomene, die nicht von der Dr des Monitors verursacht werden können.</span><span class="sxs-lookup"><span data-stu-id="cb821-113">Tone mapping generally simulates optical phenomena that cannot be caused by the DR of the monitor.</span></span> <span data-ttu-id="cb821-114">Beispiele hierfür sind Flares oder blühende (in der Regel Eigenschaften von-Linsen), die blaue Schicht, die in der menschlichen Perspektive in niedrigen Lichtbedingungen auftritt, und andere Anpassungen, die das Ergebnis der Biochemie der Augen sind.</span><span class="sxs-lookup"><span data-stu-id="cb821-114">Examples of this are flares or blooming (which are mostly properties of lenses), the blue shift that happens in the human eye in low light conditions, and other adaptations that are a result of the biochemistry of the eye.</span></span> <span data-ttu-id="cb821-115">Wenn die Notfall Wiederherstellung groß genug wäre, wäre die Audiozuordnung nicht so notwendig, außer bei der Bereitstellung von künstlerischen Effekten oder einigen der Eigenschaften eines Kamerabildes oder eines gekoppelten Geräts ("-CCD").</span><span class="sxs-lookup"><span data-stu-id="cb821-115">If the DR of the display were large enough, tone mapping would not be as neccessary, except for providing artistic effects or some of the properties of a camera lens or a charge coupled device (CCD).</span></span>

<span data-ttu-id="cb821-116">Die Tone-Zuordnung dividiert den Bereich der Leuchtkraft Werte in einer Szene in eine Gruppe von Zonen.</span><span class="sxs-lookup"><span data-stu-id="cb821-116">Tone mapping divides the range of luminance values in a scene into a set of zones.</span></span> <span data-ttu-id="cb821-117">Jede Zone umfasst einen Bereich von Leuchtkraft Werten.</span><span class="sxs-lookup"><span data-stu-id="cb821-117">Each zone encompasses a range of luminance values.</span></span>

<span data-ttu-id="cb821-118">In HDR werden folgende Begriffe verwendet:</span><span class="sxs-lookup"><span data-stu-id="cb821-118">HDR uses the following terms:</span></span>

-   <span data-ttu-id="cb821-119">Zonen Bereich von Leuchtkraft Werten</span><span class="sxs-lookup"><span data-stu-id="cb821-119">Zone - range of luminance values</span></span>
-   <span data-ttu-id="cb821-120">Bereich für die Helligkeit der mittleren grauen Mitte der Szene</span><span class="sxs-lookup"><span data-stu-id="cb821-120">Middle gray - middle brightness region of the scene</span></span>
-   <span data-ttu-id="cb821-121">Dynamisches Bereichs Verhältnis der höchsten Szenen Beleuchtung zur untersten Szenen Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="cb821-121">Dynamic range - ratio of the highest scene luminance to the lowest scene luminance</span></span>
-   <span data-ttu-id="cb821-122">Schlüssel-subjektives Maß der Szenen Beleuchtung: Dies variiert zwischen Licht und Mittel bis dunkel</span><span class="sxs-lookup"><span data-stu-id="cb821-122">Key - subjective measurement of scene lighting: this varies from light to moderate to dark</span></span>

<span data-ttu-id="cb821-123">Um die Leuchtkraft aus RGB-Werten zu berechnen, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="cb821-123">To calculate luminance from RGB values, use this:</span></span>


```
L = 0.27R + 0.67G + 0.06B;
```



<span data-ttu-id="cb821-124">Die Protokoll durchschnittliche Leuchtkraft ist eine nützliche Näherung für den Schlüssel einer Szene.</span><span class="sxs-lookup"><span data-stu-id="cb821-124">The log-average luminance is a useful approximation for the key of a scene.</span></span> <span data-ttu-id="cb821-125">Eine allgemeine Gleichung sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="cb821-125">A general equation looks like this:</span></span>

<span data-ttu-id="cb821-126">L<sub>w</sub> = exp \[ 1/N (Summen \[ Protokoll (Delta + L<sub>w</sub>(x, y)) \] ) \]</span><span class="sxs-lookup"><span data-stu-id="cb821-126">L<sub>w</sub> = exp\[ 1 / N( sum\[ log( delta + L<sub>w</sub>( x, y ) ) \] ) \]</span></span>

<span data-ttu-id="cb821-127">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="cb821-127">Where:</span></span>

-   <span data-ttu-id="cb821-128">L<sub>w</sub> -durchschnittliche Leuchtkraft für Protokoll</span><span class="sxs-lookup"><span data-stu-id="cb821-128">L<sub>w</sub> - log-average luminance</span></span>
-   <span data-ttu-id="cb821-129">N-Anzahl der Pixel im Bild</span><span class="sxs-lookup"><span data-stu-id="cb821-129">N - number of pixels in the image</span></span>
-   <span data-ttu-id="cb821-130">Delta-ein kleiner Faktor, um Probleme mit schwarzen Pixeln zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="cb821-130">delta - a small factor to avoid problems with black pixels</span></span>
-   <span data-ttu-id="cb821-131">L<sub>w</sub>(x, y)-die Welt Raumbeleuchtung für Pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="cb821-131">L<sub>w</sub>( x, y ) - the world space luminance for pixel ( x, y )</span></span>

<span data-ttu-id="cb821-132">Um diese einem mittelgrauen Wert zuzuordnen, finden Sie hier einen "Leuchtkraft Skalierungs Operator":</span><span class="sxs-lookup"><span data-stu-id="cb821-132">To map this to a middle-gray value, here is a luminance scaling operator:</span></span>

<span data-ttu-id="cb821-133">L (x, y) = a \* L<sub>w</sub>(x, y)/L<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="cb821-133">L( x, y ) = a \* L<sub>w</sub>( x, y ) / L<sub>w</sub></span></span>

<span data-ttu-id="cb821-134">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="cb821-134">Where:</span></span>

-   <span data-ttu-id="cb821-135">L (x, y): skalierte Leuchtkraft für Pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="cb821-135">L( x, y ) - scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="cb821-136">Schlüsselwert eines Bilds nach dem Anwenden der Skalierung</span><span class="sxs-lookup"><span data-stu-id="cb821-136">a - image key value after applying the scaling</span></span>

<span data-ttu-id="cb821-137">Und schließlich ist hier ein einfacher tonzuordnungsoperator zum Komprimieren der hohen Leuchtkraft:</span><span class="sxs-lookup"><span data-stu-id="cb821-137">And finally, here is a simple tone mapping operator for compressing the high luminances:</span></span>

<span data-ttu-id="cb821-138">L<sub>d</sub>(x, y) = l (x, y)/(1 + L (x, y))</span><span class="sxs-lookup"><span data-stu-id="cb821-138">L<sub>d</sub>( x, y ) = L( x, y ) / ( 1 + L( x, y ) )</span></span>

<span data-ttu-id="cb821-139">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="cb821-139">Where:</span></span>

-   <span data-ttu-id="cb821-140">L<sub>d</sub>(x, y)-komprimierte und skalierte Leuchtkraft für Pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="cb821-140">L<sub>d</sub>( x, y ) - compressed and scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="cb821-141">Schlüsselwert eines Bilds nach dem Anwenden der Skalierung</span><span class="sxs-lookup"><span data-stu-id="cb821-141">a - image key value after applying the scaling</span></span>

<span data-ttu-id="cb821-142">Dieser Operator skaliert hohe Leuchtkraft um 1/L und niedrige Leucht Ordnungen um 1.</span><span class="sxs-lookup"><span data-stu-id="cb821-142">This operator scales high luminances by 1/L and low luminances by 1.</span></span> <span data-ttu-id="cb821-143">Weitere Informationen finden Sie im folgenden Artikel.</span><span class="sxs-lookup"><span data-stu-id="cb821-143">For more details, see the following paper.</span></span>

<span data-ttu-id="cb821-144">Reinhard, Erik, Mike stark, Peter Shirley und James Ferwerda.</span><span class="sxs-lookup"><span data-stu-id="cb821-144">Reinhard, Erik, Mike Stark, Peter Shirley, and James Ferwerda.</span></span> <span data-ttu-id="cb821-145">["Fototon-Reproduktion für digitale Images"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span><span class="sxs-lookup"><span data-stu-id="cb821-145">["Photographic Tone Reproduction for Digital Images"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span></span> <span data-ttu-id="cb821-146">ACM-Transaktionen auf Grafiken (Info), das Sitzungsprotokoll der 29. jährlichen Konferenz zu Computer Grafiken und interaktiven Techniken (SIGGRAPH), pp. 267-276.</span><span class="sxs-lookup"><span data-stu-id="cb821-146">ACM Transactions on Graphics (TOG), Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques (SIGGRAPH), pp. 267-276.</span></span> <span data-ttu-id="cb821-147">New York, NY: ACM, 2002.</span><span class="sxs-lookup"><span data-stu-id="cb821-147">New York, NY: ACM Press, 2002.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb821-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb821-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb821-149">Erweiterte Themen</span><span class="sxs-lookup"><span data-stu-id="cb821-149">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 



