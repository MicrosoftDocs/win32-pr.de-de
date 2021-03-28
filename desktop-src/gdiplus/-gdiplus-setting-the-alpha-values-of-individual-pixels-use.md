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
# <a name="setting-the-alpha-values-of-individual-pixels"></a><span data-ttu-id="44256-103">Festlegen der Alpha Werte einzelner Pixel</span><span class="sxs-lookup"><span data-stu-id="44256-103">Setting the Alpha Values of Individual Pixels</span></span>

<span data-ttu-id="44256-104">Das Thema [Verwenden einer Farb Matrix zum Festlegen von Alpha Werten in Bildern](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) zeigt eine nicht zerstörerische Methode zum Ändern der Alpha Werte eines Bilds.</span><span class="sxs-lookup"><span data-stu-id="44256-104">The topic [Using a Color Matrix to Set Alpha Values in Images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) shows a nondestructive method for changing the alpha values of an image.</span></span> <span data-ttu-id="44256-105">Im Beispiel in diesem Thema wird ein Bild halbtransparent gerendert, die Pixeldaten in der Bitmap werden jedoch nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="44256-105">The example in that topic renders an image semitransparently, but the pixel data in the bitmap is not changed.</span></span> <span data-ttu-id="44256-106">Die Alpha Werte werden nur während des Renderings geändert.</span><span class="sxs-lookup"><span data-stu-id="44256-106">The alpha values are altered only during rendering.</span></span>

<span data-ttu-id="44256-107">Im folgenden Beispiel wird gezeigt, wie die Alpha Werte einzelner Pixel geändert werden.</span><span class="sxs-lookup"><span data-stu-id="44256-107">The following example shows how to change the alpha values of individual pixels.</span></span> <span data-ttu-id="44256-108">Der Code im Beispiel ändert tatsächlich die Alpha Informationen in einem [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="44256-108">The code in the example actually changes the alpha information in a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="44256-109">Der Ansatz ist weitaus langsamer als die Verwendung einer Farbmatrix und eines [**imageattribute**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) -Objekts, bietet Ihnen jedoch die Kontrolle über die einzelnen Pixel in der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="44256-109">The approach is much slower than using a color matrix and an [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object but gives you control over the individual pixels in the bitmap.</span></span>


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



<span data-ttu-id="44256-110">In der folgenden Abbildung wird das resultierende Bild gezeigt.</span><span class="sxs-lookup"><span data-stu-id="44256-110">The following illustration shows the resulting image.</span></span>

![Abbildung, die ein Bild anzeigt, das von links nach rechts und über ein schwarzes Rechteck transparenter wird](images/image3.png)

<span data-ttu-id="44256-112">Im vorangehenden Codebeispiel wird die Verwendung von geschachtelte Loops zum Ändern des Alphawerts der einzelnen Pixel in der Bitmap verwendet.</span><span class="sxs-lookup"><span data-stu-id="44256-112">The preceding code example uses nested loops to change the alpha value of each pixel in the bitmap.</span></span> <span data-ttu-id="44256-113">Für jedes Pixel ruft [**Bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) die vorhandene Farbe ab, [**Color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) erstellt eine temporäre Farbe, die den neuen Alpha-Wert enthält, und [**Bitmap:: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) legt die neue Farbe fest.</span><span class="sxs-lookup"><span data-stu-id="44256-113">For each pixel, [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) gets the existing color, [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) creates a temporary color that contains the new alpha value, and then [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) sets the new color.</span></span> <span data-ttu-id="44256-114">Der Alpha-Wert wird basierend auf der Spalte der Bitmap festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44256-114">The alpha value is set based on the column of the bitmap.</span></span> <span data-ttu-id="44256-115">In der ersten Spalte wird Alpha auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44256-115">In the first column, alpha is set to 0.</span></span> <span data-ttu-id="44256-116">In der letzten Spalte ist Alpha auf 255 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44256-116">In the last column, alpha is set to 255.</span></span> <span data-ttu-id="44256-117">Daher wird das resultierende Bild von vollständig transparent (auf der linken Seite) in vollständig deckend (am rechten Rand).</span><span class="sxs-lookup"><span data-stu-id="44256-117">So the resulting image goes from fully transparent (on the left edge) to fully opaque (on the right edge).</span></span>

<span data-ttu-id="44256-118">[**Bitmap:: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) und [**Bitmap:: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) gibt Ihnen die Kontrolle über die einzelnen Pixelwerte.</span><span class="sxs-lookup"><span data-stu-id="44256-118">[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) and [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) give you control of the individual pixel values.</span></span> <span data-ttu-id="44256-119">Die Verwendung von **Bitmap:: GetPixel** und **Bitmap:: SetPixel** ist jedoch nicht fast so schnell wie die Verwendung der [**imageattribute**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) -Klasse und der [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="44256-119">However, using **Bitmap::GetPixel** and **Bitmap::SetPixel** is not nearly as fast as using the [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class and the [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>

 

 



