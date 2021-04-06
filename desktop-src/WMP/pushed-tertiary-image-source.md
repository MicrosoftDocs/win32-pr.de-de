---
title: Quelle für tertiäres Image übermittelt
description: Quelle für tertiäres Image übermittelt
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947741"
---
# <a name="pushed-tertiary-image-source"></a><span data-ttu-id="a0ee3-108">Quelle für tertiäres Image übermittelt</span><span class="sxs-lookup"><span data-stu-id="a0ee3-108">Pushed Tertiary Image Source</span></span>

<span data-ttu-id="a0ee3-109">Die playpautsstopsfunktion erfordert, dass Sie den Speicherort des gedrückten Bilds für den tertiären Zustand der Schaltfläche definieren.</span><span class="sxs-lookup"><span data-stu-id="a0ee3-109">The PlayPauseStop button function requires that you define the location of the pushed image for the tertiary state of the button.</span></span> <span data-ttu-id="a0ee3-110">Dies ist das Bild, das Benutzern angezeigt wird, wenn Sie die Schaltfläche "playpaust beenden" beim Streaming einer Liveübertragung pushen.</span><span class="sxs-lookup"><span data-stu-id="a0ee3-110">This will be the image users see when they push the PlayPauseStop button while streaming a live broadcast.</span></span>

<span data-ttu-id="a0ee3-111">Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="a0ee3-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="a0ee3-112">Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in den zu zeichnenden Bitmaptyp verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="a0ee3-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="a0ee3-113">Wenn Sie z. b. das pushbild für eine tertiäre Bildquelle definieren möchten, geben Sie Folgendes ein, wenn sich das Bild in der über drückten Bitmap befindet:</span><span class="sxs-lookup"><span data-stu-id="a0ee3-113">For example, to define the pushed image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 324,0

```



<span data-ttu-id="a0ee3-114">Tertiäre Zustände dürfen kein deaktiviertes Image aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a0ee3-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="a0ee3-115">Es wird davon ausgegangen, dass es sich um die gleiche Breite und Höhe wie die primären und sekundären Images handelt.</span><span class="sxs-lookup"><span data-stu-id="a0ee3-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0ee3-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a0ee3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0ee3-117">**Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="a0ee3-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




