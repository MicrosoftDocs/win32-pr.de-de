---
title: Ziehpunkt Bildquelle
description: Ziehpunkt Bildquelle
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player Mobile Skins, trackbars
- Skins, trackbars
- Verweis für Skins, trackbars
- trackbars in Skins, Bildquelle
- trackbars in Skins, Thumb-Bildquelle
- Bildquelle für Skins, trackbars
- Thumb, Bildquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036624"
---
# <a name="thumb-image-source"></a><span data-ttu-id="7301c-110">Ziehpunkt Bildquelle</span><span class="sxs-lookup"><span data-stu-id="7301c-110">Thumb Image Source</span></span>

<span data-ttu-id="7301c-111">Sie müssen den Namen der Datei definieren, die das Thumb-Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="7301c-111">You must define the name of the file that contains the thumb image.</span></span> <span data-ttu-id="7301c-112">Dies muss ein gültiger Dateiname mit der Erweiterung BMP, GIF, JPG oder PNG sein.</span><span class="sxs-lookup"><span data-stu-id="7301c-112">This must be a valid file name with the extension .bmp, .gif, .jpg, or .png.</span></span> <span data-ttu-id="7301c-113">Die Datei muss drei nebeneinander Abbilder gleicher Größe enthalten.</span><span class="sxs-lookup"><span data-stu-id="7301c-113">The file must contain three side-by-side images of identical size.</span></span> <span data-ttu-id="7301c-114">Sie müssen einander nebeneinander und ohne Leerzeichen dazwischen liegen.</span><span class="sxs-lookup"><span data-stu-id="7301c-114">They must be adjacent to each other with no space between.</span></span> <span data-ttu-id="7301c-115">Die linke obere Position des linken Bilds muss sich in der linken oberen Ecke der Datei befinden.</span><span class="sxs-lookup"><span data-stu-id="7301c-115">The top-left position of the left image must be at the top-left corner of the file.</span></span> <span data-ttu-id="7301c-116">Das Bild auf der linken Seite ist das normale Bild für das Ziehpunkt Bild, und das Bild in der Mitte zeigt den gedrückten Zustand an, und das Bild auf der rechten Seite stellt den deaktivierten Zustand dar.</span><span class="sxs-lookup"><span data-stu-id="7301c-116">The image on the left side is the normal image for the thumb image, and the image in the middle depicts the pushed state and the image on the right depicts the disabled state.</span></span>


```C++
SeekThumb.bmp

```



<span data-ttu-id="7301c-117">Möglicherweise möchten Sie bestimmte Bereiche des Thumb-Bilds transparent machen.</span><span class="sxs-lookup"><span data-stu-id="7301c-117">You may want to make certain areas of the thumb image transparent.</span></span> <span data-ttu-id="7301c-118">Auf diese Weise können Sie Thumb-Bilder in anderen Formen als rechteckig erstellen.</span><span class="sxs-lookup"><span data-stu-id="7301c-118">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="7301c-119">Jeder Bereich des Zieh Punkts, den Sie mit der Farbe ausfüllen, die durch den RGB-Wert 255, 0, 255 angegeben wird, wird in der Skin als transparent angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7301c-119">Any region of the thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7301c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7301c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7301c-121">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="7301c-121">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




