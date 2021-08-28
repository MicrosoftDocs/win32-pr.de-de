---
description: Das Thema Using a Color Matrix to Set Alpha Values in Images (Verwenden einer Farbmatrix zum Festlegen von Alphawerten in Bildern) zeigt eine nicht destruktive Methode zum Ändern der Alphawerte eines Bilds.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Festlegen der Alphawerte einzelner Pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c88c7ef8cc343b99f7a50c3fad012b62ef2a8d79ab38de6988efb6b5643e0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830730"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a>Festlegen der Alphawerte einzelner Pixel

Das Thema [Verwenden einer Farbmatrix zum Festlegen von Alphawerten in](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) Bildern zeigt eine nicht destruktive Methode zum Ändern der Alphawerte eines Bilds. Im Beispiel in diesem Thema wird ein Bild halbtransparent gerendert, aber die Pixeldaten in der Bitmap werden nicht geändert. Die Alphawerte werden nur während des Renderings geändert.

Das folgende Beispiel zeigt, wie die Alphawerte einzelner Pixel geändert werden. Der Code im Beispiel ändert tatsächlich die Alphainformationen in einem [**Bitmap-Objekt.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) Der Ansatz ist viel langsamer als die Verwendung einer Farbmatrix und eines [**ImageAttributes-Objekts,**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) bietet Ihnen jedoch die Kontrolle über die einzelnen Pixel in der Bitmap.


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



Die folgende Abbildung zeigt das resultierende Bild.

![Abbildung eines Bilds, das von links nach rechts über einem schwarzen Rechteck undurchsichtiger wird](images/image3.png)

Im obigen Codebeispiel werden geschachtelte Schleifen verwendet, um den Alphawert jedes Pixels in der Bitmap zu ändern. Für jedes Pixel ruft [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) die vorhandene Farbe ab. [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) erstellt eine temporäre Farbe, die den neuen Alphawert enthält, und legt dann [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) die neue Farbe fest. Der Alphawert wird basierend auf der Spalte der Bitmap festgelegt. In der ersten Spalte ist alpha auf 0 festgelegt. In der letzten Spalte ist alpha auf 255 festgelegt. Das resultierende Bild geht also von vollständig transparent (am linken Rand) zu vollständig deckend (am rechten Rand) über.

[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) und [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) geben Ihnen die Kontrolle über die einzelnen Pixelwerte. Die Verwendung **von Bitmap::GetPixel** und **Bitmap::SetPixel** ist jedoch nicht fast so schnell wie die Verwendung der [**ImageAttributes-Klasse**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) und der [**ColorMatrix-Struktur.**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix)

 

 



