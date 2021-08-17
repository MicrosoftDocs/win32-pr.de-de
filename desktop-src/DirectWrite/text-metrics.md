---
title: Textmetriken
description: Um Ihr Layout, die benutzerdefinierte Schriftartauswahl und andere metrikintensive Vorgänge ab Windows 8 zu unterstützen, verfügt DirectWrite über eine Reihe neuer APIs, um alle Informationen zu Schriftarten auszudrücken, die Sie möglicherweise zum Entwickeln von Rich-Text-Apps benötigen.
ms.assetid: 9df8c675-6f4d-4de7-916e-7dc51f5f04aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e5c5eecce93eac3726195410cf5b215bd65de3d7e48248a68d6d96858f8fed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329240"
---
# <a name="text-metrics"></a>Textmetriken

Um Ihr Layout, die benutzerdefinierte Schriftartauswahl und andere metrikintensive Vorgänge zu unterstützen, verfügt [DirectWrite](direct-write-portal.md) ab Windows 8 über eine Reihe neuer APIs, um alle Informationen zu Schriftarten auszudrücken, die Sie möglicherweise zum Entwickeln von Rich-Text-Apps benötigen.

## <a name="panose"></a>Panose

PANOSE ist ein visuelles Klassifizierungssystem zum Identifizieren von Schriftarten. Die PANOSE-Klassifizierung enthält Informationen zu Familie, Serifenstil, Gewicht, Verhältnis, Kontrast, Strich, Armstil, X-Höhe usw. Diese Informationen beschreiben den visuellen Stil der Schriftart. Diese Informationen sind wichtig, da Schriftarten mit ähnlichen PANOSE-Werten ähnlich aussehen. Dies ist sehr nützlich in Situationen, in denen eine Schriftart nicht verfügbar ist und die App auf eine verfügbare Schriftart zurückfallen muss. Wenn Sie PANOSE-Werte für Schriftarten vergleichen, können Sie eine Schriftart auswählen, die der ursprünglichen Schriftart visuell ähnelt.

Um auf die PANOSE-Informationen für eine Schriftart zu zugreifen, verwenden Sie die [**GetPanose-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) auf den Schnittstellen [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) und [**IDWriteFontFace1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) Diese Methode gibt eine [**DWRITE \_ PANOSE-Enumeration**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_panose) zurück, die alle PANOSE-Informationen für diese Schriftart enthält.

## <a name="additional-metrics"></a>Zusätzliche Metriken

Ab Windows 8 unterstützt die [DirectWrite-API](direct-write-portal.md) auch eine Reihe neuer Metriken, um nützliche Informationen zu den Schriftarten für Ihre App auszudrücken. Diese neuen Metriken enthalten diese Informationen.

-   Metriken für linke, rechte, obere und untere Begrenzungsfelde.
-   X- und Y-Positionierung für hoch- und untergestellte Elemente.
-   X- und Y-Skalierungsinformationen für hoch- und untergestellte Elemente.
-   Gibt an, ob die Schriftart typografische Metriken hat.

Diese Informationen sind alle über die neue [**GetMetrics-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics) auf den Schnittstellen [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) und [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) verfügbar. Diese Methode gibt eine [**DWRITE \_ FONT \_ METRICS1-Struktur zurück,**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_font_metrics1) die alle diese Informationen enthält.

## <a name="caret-metrics"></a>Caretmetriken

Zum Erstellen von Textbearbeitungs-Apps benötigen Sie Zugriff auf Informationen zum Zeichnen des Caret-Texts, der durch den Text navigiert. Ab Windows 8 [stellt DirectWrite](direct-write-portal.md) die [**GetCaretMetrics-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics) für die [**Schnittstellen IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) und [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) für dieses Szenario bereit. **GetCaretMetrics gibt eine** [**DWRITE \_ CARET \_ METRICS-Enumeration**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_caret_metrics) zurück, die Informationen über die Steigung und den Offset für die Caretlinie entlang der Baseline enthält.

Diese Informationen sind besonders hilfreich, wenn Sie ihre Caretpiste mit italischem Text entsprechend anpassen möchten.

## <a name="monospaced-discoverability"></a>Monospaced Discoverability

Apps, die es Benutzern ermöglichen, Computercode zu schreiben, verwenden häufig Schriftarten mit Eintasten statt herkömmlicher Schriftarten. So können Sie mehr Kontrolle über die Schriftartauswahl in Apps [haben,](direct-write-portal.md) die sich auf die Entwicklung bezieht, DirectWrite, ob eine Schriftart über die API monospacediert ist. Die [**IsMonospacedFont-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont) für die [**IDWriteFontFace1-Schnittstelle**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) gibt einen booleschen Wert zurück, der angibt, ob die Schriftart monospaced ist.

## <a name="font-name-matching"></a>Abgleich von Schriftartnamen

Rich-Text-Apps wie PDF-Reader müssen Schriftarten in ihren Inhalten mit Schriftarten im System abeinheitlichen können und Zugriff auf die vollständigen Namen von Schriftarten in mehreren Formaten benötigen. So können Sie Schriftarten besser ab passen, [DirectWrite](direct-write-portal.md) eine Enumeration enthält, die vollständige Namensinformationen zu einer Schriftart in vielen Formaten ausdrückt.

Sie verwenden die [**ENUMERATION DWRITE \_ INFORMATIONAL \_ STRING \_ ID,**](/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id) um den vollständigen Namen, PostScript Namen und PostScript CID-Namen einer beliebigen Schriftart im System zu erhalten. Diese Informationen sind nützlich, wenn Sie Schriftarten in Ihrer App mit den entsprechenden Schriftarten auf dem lokalen System abeinheitlichen müssen.

## <a name="glyph-advances"></a>Glyphenvorkungen

Die **GetGlyphAdvances-Methode** für die [**Schnittstellen IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) und [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) übernimmt die Anzahl der Glyphen und Indizes, zu denen Sie Informationen zu Vorrückungen benötigen, und gibt dann die Fortschritte für die in Frage gestellten Glyphen zurück.

## <a name="unicode-ranges"></a>Unicode-Bereiche

Apps, die ihre eigene Schriftartauswahl verarbeiten möchten, benötigen Zugriff auf die Unicode-Bereiche, die von der Schriftart unterstützt werden. Auf diese Weise kann die App eine geeignete Schriftart auswählen, die dieses Symbol enthält, wenn ein Unicode-Codepunkt von der Schriftart nicht unterstützt wird. Ohne diese Informationen kann die App eine Schriftart verwenden, die nicht alle Glyphen enthält, die zum Anzeigen der angezeigten Informationen erforderlich sind.

Die [**GetUnicodeRanges-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges) für die [**Schnittstellen IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) und [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) übernimmt die maximale Anzahl von Bereichen, die vom Client übergeben werden, und gibt die tatsächlichen Bereiche zurück, die von der Schriftart unterstützt werden.

## <a name="eudc-font-collection"></a>EUDC-Schriftartsammlung

Verwenden Sie [**die GetEudcFontCollection-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefactory1-geteudcfontcollection) auf der [**IDWriteFactory1-Schnittstelle,**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) um auf die EUDC-Schriftartenauflistung zu zugreifen. Diese Methode funktioniert auf die gleiche Weise wie [**GetSystemFontCollection,**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection)gibt aber stattdessen einen Zeiger auf eine EUDC-Schriftartauflistung zurück.

 

 