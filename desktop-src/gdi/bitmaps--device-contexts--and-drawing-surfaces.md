---
description: Ein Gerätekontext (DC) ist eine Datenstruktur, die die Grafikobjekte, die zugehörigen Attribute und die Grafikmodi definiert, die sich auf die Ausgabe auf einem Gerät beeinflussen. Um einen DC zu erstellen, rufen Sie die CreateDC-Funktion auf. um einen DC abzurufen, rufen Sie die GetDC-Funktion auf.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Bitmaps, Gerätekontexte und Zeichnungsoberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed42215dc98ce179f9d36ddc0a24244c018c4177287d1fdfff974a2814e14d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966390"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a>Bitmaps, Gerätekontexte und Zeichnungsoberflächen

Ein *Gerätekontext* (DC) ist eine Datenstruktur, die die Grafikobjekte, ihre zugeordneten Attribute und die Grafikmodi definiert, die sich auf die Ausgabe auf einem Gerät beeinflussen. Um einen DC zu erstellen, rufen Sie die [**CreateDC-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) auf. Um einen DC abzurufen, rufen Sie die [**GetDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdc) auf.

Vor der Rückgabe eines Ziehpunkts, der diesen Domänencontroller identifiziert, wählt das System eine Zeichenoberfläche in den DC aus. Wenn die Anwendung die [**CreateDC-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) aufgerufen hat, um einen Gerätekontext für eine VGA-Anzeige zu erstellen, sind die Abmessungen dieser Zeichenoberfläche 640 x 480 Pixel. Wenn die Anwendung die [**GetDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdc) aufgerufen hat, spiegeln die Dimensionen die Größe des Clientbereichs wider.

Bevor eine Anwendung mit dem Zeichnen beginnen kann, muss sie eine Bitmap mit der entsprechenden Breite und Höhe im DC auswählen, indem die [**SelectObject-Funktion aufruft.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Wenn eine Anwendung das Handle an den Domänencontroller an eine der GDI-Zeichnungsfunktionen (Graphics Device Interface) übergibt, wird die angeforderte Ausgabe auf der im DC ausgewählten Zeichenoberfläche angezeigt.

Weitere Informationen finden Sie unter [Speichergerätekontexte.](memory-device-contexts.md)

 

 



