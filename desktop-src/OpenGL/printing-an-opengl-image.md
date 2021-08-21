---
title: Drucken eines OpenGL-Bilds
description: Sie können OpenGL-Bilder drucken, die in erweiterten Metadateien gerendert werden.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL auf Windows,Drucken
- Drucken von OpenGL-Bildern OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d5cb2e08a247ad8ebd5d333a8a680b57e38a3fc1a9c2281dfb2bd8671f4c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980704"
---
# <a name="printing-an-opengl-image"></a>Drucken eines OpenGL-Bilds

Sie können OpenGL-Bilder drucken, die in erweiterten Metadateien gerendert werden. Wenn Sie auf einem Druckergerät (HDC) rendern, muss es durch einen Metafile-Spooler gesichert werden. OpenGL verwendet Arbeitsspeicher für Tiefe, Farbe und andere Puffer, um die Grafikausgabe auf einem Drucker zu speichern. Da die typische Druckerauflösung eine beträchtliche Menge an Arbeitsspeicher zum Speichern der Grafikausgabe erfordert, benötigt das Drucken eines OpenGL-Bilds möglicherweise mehr Arbeitsspeicher als im System verfügbar ist. Um diese Einschränkung zu umgehen, druckt die aktuelle Implementierung von OpenGL OpenGL-Grafiken in Bändern. Dies erhöht jedoch die Zeit, die zum Drucken von OpenGL-Bildern benötigt wird.

Bevor Sie ein OpenGL-Image drucken, müssen Sie die [StartDoc-Funktion](/windows/desktop/api/wingdi/nf-wingdi-startdoca) aufrufen, um die Initialisierung eines Druckergerätekontexts (DC) abzuschließen. Nach dem Aufruf von **StartDoc** können Sie Renderingkontexte (HGLRC) zum Rendern auf dem Druckergerät erstellen. Wenn Sie Renderingkontexte vor dem Aufruf von **StartDoc** erstellen, gibt es keine Möglichkeit, zu bestimmen, ob eine Metadatei gespoolt wird.

Das folgende Codebeispiel zeigt, wie Sie ein OpenGL-Bild drucken:

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

Weitere Informationen zur Verwendung von Metadateien finden Sie unter [Erweiterte Metadateivorgänge.](/windows/desktop/gdi/enhanced-metafile-operations)

 

 