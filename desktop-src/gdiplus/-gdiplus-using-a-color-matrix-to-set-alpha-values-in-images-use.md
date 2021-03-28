---
description: Die Bitmap-Klasse (die von der Image-Klasse erbt) und die imageattributeklasse bieten Funktionen zum erhalten und Festlegen von Pixelwerten.
ms.assetid: e3d67431-6098-4b2a-8910-5695a8473216
title: Verwenden einer Farbmatrix zum Festlegen von Alphawerten in Bildern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81180b1f09b11e37b322e37106dab1879a00bbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526060"
---
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a>Verwenden einer Farbmatrix zum Festlegen von Alphawerten in Bildern

Die [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klasse (die von der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse erbt) und die [**imageattributeklasse**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) bieten Funktionen zum erhalten und Festlegen von Pixelwerten. Sie können die **imageattribute** -Klasse verwenden, um die Alpha Werte für ein gesamtes Bild zu ändern, oder Sie können die [**Bitmap:: SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) -Methode der **Bitmap** -Klasse aufrufen, um einzelne Pixelwerte zu ändern. Weitere Informationen zum Festlegen einzelner Pixelwerte finden Sie unter [Setting the alphavalues of Individual Pixels](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).

Im folgenden Beispiel wird eine breite schwarze Linie gezeichnet und dann ein nicht transparentes Bild angezeigt, das einen Teil dieser Zeile abdeckt.


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



Die folgende Abbildung zeigt das resultierende Bild, das bei (30, 0) gezeichnet wird. Beachten Sie, dass die breite schwarze Linie nicht durch das Bild angezeigt wird.

![Abbildung: ein undurchsichtiges Bild, das ein schlankes, breites, schwarzes Rechteck überlappt](images/image1.png)

Die [**imageattribute**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) -Klasse verfügt über zahlreiche Eigenschaften, mit denen Sie Bilder während des Renderings ändern können. Im folgenden Beispiel wird ein **imageattributobjekt** verwendet, um alle Alpha Werte auf 80 Prozent ihrer Werte festzulegen. Dies erfolgt durch Initialisieren einer Farbmatrix und Festlegen des alphaskalierungswerts in der Matrix auf 0,8. Die Adresse der Farbmatrix wird an die [**imageattributs:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) -Methode des **imageattribute** -Objekts und die Adresse des **imageattribute** -Objekts an die [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) -Methode eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts übermittelt.


```
// Create a Bitmap object and load it with the texture image.
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// Initialize the color matrix.
// Notice the value 0.8 in row 4, column 4.
ColorMatrix colorMatrix = {1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.8f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
// Create an ImageAttributes object and set its color matrix.
ImageAttributes imageAtt;
imageAtt.SetColorMatrix(&colorMatrix, ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw the semitransparent bitmap image.
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
graphics.DrawImage(
   &bitmap, 
   Rect(30, 0, iWidth, iHeight),  // Destination rectangle
   0,                             // Source rectangle X 
   0,                             // Source rectangle Y
   iWidth,                        // Source rectangle width
   iHeight,                       // Source rectangle height
   UnitPixel, 
   &imageAtt);
```



Während des Renderings werden die Alpha Werte in der Bitmap in 80 Prozent ihrer Art konvertiert. Dies führt zu einem Bild, das mit dem Hintergrund kombiniert wird. Wie die folgende Abbildung zeigt, sieht das Bitmap-Bild transparent aus. Sie sehen, dass die schwarze Linie durchlaufen wird.

![die Abbildung ähnelt der vorherigen, aber das Bild ist mit dem Typ ""](images/image2.png)

Wenn sich das Bild über dem weißen Teil des Hintergrunds befindet, wurde das Bild mit der Farbe weiß gemischt. Wenn das Bild die schwarze Linie überschreitet, wird das Bild mit der Farbe schwarz gemischt.

 

 



