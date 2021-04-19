---
title: DirectWrite-Strukturen
description: DirectWrite definiert die folgenden Strukturen.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea132cde1ea6b740cc02b938767f941e9c999e5a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361748"
---
# <a name="directwrite-structures"></a>DirectWrite-Strukturen

DirectWrite definiert die folgenden Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md) | Stellt Bitmapdaten im BGRA32-Format dar. |
| [**dwrite- \_ Caretzeichen \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | Die [**dwrite \_ Einfügemarke \_ Metrics**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) -Struktur gibt die Metriken für die Platzierung der Einfügemarke in einer Schriftart an. |
| [**dwrite \_ - \_ clustermetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Enthält Informationen zu einem Symbol Cluster. |
| [**dwrite- \_ Farbe \_ F**](dwrite-color-f.md) | Beschreibt die Komponenten rot, grün, blau und Alpha einer Farbe. |
| [**dwrite- \_ Farb \_ Glyphe \_ Ausführen**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Enthält die Informationen, die von Renderer benötigt werden, um Glyphe mit Symbol Farben zu zeichnen. |
| [**Dwrite- \_ Farb \_ Glyphe \_ RUN1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Stellt eine farbglyphe dar. Die IDWriteFactory4:: translatecolorglyphrun-Methode gibt eine geordnete Auflistung von Farb Glyphe mit unterschiedlichen Typen zurück, abhängig davon, was von der Schriftart unterstützt wird. |
| [**dwrite- \_ Datei \_ Fragment**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Stellt einen Bereich von Bytes in einer Schriftart Datei dar. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Stellt den minimalen und maximalen Bereich der möglichen Werte für eine Schriftart Achse dar. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Stellt einen Wert für eine Schriftart Achse dar. Wird beim Abfragen und Erstellen von Schriftart Instanzen verwendet. |
| [**dwrite- \_ Schriftart ( \_ Funktion)**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Gibt Eigenschaften an, die zum Identifizieren und Ausführen von typografischen Funktionen in der aktuellen Schriftart verwendet werden. |
| [**\_Schriftart Metriken für dwrite \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | Die [**dwrite- \_ Schriftart \_ metrikstruktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) gibt die Metriken an, die auf alle Symbole innerhalb der Schriftart angewendet werden. |
| [**Dwrite- \_ Schriftart \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | Die [**dwrite- \_ Schriftart \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) -Struktur gibt die Metriken an, die auf alle Symbole innerhalb der Schriftart angewendet werden. |
| [**dwrite- \_ Schriftart ( \_ Eigenschaft)**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Schriftart Eigenschaft, die zum Filtern von Schriftart Sätzen und zum Aufbau eines Schriftart Satzes mit expliziten Eigenschaften verwendet wird. |
| [**dwrite- \_ Glyphe- \_ \_ Bilddaten**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Daten für ein einzelnes Symbol aus getglyphimagedata. |
| [**dwrite- \_ Glyphe- \_ Metriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Gibt die Metriken eines einzelnen Symbols an. |
| [**Offset der dwrite- \_ Glyphe \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | Die optionale Anpassung an die Position eines Symbols. |
| [**dwrite- \_ Glyphe \_ Ausführen**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Enthält die Informationen, die von Renderer zum Zeichnen von Glyphe benötigt werden. |
| [**Beschreibung der dwrite- \_ Glyphe \_ Ausführen \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Enthält zusätzliche Eigenschaften im Zusammenhang mit den in der [**dwrite- \_ Glyphe- \_ Ausführen**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**dwrite \_ - \_ Treffer \_ Testmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Beschreibt den Bereich, der von einem Treffer Test abgerufen wird. |
| [**dwrite \_ - \_ Inline \_ objektmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Enthält Eigenschaften, die die geometrische Messung eines von der Anwendung definierten Inline Objekts beschreiben. |
| [**dwrite- \_ Begründung \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | Die Grundstruktur der [**dwrite- \_ Rechtfertigung \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) gibt Informationen zur Begründung pro Glyphe an. |
| [**dwrite-Zeilen-halte \_ \_ Punkt**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Zeilen Haltepunkt-Eigenschaften eines Zeichens. |
| [**dline \_ - \_ Metriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Enthält Informationen über eine formatierte Textzeile. |
| [**Dwrite- \_ Zeile \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Enthält Informationen über eine formatierte Textzeile. |
| [**Abstand der dwrite- \_ Zeile \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**dwrite- \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | Die [**dwrite- \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) Struktur gibt die Grafik Transformation an, die auf gerenderte Symbole angewendet werden soll. |
| [**dwrite- \_ \_ überschreitungsmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Gibt an, wie viel alle sichtbaren Dips (geräteunabhängige Pixel) jede Seite des Layouts oder der Inline Objekte überschreiten. |
| [**dwrite- \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | Die [**dwrite \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) -Union beschreibt Schriftart Klassifizierungs Werte, die Sie mit [**IDWriteFont1:: getpanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) verwenden, um die Schriftart auszuwählen und abzugleichen. |
| [**dwrite- \_ Skript \_ Analyse**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Speichert die Zuordnung von Text und das zugehörige System Skript sowie einige Anzeige Attribute. |
| [**Eigenschaften von dwrite- \_ Skripts \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | Die [**Eigenschaften Struktur des dwrite- \_ Skripts \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) gibt Skript Eigenschaften für die Navigation und Ausrichtung von Caretzeichen an. |
| [**dwrite-Strukturierungs Symbol \_ \_ \_ Eigenschaften**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Enthält Strukturierungs Ausgabe Eigenschaften für ein Ausgabe Symbol. |
| [**dwrite-Strukturieren von \_ \_ Text \_ Eigenschaften**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Strukturieren von Ausgabe Eigenschaften für ein Ausgabe Symbol. |
| [**dwrite- \_ durchgestrichen**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Enthält Informationen zur Größe und Platzierung von durch Strichen. |
| [**dwrite \_ - \_ textmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Enthält die Metriken, die Text nach dem Layout zugeordnet sind. |
| [**Dwrite- \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Enthält die Metriken, die Text nach dem Layout zugeordnet sind. |
| [**dwrite- \_ Text \_ Bereich**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Gibt einen Bereich von Textpositionen an, in denen das Format im Text angewendet wird, der durch ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt dargestellt wird. |
| [**dwrite- \_ Kürzung**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Gibt die Kürzungs Option für Text an, der das layoutfeld über läuft  |
| [**typografische dwrite- \_ \_ Funktionen**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Enthält einen Satz von typografischen Features, die bei der Text Strukturierung angewendet werden sollen. |
| [**dwrite-unter \_ Streichung**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Enthält Informationen über die Breite, die Stärke, den Offset, die Laufhöhe, die Leserichtung und die Fluss Richtung einer Unterstreichung.  |
| [**dwrite- \_ Unicode- \_ Bereich**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | Die [**dwrite- \_ Unicode- \_ Bereichs**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) Struktur gibt den Bereich von Unicode-Code Punkten an. |



 

