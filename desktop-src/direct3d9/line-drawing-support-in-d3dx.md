---
description: Erfahren Sie mehr über die Unterstützung von Linienzeichnungen in D3DX. D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bietet. Es handelt sich um eine Ebene über der Direct3D-Komponente.
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: Unterstützung für Linienzeichnung in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9cf107615410da6dcfba02d6f708129429e31586360183277fb8f669653d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799681"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>Unterstützung für Linienzeichnung in D3DX (Direct3D 9)

D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bietet. Es handelt sich um eine Ebene über der Direct3D-Komponente.

D3DX unterstützt Einpixelweite Antialiasinglinien. Linienmuster werden nicht mehr unterstützt.

Die Linienzeichnungsbibliothek emuliert Linien mithilfe von Texturdreiecken und geht von Folgendem aus:

-   Hardware ist über die Direct3D 9-Schnittstellen verfügbar.
-   Es ist mindestens eine Texturphase verfügbar.
-   Es werden 64 x 64 Texturen verwendet.
-   Die folgenden Modi sind verfügbar:
    -   Bilineare Filterung
    -   Adressmodus "Klammer"
    -   Adressmodus umschließen
    -   Alpha op modulate
    -   Alphamischung (SRCBLEND = SRC \_ ALPHA, DESTBLEND = INV \_ SRC \_ ALPHA)
    -   Alphatest, wenn alpha blending nicht verfügbar ist; Ergebnis mit niedrigerer Qualität

Verwenden Sie für das Antialiasing von Linienrendering in Multisample-Renderzielen [**ID3DXLine,**](id3dxline.md) wodurch texturierte Polygone generiert werden. Die Pixelabdeckungswerte, die durch antialiasierte Linienrasterung generiert werden, modulieren den alpha-Wert des Pixels, der vom Pixel-Shader berechnet wird. Um eine Antialiasinglinie zu zeichnen, muss eine Anwendung alpha blending aktivieren und dann den D3DRS \_ ANTIALIASEDLINEENABLE-Renderzustand auf **TRUE festlegen.**

## <a name="functionality-description"></a>Funktionsbeschreibung

Die Bibliothek unterstützt das Zeichnen farbiger Linienstreifen mit den folgenden Linienfeatures, die jeweils unabhängig von anderen sind:

-   Linienstärke
-   Zeilenmuster mit Wiederholung (der Zeilenmusterzähler wird mit jedem [**ID3DXLine::D raw-**](id3dxline--draw.md) oder [**ID3DXLine::D rawTransform-Aufruf**](id3dxline--drawtransform.md) zurückgesetzt. Es wird nicht mit jedem Segment des Linienstreifens zurückgesetzt.)
-   Antialiasing
-   OpenGL-Stillinien

> [!Note]  
> Es wird keine Minderung unterstützt.

 

Die Bibliothek verwendet die Native Hardware-Strichzeichnungsunterstützung (sofern auf dem Gerät verfügbar) nur in folgenden Anwendungen:

-   Die Linienbreite ist 1.
-   Es ist kein Linienmuster aktiviert.

Antialiasinglinien mit einem Pixel werden von einigen Hardwarekomponenten unterstützt, daher verwendet die Bibliothek diese, falls verfügbar. Das LineCaps-Mitglied der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) aufzählt Hardwarefunktionen für Grundtypen zum Zeichnen von Linien.

Wenn die Softwarelinienzeichnung verwendet wird, wird jede Linie zu einem Rechteck erweitert, und vier Scheitellinien werden an den Treiber gesendet.

Jedes Liniensegment wird mit zwei Dreiecken gezeichnet. Die Breite des Primitiven ist die angegebene Breite plus 1,0, was zu einer zusätzlichen Zeile oder Spalte von Pixeln führen kann. Wenn die Linie breiter wird, wird der Antialias-Farbverlauf in der Textur ungefährer, und in der Mitte werden mehr vollständig deckende Texel repliziert. Der Farbverlauf wird in v-Richtung der Textur codiert und in der Regel entlang der U-Richtung repliziert. Der Texturadrierungsmodus für v ist "Klammer".

Jedes Liniensegment in der Liste kann als separate Zeile betrachtet werden, die ab dem vorherigen Endpunkt beginnt.

Die Antialiasingqualität entlang der Kanten, die parallel zur Länge der ursprünglichen Linie verlaufen, wird durch die Breite der Linie nicht mehr länger. Es wird erwartet, dass Linienbreiten größer als 32,0 Artefakte entlang dieser Ränder zeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3dx](d3dx.md)
</dt> </dl>

 

 



