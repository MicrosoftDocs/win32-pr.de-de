---
title: Geräteabhängige Farbräume
description: Die meisten Farbbereiche sind Geräte abhängig.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Color System (WCS), Geräte abhängige Farbbereiche
- WCS (Windows Color System), Geräte abhängige Farbbereiche
- Bild Farbverwaltung, Geräte abhängige Farbbereiche
- Farbverwaltung, Geräte abhängige Farbbereiche
- Farben, Geräte abhängige Farbbereiche
- Farbbereiche, Geräte abhängig
- Geräte abhängige Farbbereiche
- weißer Punkt
- Colorants
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106366346"
---
# <a name="device-dependent-color-spaces"></a><span data-ttu-id="6f482-112">Geräteabhängige Farbräume</span><span class="sxs-lookup"><span data-stu-id="6f482-112">Device-Dependent Color Spaces</span></span>

<span data-ttu-id="6f482-113">Die meisten [Farbbereiche](c.md) sind Geräte abhängig.</span><span class="sxs-lookup"><span data-stu-id="6f482-113">Most [color spaces](c.md) are device dependent.</span></span> <span data-ttu-id="6f482-114">Obwohl ein bestimmtes Gerät (z. b. ein Drucker) den CMYK-Farbraum verwenden kann, sind die Farben, die für bestimmte CMYK-Werte gerendert werden, oft etwas anders als alle anderen Druckertypen.</span><span class="sxs-lookup"><span data-stu-id="6f482-114">Even though a particular device, such as a printer, may use the CMYK color space, the colors it renders for specific CMYK values are often slightly different than all other types of printers..</span></span> <span data-ttu-id="6f482-115">Der Grund hierfür ist, dass das WCS 1,0 Color Management System so nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="6f482-115">It is precisely for this reason that the WCS 1.0 color management system is so useful.</span></span>

<span data-ttu-id="6f482-116">Alle Farbbereiche verfügen über einen *weißen Punkt*, der als whitetestweiß definiert ist, das in diesem Farbraum erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6f482-116">All color spaces have a *white point*, which is defined as the whitest white that can be produced in that color space.</span></span> <span data-ttu-id="6f482-117">Da sich die Geräte voneinander unterscheiden können, können sich auch die zugehörigen weißen Punkte unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="6f482-117">Since devices can differ from one another, their white points can also differ.</span></span> <span data-ttu-id="6f482-118">Alle Farben, die von einem Gerät erzeugt werden können, sind relativ zum weißen Punkt.</span><span class="sxs-lookup"><span data-stu-id="6f482-118">All colors that a device can produce are relative to its white point.</span></span> <span data-ttu-id="6f482-119">Daher muss ein Farb Verwaltungssystem in der Lage sein, den weißen Punkt eines Farbraum einer anderen Farbe zuzuordnen und die relativen Positionen aller Farben beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="6f482-119">Therefore, a color management system must be able to map the white point of one color space into another and preserve the relative locations of all colors.</span></span> <span data-ttu-id="6f482-120">Es muss auch in der Lage sein, eine Farbe in einem Farbraum der nächstgelegenen Entsprechung in einem anderen Farbraum zuzuordnen, unabhängig von den Unterschieden in den weißen Punkten.</span><span class="sxs-lookup"><span data-stu-id="6f482-120">It must also be able to map a color in one color space to its closest match in another color space regardless of the differences in the white points.</span></span> <span data-ttu-id="6f482-121">WCS 1,0 ist in der Lage, beide Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6f482-121">WCS 1.0 is able to accomplish both of these tasks.</span></span>

<span data-ttu-id="6f482-122">Der RGB-Farbraum wird häufig für Computer Monitore verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f482-122">The RGB color space is often used on computer monitors.</span></span> <span data-ttu-id="6f482-123">Daher ist es Geräte abhängig.</span><span class="sxs-lookup"><span data-stu-id="6f482-123">As such, it is device dependent.</span></span> <span data-ttu-id="6f482-124">Drucker verwenden normalerweise CMYK- [Colorants](c.md).</span><span class="sxs-lookup"><span data-stu-id="6f482-124">Printers typically use CMYK [colorants](c.md).</span></span> <span data-ttu-id="6f482-125">Jeder Drucker implementiert seine eigene Version des CMYK-Farbraum.</span><span class="sxs-lookup"><span data-stu-id="6f482-125">Each printer implements its own version of the CMYK color space.</span></span> <span data-ttu-id="6f482-126">In digitalen Images werden die darin gespeicherten Farben möglicherweise nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6f482-126">Digital images may not actually store colors in them.</span></span> <span data-ttu-id="6f482-127">Sie können Indexnummern in einer Palette von Farben speichern.</span><span class="sxs-lookup"><span data-stu-id="6f482-127">They may store index numbers into a palette of colors.</span></span> <span data-ttu-id="6f482-128">Das Ergebnis ist, dass es für einzelne Anwendungsentwickler sehr schwierig ist, eine standardisierte Methode zum Verschieben von Farbbildern von einem Gerät zu einem anderen zu verwenden oder bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6f482-128">The result is that it is very hard for individual application developers to use or provide a standardized method of moving color images from one device to another.</span></span> <span data-ttu-id="6f482-129">Abbild Fachleute treten häufig die Frustration auf, wenn ein Grafik Bild auf einem Computerbildschirm erstellt wird und es beim Drucken sehr unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="6f482-129">Imaging professionals commonly experience the frustration of creating a graphic image on a computer screen and having it turn out very differently when it is printed.</span></span> <span data-ttu-id="6f482-130">WCS 1,0 behandelt diese Abbild Erstellungs Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="6f482-130">WCS 1.0 addresses these imaging needs.</span></span>

 

 




