---
title: Rendering von Absichten
description: Das International Color Consortium (ICC) hat vier verschiedene Werte definiert, die als renderintents bezeichnet werden.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Windows Color System (WCS), renderintents
- WCS (Windows Color System), renderintents
- Bild Farbverwaltung, renderintents
- Farbverwaltung, renderintents
- Farben, renderintents
- renderintents
- International Color Consortium (ICC)
- IIC (International Color Consortium)
- Bild Absicht
- Grafische Absicht
- Nachweis Absicht
- Ziel Übereinstimmung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106357170"
---
# <a name="rendering-intents"></a><span data-ttu-id="e0734-115">Rendering von Absichten</span><span class="sxs-lookup"><span data-stu-id="e0734-115">Rendering Intents</span></span>

<span data-ttu-id="e0734-116">Das International Color Consortium (ICC) hat vier verschiedene Werte definiert, die als *renderintents* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e0734-116">The International Color Consortium (ICC) has defined four different values called *rendering intents*.</span></span> <span data-ttu-id="e0734-117">Diese stellen vier verschiedene Ansätze zum Erstellen eines Farb Rendering dar.</span><span class="sxs-lookup"><span data-stu-id="e0734-117">These represent four different approaches to creating a color rendering.</span></span> <span data-ttu-id="e0734-118">Diese vier Intents und die Konstanten, die verwendet werden, um Sie im Code zu verweisen, lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="e0734-118">These four intents, and the constants used to refer to them in code are as follows.</span></span>



| <span data-ttu-id="e0734-119">Intent</span><span class="sxs-lookup"><span data-stu-id="e0734-119">Intent</span></span>                            | <span data-ttu-id="e0734-120">Name des ICC</span><span class="sxs-lookup"><span data-stu-id="e0734-120">ICC Name</span></span>              | <span data-ttu-id="e0734-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0734-121">Description</span></span>                    |
|-----------------------------------|-----------------------|--------------------------------|
| <span data-ttu-id="e0734-122">Picture</span><span class="sxs-lookup"><span data-stu-id="e0734-122">Picture</span></span> | <span data-ttu-id="e0734-123">Wahrnehmungs</span><span class="sxs-lookup"><span data-stu-id="e0734-123">Perceptual</span></span>            | <span data-ttu-id="e0734-124">beabsichtigte \_ Absicht</span><span class="sxs-lookup"><span data-stu-id="e0734-124">INTENT\_PERCEPTUAL</span></span>             |
| <span data-ttu-id="e0734-125">Graphic</span><span class="sxs-lookup"><span data-stu-id="e0734-125">Graphic</span></span> | <span data-ttu-id="e0734-126">Sättigung</span><span class="sxs-lookup"><span data-stu-id="e0734-126">Saturation</span></span>            | <span data-ttu-id="e0734-127">beabsichtigte \_ Sättigung</span><span class="sxs-lookup"><span data-stu-id="e0734-127">INTENT\_SATURATION</span></span>             |
| <span data-ttu-id="e0734-128">Proof</span><span class="sxs-lookup"><span data-stu-id="e0734-128">Proof</span></span>     | <span data-ttu-id="e0734-129">Relative farbige Metrik</span><span class="sxs-lookup"><span data-stu-id="e0734-129">Relative Colorimetric</span></span> | <span data-ttu-id="e0734-130">beabsichtigte \_ relative \_ farbige Metrik</span><span class="sxs-lookup"><span data-stu-id="e0734-130">INTENT\_RELATIVE\_COLORIMETRIC</span></span> |
| <span data-ttu-id="e0734-131">Match</span><span class="sxs-lookup"><span data-stu-id="e0734-131">Match</span></span>     | <span data-ttu-id="e0734-132">Absolute farbige Metrik</span><span class="sxs-lookup"><span data-stu-id="e0734-132">Absolute Colorimetric</span></span> | <span data-ttu-id="e0734-133">beabsichtigte \_ absolute \_ farbige Metrik</span><span class="sxs-lookup"><span data-stu-id="e0734-133">INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> |




 

<span data-ttu-id="e0734-134">Die Version 3,4, in der diese Intents beschrieben werden, kann von Color.org heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="e0734-134">The ICC Profile Format Specification Version 3.4, which describes these intents, can be downloaded from color.org.</span></span>

## <a name="picture-intent"></a><span data-ttu-id="e0734-135">Bild Absicht</span><span class="sxs-lookup"><span data-stu-id="e0734-135">Picture Intent</span></span>

<span data-ttu-id="e0734-136">Eine Bild Absicht, die als perzeptive Absicht in der ICC-Spezifikations Klausel 4,9 bezeichnet wird, bewirkt, dass [die vollständige](./g.md) Spiel Größe des Bilds komprimiert oder erweitert wird, um die Größe des Zielgeräts zu füllen, sodass das graue Gleichgewicht beibehalten wird, die farbige metrikgenauigkeit jedoch möglicherweise nicht beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="e0734-136">Called perceptual intent in the ICC specification clause 4.9, a Picture intent causes the full [gamut](./g.md) of the image to be compressed or expanded to fill the gamut of the destination device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span>

<span data-ttu-id="e0734-137">Anders ausgedrückt: Wenn bestimmte Farben in einem Bild außerhalb des Bereichs von Farben liegen, die das Ausgabegerät rendern kann, bewirkt die Bild Absicht, dass alle Farben im Bild so angepasst werden, dass jede Farbe im Bild innerhalb des Bereichs liegt, der gerendert werden kann, sodass die Beziehung zwischen Farben so weit wie möglich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="e0734-137">In other words, if certain colors in an image fall outside of the range of colors that the output device can render, the picture intent will cause all the colors in the image to be adjusted so that the every color in the image falls within the range that can be rendered and so that the relationship between colors is preserved as much as possible.</span></span>

<span data-ttu-id="e0734-138">Diese Absicht eignet sich am besten für die Anzeige von Fotos und Bildern und ist in der Regel die Standard Absicht.</span><span class="sxs-lookup"><span data-stu-id="e0734-138">This intent is most suitable for display of photographs and images, and is generally the default intent.</span></span>

## <a name="graphic-intent"></a><span data-ttu-id="e0734-139">Grafische Absicht</span><span class="sxs-lookup"><span data-stu-id="e0734-139">Graphic Intent</span></span>

<span data-ttu-id="e0734-140">Die Klausel der ICC-Spezifikation 4,12 Ruft die Absicht einer [Sättigung](s.md) der Absicht auf.</span><span class="sxs-lookup"><span data-stu-id="e0734-140">The ICC specification clause 4.12 calls the Graphic intent a [saturation](s.md) intent.</span></span> <span data-ttu-id="e0734-141">Es behält den Chroma der Farben im Bild bei möglichen Ausgaben von [Hue](h.md) und [Helligkeit](l.md)bei.</span><span class="sxs-lookup"><span data-stu-id="e0734-141">It preserves the chroma of colors in the image at the possible expense of [hue](h.md) and [lightness](l.md).</span></span>

<span data-ttu-id="e0734-142">Die Implementierung dieser Absicht bleibt etwas problematisch, und der IStGH arbeitet immer noch an Methoden, um die gewünschten Effekte zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="e0734-142">Implementation of this intent remains somewhat problematic, and the ICC is still working on methods to achieve the desired effects.</span></span>

<span data-ttu-id="e0734-143">Diese Absicht eignet sich am besten für Unternehmens Grafiken, wie z. b. Diagramme, bei denen es wichtiger ist, dass die Farben lebhaft sind und einander gegenseitig und nicht eine bestimmte Farbe vergleichen.</span><span class="sxs-lookup"><span data-stu-id="e0734-143">This intent is most suitable for business graphics such as charts, where it is more important that the colors be vivid and contrast well with each other rather than a specific color.</span></span>

## <a name="proof-intent"></a><span data-ttu-id="e0734-144">Nachweis Absicht</span><span class="sxs-lookup"><span data-stu-id="e0734-144">Proof Intent</span></span>

<span data-ttu-id="e0734-145">Die Nachweis Absicht, die als farbige Metrik in der Bezeichnung "ICC" bezeichnet wird, ist so definiert, dass alle Farben, die außerhalb des Bereichs liegen, den das Ausgabegerät rendern kann, an die nächstgelegene Farbe angepasst werden, die gerendert werden kann, während alle anderen Farben unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="e0734-145">The Proof intent, called the colorimetric intent in the ICC specification, is defined such that any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span>

<span data-ttu-id="e0734-146">Die Nachweis Absicht behält den [weißen Punkt](w.md)nicht bei.</span><span class="sxs-lookup"><span data-stu-id="e0734-146">Proof intent does not preserve the [white point](w.md).</span></span>

<span data-ttu-id="e0734-147">Beispielsweise ist das weiß eines Whitepapers mit einem Whitepaper besser gelb als das whitetestweiß eines Computermonitors.</span><span class="sxs-lookup"><span data-stu-id="e0734-147">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="e0734-148">Ein Bild, das mithilfe relativer farbige metrikabsicht in die Spiel Palette konvertiert wurde, würde dazu führen, dass alle Farben Gelb werden.</span><span class="sxs-lookup"><span data-stu-id="e0734-148">An image converted into the gamut of the printer using relative colorimetric intent would result in all colors becoming more yellow.</span></span> <span data-ttu-id="e0734-149">Der weiße Punkt des Bilds wird so verschoben, dass er dem weißen Punkt des Druckers entspricht.</span><span class="sxs-lookup"><span data-stu-id="e0734-149">The white point of the image is moved to match the white point of the printer.</span></span> <span data-ttu-id="e0734-150">Alle anderen Farben im Bild behalten ihre Position relativ zum weißen Punkt bei.</span><span class="sxs-lookup"><span data-stu-id="e0734-150">All other colors in the image keep their position relative to the white point.</span></span> <span data-ttu-id="e0734-151">Dadurch wird ein Bild erzeugt, das das Aussehen des gedruckten Bilds genauer widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="e0734-151">This produces an image that more accurately reflects what the printed image will look like.</span></span> <span data-ttu-id="e0734-152">Der Benutzer kann es jedoch visuell disconcerting finden.</span><span class="sxs-lookup"><span data-stu-id="e0734-152">However, the user may find it visually disconcerting.</span></span>

## <a name="match-intent"></a><span data-ttu-id="e0734-153">Ziel Übereinstimmung</span><span class="sxs-lookup"><span data-stu-id="e0734-153">Match Intent</span></span>

<span data-ttu-id="e0734-154">In einer Übereinstimmungs Absicht werden alle Farben, die außerhalb des Bereichs liegen, den das Ausgabegerät rendern kann, an die nächstgelegene Farbe angepasst, die gerendert werden kann, während alle anderen Farben unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="e0734-154">In a Match intent, any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span> <span data-ttu-id="e0734-155">Die Spezifikation "ICC" Ruft die Absicht "Match Intent absolute colormetric" auf.</span><span class="sxs-lookup"><span data-stu-id="e0734-155">The ICC specification calls the match intent absolute colorimetric intent.</span></span>

<span data-ttu-id="e0734-156">Die Übereinstimmungs Absicht behält den weißen Punkt bei.</span><span class="sxs-lookup"><span data-stu-id="e0734-156">Match intent preserves the white point.</span></span>

<span data-ttu-id="e0734-157">Beispielsweise ist das weiß eines Whitepapers mit einem Whitepaper besser gelb als das whitetestweiß eines Computermonitors.</span><span class="sxs-lookup"><span data-stu-id="e0734-157">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="e0734-158">Ein Bild, das mit der Übereinstimmungs Absicht in den [Farbskala](./g.md) des Druckers konvertiert wurde, würde dazu führen, dass alle Farben konvertiert und mit dem Spiel des Druckers verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="e0734-158">An image converted into the [gamut](./g.md) of the printer using match intent would result in all colors being converted and matched into the gamut of the printer.</span></span> <span data-ttu-id="e0734-159">Der weiße Punkt des Bilds wird nicht so verschoben, dass er dem weißen Punkt des Druckers entspricht.</span><span class="sxs-lookup"><span data-stu-id="e0734-159">The white point of the image is not moved to match the white point of the printer.</span></span> <span data-ttu-id="e0734-160">Daher kann sich der Abstand der Farben zum weißen Punkt ändern.</span><span class="sxs-lookup"><span data-stu-id="e0734-160">Therefore, the distance of the colors to the white point may change.</span></span> <span data-ttu-id="e0734-161">Dies erzeugt ein Bild, das weniger visuell mit dem Benutzer disconceriert, aber auch eine weniger genaue Darstellung der Druckerausgabe ist.</span><span class="sxs-lookup"><span data-stu-id="e0734-161">This produces an image that is less visually disconcerting to the user, but is also a less accurate rendition of printer output.</span></span>

 

 