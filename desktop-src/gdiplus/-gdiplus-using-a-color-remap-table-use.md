---
description: Beim Neuzuordnen werden die Farben in einem Bild entsprechend einer Farb Umwandlungs Tabelle umgerechnet. Die Farb Umwandlungs Tabelle ist ein Array von ColorMap-Strukturen. Jede ColorMap-Struktur im Array verfügt über einen OldColor-Member und einen NewColor-Member.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Verwenden von Farbneuzuordnungstabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129056"
---
# <a name="using-a-color-remap-table"></a><span data-ttu-id="10df7-105">Verwenden von Farbneuzuordnungstabellen</span><span class="sxs-lookup"><span data-stu-id="10df7-105">Using a Color Remap Table</span></span>

<span data-ttu-id="10df7-106">Beim Neuzuordnen werden die Farben in einem Bild entsprechend einer Farb Umwandlungs Tabelle umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="10df7-106">Remapping is the process of converting the colors in an image according to a color remap table.</span></span> <span data-ttu-id="10df7-107">Die Farb Umwandlungs Tabelle ist ein Array von [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="10df7-107">The color remap table is an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="10df7-108">Jede **ColorMap** -Struktur im Array verfügt über einen **OldColor** -Member und einen **NewColor** -Member.</span><span class="sxs-lookup"><span data-stu-id="10df7-108">Each **ColorMap** structure in the array has an **oldColor** member and a **newColor** member.</span></span>

<span data-ttu-id="10df7-109">Wenn GDI+ ein Bild zeichnet, wird jedes Pixel des Bilds mit dem Array Alter Farben verglichen.</span><span class="sxs-lookup"><span data-stu-id="10df7-109">When GDI+ draws an image, each pixel of the image is compared to the array of old colors.</span></span> <span data-ttu-id="10df7-110">Wenn die Farbe eines Pixels mit einer alten Farbe übereinstimmt, wird seine Farbe in die entsprechende neue Farbe geändert.</span><span class="sxs-lookup"><span data-stu-id="10df7-110">If a pixel's color matches an old color, its color is changed to the corresponding new color.</span></span> <span data-ttu-id="10df7-111">Die Farben werden nur für das Rendering geändert – die Farbwerte des Bilds selbst (in einem [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -oder [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt gespeichert) werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="10df7-111">The colors are changed only for rendering — the color values of the image itself (stored in an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object) are not changed.</span></span>

<span data-ttu-id="10df7-112">Um ein neu zugeordnetes Bild zu zeichnen, initialisieren Sie ein Array von [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="10df7-112">To draw a remapped image, initialize an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="10df7-113">Übergeben Sie die Adresse des Arrays an die [**imageattribute:: SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) -Methode eines [**imageattribute**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) -Objekts, und übergeben Sie dann die Adresse des **imageattributobjekts** an die [DrawImage-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) Methode eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts.</span><span class="sxs-lookup"><span data-stu-id="10df7-113">Pass the address of that array to the [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) method of an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object, and then pass the address of the **ImageAttributes** object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="10df7-114">Im folgenden Beispiel wird ein [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei RemapInput.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="10df7-114">The following example creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file RemapInput.bmp.</span></span> <span data-ttu-id="10df7-115">Der Code erstellt eine Farb Umwandlungs Tabelle, die aus einer einzelnen [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) -Struktur besteht.</span><span class="sxs-lookup"><span data-stu-id="10df7-115">The code creates a color remap table that consists of a single [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structure.</span></span> <span data-ttu-id="10df7-116">Der **OldColor** -Member der **ColorMap** -Struktur ist rot, und der **NewColor** -Member ist blau.</span><span class="sxs-lookup"><span data-stu-id="10df7-116">The **oldColor** member of the **ColorMap** structure is red, and the **newColor** member is blue.</span></span> <span data-ttu-id="10df7-117">Das Bild wird einmal ohne Neuzuordnen und einmal mit Neuzuordnung gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="10df7-117">The image is drawn once without remapping and once with remapping.</span></span> <span data-ttu-id="10df7-118">Der neuzustellungs Prozess ändert alle roten Pixel in blau.</span><span class="sxs-lookup"><span data-stu-id="10df7-118">The remapping process changes all the red pixels to blue.</span></span>


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="10df7-119">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das neu zugeordnete Bild auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="10df7-119">The following illustration shows the original image on the left and the remapped image on the right.</span></span>

![Abbildung mit zwei Versionen eines mehrfarbigen Bilds der Rote Bereich in der ersten Version ist in der zweiten Version blau.](images/colortrans7.png)

 

 



