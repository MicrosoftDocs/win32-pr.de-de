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
# <a name="directcomposition-glossary"></a><span data-ttu-id="213a0-103">Directcomposition-Glossar</span><span class="sxs-lookup"><span data-stu-id="213a0-103">DirectComposition glossary</span></span>

> [!NOTE]
> <span data-ttu-id="213a0-104">Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen.</span><span class="sxs-lookup"><span data-stu-id="213a0-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="213a0-105">Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="213a0-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="213a0-106">In diesem Thema werden die Microsoft directcomposition-Begriffe definiert.</span><span class="sxs-lookup"><span data-stu-id="213a0-106">This topic defines Microsoft DirectComposition terms.</span></span>

<dl> <dt>

<span data-ttu-id="213a0-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**Animations Funktion**</span><span class="sxs-lookup"><span data-stu-id="213a0-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**animation function**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-108">Ein Konstrukt, das angibt, wie sich der Wert einer einzelnen Objekt Eigenschaft über einen bestimmten Zeitraum ändert.</span><span class="sxs-lookup"><span data-stu-id="213a0-108">A construct that specifies how the value of a single object property changes over a period of time.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**Animations Objekt**</span><span class="sxs-lookup"><span data-stu-id="213a0-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**animation object**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-110">Ein-Objekt, das eine Funktion zum Animieren der Eigenschaften eines anderen Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="213a0-110">An object that represents a function for animating the properties of another object.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**Animations Segment**</span><span class="sxs-lookup"><span data-stu-id="213a0-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**animation segment**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-112">Die grundlegenden Zeit Steuerungs Definitionen einer Animations Funktion. Dabei handelt es sich um die primitiven, aus denen komplexere und übergeordnete Animations Funktionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="213a0-112">The fundamental timing definitions of an animation function; they are the primitives from which more complex and higher level animation functions are built.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**Hintergrund Puffer**</span><span class="sxs-lookup"><span data-stu-id="213a0-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**back buffer**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-114">Ein Rechteck des Arbeitsspeichers, in den eine Anwendung direkt schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="213a0-114">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="213a0-115">Der Hintergrund Puffer wird nie direkt auf dem Monitor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="213a0-115">The back buffer is never directly displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**Batches**</span><span class="sxs-lookup"><span data-stu-id="213a0-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**batch**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-117">Eine Gruppe von directcomposition-Methoden aufrufen, die atomarisch verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="213a0-117">A group of DirectComposition method calls that are processed atomically.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**Bitmap**</span><span class="sxs-lookup"><span data-stu-id="213a0-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-119">Ein Farb Puffer, entweder mit oder ohne einen Alphakanal, der sich im System-oder Videospeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="213a0-119">A color buffer, either with or without an alpha channel, that resides in system or video memory.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**Rahmen Modus**</span><span class="sxs-lookup"><span data-stu-id="213a0-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**border mode**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-121">Eine Eigenschaft eines Microsoft directcomposition-visuellen Elements, das beeinflusst, wie die Ränder einer Bitmap zusammengesetzt werden, wenn die Bitmap so transformiert wird, dass die Ränder nicht an ganzzahlige Koordinaten ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="213a0-121">A property of a Microsoft DirectComposition visual that affects how the edges of a bitmap are composed when the bitmap is transformed such that the edges are not axis-aligned with integer coordinates.</span></span> <span data-ttu-id="213a0-122">Er wirkt sich auch darauf aus, wie der Inhalt an den Ecken eines Clips mit abgerundeten Ecken abgeschnitten wird, und am Rand eines Clips, der transformiert wird, sodass die Ränder nicht an ganzzahlige Koordinaten ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="213a0-122">It also affects how content is clipped at the corners of a clip that has rounded corners, and at the edge of a clip that is transformed such that the edges are not axis-aligned with integer coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**Clip-Objekt**</span><span class="sxs-lookup"><span data-stu-id="213a0-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip object**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-124">Ein-Objekt, das ein Clip Rechteck darstellt.</span><span class="sxs-lookup"><span data-stu-id="213a0-124">A object that represents a clip rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**Clip Rechteck**</span><span class="sxs-lookup"><span data-stu-id="213a0-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**clip rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-126">Ein Satz von Koordinaten, die den Bereich des visuellen Bitmapinhalts definieren, der auf dem Bildschirm gezeichnet wird, wenn die Bitmap gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="213a0-126">A set of coordinates that define the area of visual's bitmap content that is drawn on the screen when the bitmap is rendered.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**Verdeckung**</span><span class="sxs-lookup"><span data-stu-id="213a0-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**cloak**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-128">, Um vorübergehend zu verhindern, dass Desktopfenster-Manager (DWM) ein Fenster auf die Anzeige zeichnet.</span><span class="sxs-lookup"><span data-stu-id="213a0-128">To temporarily prevent Desktop Window Manager (DWM) from drawing a window to the display.</span></span> <span data-ttu-id="213a0-129">Anwendungen verbergen in der Regel ein Fenster, während directcomposition die Bitmap des Fensters in einer Komposition verwendet.</span><span class="sxs-lookup"><span data-stu-id="213a0-129">Applications typically cloak a window while DirectComposition uses the window's bitmap in a composition.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**einzusetzen**</span><span class="sxs-lookup"><span data-stu-id="213a0-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-131">, Um für die Verarbeitung einen Batch von Befehlen an directcompositiondirectcomposition zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="213a0-131">To submit a batch of commands to DirectCompositionDirectComposition for processing.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**zusammengesetzter Modus**</span><span class="sxs-lookup"><span data-stu-id="213a0-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**composite mode**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-133">Eine von mehreren Möglichkeiten, zwei Bitmaps (Quelle und Ziel) zu mischen, um einen bestimmten Effekt zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="213a0-133">One of several ways of blending two bitmaps (a source and a destination) to achieve a particular effect.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**Gas**</span><span class="sxs-lookup"><span data-stu-id="213a0-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composition**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-135">Eine Auflistung von Bitmaps, die kombiniert und bearbeitet werden, indem verschiedene Transformationen, Effekte und Animationen angewendet werden, um ein gewünschtes visuelles Ergebnis in einer Anwendungs Benutzeroberfläche zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="213a0-135">A collection of bitmaps that are combined and manipulated by applying various transforms, effects, and animations to produce an intended visual result in an application UI.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**Fenster "Kompositions Ziel"**</span><span class="sxs-lookup"><span data-stu-id="213a0-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**composition target window**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-137">Das Fenster, an das eine visuelle Struktur gebunden ist, und in dem die resultierende Komposition gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="213a0-137">The window to which a visual tree is bound, and in which the resulting composition is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**entsprechende**</span><span class="sxs-lookup"><span data-stu-id="213a0-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**effect**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-139">Ein Vorgang, der die Art und Weise ändert, in der die Bitmaps einer visuellen Struktur durch Anwenden eines Pixelshaders gerragt werden.</span><span class="sxs-lookup"><span data-stu-id="213a0-139">An operation that modifies how the bitmaps of a visual tree are rasterized, typically by applying a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**Gruppe "Auswirkung"**</span><span class="sxs-lookup"><span data-stu-id="213a0-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**effect group**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-141">Eine Gruppe von Bitmapeffekten, die zusammen angewendet werden, um die rasterisierung der Unterstruktur eines visuellen Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="213a0-141">A group of bitmap effects that are applied together to modify the rasterization of a visual’s sub-tree.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**Dr**</span><span class="sxs-lookup"><span data-stu-id="213a0-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-143">Eine Iterations-Engine, die eine rasterisierung der visuellen Struktur erzeugt.</span><span class="sxs-lookup"><span data-stu-id="213a0-143">An iteration of the composition engine that produces a rasterization of the visual tree.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**Vorder-Puffer**</span><span class="sxs-lookup"><span data-stu-id="213a0-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**front buffer**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-145">Ein Rechteck des Arbeitsspeichers, der vom Grafikadapter übersetzt und auf dem Monitor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="213a0-145">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**Interpolations Modus**</span><span class="sxs-lookup"><span data-stu-id="213a0-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**interpolation mode**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-147">Eine Eigenschaft, die bestimmt, wie eine Bitmap zusammengesetzt wird, wenn Sie transformiert wird, sodass keine 1:1-Entsprechung zwischen Pixeln in der Bitmap und Pixel auf dem Bildschirm vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="213a0-147">A property that determines how a bitmap is composed when it is transformed such that there is no one-to-one correspondence between pixels in the bitmap and pixels on the screen.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**visuelle Stamm Element**</span><span class="sxs-lookup"><span data-stu-id="213a0-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**root visual**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-149">Das visuelle Element, von dem alle anderen visuellen Elemente in einer visuellen Struktur abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="213a0-149">The visual from which all other visuals in a visual tree are descended.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**Austausch Kette**</span><span class="sxs-lookup"><span data-stu-id="213a0-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-151">Eine Auflistung von einem oder mehreren Back Puffern, die seriell dem Vorder-Puffer präsentiert werden können.</span><span class="sxs-lookup"><span data-stu-id="213a0-151">A collection of one or more back buffers that can be serially presented to the front buffer</span></span>

</dd> <dt>

<span data-ttu-id="213a0-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**Oberfläche**</span><span class="sxs-lookup"><span data-stu-id="213a0-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**surface**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-153">Eine Darstellung eines linearen Bereichs des Anzeige Speichers, der sich normalerweise im Anzeige Speicher der Anzeigekarte befindet, obwohl Oberflächen im Systemspeicher vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="213a0-153">A representation of a linear area of display memory that usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**Sin**</span><span class="sxs-lookup"><span data-stu-id="213a0-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-155">Eine Matrix, die eine Koordinatentransformation in einem zweidimensionalen oder dreidimensionalen Raum darstellt.</span><span class="sxs-lookup"><span data-stu-id="213a0-155">A matrix that represents a coordinate transformation in either two-dimensional or three-dimensional space.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**Gruppe transformieren**</span><span class="sxs-lookup"><span data-stu-id="213a0-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**transform group**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-157">Eine Auflistung von Transformationen, deren Matrizen in der Reihenfolge multipliziert werden, in der Sie in der Auflistung angegeben werden, bevor Sie auf ein visuelles Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="213a0-157">A collection of transforms whose matrices are multiplied together in the order in which they are specified in the collection before they are applied to a visual.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Störungen**</span><span class="sxs-lookup"><span data-stu-id="213a0-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**visual**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-159">Ein-Objekt, das einen optionalen Verweis auf ein Bitmap-Objekt enthält, sowie einen Satz von Eigenschaften, die bestimmen, wo und wie die Bitmap auf dem Bildschirm gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="213a0-159">An object that contains an optional reference to a bitmap object, and a set of properties that determine where and how the bitmap is rendered to the screen.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**visuelles Objekt**</span><span class="sxs-lookup"><span data-stu-id="213a0-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**visual object**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-161">Siehe [*Visualisierung*](/windows).</span><span class="sxs-lookup"><span data-stu-id="213a0-161">See [*visual*](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="213a0-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**visuelle Unterstruktur**</span><span class="sxs-lookup"><span data-stu-id="213a0-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**visual subtree**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-163">Ein Teil einer visuellen Struktur, die aus einem bestimmten visuellen Element und allen untergeordneten und untergeordneten visuellen Elementen besteht.</span><span class="sxs-lookup"><span data-stu-id="213a0-163">A portion of a visual tree consisting of a particular visual and all of its child and descendent visuals.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**visuelle Struktur**</span><span class="sxs-lookup"><span data-stu-id="213a0-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**visual tree**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-165">Eine hierarchische Auflistung der visuellen Elemente, die zum Erstellen einer Komposition verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="213a0-165">A hierarchical collection of visuals used to create a composition.</span></span>

</dd> <dt>

<span data-ttu-id="213a0-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**fensterlose Austausch Kette**</span><span class="sxs-lookup"><span data-stu-id="213a0-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**windowless swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="213a0-167">Eine austauschkette, die einem visuellen directcomposition-Objekt anstelle eines Fensters zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="213a0-167">A swap chain that is associated with a DirectComposition visual object instead of a window.</span></span>

</dd> </dl>

 

 