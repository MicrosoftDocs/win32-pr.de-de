---
title: CMY- und CMYK-Farbraum
description: Die CMY-und CMYK-Farbbereiche werden häufig beim Drucken von Farben verwendet. Ein CMY-Farbraum verwendet Cyan, Magenta und gelb (CMY) als primäre Farben. Rot, grün und blau sind die sekundären Farben.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Color System (WCS), CMY Color Spaces
- WCS (Windows Color System), CMY Color Spaces
- Bild Farbverwaltung, CMY-Farbraum
- Farbverwaltung, CMY-Farbbereiche
- Farben, CMY-Farbbereiche
- Farbbereiche, CMY
- CMY-Farbbereiche
- Windows Color System (WCS), CMYK-Farbraum
- WCS (Windows Color System), CMYK-Farbraum
- Bild Farbverwaltung, CMYK-Farbraum
- Farbverwaltung, cmykcolor-Leerzeichen
- Farben, CMYK-Farbraum
- Farbbereiche, CMYK
- CMYK-Farbraum
- cyan
- magenta
- yellow
- Zyan Magenta Gelb (CMY)
- CMY (Cyan Magenta Gelb)
- Zyan Magenta Gelb Schwarz (CMYK)
- CMYK (Cyan Magenta gelb schwarz)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106354883"
---
# <a name="cmy-and-cmyk-color-spaces"></a><span data-ttu-id="d97e8-126">CMY- und CMYK-Farbraum</span><span class="sxs-lookup"><span data-stu-id="d97e8-126">CMY and CMYK Color Spaces</span></span>

<span data-ttu-id="d97e8-127">Die CMY-und CMYK- [Farbbereiche](c.md) werden häufig beim Drucken von Farben verwendet.</span><span class="sxs-lookup"><span data-stu-id="d97e8-127">The CMY and CMYK [color spaces](c.md) are often used in color printing.</span></span> <span data-ttu-id="d97e8-128">Ein CMY-Farbraum verwendet Cyan, Magenta und gelb (CMY) als [primäre Farben](p.md).</span><span class="sxs-lookup"><span data-stu-id="d97e8-128">A CMY color space uses cyan, magenta, and yellow (CMY) as its [primary colors](p.md).</span></span> <span data-ttu-id="d97e8-129">Rot, grün und blau sind die sekundären Farben.</span><span class="sxs-lookup"><span data-stu-id="d97e8-129">Red, green, and blue are the secondary colors.</span></span>

<span data-ttu-id="d97e8-130">Die folgenden Abbildungen sind Farbdarstellungen des CMY-Farbraum.</span><span class="sxs-lookup"><span data-stu-id="d97e8-130">The following figures are color representations of the CMY color space.</span></span> <span data-ttu-id="d97e8-131">Der CMY-Farbraum wird normalisiert.</span><span class="sxs-lookup"><span data-stu-id="d97e8-131">The CMY color space is normalized.</span></span>

![CMY-Farb Raum Cube mit maximalen Werten](images/cmyclrs1.png)

![CMY-Farb Raum Cube mit minimalen Werten](images/cmyclrs2.png)

<span data-ttu-id="d97e8-134">Der CMY-Farbraum ist Subtraktiv.</span><span class="sxs-lookup"><span data-stu-id="d97e8-134">The CMY color space is subtractive.</span></span> <span data-ttu-id="d97e8-135">Daher befindet sich weiß an (0,0, 0,0, 0,0) und schwarz auf (1,0, 1,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="d97e8-135">Therefore, white is at (0.0, 0.0, 0.0) and black is at (1.0, 1.0, 1.0).</span></span> <span data-ttu-id="d97e8-136">Wenn Sie mit weiß beginnen und keine Farben subtrahieren, erhalten Sie weiß.</span><span class="sxs-lookup"><span data-stu-id="d97e8-136">If you start with white and subtract no colors, you get white.</span></span> <span data-ttu-id="d97e8-137">Wenn Sie mit weiß beginnen und alle Farben gleichmäßig subtrahieren, werden Sie schwarz.</span><span class="sxs-lookup"><span data-stu-id="d97e8-137">If you start with white and subtract all colors equally, you get black.</span></span>

<span data-ttu-id="d97e8-138">Der CMYK-Farbraum ist eine Variation des CMY-Modells.</span><span class="sxs-lookup"><span data-stu-id="d97e8-138">The CMYK color space is a variation on the CMY model.</span></span> <span data-ttu-id="d97e8-139">Er fügt schwarz (Cyan, Magenta, gelb und schwarz) hinzu.</span><span class="sxs-lookup"><span data-stu-id="d97e8-139">It adds black (Cyan, Magenta, Yellow, and blacK).</span></span> <span data-ttu-id="d97e8-140">Der CMYK-Farbraum schließt die Lücke zwischen Theorie und Praxis.</span><span class="sxs-lookup"><span data-stu-id="d97e8-140">The CMYK color space closes the gap between theory and practice.</span></span> <span data-ttu-id="d97e8-141">Theoretisch ist die extra schwarze Komponente nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d97e8-141">In theory, the extra black component is not needed.</span></span> <span data-ttu-id="d97e8-142">Allerdings hat die Darstellung mit verschiedenen Arten von Farben und Dokumenten gezeigt, dass das Ergebnis in der Regel eine dunkelbraune, nicht schwarz ist, wenn die gleichen Komponenten von Cyan, Magenta und gelben Farben gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="d97e8-142">However, experience with various types of inks and papers has shown that when equal components of cyan, magenta, and yellow inks are mixed, the result is usually a dark brown, not black.</span></span> <span data-ttu-id="d97e8-143">Durch das Hinzufügen von blackink zur Mischung wird dieses Problem gelöst.</span><span class="sxs-lookup"><span data-stu-id="d97e8-143">Adding black ink to the mix solves this problem.</span></span>

<span data-ttu-id="d97e8-144">Die "CMY"-und "CMYK"-Farben können Geräte unabhängig sein, aber Sie werden in den meisten Fällen als Verweis auf ein bestimmtes Gerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="d97e8-144">The CMY and CMYK colors spaces can be device independent, but most often they are used in reference to a specific device.</span></span>

 

 




