---
description: Der Interpolationsmodus eines Grafikobjekts beeinflusst die Art und Weise, wie bilder Windows GDI+ skaliert (gestreckt und verkleinert) werden.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Verwenden des Interpolationsmodus zum Steuern der Bildqualität während der Skalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fefe314ef680a54f9d885bb185c77b3349e84cbe5f7bcf347cf9ff3fa0a4ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943700"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a>Verwenden des Interpolationsmodus zum Steuern der Bildqualität während der Skalierung

Der Interpolationsmodus eines [**Grafikobjekts**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) beeinflusst die Art und Weise, wie Windows GDI+ Bilder skaliert (gestreckt und verkleinert). Die [**InterpolationMode-Enumeration**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) in Gdiplusenums.h definiert mehrere Interpolationsmodi, von denen einige in der folgenden Liste angezeigt werden:

-   InterpolationModeModeRestNeighbor
-   InterpolationModeBilinear
-   InterpolationModeHighQualityBilinear
-   InterpolationModeBicubic
-   InterpolationModeHighQualityBicubic

Um ein Bild zu strecken, muss jedes Pixel im ursprünglichen Bild einer Gruppe von Pixeln im größeren Bild zugeordnet werden. Um ein Bild zu verkleinern, müssen Gruppen von Pixeln im ursprünglichen Bild einzelnen Pixeln im kleineren Bild zugeordnet werden. Die Effektivität der Algorithmen, die diese Zuordnungen durchführen, bestimmt die Qualität eines skalierten Bilds. Algorithmen, die qualitativ hochwertigere skalierte Bilder erzeugen, erfordern in der Regel mehr Verarbeitungszeit. In der obigen Liste ist InterpolationModeRestNeighbor der Modus mit der niedrigsten Qualität und InterpolationModeHighQualityBicubic der Modus mit der höchsten Qualität.

Um den Interpolationsmodus festzulegen, übergeben Sie einen der Member der [**InterpolationMode-Enumeration**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) an die **SetInterpolationMode-Methode** eines [**Graphics-Objekts.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

Im folgenden Beispiel wird ein Bild zeichnet und dann mit drei verschiedenen Interpolationsmodi verkleinert:


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



Die folgende Abbildung zeigt das ursprüngliche Bild und die drei kleineren Bilder.

![Abbildung eines großen Originalbilds und der drei kleineren Bilder mit unterschiedlicher Qualität](images/grapes1.png)

 

 



