---
description: Nachdem eine Anwendung einen Anzeige- oder Druckerdomänencontroller erstellt hat, kann sie mit dem Zeichnen auf dem zugeordneten Gerät beginnen, oder im Fall des Speicherdomänencontrollers kann sie mit dem Zeichnen auf der bitmap beginnen, die im Arbeitsspeicher gespeichert ist.
ms.assetid: 73657a66-9415-4db0-a800-463c3d639240
title: Vorgänge für Grafikobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ae7467e04f53196c839b6daa72482ab73845c3185208eb3cb886cb0ce6a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965620"
---
# <a name="operations-on-graphic-objects"></a>Vorgänge für Grafikobjekte

Nachdem eine Anwendung einen Anzeige- oder Druckerdomänencontroller erstellt hat, kann sie mit dem Zeichnen auf dem zugeordneten Gerät beginnen, oder im Fall des Speicherdomänencontrollers kann sie mit dem Zeichnen auf der bitmap beginnen, die im Arbeitsspeicher gespeichert ist. Bevor das Zeichnen beginnt und manchmal während des Zeichnens, ist es jedoch häufig erforderlich, die Standardobjekte durch neue Objekte zu ersetzen.

Eine Anwendung kann die Attribute eines Standardobjekts untersuchen, indem sie die Funktionen [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) und [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) aufruft. Die **GetCurrentObject-Funktion** gibt ein Handle zurück, das den aktuellen Stift, Pinsel, die Aktuelle Palette, Bitmap oder Schriftart identifiziert, und die **GetObject-Funktion** initialisiert eine -Struktur, die die Attribute dieses Objekts enthält.

Einige Drucker stellen residente Stifte, Pinsel und Schriftarten bereit, die verwendet werden können, um die Zeichnungsgeschwindigkeit in einer Anwendung zu verbessern. Zum Aufzählen dieser Objekte können zwei Funktionen verwendet werden: [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) und [**EnumFontFamilies.**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) Wenn die Anwendung residente Stifte oder Pinsel aufzählen muss, kann sie die **EnumObjects-Funktion** aufrufen, um die entsprechenden Attribute zu untersuchen. Wenn die Anwendung residente Schriftarten aufzählen muss, kann sie die **EnumFontFamilies-Funktion** aufrufen (die auch GDI-Schriftarten aufzählen kann).

Sobald eine Anwendung ermittelt, dass ein Standardobjekt ersetzt werden muss, erstellt sie ein neues -Objekt, indem eine der folgenden Erstellungsfunktionen aufgerufen wird.



| Grafikobjekt | Funktion                                                                                                                                                                                                                                                                                                                                                             |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitmap         | [**CreateBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) [**CreateBitmapIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) [**CreateCompatibleBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) [**CreateDiscardableBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                                                                                                           |
| Brush          | [**CreateBrushIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) [**CreateDIBPatternBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush) [**CreateDIBPatternBrushPt,**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) [**CreateHatchBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush) [**CreatePatternBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)                                                 |
| Farbpalette  | [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                               |
| Schriftart           | [**CreateFont,**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) [ **CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                   |
| Stift            | [**CreatePen,**](/windows/desktop/api/Wingdi/nf-wingdi-createpen) [**CreatePenIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect) [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)                                                                                                                                                                                                                                                 |
| Region         | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect), [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn), [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn) |



 

Jede dieser Funktionen gibt ein Handle zurück, das ein neues -Objekt identifiziert. Nachdem eine Anwendung ein Handle abgerufen hat, muss sie die [**SelectObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) aufrufen, um das Standardobjekt zu ersetzen. Die Anwendung sollte jedoch das Handle speichern, das das Standardobjekt identifiziert, und dieses Handle verwenden, um das neue Objekt zu ersetzen, wenn es nicht mehr benötigt wird. Wenn die Anwendung das Zeichnen mit dem neuen Objekt abgeschlossen hat, muss sie das Standardobjekt wiederherstellen, indem sie die **SelectObject-Funktion** aufruft und dann das neue Objekt durch Aufrufen der [**DeleteObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) löscht. Das Nichtlöschen von Objekten führt zu schwerwiegenden Leistungsproblemen.

 

 



