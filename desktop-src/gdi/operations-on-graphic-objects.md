---
description: Nachdem eine Anwendung eine Anzeige oder einen Drucker-DC erstellt hat, kann Sie mit dem Zeichnen auf dem zugeordneten Gerät beginnen, oder im Fall des Speicher-DC kann Sie mit dem Zeichnen der im Arbeitsspeicher gespeicherten Bitmap beginnen.
ms.assetid: 73657a66-9415-4db0-a800-463c3d639240
title: Vorgänge für Grafik Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0574b8527dbf83b4cb4a38163dcf7b33017336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978489"
---
# <a name="operations-on-graphic-objects"></a>Vorgänge für Grafik Objekte

Nachdem eine Anwendung eine Anzeige oder einen Drucker-DC erstellt hat, kann Sie mit dem Zeichnen auf dem zugeordneten Gerät beginnen, oder im Fall des Speicher-DC kann Sie mit dem Zeichnen der im Arbeitsspeicher gespeicherten Bitmap beginnen. Allerdings ist es oft erforderlich, die Standardobjekte durch neue Objekte zu ersetzen, bevor das Zeichnen beginnt, und manchmal während des Zeichnens.

Eine Anwendung kann die Attribute eines Standard Objekts überprüfen, indem Sie die Funktionen [**getcurrentobject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) und [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) aufruft. Die **getcurrentobject** -Funktion gibt ein Handle zurück, das den aktuellen Stift, den Pinsel, die Palette, die Bitmap oder die Schriftart identifiziert, und die **GetObject** -Funktion initialisiert eine-Struktur, die die Attribute dieses Objekts enthält.

Einige Drucker stellen residente Stifte, Pinsel und Schriftarten bereit, die zur Verbesserung der Zeichnungs Geschwindigkeit in einer Anwendung verwendet werden können. Zwei Funktionen können verwendet werden, um diese Objekte aufzulisten: " [**enumeriubjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) " und " [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)". Wenn die Anwendung residente Stifte oder Pinsel aufzählen muss, kann Sie die **enumubjects** -Funktion zum Überprüfen der entsprechenden Attribute aufruft. Wenn die Anwendung residente Schriftarten aufzählen muss, kann Sie die **EnumFontFamilies** -Funktion (die GDI-Schriftarten ebenfalls auflisten kann) aufzurufen.

Sobald eine Anwendung ermittelt, dass ein Standard Objekt ersetzt werden muss, wird ein neues-Objekt erstellt, indem eine der folgenden Erstellungs Funktionen aufgerufen wird.



| Grafik Objekt | Funktion                                                                                                                                                                                                                                                                                                                                                             |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitmap         | " [**Kreatebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)", " [**kreatebitmapindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)", " [**kreatecompatiblebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap)", " [**kreateverwerdablebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)", " [**kreatedibitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) "                                                                                                           |
| Brush          | " [**Kreatebrushindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)", " [**kreatedibpatternbrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)", " [**kreatedibpatternbrushpt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt)", " [**kreatehatchbrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)", " [**kreatepatternbrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)", " [**kreatesolidbrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) "                                                 |
| Farbpalette  | [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                               |
| Schriftart           | " [**Kreatefont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)", " [ **kreatefontindirekte** "](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                   |
| Stift            | " [**Kreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)", " [**kreateperindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)", " [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) "                                                                                                                                                                                                                                                 |
| Region         | " [**Kreateellipticrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)", " [**kreateellipticrgnindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)", " [**kreatepolygonrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)", " [**kreatepolypolygonrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)", " [**kreaterectrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)", " [**kreaterectrgnindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)", " [**kreateroundrectrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn) " |



 

Jede dieser Funktionen gibt ein Handle zurück, das ein neues-Objekt identifiziert. Nachdem eine Anwendung ein Handle abgerufen hat, muss Sie die [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion aufrufen, um das Standard Objekt zu ersetzen. Die Anwendung sollte jedoch das Handle speichern, das das Standard Objekt identifiziert, und dieses Handle verwenden, um das neue Objekt zu ersetzen, wenn es nicht mehr benötigt wird. Wenn die Anwendung das Zeichnen mit dem neuen Objekt abgeschlossen hat, muss Sie das Standard Objekt wiederherstellen, indem Sie die **SelectObject** -Funktion aufrufen und dann das neue-Objekt durch Aufrufen der [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) -Funktion löschen. Fehler beim Löschen von Objekten verursachen schwerwiegende Leistungsprobleme.

 

 



