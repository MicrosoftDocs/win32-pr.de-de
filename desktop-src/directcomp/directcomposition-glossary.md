---
title: Directcomposition-Glossar
description: In diesem Thema werden die Microsoft directcomposition-Begriffe definiert.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c72186f65f64e1187069963f0aae36de2835fd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315566"
---
# <a name="directcomposition-glossary"></a>Directcomposition-Glossar

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema werden die Microsoft directcomposition-Begriffe definiert.

<dl> <dt>

<span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**Animations Funktion**
</dt> <dd>

Ein Konstrukt, das angibt, wie sich der Wert einer einzelnen Objekt Eigenschaft über einen bestimmten Zeitraum ändert.

</dd> <dt>

<span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**Animations Objekt**
</dt> <dd>

Ein-Objekt, das eine Funktion zum Animieren der Eigenschaften eines anderen Objekts darstellt.

</dd> <dt>

<span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**Animations Segment**
</dt> <dd>

Die grundlegenden Zeit Steuerungs Definitionen einer Animations Funktion. Dabei handelt es sich um die primitiven, aus denen komplexere und übergeordnete Animations Funktionen erstellt werden.

</dd> <dt>

<span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**Hintergrund Puffer**
</dt> <dd>

Ein Rechteck des Arbeitsspeichers, in den eine Anwendung direkt schreiben kann. Der Hintergrund Puffer wird nie direkt auf dem Monitor angezeigt.

</dd> <dt>

<span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**Batches**
</dt> <dd>

Eine Gruppe von directcomposition-Methoden aufrufen, die atomarisch verarbeitet werden.

</dd> <dt>

<span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**Bitmap**
</dt> <dd>

Ein Farb Puffer, entweder mit oder ohne einen Alphakanal, der sich im System-oder Videospeicher befindet.

</dd> <dt>

<span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**Rahmen Modus**
</dt> <dd>

Eine Eigenschaft eines Microsoft directcomposition-visuellen Elements, das beeinflusst, wie die Ränder einer Bitmap zusammengesetzt werden, wenn die Bitmap so transformiert wird, dass die Ränder nicht an ganzzahlige Koordinaten ausgerichtet sind. Er wirkt sich auch darauf aus, wie der Inhalt an den Ecken eines Clips mit abgerundeten Ecken abgeschnitten wird, und am Rand eines Clips, der transformiert wird, sodass die Ränder nicht an ganzzahlige Koordinaten ausgerichtet sind.

</dd> <dt>

<span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**Clip-Objekt**
</dt> <dd>

Ein-Objekt, das ein Clip Rechteck darstellt.

</dd> <dt>

<span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**Clip Rechteck**
</dt> <dd>

Ein Satz von Koordinaten, die den Bereich des visuellen Bitmapinhalts definieren, der auf dem Bildschirm gezeichnet wird, wenn die Bitmap gerendert wird.

</dd> <dt>

<span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**Verdeckung**
</dt> <dd>

, Um vorübergehend zu verhindern, dass Desktopfenster-Manager (DWM) ein Fenster auf die Anzeige zeichnet. Anwendungen verbergen in der Regel ein Fenster, während directcomposition die Bitmap des Fensters in einer Komposition verwendet.

</dd> <dt>

<span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**einzusetzen**
</dt> <dd>

, Um für die Verarbeitung einen Batch von Befehlen an directcompositiondirectcomposition zu übermitteln.

</dd> <dt>

<span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**zusammengesetzter Modus**
</dt> <dd>

Eine von mehreren Möglichkeiten, zwei Bitmaps (Quelle und Ziel) zu mischen, um einen bestimmten Effekt zu erzielen.

</dd> <dt>

<span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**Gas**
</dt> <dd>

Eine Auflistung von Bitmaps, die kombiniert und bearbeitet werden, indem verschiedene Transformationen, Effekte und Animationen angewendet werden, um ein gewünschtes visuelles Ergebnis in einer Anwendungs Benutzeroberfläche zu erzeugen.

</dd> <dt>

<span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**Fenster "Kompositions Ziel"**
</dt> <dd>

Das Fenster, an das eine visuelle Struktur gebunden ist, und in dem die resultierende Komposition gezeichnet wird.

</dd> <dt>

<span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**entsprechende**
</dt> <dd>

Ein Vorgang, der die Art und Weise ändert, in der die Bitmaps einer visuellen Struktur durch Anwenden eines Pixelshaders gerragt werden.

</dd> <dt>

<span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**Gruppe "Auswirkung"**
</dt> <dd>

Eine Gruppe von Bitmapeffekten, die zusammen angewendet werden, um die rasterisierung der Unterstruktur eines visuellen Elements zu ändern.

</dd> <dt>

<span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**Dr**
</dt> <dd>

Eine Iterations-Engine, die eine rasterisierung der visuellen Struktur erzeugt.

</dd> <dt>

<span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**Vorder-Puffer**
</dt> <dd>

Ein Rechteck des Arbeitsspeichers, der vom Grafikadapter übersetzt und auf dem Monitor angezeigt wird.

</dd> <dt>

<span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**Interpolations Modus**
</dt> <dd>

Eine Eigenschaft, die bestimmt, wie eine Bitmap zusammengesetzt wird, wenn Sie transformiert wird, sodass keine 1:1-Entsprechung zwischen Pixeln in der Bitmap und Pixel auf dem Bildschirm vorhanden ist.

</dd> <dt>

<span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**visuelle Stamm Element**
</dt> <dd>

Das visuelle Element, von dem alle anderen visuellen Elemente in einer visuellen Struktur abgeleitet werden.

</dd> <dt>

<span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**Austausch Kette**
</dt> <dd>

Eine Auflistung von einem oder mehreren Back Puffern, die seriell dem Vorder-Puffer präsentiert werden können.

</dd> <dt>

<span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**Oberfläche**
</dt> <dd>

Eine Darstellung eines linearen Bereichs des Anzeige Speichers, der sich normalerweise im Anzeige Speicher der Anzeigekarte befindet, obwohl Oberflächen im Systemspeicher vorhanden sein können.

</dd> <dt>

<span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**Sin**
</dt> <dd>

Eine Matrix, die eine Koordinatentransformation in einem zweidimensionalen oder dreidimensionalen Raum darstellt.

</dd> <dt>

<span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**Gruppe transformieren**
</dt> <dd>

Eine Auflistung von Transformationen, deren Matrizen in der Reihenfolge multipliziert werden, in der Sie in der Auflistung angegeben werden, bevor Sie auf ein visuelles Element angewendet werden.

</dd> <dt>

<span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Störungen**
</dt> <dd>

Ein-Objekt, das einen optionalen Verweis auf ein Bitmap-Objekt enthält, sowie einen Satz von Eigenschaften, die bestimmen, wo und wie die Bitmap auf dem Bildschirm gerendert wird.

</dd> <dt>

<span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**visuelles Objekt**
</dt> <dd>

Siehe [*Visualisierung*](/windows).

</dd> <dt>

<span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**visuelle Unterstruktur**
</dt> <dd>

Ein Teil einer visuellen Struktur, die aus einem bestimmten visuellen Element und allen untergeordneten und untergeordneten visuellen Elementen besteht.

</dd> <dt>

<span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**visuelle Struktur**
</dt> <dd>

Eine hierarchische Auflistung der visuellen Elemente, die zum Erstellen einer Komposition verwendet werden.

</dd> <dt>

<span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**fensterlose Austausch Kette**
</dt> <dd>

Eine austauschkette, die einem visuellen directcomposition-Objekt anstelle eines Fensters zugeordnet ist.

</dd> </dl>

 

 