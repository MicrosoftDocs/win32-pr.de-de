---
title: Regions Dateien
description: Regions Dateien
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Windows Media Player Mobile Skins, Art Dateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Regions Dateien
- Windows Media Player Mobile Skins, Regions Dateien
- Skins, Regions Dateien
- Regions Dateien in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311112"
---
# <a name="region-files"></a><span data-ttu-id="979fa-110">Regions Dateien</span><span class="sxs-lookup"><span data-stu-id="979fa-110">Region Files</span></span>

<span data-ttu-id="979fa-111">Regions Dateien sind erforderlich, wenn Sie eine beliebige Art von Treffer Schaltfläche verwenden (2pushhit, pushhit oder degglehit).</span><span class="sxs-lookup"><span data-stu-id="979fa-111">Region files are required if you use any type of hit button (2PushHit, PushHit, or ToggleHit).</span></span>

<span data-ttu-id="979fa-112">Regions Dateien werden verwendet, um Bereiche zu definieren, die auf eine Tap (auch als Treffer bezeichnet) auf einer bestimmten Schaltfläche reagieren.</span><span class="sxs-lookup"><span data-stu-id="979fa-112">Region files are used to define areas that will respond to a tap, also known as a hit, on a specific button.</span></span> <span data-ttu-id="979fa-113">Für jede Treffer Schaltfläche erhält ein Bereich in der Bereichs Bitmap eine bestimmte Webfarbe (z. b. \# FF0000, bei der es sich um den Wert für ein voll tonrot handelt).</span><span class="sxs-lookup"><span data-stu-id="979fa-113">For each hit button, an area in the Region bitmap is given a specific Web color (such as \#FF0000, which is the value for solid red).</span></span> <span data-ttu-id="979fa-114">Die Farbnummer wird in der Definition der Bereichs Schaltfläche angegeben.</span><span class="sxs-lookup"><span data-stu-id="979fa-114">The color number is specified in the region button definition.</span></span> <span data-ttu-id="979fa-115">Wenn der Benutzer die Skin anzeigt, wird das Schaltflächen Bild mithilfe der Koordinaten des Bereichs in der Bereichs Bitmap auf dem Hintergrund dargestellt.</span><span class="sxs-lookup"><span data-stu-id="979fa-115">When the user displays the skin, the button image is superimposed onto the background using the coordinates of the area in the Region bitmap.</span></span>

<span data-ttu-id="979fa-116">Sie können z. b. einen roten Kreis an einem Speicherort zeichnen, der dem Speicherort der Schaltfläche "weiter" entspricht, und die Farbe "rot" ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="979fa-116">For example, you could draw a red circle in a location corresponding to the location of the Next button and color it solid red (\#FF0000).</span></span> <span data-ttu-id="979fa-117">Anschließend können Sie in der Schaltflächen Definition den Wert "Treffer RGB" von 255, 0, 0 (der RGB-Entsprechung von \# FF0000) zuweisen.</span><span class="sxs-lookup"><span data-stu-id="979fa-117">Then in the button definition, you could assign a hit RGB value of 255,0,0 (which is the RGB equivalent of \#FF0000).</span></span> <span data-ttu-id="979fa-118">In diesem Fall würde die Schaltfläche "weiter" nur auf Abzweigungen (Treffer) innerhalb des roten Kreises reagieren.</span><span class="sxs-lookup"><span data-stu-id="979fa-118">In this case, the Next button would only respond to taps (hits) inside the red circle.</span></span>

<span data-ttu-id="979fa-119">Wenn Sie andere Formen als Rechtecke definieren möchten, werden Treffer Schaltflächen verwendet.</span><span class="sxs-lookup"><span data-stu-id="979fa-119">Hit buttons are used when you want to define shapes other than rectangles.</span></span> <span data-ttu-id="979fa-120">Sie müssen immer noch die Koordinaten für jede Schaltfläche definieren, damit sekundäre Images wie z. b. gepusht und deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="979fa-120">You must still define the coordinates for each button so that secondary images such as Pushed and Disabled can be located correctly.</span></span> <span data-ttu-id="979fa-121">In der Praxis wird jede Schaltfläche durch ein Rechteck gebunden, und diese imaginären Begrenzungs Rechtecke dürfen sich nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="979fa-121">In practice, each button is bounded by a rectangle, and these imaginary boundary rectangles must not overlap.</span></span>

> [!Note]  
> <span data-ttu-id="979fa-122">Regions kunstdateien werden in Windows Media Player 10 Mobile-Skins nicht benötigt, da Schaltflächen Typen in Windows Media Player 10 Mobile oder höher nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="979fa-122">Region art files are not needed in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="979fa-123">Das folgende Bild ist eine typische Regions Datei.</span><span class="sxs-lookup"><span data-stu-id="979fa-123">The following image is a typical Region file.</span></span>

![Regions Datei](images/cesdkreg.png)

<span data-ttu-id="979fa-125">Diese Datei definiert die Teile der Skin für jede Schaltfläche des Treffer Typs.</span><span class="sxs-lookup"><span data-stu-id="979fa-125">This file defines the parts of the skin for each hit-type button.</span></span> <span data-ttu-id="979fa-126">Jede Farbe wird anhand ihrer Farbzahl im Schaltflächen Abschnitt der Skin-Definitionsdatei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="979fa-126">Each color will be identified by its color number in the Buttons section of the skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="979fa-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="979fa-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="979fa-128">**Kunstdateien**</span><span class="sxs-lookup"><span data-stu-id="979fa-128">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




