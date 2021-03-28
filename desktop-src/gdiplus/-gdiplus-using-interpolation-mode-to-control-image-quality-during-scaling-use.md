---
description: Der Interpolations Modus eines Grafik Objekts wirkt sich auf die Art und Weise aus, wie Bilder von Windows GDI+ skaliert (gestreckt und verkleinert) werden.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Verwenden des Interpolations Modus zum Steuern der Bildqualität während der Skalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977529"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a><span data-ttu-id="883ff-103">Verwenden des Interpolations Modus zum Steuern der Bildqualität während der Skalierung</span><span class="sxs-lookup"><span data-stu-id="883ff-103">Using Interpolation Mode to Control Image Quality During Scaling</span></span>

<span data-ttu-id="883ff-104">Der Interpolations Modus eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts wirkt sich auf die Art und Weise aus, wie Bilder von Windows GDI+ skaliert (gestreckt und verkleinert) werden.</span><span class="sxs-lookup"><span data-stu-id="883ff-104">The interpolation mode of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object influences the way Windows GDI+ scales (stretches and shrinks) images.</span></span> <span data-ttu-id="883ff-105">Die [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) -Enumeration in "gdiplusenums. h" definiert mehrere Interpolations Modi, von denen einige in der folgenden Liste aufgeführt sind:</span><span class="sxs-lookup"><span data-stu-id="883ff-105">The [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration in Gdiplusenums.h defines several interpolation modes, some of which are shown in the following list:</span></span>

-   <span data-ttu-id="883ff-106">Interpolationmudenearestneighbor</span><span class="sxs-lookup"><span data-stu-id="883ff-106">InterpolationModeNearestNeighbor</span></span>
-   <span data-ttu-id="883ff-107">Interpolationmodebilinear</span><span class="sxs-lookup"><span data-stu-id="883ff-107">InterpolationModeBilinear</span></span>
-   <span data-ttu-id="883ff-108">Interpolationmodehighqualitybilinear</span><span class="sxs-lookup"><span data-stu-id="883ff-108">InterpolationModeHighQualityBilinear</span></span>
-   <span data-ttu-id="883ff-109">Interpolationmodebikubisch</span><span class="sxs-lookup"><span data-stu-id="883ff-109">InterpolationModeBicubic</span></span>
-   <span data-ttu-id="883ff-110">Interpolationmodehighqualitybikubisch</span><span class="sxs-lookup"><span data-stu-id="883ff-110">InterpolationModeHighQualityBicubic</span></span>

<span data-ttu-id="883ff-111">Zum Strecken eines Bilds muss jedes Pixel im ursprünglichen Bild einer Gruppe von Pixeln im größeren Bild zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="883ff-111">To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image.</span></span> <span data-ttu-id="883ff-112">Zum Verkleinern eines Bilds müssen Gruppen von Pixeln im ursprünglichen Bild einem einzelnen Pixel im kleineren Bild zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="883ff-112">To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image.</span></span> <span data-ttu-id="883ff-113">Die Effektivität der Algorithmen, die diese Zuordnungen durchführen, bestimmt die Qualität eines skalierten Bilds.</span><span class="sxs-lookup"><span data-stu-id="883ff-113">The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image.</span></span> <span data-ttu-id="883ff-114">Algorithmen, die skalierbare Images höherer Qualität liefern, erfordern tendenziell mehr Verarbeitungszeit.</span><span class="sxs-lookup"><span data-stu-id="883ff-114">Algorithms that produce higher-quality scaled images tend to require more processing time.</span></span> <span data-ttu-id="883ff-115">In der vorangehenden Liste ist interpolationmudenearestneighbor der Modus mit der niedrigsten Qualität und interpolationmodehighqualitybikubisch der Modus mit der höchsten Qualität.</span><span class="sxs-lookup"><span data-stu-id="883ff-115">In the preceding list, InterpolationModeNearestNeighbor is the lowest-quality mode and InterpolationModeHighQualityBicubic is the highest-quality mode.</span></span>

<span data-ttu-id="883ff-116">Um den Interpolations Modus festzulegen, übergeben Sie einen der Member der [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) -Enumeration an die **setinterpolationmode** -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts.</span><span class="sxs-lookup"><span data-stu-id="883ff-116">To set the interpolation mode, pass one of the members of the [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration to the **SetInterpolationMode** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="883ff-117">Im folgenden Beispiel wird ein Bild gezeichnet und dann mit drei verschiedenen Interpolations Modi verkleinert:</span><span class="sxs-lookup"><span data-stu-id="883ff-117">The following example draws an image and then shrinks the image with three different interpolation modes:</span></span>


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



<span data-ttu-id="883ff-118">Die folgende Abbildung zeigt das ursprüngliche Bild und die drei kleineren Bilder.</span><span class="sxs-lookup"><span data-stu-id="883ff-118">The following illustration shows the original image and the three smaller images.</span></span>

![Abbildung zeigt ein großes ursprüngliches Bild und die drei kleineren Bilder mit unterschiedlicher Qualität](images/grapes1.png)

 

 



