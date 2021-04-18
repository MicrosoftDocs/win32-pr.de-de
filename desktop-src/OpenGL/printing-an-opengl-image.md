---
title: Drucken eines OpenGL-Bilds
description: Sie können die in erweiterten Metadateien gerenderten OpenGL-Bilder drucken.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL unter Windows, Drucken
- Drucken von OpenGL-Bildern OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338287"
---
# <a name="printing-an-opengl-image"></a>Drucken eines OpenGL-Bilds

Sie können die in erweiterten Metadateien gerenderten OpenGL-Bilder drucken. Wenn Sie zu einem Druckergerät (HDC) gerenden werden, muss es von einem metadateispooler unterstützt werden. OpenGL verwendet Arbeitsspeicher für tiefe, Farbe und andere Puffer zum Speichern der Grafikausgabe an einen Drucker. Da bei der normalen Drucker Auflösung eine beträchtliche Menge an Arbeitsspeicher zum Speichern der Grafikausgabe erforderlich ist, ist für das Drucken eines OpenGL-Images möglicherweise mehr Arbeitsspeicher erforderlich, als im System verfügbar ist. Um diese Einschränkung zu umgehen, druckt die aktuelle Implementierung von OpenGL OpenGL-Grafiken in Bändern. Dies erhöht jedoch die Zeit, die zum Drucken von OpenGL-Bildern benötigt wird.

Vor dem Drucken eines OpenGL-Bilds müssen Sie die [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) -Funktion aufrufen, um die Initialisierung eines Drucker Geräte Kontexts (DC) abzuschließen. Nachdem Sie **StartDoc** aufgerufen haben, können Sie renderingkontexte (hglrc) erstellen, die auf dem Druckergerät gerendert werden. Wenn Sie vor dem Aufrufen von **StartDoc** renderingkontexte erstellen, gibt es keine Möglichkeit, zu bestimmen, ob eine Metadatei gespoolte ist.

Im folgenden Codebeispiel wird gezeigt, wie ein OpenGL-Bild gedruckt wird:

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

Weitere Informationen zur Verwendung von Metadateien finden Sie unter [erweiterte Metafile-Vorgänge](/windows/desktop/gdi/enhanced-metafile-operations).

 

 