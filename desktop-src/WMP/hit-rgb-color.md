---
title: RGB-Farbe
description: RGB-Farbe
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Farben
- Skins, Schaltflächen Farben
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Farben
- Farb Verweis für Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340640"
---
# <a name="hit-rgb-color"></a><span data-ttu-id="217f0-108">RGB-Farbe</span><span class="sxs-lookup"><span data-stu-id="217f0-108">Hit RGB Color</span></span>

<span data-ttu-id="217f0-109">Wenn Sie die Bereichs Schaltflächen (pushhit, degglehit und 2pushhit) verwenden, müssen Sie die Farbe definieren, mit der Windows Media Player den Trefferbereich der Schaltfläche bestimmen soll.</span><span class="sxs-lookup"><span data-stu-id="217f0-109">If you are using region buttons (PushHit, ToggleHit, and 2PushHit), you must define the color that Windows Media Player will use to determine the hit area of your button.</span></span> <span data-ttu-id="217f0-110">Dieser Wert muss mithilfe von drei positiven ganzen Zahlen angegeben werden, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="217f0-110">This value must be specified using three positive integers separated by commas.</span></span> <span data-ttu-id="217f0-111">Diese ganzen Zahlen stellen die Menge von rot, grün und blau für eine bitmapfarbe dar und reichen von 0 bis 255.</span><span class="sxs-lookup"><span data-stu-id="217f0-111">These integers represent the amount of red, green, and blue for a bitmap color, and range from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="217f0-112">Schaltflächen Typen sind in Skins für Windows Media Player 10 Mobile oder höher veraltet.</span><span class="sxs-lookup"><span data-stu-id="217f0-112">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="217f0-113">Sie können für die Werte beliebige Farben verwenden. Stellen Sie jedoch sicher, dass jede von Ihnen definierte Regions Schaltfläche eine eindeutige Farbe in der Regions Bilddatei aufweist und dass der Farbwert, den Sie hier als Zahl definieren, mit der im Regions Bild verwendeten tatsächlichen Farbe übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="217f0-113">You can use any colors for the values, but be sure that each region button you define has a unique color in the Region image file and that the color value you define here as a number matches the actual color used in the Region image.</span></span>

<span data-ttu-id="217f0-114">In der folgenden Tabelle werden einige typische Farben angezeigt, die Sie möglicherweise verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="217f0-114">The following table shows some typical colors you might want to use.</span></span>



| <span data-ttu-id="217f0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="217f0-115">Value</span></span>       | <span data-ttu-id="217f0-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="217f0-116">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="217f0-117">0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="217f0-117">0,0,0</span></span>       | <span data-ttu-id="217f0-118">Schwarz</span><span class="sxs-lookup"><span data-stu-id="217f0-118">Black</span></span>       |
| <span data-ttu-id="217f0-119">255.255.255</span><span class="sxs-lookup"><span data-stu-id="217f0-119">255,255,255</span></span> | <span data-ttu-id="217f0-120">Weiß</span><span class="sxs-lookup"><span data-stu-id="217f0-120">White</span></span>       |
| <span data-ttu-id="217f0-121">255, 0, 0</span><span class="sxs-lookup"><span data-stu-id="217f0-121">255,0,0</span></span>     | <span data-ttu-id="217f0-122">Red</span><span class="sxs-lookup"><span data-stu-id="217f0-122">Red</span></span>         |
| <span data-ttu-id="217f0-123">RGB, 0</span><span class="sxs-lookup"><span data-stu-id="217f0-123">0,255,0</span></span>     | <span data-ttu-id="217f0-124">Grün</span><span class="sxs-lookup"><span data-stu-id="217f0-124">Green</span></span>       |
| <span data-ttu-id="217f0-125">0, RGB</span><span class="sxs-lookup"><span data-stu-id="217f0-125">0,0,255</span></span>     | <span data-ttu-id="217f0-126">Blau</span><span class="sxs-lookup"><span data-stu-id="217f0-126">Blue</span></span>        |



 

<span data-ttu-id="217f0-127">Wenn Sie keine Bereichs Schaltflächen verwenden, müssen Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="217f0-127">If you do not use region buttons, you must enter the following:</span></span>


```C++
0,0,0

```



## <a name="related-topics"></a><span data-ttu-id="217f0-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="217f0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="217f0-129">**Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="217f0-129">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




