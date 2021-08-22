---
description: Die C++-Schnittstelle zum Windows GDI+ enthält etwa 40 Klassen, 50 Enumerationen und 6 Strukturen. Es gibt auch einige Funktionen, die keine Member einer Klasse sind.
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: Struktur der klassenbasierten Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30909917ad89a65e88c4ca31ca229a5f25d503bced7a9cac81e4199ced1ba7d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830660"
---
# <a name="the-structure-of-the-class-based-interface"></a>Struktur der klassenbasierten Schnittstelle

Die C++-Schnittstelle zum Windows GDI+ enthält etwa 40 Klassen, 50 Enumerationen und 6 Strukturen. Es gibt auch einige Funktionen, die keine Member einer Klasse sind.

Sie müssen angeben, dass der Namespace Gdiplus verwendet wird, bevor GDI+ Funktionen aufgerufen werden. Die folgende Anweisung gibt an, dass der Gdiplus-Namespace in der Anwendung verwendet wird.

`using namespace Gdiplus;`

Die [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ist der Kern der GDI+-Schnittstelle. es ist die Klasse, die tatsächlich Linien, Kurven, Abbildungen, Bilder und Text zeichnet.

Viele Klassen arbeiten mit der [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) zusammen. Beispielsweise empfängt die [Graphics::D rawLine-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) einen Zeiger auf ein [**Stiftobjekt,**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) das Attribute (Farbe, Breite, Bindestrichart usw.) der zu zeichnenden Linie enthält. Die [Graphics::FillRectangle-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) kann einen Zeiger auf ein [**LinearGradientBrush-Objekt**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) empfangen, das mit dem **Graphics-Objekt** zusammenarbeitet, um ein Rechteck mit einer sich allmählich ändernden Farbe auszufüllen. [**Schriftart-**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) und [**StringFormat-Objekte**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) beeinflussen die Art und Weise, wie ein **Graphics-Objekt** Text zeichnet. Ein [**Matrixobjekt**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) speichert und bearbeitet die Welttransformation eines **Grafikobjekts,** das zum Drehen, Skalieren und Spiegeln von Bildern verwendet wird.

Bestimmte Klassen dienen in erster Linie als strukturierte Datentypen. Einige dieser Klassen (z. [**B. Rect,**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)und [**Size)**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)sind für allgemeine Zwecke vorgesehen. Andere dienen speziellen Zwecken und gelten als Hilfsklassen. Beispielsweise ist die [**BitmapData-Klasse**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) ein Hilf hilft für die [**Bitmap-Klasse,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) und die [**PathData-Klasse**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) ist ein Hilf hilft für die [**GraphicsPath-Klasse.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) GDI+ definiert auch einige Strukturen, die zum Organisieren von Daten verwendet werden. Die [**ColorMap-Struktur**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) enthält beispielsweise ein Paar von [**Color-Objekten,**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) die einen Eintrag in einer Farbkonvertierungstabelle bilden.

GDI+ definiert mehrere Enumerationen, bei denen es sich um Auflistungen verwandter Konstanten handelt. Die [**LineJoin-Enumeration**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) enthält beispielsweise die Elemente ["LineJoinBevel",](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) ["*LineJoinMiter"](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)und ["LineJoinRound",](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)die Stile angeben, die zum Verbinden von zwei Zeilen verwendet werden können.

GDI+ stellt einige Funktionen bereit, die nicht Teil einer Klasse sind. Zwei dieser Funktionen sind [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) und [**GdiplusShutdown.**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) Sie müssen **GdiplusStartup** aufrufen, bevor Sie andere GDI+ aufrufen, und Sie müssen **GdiplusShutdown** aufrufen, wenn Sie GDI+ verwendet haben.

 

 
