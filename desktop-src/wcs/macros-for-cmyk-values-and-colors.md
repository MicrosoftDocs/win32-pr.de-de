---
title: Makros für CMYK-Werte und -Farben
description: Die folgenden Makros sind hilfreich beim Bearbeiten von CMYK-Werten.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows Color System (WCS), CMYK-Makros
- WCS (Windows Color System), CMYK-Makros
- Bild Farbverwaltung, CMYK-Makros
- Farbverwaltung, CMYK-Makros
- Farben, CMYK-Makros
- WCS-Referenz, CMYK-Makros
- Referenz für WCs, CMYK-Makros
- CMYK-Makros
- Zyan Magenta Gelb Schwarz (CMYK)
- CMYK (Cyan Magenta gelb schwarz)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106367256"
---
# <a name="macros-for-cmyk-values-and-colors"></a><span data-ttu-id="926d7-113">Makros für CMYK-Werte und -Farben</span><span class="sxs-lookup"><span data-stu-id="926d7-113">Macros for CMYK Values and Colors</span></span>

<span data-ttu-id="926d7-114">Die folgenden Makros sind hilfreich beim Bearbeiten von CMYK-Werten.</span><span class="sxs-lookup"><span data-stu-id="926d7-114">The following macros are useful in manipulating CMYK values.</span></span>



| <span data-ttu-id="926d7-115">Makro</span><span class="sxs-lookup"><span data-stu-id="926d7-115">Macro</span></span>                          | <span data-ttu-id="926d7-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="926d7-116">Description</span></span>                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="926d7-117">**CMYK**</span><span class="sxs-lookup"><span data-stu-id="926d7-117">**CMYK**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | <span data-ttu-id="926d7-118">Erstellt einen CMYK-Wert aus den Werten einzelner Cyan, Magenta, gelb und schwarz.</span><span class="sxs-lookup"><span data-stu-id="926d7-118">Builds a CMYK value from individual cyan, magenta, yellow, and black values.</span></span> |
| [<span data-ttu-id="926d7-119">**Getcvalue**</span><span class="sxs-lookup"><span data-stu-id="926d7-119">**GetCValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | <span data-ttu-id="926d7-120">Ruft den Zyan-Farbwert aus einem CMYK-Farbwert ab.</span><span class="sxs-lookup"><span data-stu-id="926d7-120">Retrieves the cyan color value from a CMYK color value.</span></span>                      |
| [<span data-ttu-id="926d7-121">**Getkvalue**</span><span class="sxs-lookup"><span data-stu-id="926d7-121">**GetKValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | <span data-ttu-id="926d7-122">Ruft den schwarzen Farbwert aus einem CMYK-Farbwert ab.</span><span class="sxs-lookup"><span data-stu-id="926d7-122">Retrieves the black color value from a CMYK color value.</span></span>                     |
| [<span data-ttu-id="926d7-123">**Getmvalue**</span><span class="sxs-lookup"><span data-stu-id="926d7-123">**GetMValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | <span data-ttu-id="926d7-124">Ruft den Magenta-Wert aus einem CMYK-Farbwert ab.</span><span class="sxs-lookup"><span data-stu-id="926d7-124">Retrieves the magenta value from a CMYK color value.</span></span>                         |
| [<span data-ttu-id="926d7-125">**Getyvalue**</span><span class="sxs-lookup"><span data-stu-id="926d7-125">**GetYValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | <span data-ttu-id="926d7-126">Ruft den gelben Farbwert aus einem CMYK-Farbwert ab.</span><span class="sxs-lookup"><span data-stu-id="926d7-126">Retrieves the yellow color value from a CMYK color value.</span></span>                    |



 

<span data-ttu-id="926d7-127">Die folgenden Makros werden mit Color verwendet.</span><span class="sxs-lookup"><span data-stu-id="926d7-127">The following macros are used with color.</span></span>



| <span data-ttu-id="926d7-128">Makro</span><span class="sxs-lookup"><span data-stu-id="926d7-128">Macro</span></span>                                | <span data-ttu-id="926d7-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="926d7-129">Description</span></span>                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="926d7-130">**Getbvalue**</span><span class="sxs-lookup"><span data-stu-id="926d7-130">**GetBValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | <span data-ttu-id="926d7-131">Ruft einen RGB-blauen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="926d7-131">Gets an RGB blue value.</span></span>                                                                                                                               |
| [<span data-ttu-id="926d7-132">**Getgvalue**</span><span class="sxs-lookup"><span data-stu-id="926d7-132">**GetGValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | <span data-ttu-id="926d7-133">Ruft einen grünen RGB-Wert ab.</span><span class="sxs-lookup"><span data-stu-id="926d7-133">Gets an RGB green value.</span></span>                                                                                                                              |
| [<span data-ttu-id="926d7-134">**Getrvalue**</span><span class="sxs-lookup"><span data-stu-id="926d7-134">**GetRValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | <span data-ttu-id="926d7-135">Ruft einen RGB-roten Wert ab.</span><span class="sxs-lookup"><span data-stu-id="926d7-135">Gets an RGB red value.</span></span>                                                                                                                                |
| <span data-ttu-id="926d7-136">[**Paletteingedex**](/previous-versions//dd162770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="926d7-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span></span> | <span data-ttu-id="926d7-137">Akzeptiert einen Index für einen Eintrag in der logischen Farbpalette und gibt einen paletteneintrags Bezeichner zurück.</span><span class="sxs-lookup"><span data-stu-id="926d7-137">Accepts an index to a logical-color palette entry and returns a palette-entry specifier.</span></span>                                                              |
| [<span data-ttu-id="926d7-138">**Palettergb**</span><span class="sxs-lookup"><span data-stu-id="926d7-138">**PALETTERGB**</span></span>](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | <span data-ttu-id="926d7-139">Akzeptiert drei Werte, die die relativen Intensitäten von rot, grün und blau darstellen, und gibt einen palettenrelativen roten, grünen, blauen (RGB) Spezifizierer zurück.</span><span class="sxs-lookup"><span data-stu-id="926d7-139">Accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier.</span></span> |
| [<span data-ttu-id="926d7-140">RGB</span><span class="sxs-lookup"><span data-stu-id="926d7-140">RGB</span></span>](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | <span data-ttu-id="926d7-141">Wählt eine rote, grüne, blaue (RGB) Farbe basierend auf den angegebenen Argumenten und den Farbfunktionen des Ausgabegeräts aus.</span><span class="sxs-lookup"><span data-stu-id="926d7-141">Selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.</span></span>                               |



 

 

 