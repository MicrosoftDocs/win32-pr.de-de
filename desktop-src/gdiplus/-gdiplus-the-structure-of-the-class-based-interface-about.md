---
description: Die C++-Schnittstelle zu Windows GDI+ enthält ungefähr 40 Klassen, 50 Enumerationen und 6 Strukturen. Es gibt auch einige Funktionen, die keine Member einer Klasse sind.
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: Struktur der klassenbasierten Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2627d695330c316a57c2593e75233d73b27a1524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993742"
---
# <a name="the-structure-of-the-class-based-interface"></a>Struktur der klassenbasierten Schnittstelle

Die C++-Schnittstelle zu Windows GDI+ enthält ungefähr 40 Klassen, 50 Enumerationen und 6 Strukturen. Es gibt auch einige Funktionen, die keine Member einer Klasse sind.

Sie müssen angeben, dass der Namespace gdiplus verwendet wird, bevor GDI+-Funktionen aufgerufen werden. Die folgende Anweisung gibt an, dass der gdiplus-Namespace in der Anwendung verwendet wird.

`using namespace Gdiplus;`

Die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse ist der Kern der GDI+-Schnittstelle. Dabei handelt es sich um die Klasse, die tatsächlich Linien, Kurven, Abbildungen, Bilder und Text zeichnet.

Viele Klassenarbeiten zusammen mit der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse. Beispielsweise empfängt die [Grafik::D rawline](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode einen Zeiger auf ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt, das Attribute (Farbe, Breite, Strich Stil und ähnliches) der zu Zeichenden Linie enthält. Die [Graphics:: fillrechteck](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) -Methode kann einen Zeiger auf ein [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) -Objekt erhalten, das mit dem **Grafik** Objekt zum Auffüllen eines Rechtecks mit einer allmählich ändernden Farbe verwendet wird. [**Schriftart**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) -und [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) -Objekte beeinflussen die Art und Weise, wie ein **Grafik** Objekt Text zeichnet. Ein [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Objekt speichert und manipuliert die weltweite Transformation eines **Grafik** Objekts, das zum drehen, skalieren und Kippen von Bildern verwendet wird.

Bestimmte Klassen dienen in erster Linie als strukturierte Datentypen. Einige dieser Klassen (z. b. " [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect)", " [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)" und " [**size**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)") sind für allgemeine Zwecke vorgesehen. Andere sind für spezielle Zwecke bestimmt und werden als Hilfsklassen angesehen. Beispielsweise ist die [**BitmapData**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) -Klasse ein Hilfsobjekt für die [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klasse, und die [**PathData**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) -Klasse ist ein Hilfsprogramm für die [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) -Klasse. GDI+ definiert außerdem einige Strukturen, die zum Organisieren von Daten verwendet werden. Die [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) -Struktur enthält z. b. ein paar von [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Objekten, die einen Eintrag in einer Farb Konvertierungstabelle bilden.

GDI+ definiert mehrere Enumerationen, bei denen es sich um Auflistungen verwandter Konstanten handelt. Die [**LineJoin**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) -Enumeration enthält z. b. die Elemente [* * * * linejoinbevel * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin), [* * * * linejoinmiter * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)und [* * * * linejoinround * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* *, die Stile angeben, die zum Verknüpfen von zwei Zeilen verwendet werden können.

GDI+ bietet einige Funktionen, die nicht Teil einer Klasse sind. Zwei dieser Funktionen sind " [**gdipl-Start**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) " und " [**gdiplstartshutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown)". Sie müssen **gdipl-Start** aufrufen, bevor Sie GDI+-Aufrufe ausführen, und Sie müssen **gdipl| Shutdown** aufrufen, wenn Sie die Verwendung von GDI+ abgeschlossen haben.

 

 
