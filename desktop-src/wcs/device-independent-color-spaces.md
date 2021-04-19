---
title: Geräteunabhängige Farbräume
description: Wenn Sie den Bedarf an standardmäßigen, geräteunabhängigen Farbmessungen, der International de d. d. d. d. d. d. d. d. d. d. 0034 d. Primärfarben.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Windows Color System (WCS), geräteunabhängige Farbbereiche
- WCS (Windows Color System), geräteunabhängige Farbbereiche
- Bild Farbverwaltung, geräteunabhängige Farbbereiche
- Farbverwaltung, geräteunabhängige Farbbereiche
- Farben, geräteunabhängige Farbbereiche
- Farbbereiche, Geräte unabhängig
- geräteunabhängige Farbbereiche
- Commission International de/Eclairage (CIE)
- International Commission on Illumination (CIE)
- Cie (Commission International de l Eclairage)
- Cie (Internationale Kommission bei der Beleuchtung)
- CIEXYZ-Farbraum
- XYZ-Farbraum
- sRGB-Farbraum
- Farbbereiche, CIEXYZ
- Farbbereiche, sRGB
- Farbbereiche, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106357134"
---
# <a name="device-independent-color-spaces"></a><span data-ttu-id="cfca5-120">Geräteunabhängige Farbräume</span><span class="sxs-lookup"><span data-stu-id="cfca5-120">Device-Independent Color Spaces</span></span>

<span data-ttu-id="cfca5-121">Wenn Sie den Bedarf an standardmäßigen, geräteunabhängigen Farbmessungen, der International de [d. d](p.md). d. d. d. d. d. d. d [](c.md) . d. d.</span><span class="sxs-lookup"><span data-stu-id="cfca5-121">Recognizing the need for standard, device-independent color measurements, the Commission International de l'Eclairage (International Commission on Illumination), or CIE, created a [color space](c.md) based on "imaginary" [primary colors](p.md).</span></span> <span data-ttu-id="cfca5-122">Es wird nicht erwartet, dass das Gerät in diesem Farbraum Farben erzeugt.</span><span class="sxs-lookup"><span data-stu-id="cfca5-122">No actual device is expected to produce colors in this color space.</span></span> <span data-ttu-id="cfca5-123">Sie wird als Mittel zum Umrechnen von Farben von einem Farb Raum in einen anderen verwendet.</span><span class="sxs-lookup"><span data-stu-id="cfca5-123">It is used as a means of converting colors from one color space to another.</span></span> <span data-ttu-id="cfca5-124">Die Hauptfarben in diesem Farbraum sind die abstrakten Farben X, Y und Z.</span><span class="sxs-lookup"><span data-stu-id="cfca5-124">The primary colors in this color space are the abstract colors X, Y, and Z.</span></span>

<span data-ttu-id="cfca5-125">Der 1931 CIEXYZ-Farbraum wird häufig als Grundlage für die Farb Raum Konvertierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cfca5-125">The 1931 CIEXYZ color space is widely used as the basis for color space conversion.</span></span> <span data-ttu-id="cfca5-126">Mit dem Anstieg des Internets hat die Überlegungen zur Bandbreite jedoch den XYZ-Farbraum nicht schwerfällig.</span><span class="sxs-lookup"><span data-stu-id="cfca5-126">With the rise of the Internet, however, bandwidth considerations have made the XYZ color space unwieldy.</span></span> <span data-ttu-id="cfca5-127">Der Austausch von Images über die begrenzte Bandbreite des Internets erfordert ein kompakteres [Farbmodell](c.md).</span><span class="sxs-lookup"><span data-stu-id="cfca5-127">The exchange of images over the limited bandwidth of the Internet necessitates a more compact [color model](c.md).</span></span>

<span data-ttu-id="cfca5-128">Daher haben Hewlett-Packard und Microsoft die Übernahme eines vordefinierten standardmäßigen RGB-Farbraum, der als sRGB bezeichnet wird, vorgeschlagen, um eine exakte Farbverwaltung mit sehr geringem Daten Aufwand zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cfca5-128">As a result, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined RGB color space known as sRGB, so as to allow accurate color management with very little data overhead.</span></span> <span data-ttu-id="cfca5-129">Dieser Standard wurde als formaler internationaler Standard vom Internationale Elektrotechnische Kommission (IEC) als IEC 61966-2-1: Multimedia Systems und equipmentcolor Messung und managementpart 2-1: Color managementdefault RGB-Farbraum genehmigt.</span><span class="sxs-lookup"><span data-stu-id="cfca5-129">This standard has been approved as a formal international standard by the International Electrotechnical Commission (IEC) as IEC 61966-2-1: Multimedia Systems and EquipmentColour Measurement and ManagementPart 2-1: Colour ManagementDefault RGB Colour Space.</span></span> <span data-ttu-id="cfca5-130">Er ist direkt von der IEC unter verfügbar <https://www.iec.ch/> .</span><span class="sxs-lookup"><span data-stu-id="cfca5-130">It is available directly from the IEC at <https://www.iec.ch/>.</span></span> <span data-ttu-id="cfca5-131">Informationen über die technischen Probleme, die bei sRGB auftreten, sind im Internet verfügbar unter:</span><span class="sxs-lookup"><span data-stu-id="cfca5-131">Information discussing the technical issues involved in sRGB is available on the Internet at:</span></span>

[<span data-ttu-id="cfca5-132">Ein standardmäßiger Standard Farbraum für das Internet (sRGB)</span><span class="sxs-lookup"><span data-stu-id="cfca5-132">A Standard Default Color Space for the Internet - sRGB</span></span>](https://www.w3.org/Graphics/Color/sRGB.html)

<span data-ttu-id="cfca5-133">Eine Hilfedatei Version eines Whitepaper, in dem die technischen Probleme erläutert werden, die mit sRGB (sRGB. hlp) verbunden sind, finden Sie im \\ Hilfe Ordner der WCS 1,0-Programmier Referenz im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="cfca5-133">A help-file version of a white paper discussing the technical issues involved in sRGB, sRGB.HLP, is available in the \\Help folder of the WCS 1.0 Programmer's Reference in the Platform SDK.</span></span>

<span data-ttu-id="cfca5-134">Unterschiedliche Dateiformate können ein Flag verwenden oder hinzufügen, um anzugeben, dass sich das Image im sRGB-Farbraum befindet.</span><span class="sxs-lookup"><span data-stu-id="cfca5-134">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="cfca5-135">Im Windows-DIB-Format (geräteunabhängige Bitmap) wird durch Festlegen des **bV5CSType** -Members der [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) -Struktur auf LCS \_ sRGB festgelegt, dass die DIB-Farben den sRGB-Farbraum aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cfca5-135">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) structure to LCS\_sRGB specifies that the DIB colors are in the sRGB color space.</span></span>

 

 




