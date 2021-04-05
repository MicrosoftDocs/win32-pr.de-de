---
title: Quelle für das sekundäre Image
description: Quelle für das sekundäre Image
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037037"
---
# <a name="pushed-secondary-image-source"></a><span data-ttu-id="bb12b-108">Quelle für das sekundäre Image</span><span class="sxs-lookup"><span data-stu-id="bb12b-108">Pushed Secondary Image Source</span></span>

<span data-ttu-id="bb12b-109">Abhängig von der Schaltflächen Funktion müssen Sie möglicherweise den Speicherort des gedrückten Bilds für den sekundären Zustand der Schaltfläche definieren.</span><span class="sxs-lookup"><span data-stu-id="bb12b-109">Depending on the button function, you may need to define the location of the pushed image for the secondary state of the button.</span></span> <span data-ttu-id="bb12b-110">Dies ist das Bild, das Benutzern angezeigt wird, wenn Sie eine PLAYPAUSE-Funktions Schaltfläche beim zweiten Mal pushen.</span><span class="sxs-lookup"><span data-stu-id="bb12b-110">This will be the image users see when they push a PlayPause function button the second time.</span></span>

<span data-ttu-id="bb12b-111">Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="bb12b-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="bb12b-112">Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, aus dem Sie zeichnen möchten.</span><span class="sxs-lookup"><span data-stu-id="bb12b-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the image type you are drawing from.</span></span>

<span data-ttu-id="bb12b-113">Wenn Sie z. b. das pushbild für eine sekundäre Bildquelle definieren möchten, geben Sie Folgendes ein, wenn sich das Bild in der über drückten Bitmap befindet:</span><span class="sxs-lookup"><span data-stu-id="bb12b-113">For example, to define the Pushed image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 248,0

```



<span data-ttu-id="bb12b-114">Sekundäre Zustände können nicht über ein deaktiviertes Image verfügen.</span><span class="sxs-lookup"><span data-stu-id="bb12b-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="bb12b-115">Bei sekundären Images wird davon ausgegangen, dass Sie dieselbe Breite und Höhe aufweisen wie das primäre Image.</span><span class="sxs-lookup"><span data-stu-id="bb12b-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb12b-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb12b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb12b-117">**Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="bb12b-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




