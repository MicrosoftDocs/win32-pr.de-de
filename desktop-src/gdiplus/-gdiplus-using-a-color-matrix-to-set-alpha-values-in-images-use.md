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
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a><span data-ttu-id="0cb3a-103">Verwenden einer Farbmatrix zum Festlegen von Alphawerten in Bildern</span><span class="sxs-lookup"><span data-stu-id="0cb3a-103">Using a Color Matrix to Set Alpha Values in Images</span></span>

<span data-ttu-id="0cb3a-104">Die [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klasse (die von der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse erbt) und die [**imageattributeklasse**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) bieten Funktionen zum erhalten und Festlegen von Pixelwerten.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-104">The [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class (which inherits from the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class) and the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class provide functionality for getting and setting pixel values.</span></span> <span data-ttu-id="0cb3a-105">Sie können die **imageattribute** -Klasse verwenden, um die Alpha Werte für ein gesamtes Bild zu ändern, oder Sie können die [**Bitmap:: SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) -Methode der **Bitmap** -Klasse aufrufen, um einzelne Pixelwerte zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-105">You can use the **ImageAttributes** class to modify the alpha values for an entire image, or you can call the [**Bitmap::SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) method of the **Bitmap** class to modify individual pixel values.</span></span> <span data-ttu-id="0cb3a-106">Weitere Informationen zum Festlegen einzelner Pixelwerte finden Sie unter [Setting the alphavalues of Individual Pixels](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span><span class="sxs-lookup"><span data-stu-id="0cb3a-106">For more information on setting individual pixel values, see [Setting the Alpha Values of Individual Pixels](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span></span>

<span data-ttu-id="0cb3a-107">Im folgenden Beispiel wird eine breite schwarze Linie gezeichnet und dann ein nicht transparentes Bild angezeigt, das einen Teil dieser Zeile abdeckt.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-107">The following example draws a wide black line and then displays an opaque image that covers part of that line.</span></span>


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



<span data-ttu-id="0cb3a-108">Die folgende Abbildung zeigt das resultierende Bild, das bei (30, 0) gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-108">The following illustration shows the resulting image, which is drawn at (30, 0).</span></span> <span data-ttu-id="0cb3a-109">Beachten Sie, dass die breite schwarze Linie nicht durch das Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-109">Note that the wide black line doesn't show through the image.</span></span>

![Abbildung: ein undurchsichtiges Bild, das ein schlankes, breites, schwarzes Rechteck überlappt](images/image1.png)

<span data-ttu-id="0cb3a-111">Die [**imageattribute**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) -Klasse verfügt über zahlreiche Eigenschaften, mit denen Sie Bilder während des Renderings ändern können.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-111">The [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class has many properties that you can use to modify images during rendering.</span></span> <span data-ttu-id="0cb3a-112">Im folgenden Beispiel wird ein **imageattributobjekt** verwendet, um alle Alpha Werte auf 80 Prozent ihrer Werte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-112">In the following example, an **ImageAttributes** object is used to set all the alpha values to 80 percent of what they were.</span></span> <span data-ttu-id="0cb3a-113">Dies erfolgt durch Initialisieren einer Farbmatrix und Festlegen des alphaskalierungswerts in der Matrix auf 0,8.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-113">This is done by initializing a color matrix and setting the alpha scaling value in the matrix to 0.8.</span></span> <span data-ttu-id="0cb3a-114">Die Adresse der Farbmatrix wird an die [**imageattributs:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) -Methode des **imageattribute** -Objekts und die Adresse des **imageattribute** -Objekts an die [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) -Methode eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-114">The address of the color matrix is passed to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object, and the address of the **ImageAttributes** object is passed to the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


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



<span data-ttu-id="0cb3a-115">Während des Renderings werden die Alpha Werte in der Bitmap in 80 Prozent ihrer Art konvertiert.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-115">During rendering, the alpha values in the bitmap are converted to 80 percent of what they were.</span></span> <span data-ttu-id="0cb3a-116">Dies führt zu einem Bild, das mit dem Hintergrund kombiniert wird.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-116">This results in an image that is blended with the background.</span></span> <span data-ttu-id="0cb3a-117">Wie die folgende Abbildung zeigt, sieht das Bitmap-Bild transparent aus. Sie sehen, dass die schwarze Linie durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-117">As the following illustration shows, the bitmap image looks transparent; you can see the solid black line through it.</span></span>

![die Abbildung ähnelt der vorherigen, aber das Bild ist mit dem Typ ""](images/image2.png)

<span data-ttu-id="0cb3a-119">Wenn sich das Bild über dem weißen Teil des Hintergrunds befindet, wurde das Bild mit der Farbe weiß gemischt.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-119">Where the image is over the white portion of the background, the image has been blended with the color white.</span></span> <span data-ttu-id="0cb3a-120">Wenn das Bild die schwarze Linie überschreitet, wird das Bild mit der Farbe schwarz gemischt.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-120">Where the image crosses the black line, the image is blended with the color black.</span></span>

 

 



