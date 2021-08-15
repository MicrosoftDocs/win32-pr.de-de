---
title: DirectWrite Strukturen
description: DirectWrite definiert die folgenden Strukturen.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite,strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa3d4d98588e3585022bb0887c6224e29d67e0c0d011437526b33ff0bcf1334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815953"
---
# <a name="directwrite-structures"></a>DirectWrite Strukturen

DirectWrite definiert die folgenden Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32) | Stellt Bitmapdaten im BGRA32-Format dar. |
| [**DWRITE \_ CARET \_ METRICS**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | Die [**DWRITE \_ CARET \_ METRICS-Struktur**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) gibt die Metriken für die Ein caretplatzierung in einer Schriftart an. |
| [**DWRITE \_ CLUSTER METRICS (DWRITE-CLUSTERMETRIKEN) \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Enthält Informationen zu einem Glyphencluster. |
| [**DWRITE \_ COLOR \_ F**](dwrite-color-f.md) | Beschreibt die Rot-, Grün-, Blau- und Alphakomponenten einer Farbe. |
| [**DWRITE \_ COLOR \_ GLYPH \_ RUN**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Enthält die Informationen, die von Renderern zum Zeichnen von Glyphenläufen mit Informationen zur Glyphenfarbe benötigt werden. |
| [**DWRITE \_ COLOR \_ GLYPH \_ RUN1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Stellt eine Ausführung eines Farbstrichs dar. Die IDWriteFactory4::TranslateColorGlyphRun-Methode gibt eine geordnete Auflistung von Farbglyphenläufen unterschiedlicher Typen zurück, je nachdem, was die Schriftart unterstützt. |
| [**\_DWRITE-DATEIFRAGMENT \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Stellt einen Bytebereich in einer Schriftartdatei dar. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Stellt den minimalen und maximalen Bereich der möglichen Werte für eine Schriftartachse dar. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Stellt einen Wert für eine Schriftartachse dar. Wird beim Abfragen und Erstellen von Schriftartinstanzen verwendet. |
| [**\_ \_ DWRITE-SCHRIFTARTFEATURE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Gibt Eigenschaften an, die verwendet werden, um typografische Merkmale im aktuellen Schriftartgesicht zu identifizieren und auszuführen. |
| [**METRIKEN FÜR \_ \_ DWRITE-SCHRIFTARTEN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | Die [**DWRITE \_ FONT \_ METRICS-Struktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) gibt die Metriken an, die für alle Glyphen innerhalb des Schriftartengesichts gelten. |
| [**\_METRIKEN DER \_ DWRITE-SCHRIFTART1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | Die [**Struktur DWRITE \_ FONT \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) gibt die Metriken an, die für alle Glyphen innerhalb des Schriftartengesichts gelten. |
| [**DWRITE \_ \_ FONT-EIGENSCHAFT**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Die Schriftarteigenschaft, die zum Filtern von Schriftartsätzen und zum Erstellen eines Schriftartensets mit expliziten Eigenschaften verwendet wird. |
| [**DWRITE \_ GLYPH \_ IMAGE \_ DATA**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Daten für ein einzelnes Glyphen aus GetGlyphImageData. |
| [**\_METRIKEN DES DWRITE-GLYPHEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Gibt die Metriken eines einzelnen Glyphen an. |
| [**\_DWRITE-GLYPHENOFFSET \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | Die optionale Anpassung an die Position eines Glyphen. |
| [**AUSFÜHRUNG DES \_ DWRITE-GLYPHEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Enthält die Informationen, die von Renderern zum Zeichnen von Glyphenläufen benötigt werden. |
| [**BESCHREIBUNG DER \_ AUSFÜHRUNG DES \_ DWRITE-GLYPHEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Enthält zusätzliche Eigenschaften im Zusammenhang mit denen in [**DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**METRIKEN \_ FÜR \_ DWRITE-TREFFERTEST \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Beschreibt den durch einen Treffertest erhaltenen Bereich. |
| [**DWRITE \_ INLINE OBJECT METRICS (INLINEOBJEKTMETRIKEN \_ \_ SCHREIBEN)**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Enthält Eigenschaften, die die geometrische Messung eines anwendungsdefinierten Inlineobjekts beschreiben. |
| [**DWRITE \_ JUSTIFICATION \_ OPPORTUNITY**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | Die [**DWRITE \_ JUSTIFICATION \_ OPPORTUNITY-Struktur**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) gibt Begründungsinformationen pro Glyphe an. |
| [**DWRITE \_ LINE \_ BREAKPOINT**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Linien-Haltepunktmerkmale eines Zeichens. |
| [**DWRITE \_ \_ LINE-METRIKEN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Enthält Informationen zu einer formatierten Textzeile. |
| [**DWRITE \_ LINE \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Enthält Informationen zu einer formatierten Textzeile. |
| [**DWRITE \_ LINE \_ SPACING**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**\_DWRITE-MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | Die [**DWRITE \_ MATRIX-Struktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) gibt die Grafiktransformation an, die auf gerenderte Glyphen angewendet werden soll. |
| [**DWRITE \_ \_ OVERHANG-METRIKEN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Gibt an, wie viele sichtbare DIPs (geräteunabhängige Pixel) jede Seite des Layout- oder Inlineobjekts überschreiten. |
| [**DWRITE \_ PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | Die [**Union DWRITE \_ PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) beschreibt Klassifizierungswerte für Schriftarten, die Sie mit [**IDWriteFont1::GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) verwenden, um die Schriftart auszuwählen und mit ihr zu übereinstimmen. |
| [**DWRITE \_ SCRIPT \_ ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Speichert die Zuordnung von Text und dessen Schreibsystemskript sowie einige Anzeigeattribute. |
| [**EIGENSCHAFTEN DES \_ \_ DWRITE-SKRIPTS**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | Die [**DWRITE \_ SCRIPT \_ PROPERTIES-Struktur**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) gibt Skripteigenschaften für die Ein caretnavigation und -begründung an. |
| [**EIGENSCHAFTEN DER \_ \_ DWRITE-SHAPING-GLYPHEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Enthält die Ausgabeeigenschaften für das Gestalten eines Ausgabeglyphen. |
| [**\_ \_ DWRITE-SHAPING-TEXTEIGENSCHAFTEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Gestalten von Ausgabeeigenschaften für ein Ausgabeglyphen. |
| [**DWRITE \_ STRIKETHROUGH**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Enthält Informationen zur Größe und Platzierung von Durchstreichungen. |
| [**DWRITE \_ TEXT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Enthält die Metriken, die text nach dem Layout zugeordnet sind. |
| [**DWRITE \_ TEXT \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Enthält die Metriken, die text nach dem Layout zugeordnet sind. |
| [**\_DWRITE-TEXTBEREICH \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Gibt einen Bereich von Textpositionen an, in denen das Format in dem Text angewendet wird, der durch ein [**IDWriteTextLayout-Objekt dargestellt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) wird. |
| [**DWRITE \_ TRIMMING**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Gibt die Kürzungsoption für Text an, der das Layoutfeld überläuft.  |
| [**DWRITE TYPOGRAPHIC FEATURES (TYPOGRAFISCHE FEATURES ZUM \_ \_ SCHREIBEN)**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Enthält eine Reihe von typografischen Merkmalen, die während der Textgestaltung angewendet werden sollen. |
| [**DWRITE \_ UNDERLINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Enthält Informationen zu Breite, Stärke, Offset, Ausführungshöhe, Leserichtung und Flussrichtung einer Unterstreichung.  |
| [**DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | Die [**DWRITE \_ UNICODE \_ RANGE-Struktur**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) gibt den Bereich von Unicode-Codepunkten an. |



 

