---
title: DirectWrite Enumerationen
description: DirectWrite werden die folgenden Enumerationen definiert.
ms.assetid: 809ccacd-ff23-4d7b-a177-e7a9937c0c5a
keywords:
- DirectWrite,Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71edfe3f60bb3ae2568c38d92352c62b6890721e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468177"
---
# <a name="directwrite-enumerations"></a>DirectWrite Enumerationen

DirectWrite werden die folgenden Enumerationen definiert.

## <a name="in-this-section"></a>In diesem Abschnitt


| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes"><strong>DWRITE_AUTOMATIC_FONT_AXES</strong></a> | Definiert Konstanten, die bestimmte Achsen angeben, die während der Schriftartauswahl automatisch im Layout angewendet werden können. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE-Enumeration</strong></a> enthält Werte, die die Baseline für die Textausrichtung angeben. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition"><strong>DWRITE_BREAK_CONDITION</strong></a> | Gibt die Bedingung an den Rändern des Inlineobjekts oder Texts an, der verwendet wird, um das Verhalten beim Zeilenumbruch zu bestimmen. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_container_type"><strong>DWRITE_CONTAINER_TYPE</strong></a> | Gibt das Containerformat einer Schriftartressource an. Ein Containerformat unterscheiden sich von einem Schriftdateiformat (DWRITE_FONT_FILE_TYPE), da der Container den Container beschreibt, in dem die zugrunde liegende Schriftartdatei gepackt ist.  | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE</strong></a> | Gibt den Typ DirectWrite Factoryobjekts an. | 
| <a href="/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE (DWriteCore)</strong></a> | Gibt den Typ DirectWrite Factoryobjekts an. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction"><strong>DWRITE_FLOW_DIRECTION</strong></a> | Gibt die Richtung an, in der Textzeilen relativ zueinander platziert werden.  | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes"><strong>DWRITE_FONT_AXIS_ATTRIBUTES</strong></a> | Definiert Konstanten, die Attribute für eine Schriftartachse angeben. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag"><strong>DWRITE_FONT_AXIS_TAG</strong></a> | Definiert Konstanten, die einen Vier-Zeichen-Bezeichner für eine Schriftartachse angeben. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_face_type"><strong>DWRITE_FONT_FACE_TYPE</strong></a> | Gibt das Dateiformat eines vollständigen Schriftartgesichts an. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model"><strong>DWRITE_FONT_FAMILY_MODEL</strong></a> | Definiert Konstanten, die angeben, wie Schriftfamilien gruppiert werden. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag"><strong>DWRITE_FONT_FEATURE_TAG</strong></a> | Ein -Wert, der das typografische Feature von Text angibt, der von der Schriftart bereitgestellt wird. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_file_type"><strong>DWRITE_FONT_FILE_TYPE</strong></a> | Der Typ einer Schriftart, die durch eine einzelne Schriftartdatei dargestellt wird. Schriftformate, die aus mehreren Dateien bestehen, z. B. Typ 1 . PFM und . PFB, verfügen über separate Aufzählwerte für jeden Dateityp. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage"><strong>DWRITE_FONT_LINE_GAP_USAGE</strong></a> | Geben Sie <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics"><strong>DWRITE_FONT_METRICS</strong></a>::lineGap-Wert an, der Teil der Zeilenmetriken sein soll. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id"><strong>DWRITE_FONT_PROPERTY_ID</strong></a> | Identifiziert eine Zeichenfolge in einer Schriftart. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations"><strong>DWRITE_FONT_SIMULATIONS</strong></a> | Gibt algorithmische Stilsimulationen an, die auf das Schriftartgesicht angewendet werden sollen. Fette und schräge Simulationen können über bitweise OR-Operation kombiniert werden. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type"><strong>DWRITE_FONT_SOURCE_TYPE</strong></a> | Definiert Konstanten, die den Mechanismus angeben, mit dem eine Schriftart in einen Schriftartensatz aufgenommen werden soll. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch"><strong>DWRITE_FONT_STRETCH</strong></a> | Stellt den Grad dar, in dem eine Schriftart gestreckt wurde, verglichen mit dem normalen Seitenverhältnis einer Schriftart. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style"><strong>DWRITE_FONT_STYLE</strong></a> | Stellt den Stil eines Schriftartgesichts wie normal, italisch oder schräg dar. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight"><strong>DWRITE_FONT_WEIGHT</strong></a> | Stellt die Dichte einer Schriftart in Bezug auf die Lichtheit oder Schwerigkeit der Striche dar. | 
| <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats"><strong>DWRITE_GLYPH_IMAGE_FORMATS</strong></a> | Gibt an, welche Formate in der Schriftart unterstützt werden, entweder auf einer schriftweiten Ebene oder pro Glyphe. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE-Enumeration</strong></a> enthält Werte, die angeben, wie das Glyph an der X-Achse ausgerichtet ist. | 
| <a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode"><strong>DWRITE_GRID_FIT_MODE</strong></a> | Gibt an, ob die Rasteranpassung von Glyphengliederungen (auch als Hinweise bezeichnet) aktiviert werden soll. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id"><strong>DWRITE_INFORMATIONAL_STRING_ID</strong></a> | Die Enumeration der Informationszeichenfolge, die eine in eine Schriftartdatei eingebettete Zeichenfolge identifiziert. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method"><strong>DWRITE_LINE_SPACING_METHOD</strong></a> | Die Methode, die für den Zeilenabstand in einem Textlayout verwendet wird. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality"><strong>DWRITE_LOCALITY</strong></a> | Gibt den Speicherort einer Ressource an. | 
| <a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode"><strong>DWRITE_MEASURING_MODE</strong></a> | Gibt die für das Textlayout verwendete Messmethode an. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_number_substitution_method"><strong>DWRITE_NUMBER_SUBSTITUTION_METHOD</strong></a> | Gibt an, wie die Zahlenersetzung auf Ziffern und die zugehörige Interpunktion angewendet wird. | 
| <a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_optical_alignment"><strong>DWRITE_OPTICAL_ALIGNMENT</strong></a> | Der Ausrichtungsmodus für den optischen Rand. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD-Enumeration</strong></a> enthält Werte, die die Richtlinie angeben, die von der <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode"><strong>IDWriteFontFace1::GetRecommendedRenderingMode-Methode</strong></a> verwendet wird, um zu bestimmen, ob Glyphen im Konturmodus gerendert werden. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE-Enumeration</strong></a> enthält Werte, die den Stil der Beendigung von Stammen und gerundeten Buchstabenform für Text angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT-Enumeration</strong></a> enthält Werte, die das Verhältnis zwischen Breite und Höhe des Zeichengesichts angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO-Enumeration</strong></a> enthält Werte, die Informationen über das Verhältnis zwischen Breite und Höhe des Zeichengesichts angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES-Enumeration</strong></a> enthält Werte, die den In der Schriftart verfügbaren Zeichentyp angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST-Enumeration</strong></a> enthält Werte, die das Verhältnis zwischen dem dichtesten und dem dünnsten Punkt des Strichs für einen Buchstaben wie groß geschriebenes "O" angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS-Enumeration</strong></a> enthält Werte, die das allgemeine Aussehen des Zeichengesichts angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY-Enumeration</strong></a> enthält Werte, die die allgemeinen Formmerkmale der Schriftart angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY-Enumeration</strong></a> enthält Werte, die die Art der Schriftartklassifizierung angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL-Enumeration</strong></a> enthält Werte, die den Typ der Füll- und Linienbehandlung angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS-Enumeration</strong></a> enthält Werte, die angeben, wie Zeichenenden und miniscule-Aufsteigende behandelt werden. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM-Enumeration</strong></a> enthält Werte, die die Rundung der Buchstabenform für Text angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING-Enumeration</strong></a> enthält Werte, die die Behandlung der Kontur für die Zierschrift angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE-Enumeration</strong></a> enthält Werte, die Informationen über die Platzierung der Mittellinie in Großbuchstaben und die Behandlung diagonaler Stamm apexes angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION-Enumeration</strong></a> enthält Werte, die den Anteil der Glyphenform angeben, indem zusätzliche Details zu Standardzeichen in Betracht ziehen. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM-Enumeration</strong></a> enthält Werte, die das allgemeine Aussehen des Zeichengesichts unter Berücksichtigung der Steigung und der Tails angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY-Enumeration</strong></a> enthält Werte, die die Topologie von Letterforms angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE-Enumeration</strong></a> enthält Werte, die die Darstellung des Serifentexts angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING-Enumeration</strong></a> enthält Werte, die Zeichenabstand (Monospace im Vergleich zu proportional) angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION-Enumeration</strong></a> enthält Werte, die die Beziehung zwischen schlanken und dichten Wortstamm von Textzeichen angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO-Enumeration</strong></a> enthält Werte, die das Seitenverhältnis symbolischer Zeichen angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND-Enumeration</strong></a> enthält Werte, die die Art des Symbolsatzes angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND-Enumeration</strong></a> enthält Werte, die die Art des Tools angeben, das zum Erstellen von Zeichenformularen verwendet wird. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT-Enumeration</strong></a> enthält Werte, die die Gewichtung von Zeichen angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT-Enumeration</strong></a> enthält Werte, die die relative Größe der Kleinbuchstaben angeben. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT-Enumeration</strong></a> enthält Werte, die Informationen zur relativen Größe von Kleinbuchstaben und zur Behandlung diakritischer Markierungen (xheight) angeben. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_paragraph_alignment"><strong>DWRITE_PARAGRAPH_ALIGNMENT</strong></a> | Gibt die Ausrichtung des Absatztexts entlang der Flussrichtungsachse relativ zum oberen und unteren Rand des Layoutfelds des Flows an.  | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry"><strong>DWRITE_PIXEL_GEOMETRY</strong></a> | Stellt die interne Struktur eines Gerätepixels (d. h. die physische Anordnung von Rot-, Grün- und Blaufarbkomponenten) dar, die zum Rendern von Text angenommen wird.  | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction"><strong>DWRITE_READING_DIRECTION</strong></a> | Gibt die Richtung an, in der das Lesen verläuft. <blockquote>[!Note]<br /><strong>DWRITE_READING_DIRECTION_TOP_TO_BOTTOM</strong> und <strong>DWRITE_READING_DIRECTION_BOTTOM_TO_TOP</strong> sind nur in Windows 8.1 und höher verfügbar.</blockquote> | 
| <a href="/windows/win32/directwrite/dwrite-rendering-mode-enumerations">DWRITE_RENDERING_MODE-Enumerationen</a> | Ab Windows 8 hat die <strong>DWRITE_RENDERING_MODE-Enumeration</strong> neue Enumerationswerte hinzugefügt und andere als veraltet bezeichnet. | 
| <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1"><strong>DWRITE_RENDERING_MODE1</strong></a> | Gibt an, wie Glyphen gerendert werden. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_script_shapes"><strong>DWRITE_SCRIPT_SHAPES</strong></a> | Gibt zusätzliche Strukturierungsanforderungen für Text an. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment"><strong>DWRITE_TEXT_ALIGNMENT</strong></a> | Gibt die Ausrichtung des Absatztexts entlang der Leserichtungsachse relativ zum führenden und nachgestellten Rand des Layoutfelds an. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE-Enumeration</strong></a> enthält Werte, die den Typ von Antialiasing angeben, der für Text verwendet werden soll, wenn der Renderingmodus Antialiasing aufruft. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_texture_type"><strong>DWRITE_TEXTURE_TYPE</strong></a> | Identifiziert einen Typ von Alphatextur. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_trimming_granularity"><strong>DWRITE_TRIMMING_GRANULARITY</strong></a> | Gibt die Textgranularität an, die zum Kürzen von Text verwendet wird, der das Layoutfeld überläuft. | 
| <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a> | Die <a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION-Enumeration</strong></a> enthält Werte, die die gewünschte Art der Glyphenausrichtung für den Text angeben. | 
| <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_word_wrapping"><strong>DWRITE_WORD_WRAPPING</strong></a> | Gibt den Zeilenumbruch an, der in einem bestimmten mehrzeiligen Absatz verwendet werden soll. <blockquote>[!Note]<br /><strong>DWRITE_WORD_WRAPPING_EMERGENCY_BREAK</strong>, <strong>DWRITE_WORD_WRAPPING_WHOLE _WORD</strong>und <strong>DWRITE_WORD_WRAPPING_CHARACTER</strong> sind nur in Windows 8.1 und höher verfügbar.</blockquote> | 




 

 

 





