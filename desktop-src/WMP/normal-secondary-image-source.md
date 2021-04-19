---
title: Normale sekundäre Image Quelle
description: Normale sekundäre Image Quelle
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342293"
---
# <a name="normal-secondary-image-source"></a><span data-ttu-id="fd1b6-108">Normale sekundäre Image Quelle</span><span class="sxs-lookup"><span data-stu-id="fd1b6-108">Normal Secondary Image Source</span></span>

<span data-ttu-id="fd1b6-109">Abhängig von der Schaltflächen Funktion müssen Sie möglicherweise den Speicherort des normalen Bilds für den sekundären Zustand der Schaltfläche definieren.</span><span class="sxs-lookup"><span data-stu-id="fd1b6-109">Depending on the button function, you may need to define the location of the normal image for the secondary state of the button.</span></span> <span data-ttu-id="fd1b6-110">Dies ist das Bild, das Benutzern angezeigt wird, wenn Sie beim ersten Mal eine PLAYPAUSE-Funktions Schaltfläche übersetzen.</span><span class="sxs-lookup"><span data-stu-id="fd1b6-110">This will be the image users see when they push a PlayPause function button the first time.</span></span>

<span data-ttu-id="fd1b6-111">Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="fd1b6-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="fd1b6-112">Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in den zu zeichnenden Bitmaptyp verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="fd1b6-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="fd1b6-113">Wenn Sie z. b. das normale Bild für eine sekundäre Bildquelle definieren möchten, geben Sie Folgendes ein, wenn sich das Bild in der über drückten Bitmap befindet:</span><span class="sxs-lookup"><span data-stu-id="fd1b6-113">For example, to define the normal image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 210,0

```



<span data-ttu-id="fd1b6-114">Sekundäre Zustände können nicht über ein deaktiviertes Image verfügen.</span><span class="sxs-lookup"><span data-stu-id="fd1b6-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="fd1b6-115">Bei sekundären Images wird davon ausgegangen, dass Sie dieselbe Breite und Höhe aufweisen wie das primäre Image.</span><span class="sxs-lookup"><span data-stu-id="fd1b6-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd1b6-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd1b6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd1b6-117">**Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="fd1b6-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




