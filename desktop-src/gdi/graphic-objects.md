---
description: Der mit einem Domänen Controller verknüpfte Stift, Pinsel, Bitmap, Palette, Bereich und Pfad werden als Grafik Objekte bezeichnet. Die folgenden Attribute sind jedem dieser Objekte zugeordnet.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Grafikobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993983"
---
# <a name="graphic-objects"></a>Grafikobjekte

Der mit einem Domänen Controller verknüpfte Stift, Pinsel, Bitmap, Palette, Bereich und Pfad werden als Grafik Objekte bezeichnet. Die folgenden Attribute sind jedem dieser Objekte zugeordnet.



| Grafik Objekt | Zugeordnete Attribute                                                               |
|----------------|-------------------------------------------------------------------------------------|
| Bitmap         | Größe in Bytes Dimensionen in Pixel; Farb Format; Komprimierungs Schema; Und so weiter. |
| Brush          | Stil, Farbe, Muster und Ursprung.                                                  |
| Palette        | Farben und Größe (oder Anzahl von Farben).                                              |
| Schriftart           | Schriftart Name, Breite, Höhe, Gewichtung, Zeichensatz usw.                     |
| `Path`           | Gebildet.                                                                              |
| Stift            | Stil, Breite und Farbe.                                                            |
| Region         | Speicherort und Dimensionen.                                                            |



 

Wenn eine Anwendung einen DC erstellt, speichert das System automatisch eine Reihe von Standardobjekten darin (es gibt keine Standard Bitmap oder einen Standardpfad). Eine Anwendung kann die Attribute der Standardobjekte überprüfen, indem Sie die [**getcurrentobject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) -und [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) -Funktionen aufrufen. Die Anwendung kann diese Standardeinstellungen ändern, indem ein neues-Objekt erstellt und in den DC ausgewählt wird. Ein Objekt wird durch Aufrufen der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion in einem Domänen Controller ausgewählt.

Eine Anwendung kann die aktuelle Pinsel Farbe mit [**setdcbrushcolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)auf einen angegebenen Farbwert festlegen.

Die [**getdcbrushcolor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) -Funktion gibt die DC-Pinsel Farbe zurück. Die Funktion [**setdcpencolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) legt die Stift Farbe auf einen angegebenen Farbwert fest. Die [**getdcpencolor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) -Funktion gibt die DC-Stift Farbe zurück.

 

 



