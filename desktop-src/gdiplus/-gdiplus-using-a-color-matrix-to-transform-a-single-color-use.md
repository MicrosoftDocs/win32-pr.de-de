---
description: Windows GDI+ stellt die Image-und Bitmap-Klassen zum Speichern und Bearbeiten von Bildern bereit.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Verwenden einer Farbmatrix zum Transformieren einer einzelnen Farbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565513"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a>Verwenden einer Farbmatrix zum Transformieren einer einzelnen Farbe

Windows GDI+ stellt die [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -und [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klassen zum Speichern und Bearbeiten von Bildern bereit. **Image** -und **Bitmap** -Objekte speichern die Farbe jedes Pixels als 32-Bit-Zahl: 8 Bits für Rot, grün, blau und alpha. Jede der vier Komponenten ist eine Zahl zwischen 0 und 255, wobei 0 keine Intensität und 255 die volle Intensität darstellt. Die Alpha Komponente gibt die Transparenz der Farbe an: 0 ist vollständig transparent, und 255 ist vollständig undurchsichtig.

Ein Farb Vektor ist ein 4-Tupel im Formular (rot, grün, blau, Alpha). Der Farb Vektor (0, 255, 0, 255) stellt z. b. eine nicht transparente Farbe dar, die nicht rot oder blau ist, aber grün mit voller Intensität aufweist.

Eine weitere Konvention für das darstellen von Farben verwendet die Zahl 1 für die maximale Intensität und die Zahl 0 für die minimale Intensität. Mithilfe dieser Konvention würde die im vorangehenden Absatz beschriebene Farbe durch den Vektor (0, 1, 0, 1) dargestellt werden. GDI+ verwendet die Konvention 1 als vollständige Intensität, wenn Farb Transformationen durchführt werden.

Sie können lineare Transformationen (Drehung, Skalierung und ähnliches) auf Farb Vektoren anwenden, indem Sie eine Multiplikation mit einer 4 × 4-Matrix durchführen. Es ist jedoch nicht möglich, eine 4 × 4-Matrix zum Durchführen einer Übersetzung (Nonlinear) zu verwenden. Wenn Sie jedem der Farb Vektoren eine dummyminietkoordinate (z. b. die Zahl 1) hinzufügen, können Sie eine beliebige Kombination aus linearen Transformationen und Übersetzungen mit einer 5 × 5-Matrix anwenden. Eine Transformation, die aus einer linearen Transformation, gefolgt von einer Übersetzung, besteht, wird als affine Transformation bezeichnet. Eine 5 × 5-Matrix, die eine affine-Transformation darstellt, wird für eine Transformation mit vier Leerzeichen als homogene Matrix bezeichnet. Das-Element in der fünften Zeile und fünften Spalte einer homogenen 5 × 5-Matrix muss 1 sein, und alle anderen Einträge in der fünften Spalte müssen 0 (null) sein.

Nehmen Sie beispielsweise an, Sie möchten mit der Farbe (0,2, 0,0, 0,4, 1,0) beginnen und die folgenden Transformationen anwenden:

1.  Doppelte der roten Komponente
2.  Fügen Sie 0,2 der roten, grünen und blauen Komponenten hinzu.

Die folgende Matrix Multiplikation führt das Transformations Paar in der aufgeführten Reihenfolge aus.

![Abbildung, die eine 5x1-Matrix mit Zahlen multipliziert mit einer 5 x 5-Matrix zum Erstellen einer neuen 5x1-Matrix anzeigt](images/recoloring01.png)

Die Elemente einer Farbmatrix werden nach Zeile und Spalte indiziert (null basiert). Der Eintrag in der fünften Zeile und die dritte Spalte der Matrix m werden z. b. durch M \[ 4 \] \[ 2 angegeben \] .

Die 5 × 5-Identitätsmatrix (in der folgenden Abbildung dargestellt) verfügt über 1 s auf der diagonalen und an allen anderen Orten. Wenn Sie einen Farb Vektor anhand der Identitätsmatrix multiplizieren, wird der Farb Vektor nicht geändert. Eine bequeme Möglichkeit zum bilden der Matrix einer Farb Transformation besteht darin, mit der Identitätsmatrix zu beginnen und eine kleine Änderung vorzunehmen, die die gewünschte Transformation erzeugt.

![Abbildung, die eine 5 x 5-Identitätsmatrix zeigt 1 s oben links nach unten rechts Diagonal und 0s überall sonst](images/recoloring02.png)

Eine ausführlichere Erörterung von Matrizen und Transformationen finden Sie unter [Koordinatensysteme und Transformationen](-gdiplus-coordinate-systems-and-transformations-about.md).

Im folgenden Beispiel wird ein Bild mit allen Farben (0,2, 0,0, 0,4, 1,0) angenommen, und die in den vorherigen Abschnitten beschriebene Transformation wird angewendet.


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das transformierte Bild auf der rechten Seite.

![Darstellung eines Rechtecks, das durch eine dunkle voll Tonfarbe und dann durch eine hellere voll Tonfarbe gefüllt ist ](images/colortrans1.png)

Der Code im vorherigen Beispiel führt die folgenden Schritte aus, um die Neueinfärbung durchzuführen:

1.  Initialisieren Sie eine [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) -Struktur.
2.  Erstellen Sie ein [**imageattributobjekt**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , und übergeben Sie die Adresse der [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) -Struktur an die [**imageattribute:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) -Methode des **imageattribute** -Objekts.
3.  Übergeben Sie die Adresse des [**imageattributobjekts**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) an die [DrawImage-Methoden](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) Methode eines [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts.

 

 



