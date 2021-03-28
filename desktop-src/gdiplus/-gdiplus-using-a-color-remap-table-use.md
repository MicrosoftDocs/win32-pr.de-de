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
# <a name="using-a-color-remap-table"></a>Verwenden von Farbneuzuordnungstabellen

Beim Neuzuordnen werden die Farben in einem Bild entsprechend einer Farb Umwandlungs Tabelle umgerechnet. Die Farb Umwandlungs Tabelle ist ein Array von [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) -Strukturen. Jede **ColorMap** -Struktur im Array verfügt über einen **OldColor** -Member und einen **NewColor** -Member.

Wenn GDI+ ein Bild zeichnet, wird jedes Pixel des Bilds mit dem Array Alter Farben verglichen. Wenn die Farbe eines Pixels mit einer alten Farbe übereinstimmt, wird seine Farbe in die entsprechende neue Farbe geändert. Die Farben werden nur für das Rendering geändert – die Farbwerte des Bilds selbst (in einem [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -oder [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt gespeichert) werden nicht geändert.

Um ein neu zugeordnetes Bild zu zeichnen, initialisieren Sie ein Array von [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) -Strukturen. Übergeben Sie die Adresse des Arrays an die [**imageattribute:: SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) -Methode eines [**imageattribute**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) -Objekts, und übergeben Sie dann die Adresse des **imageattributobjekts** an die [DrawImage-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) Methode eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts.

Im folgenden Beispiel wird ein [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus dem Datei RemapInput.bmp erstellt. Der Code erstellt eine Farb Umwandlungs Tabelle, die aus einer einzelnen [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) -Struktur besteht. Der **OldColor** -Member der **ColorMap** -Struktur ist rot, und der **NewColor** -Member ist blau. Das Bild wird einmal ohne Neuzuordnen und einmal mit Neuzuordnung gezeichnet. Der neuzustellungs Prozess ändert alle roten Pixel in blau.


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



Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das neu zugeordnete Bild auf der rechten Seite.

![Abbildung mit zwei Versionen eines mehrfarbigen Bilds der Rote Bereich in der ersten Version ist in der zweiten Version blau.](images/colortrans7.png)

 

 



