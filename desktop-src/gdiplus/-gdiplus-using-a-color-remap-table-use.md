---
description: Bei der Neuzuordnung werden die Farben in einem Bild entsprechend einer Farbumrechnungstabelle konvertiert. Die Farbzuordnungstabelle ist ein Array von ColorMap-Strukturen. Jede ColorMap-Struktur im Array verfügt über ein oldColor-Member und ein newColor-Member.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Verwenden von Farbneuzuordnungstabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00f36c493bbdc696fa672b2899d4d7c6d3231a9e40c0e4162b5113d78a67164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036298"
---
# <a name="using-a-color-remap-table"></a>Verwenden von Farbneuzuordnungstabellen

Bei der Neuzuordnung werden die Farben in einem Bild entsprechend einer Farbumrechnungstabelle konvertiert. Die Farbzuordnungstabelle ist ein Array von [**ColorMap-Strukturen.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) Jede **ColorMap-Struktur** im Array verfügt über ein **oldColor-Member** und ein **newColor-Member.**

Wenn GDI+ Bild zeichnet, wird jedes Pixel des Bilds mit dem Array alter Farben verglichen. Wenn die Farbe eines Pixels einer alten Farbe entspricht, wird seine Farbe in die entsprechende neue Farbe geändert. Die Farben werden nur für das Rendering geändert. Die Farbwerte des Bilds selbst (gespeichert in einem [**Bild-**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) oder [**Bitmapobjekt)**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) werden nicht geändert.

Initialisieren Sie ein Array von [**ColorMap-Strukturen,**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) um ein neu zugeordnetes Bild zu zeichnen. Übergeben Sie die Adresse dieses Arrays an die [**ImageAttributes::SetRemapTable-Methode**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) eines [**ImageAttributes-Objekts,**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) und übergeben Sie dann die Adresse des **ImageAttributes-Objekts** an die [DrawImage Methods-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) eines [**Graphics-Objekts.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

Im folgenden Beispiel wird ein [**Image-Objekt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aus der Datei RemapInput.bmp. Der Code erstellt eine Farbzuordnungstabelle, die aus einer einzelnen [**ColorMap-Struktur**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) besteht. Das **oldColor-Member** der **ColorMap-Struktur** ist rot, und das **newColor-Member** ist blau. Das Bild wird einmal ohne Neu- und einmal mit Neuveranschnappung gezeichnet. Bei der Neuveränderung werden alle roten Pixel in Blau geändert.


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



Die folgende Abbildung zeigt das ursprüngliche Bild links und das neu zugeordnete Bild auf der rechten Seite.

![Abbildung, die zwei Versionen eines mehrfarbigen Bilds zeigt; Der rote Bereich in der ersten Version ist in der zweiten Version blau.](images/colortrans7.png)

 

 



