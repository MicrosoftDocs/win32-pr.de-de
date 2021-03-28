---
description: Das Thema Verwenden einer Farb Matrix zum Festlegen von Alpha Werten in Bildern zeigt eine nicht zerstörerische Methode zum Ändern der Alpha Werte eines Bilds.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Festlegen der Alpha Werte einzelner Pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526072"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a>Festlegen der Alpha Werte einzelner Pixel

Das Thema [Verwenden einer Farb Matrix zum Festlegen von Alpha Werten in Bildern](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) zeigt eine nicht zerstörerische Methode zum Ändern der Alpha Werte eines Bilds. Im Beispiel in diesem Thema wird ein Bild halbtransparent gerendert, die Pixeldaten in der Bitmap werden jedoch nicht geändert. Die Alpha Werte werden nur während des Renderings geändert.

Im folgenden Beispiel wird gezeigt, wie die Alpha Werte einzelner Pixel geändert werden. Der Code im Beispiel ändert tatsächlich die Alpha Informationen in einem [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt. Der Ansatz ist weitaus langsamer als die Verwendung einer Farbmatrix und eines [**imageattribute**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) -Objekts, bietet Ihnen jedoch die Kontrolle über die einzelnen Pixel in der Bitmap.


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



In der folgenden Abbildung wird das resultierende Bild gezeigt.

![Abbildung, die ein Bild anzeigt, das von links nach rechts und über ein schwarzes Rechteck transparenter wird](images/image3.png)

Im vorangehenden Codebeispiel wird die Verwendung von geschachtelte Loops zum Ändern des Alphawerts der einzelnen Pixel in der Bitmap verwendet. Für jedes Pixel ruft [**Bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) die vorhandene Farbe ab, [**Color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) erstellt eine temporäre Farbe, die den neuen Alpha-Wert enthält, und [**Bitmap:: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) legt die neue Farbe fest. Der Alpha-Wert wird basierend auf der Spalte der Bitmap festgelegt. In der ersten Spalte wird Alpha auf 0 festgelegt. In der letzten Spalte ist Alpha auf 255 festgelegt. Daher wird das resultierende Bild von vollständig transparent (auf der linken Seite) in vollständig deckend (am rechten Rand).

[**Bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) und [**Bitmap:: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) gibt Ihnen die Kontrolle über die einzelnen Pixelwerte. Die Verwendung von **Bitmap:: GetPixel** und **Bitmap:: SetPixel** ist jedoch nicht fast so schnell wie die Verwendung der [**imageattribute**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) -Klasse und der [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) -Struktur.

 

 



