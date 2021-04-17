---
description: Eine geschlossene Abbildung, wie z. b. ein Rechteck oder eine Ellipse, besteht aus einem Umriss und einem inneren.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pinsel und gefüllte Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567247"
---
# <a name="brushes-and-filled-shapes"></a>Pinsel und gefüllte Formen

Eine geschlossene Abbildung, wie z. b. ein Rechteck oder eine Ellipse, besteht aus einem Umriss und einem inneren. Die Gliederung wird mit einem [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Objekt gezeichnet, und das Innere ist mit einem [**Pinsel**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekt gefüllt. Windows GDI+ bietet verschiedene Pinsel Klassen zum Auffüllen des Inneren von geschlossenen Abbildungen: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)und [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush). Alle diese Klassen erben von der **Brush** -Klasse. Die folgende Abbildung zeigt ein Rechteck, das mit einem Pinsel gefüllt ist, und eine Ellipse mit einem Schraffurpinsel.

![Darstellung eines blauen Rechtecks und einer Magenta-Ellipse mit einem blauen Schraffurmuster](images/aboutgdip02-art17.png)

 

-   [Vollpinsel](#solid-brushes)
-   [Pinsel Schraffur](#hatch-brushes)
-   [Textur Pinsel](#texture-brushes)
-   [Farbverlaufs Pinsel](#gradient-brushes)

## <a name="solid-brushes"></a>Vollpinsel

Um eine geschlossene Form auszufüllen, benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt und ein [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) -Objekt. Das **graphics** -Objekt stellt Methoden bereit, z. b. [fillrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) und [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), und das **Brush** -Objekt speichert Attribute der Füllung, z. b. Farbe und Muster. Die Adresse des **Pinsel** Objekts wird als eines der Argumente an die Fill-Methode übermittelt. Im folgenden Beispiel wird eine Ellipse mit einer roten Farbe gefüllt.


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



Beachten Sie, dass im vorherigen Beispiel der Pinsel den Typ [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)hat, der von [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)erbt.

## <a name="hatch-brushes"></a>Pinsel Schraffur

Wenn Sie eine Form mit einem Schraffurpinsel ausfüllen, geben Sie eine Vordergrundfarbe, eine Hintergrundfarbe und eine Schraffurart an. Die Vordergrundfarbe ist die Farbe der Schraffur.


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



GDI+ bietet mehr als 50 Schraffurstile, die in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle)angegeben sind. Die drei in der folgenden Abbildung gezeigten Stile sind horizontal, ForwardDiagonal und Cross.

![Abbildung, die drei Teal-farbige Ellipsen anzeigt, die jeweils eine andere Schraffurart haben](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a>Textur Pinsel

Mit einem Textur Pinsel können Sie eine Form mit einem Muster ausfüllen, das in einer Bitmap gespeichert ist. Angenommen, das folgende Bild ist in einer Datenträger Datei mit dem Namen MyTexture.bmp gespeichert.

![Screenshot eines kleinen Quadrats, das mit verschiedenen Farben gefüllt ist](images/aboutgdip02-art19.png)

Im folgenden Beispiel wird eine Ellipse gefüllt, indem das in MyTexture.bmp gespeicherte Bild wiederholt wird.


```
Image myImage(L"MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



Die folgende Abbildung zeigt die gefüllte Ellipse.

![Abbildung, die eine mit dem zuvor definierten Muster Gefüllte Ellipse anzeigt](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a>Farbverlaufs Pinsel

Sie können einen Farbverlaufs Pinsel verwenden, um eine Form mit einer Farbe auszufüllen, die sich allmählich von einem Teil der Form in einen anderen ändert. Ein horizontaler Farbverlaufs Pinsel ändert z. b. die Farbe, wenn Sie von der linken Seite der Abbildung auf die Rechte Seite wechseln. Im folgenden Beispiel wird eine Ellipse mit einem horizontalen Farbverlaufs Pinsel gefüllt, der sich von blau in grün ändert, wenn Sie von der linken Seite der Ellipse auf die Rechte Seite wechseln.


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



Die folgende Abbildung zeigt die gefüllte Ellipse.

![Abbildung, die eine Ellipse mit einem Farbverlaufs Füll Diagramm anzeigt, rechts nach grün Links](images/aboutgdip02-art21.png)

Ein Pinsel mit dem Pfad Farbverlauf kann so konfiguriert werden, dass die Farbe geändert wird, wenn Sie von der Mitte einer Abbildung zur Grenze wechseln.

![Ilustration einer Ellipse, die im Mittelpunkt dunkelblau ist, Schattierung auf hellblau am Rand](images/aboutgdip02-art22.png)

Pfad Farbverlaufs Pinsel sind recht flexibel. Der Farbverlaufs Pinsel, der zum Ausfüllen des Dreiecks in der folgenden Abbildung verwendet wird, ändert sich allmählich von rot in der Mitte zu jeder der drei verschiedenen Farben in den Scheitel Punkten.

![Abbildung eines Dreiecks, das in der Mitte rot ist, und Schattierung in eine andere Farbe an jedem Scheitelpunkt](images/aboutgdip02-art23.png)

 

 



