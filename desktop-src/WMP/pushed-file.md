---
title: Datei mit pushübertragung
description: Datei mit pushübertragung
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Windows Media Player Mobile Skins, Art Dateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, übersetzte Dateien
- Windows Media Player Mobile Skins, übersetzte Dateien
- Skins, übersetzte Dateien
- Dateien in Skins per pushübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388392"
---
# <a name="pushed-file"></a><span data-ttu-id="d6893-110">Datei mit pushübertragung</span><span class="sxs-lookup"><span data-stu-id="d6893-110">Pushed File</span></span>

<span data-ttu-id="d6893-111">Die gepushte Datei enthält die Bilder, die angezeigt werden, wenn der Benutzer auf eine Schaltfläche tippt.</span><span class="sxs-lookup"><span data-stu-id="d6893-111">The Pushed file contains the images that will be displayed when the user taps on a button.</span></span> <span data-ttu-id="d6893-112">Sie können auch das normale und gepushte Bild für den anhaltezustand der Schaltfläche PLAYPAUSE einschließen.</span><span class="sxs-lookup"><span data-stu-id="d6893-112">You can also include the normal and pushed images for the pause state of the PlayPause button.</span></span>

<span data-ttu-id="d6893-113">Das folgende Bild ist eine typische gepushte Datei.</span><span class="sxs-lookup"><span data-stu-id="d6893-113">The following image is a typical Pushed file.</span></span>

![Datei mit pushübertragung](images/cesdkpus.png)

<span data-ttu-id="d6893-115">Dies speichert die Bilder, die angezeigt werden, wenn die Schaltflächen für den Treffer-Typ getippt werden.</span><span class="sxs-lookup"><span data-stu-id="d6893-115">This stores the images that will be displayed when the hit-type buttons are tapped.</span></span> <span data-ttu-id="d6893-116">Auch in dieser Datei gespeichert ist das normale und übersetzte Bild für das angehaltene Bild der Schaltfläche PLAYPAUSE.</span><span class="sxs-lookup"><span data-stu-id="d6893-116">Also stored in this file are the normal and pushed images for the paused image of the PlayPause button.</span></span> <span data-ttu-id="d6893-117">Mit Ausnahme der sekundären PLAYPAUSE-Images auf der rechten Seite werden die anderen Schaltflächen Bilder mit dem Hintergrundbild angezeigt. dabei wird der Offset verwendet, der im Abschnitt Bitmaps der Skin-Definitionsdatei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d6893-117">Except for the PlayPause secondary images on the right, the other button images line up with the Background image, using the offset defined in the Bitmaps section of the skin definition file.</span></span>

<span data-ttu-id="d6893-118">Beachten Sie, dass der Hintergrund des Schaltflächen Bilds genau mit dem entsprechenden Bereich in der Hintergrund Datei übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d6893-118">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="d6893-119">Dies ist wichtig, denn wenn der Benutzer auf eine Schaltfläche vom Typ "Treffer" tippt, ersetzt das gesamte Rechteck, das für das übersetzte Bild definiert ist, den entsprechenden Bereich in der Hintergrund Datei.</span><span class="sxs-lookup"><span data-stu-id="d6893-119">This is important, because when the user taps a hit-type button, the entire rectangle defined for the pushed image will replace the matching area in the Background file.</span></span> <span data-ttu-id="d6893-120">Halten Sie die Grafik mit dem Hintergrundbild konsistent, um sicherzustellen, dass sich nur die Teile der Schaltfläche, die unterschiedlich angezeigt werden sollen, tatsächlich ändern.</span><span class="sxs-lookup"><span data-stu-id="d6893-120">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6893-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6893-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6893-122">**Kunstdateien**</span><span class="sxs-lookup"><span data-stu-id="d6893-122">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




