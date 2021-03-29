---
description: Ein Gerätekontext (DC) ist eine Datenstruktur, die die Grafik Objekte, ihre zugeordneten Attribute und die Grafikmodi zum beeinflussen der Ausgabe auf einem Gerät definiert. Um einen Domänen Controller zu erstellen, rufen Sie die Funktion "-Funktion" auf. Rufen Sie zum Abrufen eines DC die GetDC-Funktion auf.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Bitmaps, Geräte Kontexte und Zeichnungs Oberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215216"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a>Bitmaps, Geräte Kontexte und Zeichnungs Oberflächen

Ein *Gerätekontext* (DC) ist eine Datenstruktur, die die Grafik Objekte, ihre zugeordneten Attribute und die Grafikmodi zum beeinflussen der Ausgabe auf einem Gerät definiert. Um einen Domänen Controller zu erstellen, rufen Sie [**die Funktion "**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) -Funktion" auf. Rufen Sie zum Abrufen eines DC die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion auf.

Vor dem Zurückgeben eines Handles, das diesen DC identifiziert, wählt das System eine Zeichen Oberfläche in den DC aus. Wenn die Anwendung die Funktion " [**deedc**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) " aufgerufen hat, um einen Gerätekontext für eine VGA-Anzeige zu erstellen, sind die Dimensionen dieser Zeichnungs Oberfläche 640 x 480 Pixel. Wenn die Anwendung die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -Funktion aufrief, entsprechen die Dimensionen der Größe des Client Bereichs.

Bevor eine Anwendung mit dem Zeichnen beginnen kann, muss Sie durch Aufrufen der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion eine Bitmap mit der entsprechenden Breite und Höhe in den DC auswählen. Wenn eine Anwendung das Handle an den Domänen Controller an eine der Zeichenfunktionen der Grafikgeräte Schnittstelle (GDI) übergibt, wird die angeforderte Ausgabe auf der Zeichen Oberfläche angezeigt, die im DC ausgewählt ist.

Weitere Informationen finden Sie unter Arbeits [Speicher-Geräte Kontexte](memory-device-contexts.md).

 

 



