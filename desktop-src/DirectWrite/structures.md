---
title: DirectWrite Strukturen
description: DirectWrite definiert die folgenden Strukturen.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite,Strukturen
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

| Thema | Beschreibung |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32) | Stellt Bitmapdaten im BGRA32-Format dar. |
| [**DWRITE \_ \_ CARET-METRIKEN**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | Die [**DWRITE \_ CARET \_ METRICS-Struktur**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) gibt die Metriken für die Platzierung von Caretzeichen in einer Schriftart an. |
| [**\_DWRITE-CLUSTERMETRIKEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Enthält Informationen zu einem Glyphencluster. |
| [**DWRITE \_ COLOR \_ F**](dwrite-color-f.md) | Beschreibt die Rot-, Grün-, Blau- und Alphakomponenten einer Farbe. |
| [**DWRITE \_ COLOR \_ GLYPH \_ RUN**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Enthält die Informationen, die Renderer zum Zeichnen von Glyphenläufen mit Informationen zur Glyphenfarbe benötigen. |
| [**DWRITE \_ COLOR \_ GLYPH \_ RUN1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Stellt eine Farbglyphen-Ausführung dar. Die IDWriteFactory4::TranslateColorGlyphRun-Methode gibt je nach unterstützter Schriftart eine geordnete Auflistung von Farbglyphenläufen unterschiedlicher Typen zurück. |
| [**\_DWRITE-DATEIFRAGMENT \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Stellt einen Bytebereich in einer Schriftartdatei dar. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Stellt den minimalen und maximalen Bereich der möglichen Werte für eine Schriftartachse dar. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Stellt einen Wert für eine Schriftartachse dar. Wird beim Abfragen und Erstellen von Schriftartinstanzen verwendet. |
| [**\_DWRITE-SCHRIFTARTFUNKTION \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Gibt Eigenschaften an, die verwendet werden, um typografische Merkmale im aktuellen Schriftartenbild zu identifizieren und auszuführen. |
| [**\_DWRITE-SCHRIFTARTMETRIKEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | Die [**DWRITE \_ FONT \_ METRICS-Struktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) gibt die Metriken an, die für alle Glyphen innerhalb der Schriftart gelten. |
| [**\_ \_ DWRITE-SCHRIFTARTMETRIKEN1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | Die [**DWRITE \_ FONT \_ METRICS1-Struktur**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) gibt die Metriken an, die für alle Glyphen in der Schriftart gelten. |
| [**\_DWRITE-SCHRIFTARTEIGENSCHAFT \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Schriftarteigenschaft, die zum Filtern von Schriftartsätzen und erstellen eines Schriftartsatzes mit expliziten Eigenschaften verwendet wird. |
| [**\_DWRITE-GLYPHENBILDDATEN \_ \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Daten für ein einzelnes Glyphen aus GetGlyphImageData. |
| [**\_DWRITE-GLYPHENMETRIKEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Gibt die Metriken eines einzelnen Glyphens an. |
| [**\_DWRITE-GLYPHENOFFSET \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | Die optionale Anpassung an die Position eines Glyphen. |
| [**\_DWRITE-GLYPHENLAUF \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Enthält die Informationen, die Renderer zum Zeichnen von Glyphenläufen benötigen. |
| [**BESCHREIBUNG DER \_ DWRITE-GLYPHENLAUFBESCHREIBUNG \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Enthält zusätzliche Eigenschaften im Zusammenhang mit denen in [**DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**\_ \_ DWRITE–TREFFERTESTMETRIKEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Beschreibt den Von einem Treffertest abgerufenen Bereich. |
| [**\_DWRITE-INLINEOBJEKTMETRIKEN \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Enthält Eigenschaften, die die geometrische Messung eines anwendungsdefiniertes Inlineobjekts beschreiben. |
| [**\_DWRITE-BEGRÜNDUNGSMÖGLICHKEIT \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | Die [**DWRITE \_ JUSTIFICATION \_ OPPORTUNITY-Struktur**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) gibt Begründungsinformationen pro Glyphe an. |
| [**\_DWRITE-ZEILENBREAKPOINT \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Merkmale eines Zeilenbreakpoints eines Zeichens. |
| [**\_DWRITE-LINIENMETRIKEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Enthält Informationen zu einer formatierten Textzeile. |
| [**DWRITE \_ LINE \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Enthält Informationen zu einer formatierten Textzeile. |
| [**\_DWRITE-ZEILENABSTAND \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | Die [**DWRITE \_ MATRIX-Struktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) gibt die Grafiktransformation an, die auf gerenderte Glyphen angewendet werden soll. |
| [**DWRITE \_ \_ OVERHANG-METRIKEN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Gibt an, wie viele sichtbare DIPs (geräteunabhängige Pixel) die einzelnen Seiten des Layouts oder der Inlineobjekte überschreiten. |
| [**DWRITE \_ PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | Die [**DWRITE \_ PANOSE-Union**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) beschreibt Schriftartklassifizierungswerte, die Sie mit [**IDWriteFont1::GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) verwenden, um die Schriftart auszuwählen und abzugleichen. |
| [**\_DWRITE-SKRIPTANALYSE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Speichert die Zuordnung von Text und dem zugehörigen Schreibsystemskript sowie einige Anzeigeattribute. |
| [**\_DWRITE-SKRIPTEIGENSCHAFTEN \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | Die [**DWRITE \_ SCRIPT \_ PROPERTIES-Struktur**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) gibt Skripteigenschaften für die Navigation und Begründung von Caretzeichen an. |
| [**\_DWRITE-STRUKTURIEREN VON \_ GLYPHENEIGENSCHAFTEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Enthält die Strukturierung von Ausgabeeigenschaften für ein Ausgabeglyph. |
| [**\_DWRITE-STRUKTURIEREN VON \_ \_ TEXTEIGENSCHAFTEN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Strukturierung von Ausgabeeigenschaften für ein Ausgabeglyph. |
| [**DWRITE– \_ DURCHGESTRICHEN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Enthält Informationen zur Größe und Platzierung von Durchgestrichenen. |
| [**\_DWRITE-TEXTMETRIKEN \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Enthält die Metriken, die Text nach dem Layout zugeordnet sind. |
| [**\_ \_ DWRITE-TEXTMETRIKEN1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Enthält die Metriken, die Text nach dem Layout zugeordnet sind. |
| [**\_DWRITE-TEXTBEREICH \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Gibt einen Bereich von Textpositionen an, in dem format in dem Text angewendet wird, der durch ein [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) dargestellt wird. |
| [**\_DWRITE-KÜRZUNG**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Gibt die Kürzungsoption für Text an, der das Layoutfeld überläuft.  |
| [**\_TYPOGRAFISCHE \_ DWRITE-FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Enthält eine Reihe von typografischen Features, die während der Textstrukturierung angewendet werden sollen. |
| [**\_DWRITE-UNTERSTREICHUNG**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Enthält Informationen zu Breite, Stärke, Offset, Ausführungshöhe, Leserichtung und Flussrichtung einer Unterstreichung.  |
| [**DWRITE \_ \_ UNICODE-BEREICH**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | Die [**DWRITE \_ UNICODE \_ RANGE-Struktur**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) gibt den Bereich von Unicode-Codepunkten an. |



 

