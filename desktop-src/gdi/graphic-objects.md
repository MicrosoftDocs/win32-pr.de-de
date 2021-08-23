---
description: Stift, Pinsel, Bitmap, Palette, Bereich und Pfad, die einem DC zugeordnet sind, werden als grafische Objekte bezeichnet. Die folgenden Attribute sind jedem dieser Objekte zugeordnet.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Grafikobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf256cd8eafd6ee346c12f6658a7c3dd388c94fb4107b010528e47c126fce2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831960"
---
# <a name="graphic-objects"></a>Grafikobjekte

Stift, Pinsel, Bitmap, Palette, Bereich und Pfad, die einem DC zugeordnet sind, werden als grafische Objekte bezeichnet. Die folgenden Attribute sind jedem dieser Objekte zugeordnet.



| Grafikobjekt | Zugeordnete Attribute                                                               |
|----------------|-------------------------------------------------------------------------------------|
| Bitmap         | Größe in Bytes; Dimensionen in Pixel; Farbformat; Komprimierungsschema; Und so weiter. |
| Brush          | Stil, Farbe, Muster und Ursprung.                                                  |
| Palette        | Farben und Größe (oder Anzahl der Farben).                                              |
| Schriftart           | Schriftartname, Breite, Höhe, Gewichtung, Zeichensatz usw.                     |
| Pfad           | Form.                                                                              |
| Stift            | Stil, Breite und Farbe.                                                            |
| Region         | Position und Dimensionen.                                                            |



 

Wenn eine Anwendung einen DC erstellt, speichert das System automatisch einen Satz von Standardobjekten darin (es gibt keine Standardbitmap oder keinen Standardpfad). Eine Anwendung kann die Attribute der Standardobjekte untersuchen, indem sie die Funktionen [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) und [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) aufruft. Die Anwendung kann diese Standardwerte ändern, indem sie ein neues -Objekt erstellt und es auf dem DC auswählt. Ein Objekt wird in einem Domänencontroller durch Aufrufen der [**SelectObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) ausgewählt.

Eine Anwendung kann die aktuelle Pinselfarbe mit [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)auf einen angegebenen Farbwert festlegen.

Die [**GetDCBrushColor-Funktion**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) gibt die DC-Pinselfarbe zurück. Die [**SetDCPenColor-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) legt die Stiftfarbe auf einen angegebenen Farbwert fest. Die [**GetDCPenColor-Funktion**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) gibt die DC-Stiftfarbe zurück.

 

 



