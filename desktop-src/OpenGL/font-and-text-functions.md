---
title: Schriftart-und Text Funktionen (OpenGL)
description: Die folgenden Funktionen können zum Verwalten von Schriftarten und Text verwendet werden.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- WGL-Funktionen, Text
- WGL-Funktionen, Schriftart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391416"
---
# <a name="font-and-text-functions-opengl"></a>Schriftart-und Text Funktionen (OpenGL)

Die folgenden Funktionen können zum Verwalten von Schriftarten und Text verwendet werden.



| Windows-Funktion                                 | BESCHREIBUNG                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wgluseefontbitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | Erstellt einen Satz von Zeichen Bitmap-Anzeigelisten. Zeichen stammen aus der aktuellen Schriftart eines angegebenen Geräte Kontexts. Zeichen werden als aufeinander folgende Laufzeiten innerhalb des Symbol Satzes der Schriftart angegeben.                                      |
| [**wgluseelfontgliederungen**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | Erstellt einen Satz von anzeigen Listen basierend auf den Symbolen der aktuell ausgewählten Gliederungs Schriftart eines Geräte Kontexts für die Verwendung mit dem aktuellen renderingkontext. Die Anzeigelisten werden verwendet, um 3D-Zeichen von TrueType-Schriftarten zu zeichnen. |



 

Die **wglutarfontbitmaps** -und **wglutarfontgliedungsfunktionen** übernehmen ein Handle für einen Gerätekontext und verwenden die aktuelle Schriftart dieses Geräte Kontexts als Quelle für die Bitmaps. Daher ist es erforderlich, die Schriftart des Geräte Kontexts und die Schriftart Eigenschaften vor dem Aufrufen von **wglusefontbitmaps** oder **wglusefontgliederungen** festzulegen.

Die Funktionen [**wgluseefontbitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) und [**wglusetfontgliederungen**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) verwenden auch einen Parameter, der das erste Symbol in der Schriftart in eine Bitmap-Anzeigeliste verwandelt, und einen Parameter, der angibt, wie viele Symbole in Anzeigelisten umgewandelt werden. Die-Funktion erstellt dann Anzeigelisten für die angegebene aufeinanderfolgende Durchführung von Symbolen. Beispiel:

-   Legen Sie zum Erstellen eines Satzes von 224 Bitmap-Anzeigelisten für alle Symbole des Windows-Zeichensatzes diese beiden Parameter auf 32 bzw. 224 fest.
-   Zum Erstellen eines Satzes von 256 Bitmap-Anzeigelisten für alle OEM-Zeichensatz Symbole legen Sie diese beiden Parameter auf 0 bzw. 256 fest.
-   Legen Sie zum Erstellen einer einzelnen Bitmap-Anzeigeliste für ein beliebiges einzelnes Zeichensatz Symbol den zweiten dieser Parameter auf 1 fest.

Die Funktionen **wgluseefontbitmaps** und **wgluseefontgliederungen** stellen ein NULL-Symbol in einer Schriftart mit einer leeren Anzeigeliste dar.

Die anzeigen Listen, die durch einen **wglu-fontbitmaps** -oder **wglusetfont-** aufrufsbefehl erstellt wurden, werden automatisch nacheinander nummeriert.

Rufen Sie nach dem Aufrufen der [**wgluseefontbitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) -oder [**wglusetfontgliegerfunktion**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) " [**glcalllists**](glcalllists.md) " auf, um eine Zeichenfolge zu zeichnen. Beispielcode finden Sie [unterzeichnen von Text in einem Double-Buffered OpenGL-Fenster](drawing-text-in-a-double-buffered-opengl-window.md) . In diesem Kontext verwendet **glcalllists** die einzelnen Zeichen in einer Zeichenfolge als Index in das Array von in der Reihenfolge nummerierten anzeigen Listen, die von **wglutarfontbitmaps** oder **wglutarfontskizziert** erstellt werden.

Wenn Sie das Zeichnen von Text beenden, rufen Sie die Funktion " [**gldelta etelists**](gldeletelists.md) " auf, um den zusammenhängenden Satz von anzeigen Listen freizugeben, die von **wglusefontbitmaps** und **wglusefontgliedern** erstellt wurden.

 

 




