---
title: Normale tertiäre Image Quelle
description: Normale tertiäre Image Quelle
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388602"
---
# <a name="normal-tertiary-image-source"></a><span data-ttu-id="27543-108">Normale tertiäre Image Quelle</span><span class="sxs-lookup"><span data-stu-id="27543-108">Normal Tertiary Image Source</span></span>

<span data-ttu-id="27543-109">Die Funktion "playpautsplay" erfordert, dass Sie die Position des normalen Bilds für den tertiären Zustand der Schaltfläche definieren.</span><span class="sxs-lookup"><span data-stu-id="27543-109">The PlayPauseStop button function requires that you define the location of the normal image for the tertiary state of the button.</span></span> <span data-ttu-id="27543-110">Dies ist das Bild, das Benutzern angezeigt wird, nachdem Sie die playpausestopschtaste gedrückt haben, um mit dem Streamen einer Liveübertragung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="27543-110">This will be the image users see after they have pushed the PlayPauseStop button to begin streaming a live broadcast.</span></span>

<span data-ttu-id="27543-111">Um dieses Bild zu definieren, müssen Sie den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="27543-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="27543-112">Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in den zu zeichnenden Bitmaptyp verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="27543-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="27543-113">Wenn Sie z. b. das normale Bild für eine tertiäre Image Quelle definieren möchten, geben Sie Folgendes ein, wenn sich Ihr Image in der über drückten Bitmap befindet:</span><span class="sxs-lookup"><span data-stu-id="27543-113">For example, to define the normal image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 286,0

```



<span data-ttu-id="27543-114">Tertiäre Zustände dürfen kein deaktiviertes Image aufweisen.</span><span class="sxs-lookup"><span data-stu-id="27543-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="27543-115">Es wird davon ausgegangen, dass es sich um die gleiche Breite und Höhe wie die primären und sekundären Images handelt.</span><span class="sxs-lookup"><span data-stu-id="27543-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27543-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27543-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27543-117">**Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="27543-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




