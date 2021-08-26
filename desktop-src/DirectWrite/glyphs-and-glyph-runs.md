---
title: Glyphen und Glyphenläufe
description: Glyphen und Glyphenläufe sind auf der niedrigsten Funktionalitätsebene der DirectWrite-API, der Glyphenrenderingebene, verfügbar.
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite,Glyphen
- DirectWrite, Glyphenläufe
- Glyphenläufe
- Symbole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39d1ca47249adf11f4e1e2072620f24553f7e299e0690c1cc147c4f74a4939f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902922"
---
# <a name="glyphs-and-glyph-runs"></a>Glyphen und Glyphenläufe

Glyphen und Glyphenläufe sind auf der [](direct-write-portal.md) niedrigsten Funktionalitätsebene der DirectWrite-API, der Glyphenrenderingebene, verfügbar.

## <a name="glyphs"></a>Symbole

Ein Glyph ist eine physische Darstellung eines Zeichens in einer bestimmten Schriftart. Zeichen können viele Glyphen aufweisen, wobei jede Schriftart auf einem System potenziell ein anderes Glyphen für dieses Zeichen definiert.

Zwei oder mehr Glyphen können auch zu einem einzelnen Glyphen kombiniert werden. Dieser Prozess wird als Glyphenkomposition bezeichnet. Dies kann auch in umgekehrter Richtung erfolgen, wobei ein einzelnes Glyphen in mehrere Glyphen aufgeteilt wird, die als Glyphenzerlegung bezeichnet werden.

### <a name="alternate-glyphs"></a>Alternative Glyphen

Schriftarten können alternative Glyphen für Zeichen bereitstellen, z. B. die stilistischen alternativen Glyphen für die Pericles OpenType-Schriftart, wie im folgenden Screenshot gezeigt. Die Zeichen "A", "E" und "O" werden mit stilistischen alternativen Glyphen gerendert.

![Screenshot von "grünem Grün" mit "a", "e" und "o" mit alternativen Symbolen](images/opentypealternateglyphs.png)

Ein weiteres Beispiel für alternative Glyphen sind Schwenkglyphen. Der folgende Screenshot zeigt standard- und swash-Glyphen für die Schriftart Pescadero.

![Screenshot der Buchstaben "a" bis "n" in Standard- und Swash-Glyphen](images/opentypeswashstandard.png)

Swashes und andere typografische Features, einschließlich komplexerer alternativer Glyphen, sind über [OpenType](../intl/opentype-font-format.md)verfügbar. Typografische OpenType-Features können mithilfe von [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) auf einen Textbereich angewendet werden und die [**DWRITE \_ FONT FEATURE \_ TAG-Enumerationskonstante \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) übergeben, die dem gewünschten Feature zugeordnet ist.

## <a name="glyph-runs"></a>Glyphenläufe

Ein Glyphenlauf stellt einen zusammenhängenden Satz von Glyphen dar, die alle die gleiche Schriftfläche und Schriftgröße sowie ggf. denselben Clientzeichnungseffekt aufweisen. Unterstriche und Durchstriche sind nicht Teil der Glyphen-Ausführung für den Textbereich, auf den sie angewendet werden, und werden später gezeichnet. Inlineobjekte, z. B. Bilder, werden ebenfalls separat gezeichnet, da sie nicht Teil einer Schriftart sind.

### <a name="the-idwritefontface-interface"></a>Die IDWriteFontFace-Schnittstelle

[DirectWrite](direct-write-portal.md) verwendet das gleiche System für die Schriftartklassifizierung wie Windows Pesentation Foundation (WPF), sodass pro Schriftfamilie mehrere physische Schriftarten vorhanden sein können. Ein Schriftartengesicht, z. B. die [**IDWriteFontFace-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) in DirectWrite, stellt eine physische Schriftart mit einer bestimmten Gewichtung, einem bestimmten Strich und einer bestimmten Streckung dar. Sie enthält den Schriftarttyp, entsprechende Dateiverweise, Gesichtsidentifikationsdaten und verschiedene Schriftartdaten wie Metriken, Namen und Glyphengliederungen.

Die [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) kann direkt aus einem Schriftartnamen erstellt oder aus einer Schriftartauflistung abgerufen werden.

### <a name="glyph-metrics"></a>Symbolmetriken

Einzelnen Glyphen sind Metriken zugeordnet. Sie können die Metriken für alle Glyphen in einer Glyphen-Ausführung mithilfe der [**IDWriteFontFace::GetDesignGlyphMetrics-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) abrufen. Dadurch wird eine [**DWRITE-GLYPH \_ \_ METRICS-Struktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) zurückgegeben, die über die Vorbreite, die linke und rechte Seite, die obere und untere Seite, die Höhe und den vertikalen Baselineursprung verfügt.

Das folgende Diagramm zeigt verschiedene Metriken von zwei verschiedenen Glyphenzeichen.

![Diagramm der Metriken von zwei verschiedenen Glyphen](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a>Zeichnen einer Glyphen-Ausführung

Beim Implementieren eines benutzerdefinierten Textrenderers wird das Rendern von Glyphen von [**IDWriteTextRenderer::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)behandelt, einer Rückrufmethode, die Sie als Teil einer klasse implementieren, die von [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)abgeleitet ist. Die [**\_ DWRITE-GLYPH \_ RUN-Struktur,**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) die an [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) übergeben wird, enthält ein [**IDWriteFontFace-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) namens *fontFace,* das das Schriftartgesicht für die gesamte Glyphenrun darstellt.

Das [**IDWriteFontFace-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) stellt auch die [**GetGlyphRunOutline-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) bereit, die die Glyphengliederungen mithilfe eines angegebenen Rückrufs der Geometriesenke berechnet, z. B. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) beim Rendern mit [Direct2D.](../direct2d/direct2d-portal.md)

Weitere Informationen finden Sie im Thema [Implementieren eines benutzerdefinierten Textrenderers.](how-to-implement-a-custom-text-renderer.md)

 

 