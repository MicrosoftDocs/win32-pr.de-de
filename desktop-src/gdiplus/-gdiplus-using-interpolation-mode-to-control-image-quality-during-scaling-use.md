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
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a>Verwenden des Interpolations Modus zum Steuern der Bildqualität während der Skalierung

Der Interpolations Modus eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts wirkt sich auf die Art und Weise aus, wie Bilder von Windows GDI+ skaliert (gestreckt und verkleinert) werden. Die [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) -Enumeration in "gdiplusenums. h" definiert mehrere Interpolations Modi, von denen einige in der folgenden Liste aufgeführt sind:

-   Interpolationmudenearestneighbor
-   Interpolationmodebilinear
-   Interpolationmodehighqualitybilinear
-   Interpolationmodebikubisch
-   Interpolationmodehighqualitybikubisch

Zum Strecken eines Bilds muss jedes Pixel im ursprünglichen Bild einer Gruppe von Pixeln im größeren Bild zugeordnet werden. Zum Verkleinern eines Bilds müssen Gruppen von Pixeln im ursprünglichen Bild einem einzelnen Pixel im kleineren Bild zugeordnet werden. Die Effektivität der Algorithmen, die diese Zuordnungen durchführen, bestimmt die Qualität eines skalierten Bilds. Algorithmen, die skalierbare Images höherer Qualität liefern, erfordern tendenziell mehr Verarbeitungszeit. In der vorangehenden Liste ist interpolationmudenearestneighbor der Modus mit der niedrigsten Qualität und interpolationmodehighqualitybikubisch der Modus mit der höchsten Qualität.

Um den Interpolations Modus festzulegen, übergeben Sie einen der Member der [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) -Enumeration an die **setinterpolationmode** -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts.

Im folgenden Beispiel wird ein Bild gezeichnet und dann mit drei verschiedenen Interpolations Modi verkleinert:


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

![Abbildung zeigt ein großes ursprüngliches Bild und die drei kleineren Bilder mit unterschiedlicher Qualität](images/grapes1.png)

 

 



