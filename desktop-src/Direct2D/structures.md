---
title: Direct2D-Strukturen
description: Direct2D stellt die folgenden Strukturen bereit. Zusätzliche Strukturen werden im D2D1-Namespace definiert.
ms.assetid: 6c34a8c8-4b0b-4a95-8f13-25ca25c370ba
keywords:
- Direct2D, Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6be3735335abc5b9242ec150ac583f837ae5c15936aaca677b322526b1c19f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537700"
---
# <a name="direct2d-structures"></a>Direct2D-Strukturen

Direct2D stellt die folgenden Strukturen bereit. Zusätzliche Strukturen werden im [D2D1-Namespace](d2d1-namespace.md)definiert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**D2D \_ COLOR \_ F**](d2d-color-f.md) | Beschreibt die Rot-, Grün-, Blau- und Alphakomponenten einer Farbe. |
| [**D2D \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) | Stellt eine 3:2-Matrix dar. |
| [**D2D \_ MATRIX \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f) | Beschreibt eine 4-mal-3-Gleitkommamatrix. |
| [**D2D \_ MATRIX \_ 4X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f) | Beschreibt eine 4-mal-4-Gleitkommamatrix. |
| [**D2D \_ MATRIX \_ 5X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f) | Beschreibt eine 5-mal-4-Gleitkommamatrix. |
| [**D2D \_ POINT \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f) | Stellt ein x-Koordinaten- und y-Koordinatenpaar dar, ausgedrückt als Gleitkommawerte, im zweidimensionalen Raum. |
| [**D2D \_ POINT \_ 2L**](/previous-versions/windows/desktop/legacy/jj219217(v=vs.85)) | Die D2D \_ POINT \_ 2L-Struktur definiert die x- und y-Koordinaten eines Punkts. |
| [**D2D \_ POINT \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u) | Stellt ein x-Koordinaten- und y-Koordinatenpaar dar, ausgedrückt als 32-Bit-Ganzzahlwert ohne Vorzeichen, im zweidimensionalen Raum. |
| [**D2D \_ RECT \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) | Stellt ein Rechteck dar, das durch die Koordinaten der oberen linken Ecke (links, oben) und der Koordinaten der unteren rechten Ecke (rechts, unten) definiert wird.  |
| [**D2D \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) | Die [**D2D \_ RECT \_ L-Struktur**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) definiert die Koordinaten der oberen linken und unteren rechten Ecken eines Rechtecks. |
| [**D2D \_ RECT \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_u) | Stellt ein Rechteck dar, das durch das Koordinatenpaar oben links (links, oben) und das Koordinatenpaar unten rechts (rechts, unten) definiert wird. Diese Koordinaten werden als 32-Bit-Ganzzahlwerte ausgedrückt. |
| [**\_D2D-GRÖßE \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f) | Speichert ein geordnetes Paar von Gleitkommawerten, in der Regel die Breite und Höhe eines Rechtecks.  |
| [**D2D \_ SIZE \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u) | Speichert ein geordnetes Paar von ganzen Zahlen, i. d. R. die Breite und Höhe eines Rechtecks. |
| [**D2D \_ VECTOR \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f) | Ein 2D-Vektor, der aus zwei Gleitkommawerten mit einfacher Genauigkeit (x, y) besteht.  |
| [**D2D \_ VECTOR \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f) | Ein 3D-Vektor, der aus drei Gleitkommawerten mit einfacher Genauigkeit besteht (x, y, z). |
| [**D2D \_ VECTOR \_ 4F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f) | Ein 4D-Vektor, der aus vier Gleitkommawerten mit einfacher Genauigkeit besteht (x, y, z, w). |
| [**D2D1 \_ \_ ARC-SEGMENT**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment) | Beschreibt einen elliptischen Bogen zwischen zwei Punkten. |
| [**D2D1 \_ BEZIER \_ SEGMENT**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) | Stellt ein kubisches Béziersegment dar, das zwischen zwei Punkten gezeichnet wird. |
| [**EIGENSCHAFTEN DES \_ D2D1-BITMAPPINSELS \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) | Beschreibt die Erweiterungsmodi und den Interpolationsmodus eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**D2D1 \_ BITMAP \_ BRUSH \_ PROPERTIES1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1) | Beschreibt die Erweiterungsmodi und den Interpolationsmodus eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**D2D1 \_ BITMAP \_ PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) | Beschreibt das Pixelformat und die DPI einer Bitmap. |
| [**D2D1 \_ BITMAP \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) | Diese Struktur ermöglicht die Erstellung einer [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1) mit bitmap-Optionen und verfügbaren Farbkontextinformationen.  |
| [**D2D1 \_ BLEND \_ DESCRIPTION**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) | Definiert eine Blendbeschreibung, die in einer bestimmten Blendtransformation verwendet werden soll. |
| [**\_D2D1-PINSELEIGENSCHAFTEN \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties) | Beschreibt die Deckkraft und Transformation eines Pinsels. |
| [**D2D1 \_ COLOR \_ F**](d2d1-color-f.md) | Beschreibt die Rot-, Grün-, Blau- und Alphakomponenten einer Farbe. |
| [**\_D2D1-ERSTELLUNGSEIGENSCHAFTEN \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_creation_properties) | Gibt die Optionen an, mit denen das [Direct2D-Gerät,](./direct2d-portal.md) die Factory und der Gerätekontext erstellt werden.  |
| [**BENUTZERDEFINIERTE \_ \_ D2D1-VERTEXPUFFEREIGENSCHAFTEN \_ \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_custom_vertex_buffer_properties) | Definiert einen Vertex-Shader und die Beschreibung des Eingabeelements, um das Eingabelayout zu definieren. |
| [**D2D1– \_ \_ BESCHREIBUNG DES ZEICHNUNGSZUSTANDS \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description) | Beschreibt den Zeichnungszustand eines Renderziels.  |
| [**D2D1 \_ DRAWING \_ STATE \_ DESCRIPTION1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_drawing_state_description1) | Beschreibt den Zeichnungszustand eines Gerätekontexts. |
| [**BESCHREIBUNG DER \_ D2D1 \_ EFFECT-EINGABE \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_effect_input_description) | Beschreibt die Funktionen eines Effekts. |
| [**D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) | Enthält den Mittelpunkt, den X-Radius und den y-Radius einer Ellipse. |
| [**D2D1 \_ \_ FACTORY-OPTIONEN**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_factory_options) | Enthält die Debugebene eines [**ID2D1Factory-Objekts.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)  |
| [**D2D1 \_ FEATURE \_ DATA \_ DOUBLES**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_doubles) | Beschreibt die Unterstützung für Doubles in Shadern. |
| [**D2D1 \_ FEATURE \_ DATA \_ D3D10 \_ X \_ HARDWARE \_ OPTIONS**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_d3d10_x_hardware_options) | Beschreibt die Unterstützung von Compute-Shadern, eine Option auf D3D10-Featureebene. |
| [**D2D1 \_ GRADIENT \_ MESH \_ PATCH**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) | Stellt einen Tensorpatch mit 16 Kontrollpunkten, vier Eckfarben und Begrenzungsflags dar. Eine ID2D1GradientMesh besteht aus 1 oder mehr Gradient Mesh-Patches. Verwenden Sie die [**GradientMeshPatch-Funktion**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatch) oder die [**GradientMeshPatchFromCoonsPatch-Funktion,**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatchfromcoonspatch) um eine zu erstellen.  |
| [**D2D1 \_ GRADIENT \_ STOP**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) | Enthält die Position und Farbe eines Farbverlaufsstopps.  |
| [**D2D1 \_ HWND– \_ \_ \_ RENDERZIELEIGENSCHAFTEN**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) | Enthält die HWND-, Pixelgröße- und Präsentationsoptionen für eine [**ID2D1HwndRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) |
| [**EIGENSCHAFTEN DES \_ D2D1-INKSTILS \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties) | Definiert die allgemeine Stifttippform und die Transformation, die in einem [**ID2D1InkStyle-Objekt**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle) verwendet wird.  |
| [**\_D2D1-BILDPINSELEIGENSCHAFTEN \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_image_brush_properties) | Beschreibt Bildpinselfunktionen. |
| [**D2D1 \_ INK \_ BEZIER \_ SEGMENT**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment) | Stellt ein Béziersegment dar, das bei der Erstellung eines [**ID2D1Ink-Objekts**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink) verwendet werden soll. Diese Struktur unterscheidet sich von [**D2D1 \_ BEZIER \_ SEGMENT**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) darin, dass sie aus [**D2D1 \_ INK \_ POINT**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point)s besteht, die zusätzlich zu x- und y-Koordinaten einen Radius enthalten.  |
| [**D2D1 \_ INK \_ POINT**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point) | Stellt ein Punkt-Radius-Paar dar, das Teil eines [**D2D1 \_ INK \_ BEZIER \_ SEGMENT**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment)ist. |
| [**D2D1– \_ \_ EINGABEBESCHREIBUNG**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_description) | Beschreibt die Optionen, die Transformationen für Eingabetexturen festlegen können. |
| [**\_D2D1-EINGABEELEMENT \_ \_ DESC**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_element_desc) | Eine Beschreibung eines einzelnen Elements für das Scheitelpunktlayout. |
| [**\_D2D1-EBENENPARAMETER \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) | Enthält die Inhaltsgrenze, Maskierungsinformationen, Deckkrafteinstellungen und andere Optionen für eine Ebenenressource.  |
| [**D2D1 \_ LAYER \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) | Enthält die Inhaltsgrenze, Maskierungsinformationen, Deckkrafteinstellungen und andere Optionen für eine Ebenenressource. |
| [**D2D1 \_ – EIGENSCHAFTEN DES \_ LINEAREN \_ FARBVERLAUFSPINSELS \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) | Enthält den Ausgangspunkt und endpunkt der Farbverlaufsachse für einen [**ID2D1LinearGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)  |
| [**D2D1 \_ MATRIX \_ 3X2 \_ F**](d2d1-matrix-3x2-f.md) | Stellt eine 3 by 2-Matrix dar.  |
| [**D2D1 \_ MATRIX \_ 4X3 \_ F**](d2d1-matrix-4x3-f.md) | Stellt eine 4 by 3-Matrix dar.  |
| [**D2D1 \_ MATRIX \_ 4X4 \_ F**](d2d1-matrix-4x4-f.md) | Stellt eine 4 by 4-Matrix dar.  |
| [**D2D1 \_ MATRIX \_ 5X4 \_ F**](d2d1-matrix-5x4-f.md) | Stellt eine 5 by 4-Matrix dar.  |
| [**ZUGEORDNETES \_ \_ D2D1-RECT**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_mapped_rect) | Beschreibt den zugeordneten Arbeitsspeicher aus der [**ID2D1Bitmap1::Map-API.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map) |
| [**D2D1-PIXELFORMAT \_ \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) | Enthält das Datenformat und den Alphamodus für eine Bitmap oder ein Renderziel.  |
| [**D2D1 \_ POINT \_ 2F**](d2d1-point-2f.md) | Stellt ein x-Koordinaten- und y-Koordinatenpaar im zweidimensionalen Raum dar. |
| [**D2D1 \_ POINT \_ 2L**](/previous-versions/windows/desktop/legacy/hh847948(v=vs.85)) | Die POINT-Struktur definiert die x- und y-Koordinaten eines Punkts. |
| [**D2D1 \_ PUNKT \_ 2U**](d2d1-point-2u.md) | Stellt ein x-Koordinaten- und y-Koordinatenpaar im zweidimensionalen Raum dar.  |
| [**D2D1 \_ \_ PUNKTBESCHREIBUNG**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_point_description) | Beschreibt einen Punkt in einer Pfadgeometrie. |
| [**EIGENSCHAFTEN DES \_ D2D1-DRUCKSTEUERSTEUERSTEUER \_ \_ STEUERELEMENTS**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_print_control_properties) | Die Erstellungseigenschaften für ein [**ID2D1PrintControl-Objekt.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) |
| [**D2D1-EIGENSCHAFTENBINDUNG \_ \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) | Definiert eine Eigenschaftenbindung an ein Paar von Funktionen, die die entsprechende Eigenschaft erhalten und festlegen.  |
| [**D2D1 \_ QUADRATIC \_ BEZIER \_ SEGMENT**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_quadratic_bezier_segment) | Enthält den Kontrollpunkt und den Endpunkt für ein quadratisches Béziersegment. |
| [**EIGENSCHAFTEN DES RADIALEN \_ FARBVERLAUFSPINSELS D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) | Enthält den Farbverlaufs-Ursprungsoffset sowie die Größe und Position der Farbverlaufs-Ellipse für einen [**ID2D1RadialGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)  |
| [**D2D1 \_ RECT \_ F**](d2d1-rect-f.md) | Stellt ein Rechteck dar, das durch die Koordinaten der linken oberen Ecke (links, oben) und der Koordinaten der unteren rechten Ecke (rechts, unten) definiert wird.  |
| [**D2D1 \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)) | Die RECT-Struktur definiert die Koordinaten der oberen linken und unteren rechten Ecke eines Rechtecks. |
| [**D2D1 \_ RECT \_ U**](d2d1-rect-u.md) | Stellt ein Rechteck dar, das durch die Koordinaten der linken oberen Ecke (links, oben) und der Koordinaten der unteren rechten Ecke (rechts, unten) definiert wird.  |
| [**EIGENSCHAFTEN DER \_ D2D1-RESSOURCENTEXTUR \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_resource_texture_properties) | Definiert eine Ressourcentextur, wenn die ursprüngliche Ressourcentextur erstellt wird. |
| [**D2D1-RESSOURCENNUTZUNG \_ \_**](/previous-versions/windows/desktop/legacy/hh404326(v=vs.85)) | Beschreibt den Arbeitsspeicher, der von Bildtexturen und Shadern verwendet wird. |
| [**EIGENSCHAFTEN DES \_ D2D1-RENDERZIELS \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) | Enthält Renderingoptionen (Hardware oder Software), Pixelformat, DPI-Informationen, Remotingoptionen und Direct3D-Unterstützungsanforderungen für ein Renderziel.  |
| [**\_D2D1-RENDERINGSTEUERELEMENTE \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_rendering_controls) | Beschreibt die Einschränkungen, die auf einen Renderer für Bildverarbeitungseffekt angewendet werden sollen. |
| [**GERUNDETER \_ \_ D2D1-RECT**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect) | Enthält die Dimensionen und Eckradien eines abgerundeten Rechtecks. |
| [**D2D1 \_ – \_ EINFACHES \_ FARBPROFIL**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_simple_color_profile) | Einfache Beschreibung eines Farbraums. |
| [**D2D1 \_ GRÖßE \_ F**](d2d1-size-f.md) | Speichert ein geordnetes Gleitkommapaar, in der Regel die Breite und Höhe eines Rechtecks. |
| [**D2D1 \_ SIZE \_ U**](d2d1-size-u.md) | Speichert ein geordnetes Paar von ganzen Zahlen, i. d. R. die Breite und Höhe eines Rechtecks. |
| [**EIGENSCHAFTEN DES \_ D2D1-STRICHSTILS \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties) | Beschreibt den Strich, der eine Form umrissen.  |
| [**EIGENSCHAFTEN DES \_ D2D1-STRICHSTILS1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_stroke_style_properties1) | Beschreibt den Strich, der eine Form umrissen. |
| [**D2D1 \_ SVG \_ LENGTH**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length) | Stellt eine SVG-Länge dar. |
| [**D2D1 \_ SVG \_ PRESERVE \_ ASPECT \_ RATIO**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_preserve_aspect_ratio) | Stellt alle SVG preserveAspectRatio-Einstellungen dar. |
| [**D2D1 \_ SVG \_ VIEWBOX**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_viewbox) | Stellt ein SVG viewBox dar. |
| [**D2D1 \_ TRANSFORMIERTE \_ \_ \_ BILDQUELLENEIGENSCHAFTEN**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties) | Eigenschaften einer transformierten Bildquelle. |
| [**\_D2D1-DREIECK**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_triangle) | Enthält die drei Scheitelungen, die ein Dreieck beschreiben. |
| [**D2D1 \_ VECTOR \_ 2F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_2f) | Ein Vektor von 2 FLOAT-Werten (x, y). |
| [**D2D1 \_ VECTOR \_ 3F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_3f) | Ein Vektor von 3 FLOAT-Werten (x, y, z). |
| [**D2D1 \_ VECTOR \_ 4F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_4f) | Ein Vektor von 4 FLOAT-Werten (x, y, z, w). |
| [**D2D1– \_ \_ VERTEXPUFFEREIGENSCHAFTEN \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_buffer_properties) | Definiert die Eigenschaften eines Scheitelpunktpuffers, die standard für alle Vertex-Shaderdefinitionen sind. |
| [**D2D1 \_ VERTEX \_ RANGE**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_range) | Definiert einen Bereich von Scheitelpunkte, die verwendet werden, wenn weniger als der vollständige Inhalt eines Scheitelpunktpuffers gerendert wird. |
| [**D3DCOLORVALUE**](/previous-versions/windows/desktop/legacy/dd368193(v=vs.85)) | Speichert Farb- und Alphakanalinformationen. |
| [*PD2D1 \_ EFFECT \_ FACTORY*](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) | Beschreibt die Implementierung eines Effekts. |