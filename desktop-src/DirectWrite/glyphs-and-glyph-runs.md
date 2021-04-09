---
title: Symbole und Glyphe werden ausgeführt
description: Symbole und Glyphe sind auf der niedrigsten Funktionsebene der DirectWrite-API verfügbar, der Symbol Rendering-Ebene.
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite, Glyphen
- DirectWrite, Glyphe Ausführungen
- Glyphe Ausführungen
- Symbole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c5c6b30c9a44cde4704e6afd231cebbc91d2be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101858"
---
# <a name="glyphs-and-glyph-runs"></a>Symbole und Glyphe werden ausgeführt

Symbole und Glyphe sind auf der niedrigsten Funktionsebene der [DirectWrite](direct-write-portal.md) -API verfügbar, der Symbol Rendering-Ebene.

## <a name="glyphs"></a>Symbole

Ein Symbol ist eine physische Darstellung eines Zeichens in einer angegebenen Schriftart. Zeichen können viele Glyphen aufweisen, wobei jede Schriftart in einem System möglicherweise ein anderes Symbol für dieses Zeichen definiert.

Zwei oder mehr Symbole können auch zu einem einzigen Symbol kombiniert werden. dieser Prozess wird als Symbol Komposition bezeichnet. Dies kann auch in umgekehrter Richtung erfolgen, wobei ein einzelnes Symbol in mehrere Symbole aufgeteilt wird, die als Symbol Zerlegung bezeichnet werden.

### <a name="alternate-glyphs"></a>Alternative Symbole

Schriftarten können alternative Symbole für Zeichen bereitstellen, z. b. die alternativen Stil Symbole für die Schriftart "Pericles OpenType", wie im folgenden Screenshot gezeigt. Die Zeichen "A", "E" und "O" werden mit alternativen Alternativen Symbolen gerendert.

![Screenshot der "alten grünen Mythologie" mit "a", "e" und "o" mithilfe alternativer Symbole](images/opentypealternateglyphs.png)

Ein weiteres Beispiel für alternative Glyphen sind Swash-Symbole. Der folgende Screenshot zeigt Standard-und Swash-Symbole für die Schriftart Pescadero.

![Screenshot der Buchstaben "a" bis "n" in den Symbolen "Standard" und "Swash"](images/opentypeswashstandard.png)

Swashes und andere typografische Features, einschließlich ausführlichere Alternative Symbole, sind über [OpenType](../intl/opentype-font-format.md)verfügbar. Die Funktionen von OpenType typografische können auf einen Textbereich angewendet werden, indem [**idschreitetextlayout:: settypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) verwendet und die der gewünschten Funktion zugeordnete Enumerationskonstante für das [**dwrite- \_ Schriftart \_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) übergeben wird.

## <a name="glyph-runs"></a>Glyphe Ausführungen

Eine Glyphe stellt einen zusammenhängenden Satz von Symbolen dar, die alle die gleiche Schriftart und Größe aufweisen, sowie den gleichen Client Zeichnungs Effekt, falls vorhanden. Unterstreichung und durchgestrichen sind nicht Teil der Symbol Suche für den Textbereich, auf den Sie angewendet werden, und werden später gezeichnet. Inline Objekte (z. b. Bilder) werden auch separat gezeichnet, da Sie nicht Teil einer Schriftart sind.

### <a name="the-idwritefontface-interface"></a>Die idschreitefontface-Schnittstelle

[DirectWrite](direct-write-portal.md) verwendet das gleiche System für die Schriftart Klassifizierung wie Windows pesentation Foundation (WPF), sodass mehrere physische Schriftarten pro Schriftfamilie vorhanden sein können. Ein Schriftart, z. b. die [**idschreitefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) -Schnittstelle in DirectWrite, stellt eine physische Schriftart mit einer bestimmten Gewichtung, einem Schrägstrich und einer Streckung dar. Sie enthält den Schriftart Elementtyp, die entsprechenden Datei Verweise, Gesichts Identifizierungs Daten und verschiedene Schriftart Daten wie z. b. Metriken, Namen und Symbol Kontur.

[**Idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) kann direkt aus einem Schriftart Namen erstellt oder aus einer Schriftart Auflistung abgerufen werden.

### <a name="glyph-metrics"></a>Symbolmetriken

Einzelnen Symbolen sind Metriken zugeordnet. Sie können die Metriken für alle Symbole in einem Symbol mit der [**idwrite-fontface:: getdesignglyphmetrics**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) -Methode abrufen. Dies gibt eine [**dwrite-Symbol \_ \_ Metrik**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) -Struktur zurück, die über die erweiterte Breite, die linke und die Rechte Seite, die obere und untere Seite, die Höhe und den vertikalen Baseline-Ursprung verfügt.

Das folgende Diagramm zeigt verschiedene Metriken von zwei verschiedenen Symbol Zeichen.

![Diagramm der Metriken zweier verschiedener Symbole](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a>Zeichnen eines Glyphe-Laufs

Beim Implementieren eines benutzerdefinierten textrenderers wird das Rendering von Symbolen durch den [**idwrite-TextRenderer behandelt::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), eine Rückruf Methode, die Sie als Teil einer Klasse implementieren, die von [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)abgeleitet ist. Die an [**DrawGlyphRun an DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) über gegebene [**dwrite-Symbol \_ \_ Lauf**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) Struktur enthält ein [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) -Objekt mit dem Namen *fontface*, das die Schriftart für die gesamte Symbol Ausführung darstellt.

Das [**idwrite-fontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) -Objekt stellt außerdem die [**getglyphrunumriss**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) -Methode bereit, die die Symbol Gliederung mithilfe eines angegebenen Geometry-senkrückrufs berechnet, z. b. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) beim Rendern mit [Direct2D](../direct2d/direct2d-portal.md).

Weitere Informationen finden Sie im Thema [Implementieren eines benutzerdefinierten textrenderers](how-to-implement-a-custom-text-renderer.md) .

 

 