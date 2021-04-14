---
description: D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: Zeilen Zeichnungs Unterstützung in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974a0fdeb24dad1107f85e6c79603368776bce15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392690"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>Zeilen Zeichnungs Unterstützung in D3DX (Direct3D 9)

D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.

D3DX unterstützt einzelne Pixel weite, Antialiasing-Zeilen. Zeilen Muster werden nicht mehr unterstützt.

Die Zeilen Zeichnungs Bibliothek emuliert Linien mithilfe von Textur Dreiecken und setzt Folgendes voraus:

-   Hardware ist über die Direct3D 9-Schnittstellen verfügbar.
-   Mindestens eine Textur Phase ist verfügbar.
-   64 x 64-Texturen werden verwendet.
-   Die folgenden Modi sind verfügbar:
    -   Bilineare Filterung
    -   Klammer Adress Modus
    -   Adress Modus Umbruch
    -   Alpha-op-modulieren
    -   Alpha Blending (srcblend = src \_ Alpha, destblend = Inv \_ src \_ Alpha)
    -   Alpha Test, wenn Alpha Blending nicht verfügbar ist; Ergebnis der niedrigeren Qualität

Verwenden Sie zum Rendern von Zeilen mit Antialiasing in Multisampling-Renderingzielen [**ID3DXLine**](id3dxline.md) , mit dem strukturierte Polygone generiert werden. Die Pixel Coverage-Werte, die durch die Zeilen-rasterisierung mit Antialiasing generiert werden, modulieren den Alpha-Wert des Pixels, der durch den Pixelshader berechnet wird. Um eine Antialiasing-Linie zu zeichnen, muss eine Anwendung Alpha Blending aktivieren, und dann muss der D3DRS \_ antialiasedlineenable-Rendering-Zustand auf **true** festgelegt werden.

## <a name="functionality-description"></a>Funktionsbeschreibung

Die Bibliothek unterstützt das Zeichnen farbiger Linien Streifen mit den folgenden Zeilen Features, von denen jede unabhängig voneinander ist:

-   Linienstärke
-   Zeilen Muster mit Wiederholung (der Zeilen Muster-Leistungsindikators wird mit jedem [**ID3DXLine::D RAW**](id3dxline--draw.md) -oder [**ID3DXLine::D rawtransform**](id3dxline--drawtransform.md) -Aufrufsatz zurückgesetzt. Er wird nicht mit den einzelnen Segmenten des Zeilen Streifens zurückgesetzt.)
-   Antialiasing
-   OpenGL-stillinien

> [!Note]  
> Es wird keine mistration unterstützt.

 

Die Bibliothek verwendet systemeigene Zeichnungs Unterstützung für Hardware Linien (falls im Gerät verfügbar) nur, wenn:

-   Die Linienstärke ist 1.
-   Es ist kein Zeilen Muster aktiviert.

Einzelne Pixel weite Antialiasing-Linien werden von Hardware unterstützt, sodass diese von der Bibliothek verwendet wird, falls verfügbar. Der LineCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur listet die Hardwarefunktionen für Zeilen Zeichnungs primitive auf.

Wenn die Software Zeilen Zeichnung verwendet wird, wird jede Zeile in ein Rechteck erweitert, und vier Vertices werden an den Treiber gesendet.

Jedes Liniensegment wird mit zwei Dreiecken gezeichnet. Die Breite des primitiven ist die angegebene Breite Plus 1,0. Dies kann zu einer zusätzlichen Zeile oder Spalte in Pixel führen. Wenn die Linie breiter ist, wird der Farbverlauf des AntiAlias in der Textur immer größer, und die vollständig undurchsichtigeren texeln werden um die Mitte repliziert. Der Farbverlauf wird in der v-Richtung der Textur codiert und normalerweise entlang der u-Richtung repliziert. Der Textur Adressierungs Modus für v ist eine Klammer.

Jedes Zeilen Segment in der Liste kann als separate Zeile betrachtet werden, die am vorherigen Endpunkt beginnt.

Die antialiasingqualität entlang der Kanten, die bis zur Länge der ursprünglichen Zeile parallel ist, weist darauf hin, dass die Linie breiter wird. Es wird erwartet, dass die Linienbreite, die größer als 32,0 ist, die Artefakte entlang dieser Ränder anweist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



