---
title: Schriftart- und Textfunktionen (OpenGL)
description: Die folgenden Funktionen können verwendet werden, um Schriftarten und Text zu verwalten.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- WGL-Funktionen, Text
- WGL-Funktionen, Schriftart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1341dab969178a08e43c1af0a32c4cac817072ad2d5315cd051df2c87ac3c3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082440"
---
# <a name="font-and-text-functions-opengl"></a>Schriftart- und Textfunktionen (OpenGL)

Die folgenden Funktionen können verwendet werden, um Schriftarten und Text zu verwalten.



| Windows Funktion                                 | BESCHREIBUNG                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | Erstellt einen Satz von Zeichenbitmap-Anzeigelisten. Zeichen stammen aus der aktuellen Schriftart eines angegebenen Gerätekontexts. Zeichen werden als aufeinander folgende Ausführung innerhalb des Glyphensatzes der Schriftart angegeben.                                      |
| [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | Erstellt eine Reihe von Anzeigelisten basierend auf den Glyphen der aktuell ausgewählten Konturschriftart eines Gerätekontexts für die Verwendung mit dem aktuellen Renderingkontext. Die Anzeigelisten werden verwendet, um 3D-Zeichen von TrueType-Schriftarten zu zeichnen. |



 

Die Funktionen **wglUseFontBitmaps** und **wglUseFontOutlines** verwenden ein Handle für einen Gerätekontext und verwenden die aktuelle Schriftart dieses Gerätekontexts als Quelle für die Bitmaps. Daher ist es erforderlich, die Schriftart des Gerätekontexts und die Eigenschaften der Schriftart festzulegen, bevor **Sie wglUseFontBitmaps** oder **wglUseFontOutlines** aufrufen.

Die Funktionen [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) und [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) verwenden auch einen Parameter, der das erste Symbol in der Schriftart in eine Bitmapanzeigeliste umschaltet, und einen Parameter, der angibt, wie viele Glyphen in Anzeigelisten umgewandelt werden sollen. Die Funktion erstellt dann Anzeigelisten für die angegebene aufeinander folgende Ausführung von Glyphen. Beispiel:

-   Um einen Satz von 224 Bitmapanzeigelisten für alle Windows Zeichensatz-Glyphen zu erstellen, legen Sie diese beiden Parameter auf 32 bzw. 224 fest.
-   Um einen Satz von 256 Bitmapanzeigelisten für alle OEM-Zeichensatzglyphen zu erstellen, legen Sie diese beiden Parameter auf 0 bzw. 256 fest.
-   Um eine einzelne Bitmapanzeigeliste für ein einzelnes Zeichensatz-Glyphen zu erstellen, legen Sie den zweiten dieser Parameter auf 1 fest.

Die Funktionen **wglUseFontBitmaps** und **wglUseFontOutlines** stellen ein NULL-Symbol in einer Schriftart mit einer leeren Anzeigeliste dar.

Die Anzeigelisten, die durch einen Aufruf von **wglUseFontBitmaps** oder **wglUseFontOutlines** erstellt wurden, werden automatisch nacheinander nummeriert.

Nachdem Sie die Funktion [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) oder [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) aufgerufen haben, rufen Sie [**glCallLists**](glcalllists.md) auf, um eine Zeichenfolge zu zeichnen. Beispielcode finden Sie unter Zeichnen von [Text in einem Double-Buffered OpenGL-Fenster.](drawing-text-in-a-double-buffered-opengl-window.md) In diesem Kontext verwendet **glCallLists** jedes Zeichen in einer Zeichenfolge als Index im Array von aufeinanderfolgenden nummerierten Anzeigelisten, die von **wglUseFontBitmaps** oder **wglUseFontOutlines** erstellt wurden.

Wenn Sie den Zeichnungstext abgeschlossen haben, rufen Sie die [**glDeleteLists-Funktion**](gldeletelists.md) auf, um den zusammenhängenden Satz von Anzeigelisten freizugeben, die von **wglUseFontBitmaps** und **wglUseFontOutlines** erstellt wurden.

 

 




