---
title: glutessproperty-Funktion (glu. h)
description: Die Funktion "glutessproperty" legt die-Eigenschaft eines Mosaik Objekts fest.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- glutessproperty-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105897"
---
# <a name="glutessproperty-function"></a><span data-ttu-id="ad46b-104">glutessproperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="ad46b-104">gluTessProperty function</span></span>

<span data-ttu-id="ad46b-105">Die Funktion " **glutessproperty** " legt die-Eigenschaft eines Mosaik Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="ad46b-105">The **gluTessProperty** function sets the property of a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad46b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad46b-106">Syntax</span></span>


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a><span data-ttu-id="ad46b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad46b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad46b-108">*ATI*</span><span class="sxs-lookup"><span data-stu-id="ad46b-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="ad46b-109">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="ad46b-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ad46b-110">*,*</span><span class="sxs-lookup"><span data-stu-id="ad46b-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="ad46b-111">Der festzulegende Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="ad46b-111">The property value to set.</span></span> <span data-ttu-id="ad46b-112">Die folgenden Werte sind gültig: die \_ Regel "glu Tess" \_ , " \_ glu Tess" und " \_ \_ \_ glu- \_ Toleranz" \_ .</span><span class="sxs-lookup"><span data-stu-id="ad46b-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>



| <span data-ttu-id="ad46b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ad46b-113">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="ad46b-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ad46b-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <span data-ttu-id="ad46b-115"><dt>**Glu \_ - \_ aufwickungsregel \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ad46b-115"><dt>**GLU\_TESS\_WINDING\_RULE**</dt></span></span> </dl>    | <span data-ttu-id="ad46b-116">Bestimmt, welche Teile des Polygons sich im Inneren befinden.</span><span class="sxs-lookup"><span data-stu-id="ad46b-116">Determines which parts of the polygon are on the interior.</span></span> <span data-ttu-id="ad46b-117">Der value-Parameter kann auf einen der folgenden Werte festgelegt werden: glu \_ Tess \_ \_ , ungerade, Glu Tess \_ Winding ungleich \_ \_ NULL, Glu \_ Tess \_ Winding \_ positiv, Glu \_ Tess \_ Winding \_ negative oder glu \_ Tess \_ Winding \_ ABS \_ GEQ \_ Two.</span><span class="sxs-lookup"><span data-stu-id="ad46b-117">The value parameter may be set to one of the following: GLU\_TESS\_WINDING\_ODD, GLU\_TESS\_WINDING\_NONZERO, GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, or GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO.</span></span> <br/> <span data-ttu-id="ad46b-118">Um zu verstehen, wie die Regel für die Regel funktioniert, sollten Sie zuerst berücksichtigen, dass die Eingabe Kontur die Ebene in Regionen partitioniert.</span><span class="sxs-lookup"><span data-stu-id="ad46b-118">To understand how the winding rule works, first consider that the input contours partition the plane into regions.</span></span> <span data-ttu-id="ad46b-119">Die Wicklungs Regel bestimmt, welche dieser Regionen sich innerhalb des Polygons befinden.</span><span class="sxs-lookup"><span data-stu-id="ad46b-119">The winding rule determines which of these regions are inside the polygon.</span></span><br/> <span data-ttu-id="ad46b-120">Bei einer Einzel Kontur-c ist die Zahl von x Punkt x einfach die signierte Anzahl von Umdrehungen, die wir ungefähr x durchführen, während wir einmal um c herumreisen (wobei gegen den Uhrzeigersinn positiv ist).</span><span class="sxs-lookup"><span data-stu-id="ad46b-120">For a single-contour C, the winding number of a point x is simply the signed number of revolutions we make around x as we travel once around C (where counterclockwise is positive).</span></span> <span data-ttu-id="ad46b-121">Wenn mehrere Kontur vorhanden sind, werden die einzelnen aufwicklungs Zahlen summiert.</span><span class="sxs-lookup"><span data-stu-id="ad46b-121">When there are several contours, the individual winding numbers are summed.</span></span> <span data-ttu-id="ad46b-122">Diese Prozedur ordnet jedem Punkt x in der Ebene einen ganzzahligen Wert mit Vorzeichen zu.</span><span class="sxs-lookup"><span data-stu-id="ad46b-122">This procedure associates a signed integer value with each point x in the plane.</span></span> <span data-ttu-id="ad46b-123">Beachten Sie, dass die Anzahl der Wicklungen für alle Punkte in einer einzelnen Region identisch ist.</span><span class="sxs-lookup"><span data-stu-id="ad46b-123">Note that the winding number is the same for all points in a single region.</span></span><br/> <span data-ttu-id="ad46b-124">Die Wicklungs Regel klassifiziert einen Bereich als "innen", wenn die zugehörige Zahl zur ausgewählten Kategorie gehört (ungerade, nicht NULL, positiv, negativ oder absoluter Wert von mindestens zwei).</span><span class="sxs-lookup"><span data-stu-id="ad46b-124">The winding rule classifies a region as "inside" if its winding number belongs to the chosen category (odd, nonzero, positive, negative, or absolute value of at least two).</span></span> <span data-ttu-id="ad46b-125">Der vorherige glu-Mosaik Speicher (vor der Verwendung von Glu 1,2) hat die Regel "ungerade" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad46b-125">The previous GLU tessellator (prior to GLU 1.2) used the "odd" rule.</span></span> <span data-ttu-id="ad46b-126">Die Regel "nicht NULL" (GLU \_ Tess \_ \_ , nicht null) ist eine andere gängige Methode zum Definieren des Inneren.</span><span class="sxs-lookup"><span data-stu-id="ad46b-126">The "nonzero" rule (GLU\_TESS\_WINDING\_NONZERO) is another common way to define the interior.</span></span> <span data-ttu-id="ad46b-127">Die anderen drei Regeln ( \_ atentess \_ Winding \_ positiv, Glu \_ Tess \_ Winding \_ negativ, Glu \_ Tess \_ Winding \_ ABS \_ GEQ \_ Two) eignen sich für Polygon-CSG-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="ad46b-127">The other three rules (GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO) are useful for polygon CSG operations.</span></span><br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <span data-ttu-id="ad46b-128"><dt>**nur die Grenze von Glu \_ Tess \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ad46b-128"><dt>**GLU\_TESS\_BOUNDARY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="ad46b-129">Gibt einen booleschen Wert an (legen Sie den Wert auf GL \_ true oder GL \_ false fest).</span><span class="sxs-lookup"><span data-stu-id="ad46b-129">Specifies a Boolean value (set value to GL\_TRUE or GL\_FALSE).</span></span> <span data-ttu-id="ad46b-130">Wenn Sie Value auf den Wert "GL true" festlegen \_ , wird anstelle eines Mosaik Satzes eine Reihe geschlossener Kontur zurückgegeben, die das Polygon innere und das äußere trennt.</span><span class="sxs-lookup"><span data-stu-id="ad46b-130">When you set value to GL\_TRUE, a set of closed contours separating the polygon interior and exterior is returned instead of a tessellation.</span></span> <span data-ttu-id="ad46b-131">Äußere Kontur werden im Uhrzeigersinn gegen den Uhrzeigersinn ausgerichtet. innere Kontur werden im Uhrzeigersinn ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="ad46b-131">Exterior contours are oriented counterclockwise with respect to the normal; interior contours are oriented clockwise.</span></span> <span data-ttu-id="ad46b-132">Die \_ \_ Daten Rückrufe von Glu Tess BEGIN und glu \_ Tess \_ \_ verwenden die Type GL- \_ Zeilen \_ Schleife für jede Kontur.</span><span class="sxs-lookup"><span data-stu-id="ad46b-132">The GLU\_TESS\_BEGIN and GLU\_TESS\_BEGIN\_DATA callbacks use the type GL\_LINE\_LOOP for each contour.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <span data-ttu-id="ad46b-133"><dt>**Glu \_ Tess- \_ Toleranz**</dt></span><span class="sxs-lookup"><span data-stu-id="ad46b-133"><dt>**GLU\_TESS\_TOLERANCE**</dt></span></span> </dl>              | <span data-ttu-id="ad46b-134">Gibt eine Toleranz für das Zusammenführen von Features an, um die Größe der Ausgabe zu verringern.</span><span class="sxs-lookup"><span data-stu-id="ad46b-134">Specifies a tolerance for merging features to reduce the size of the output.</span></span> <span data-ttu-id="ad46b-135">Beispielsweise können zwei vertexen, die sich sehr nahe beieinander befinden, durch einen einzelnen Scheitelpunkt ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ad46b-135">For example, two vertexes that are very close to each other might be replaced by a single vertex.</span></span> <span data-ttu-id="ad46b-136">Die Toleranz wird mit der größten Koordinaten Größe eines beliebigen Eingabe Vertex multipliziert. Gibt den maximalen Abstand an, den ein beliebiges Feature als Ergebnis eines einzelnen zusammenlaufvorgangs verschieben kann.</span><span class="sxs-lookup"><span data-stu-id="ad46b-136">The tolerance is multiplied by the largest coordinate magnitude of any input vertex; this specifies the maximum distance that any feature can move as the result of a single merge operation.</span></span> <span data-ttu-id="ad46b-137">Wenn eine einzelne Funktion an mehreren Merge-Vorgängen beteiligt ist, kann die gesamte verschoderte Entfernung größer sein.</span><span class="sxs-lookup"><span data-stu-id="ad46b-137">If a single feature takes part in several merge operations, the total distance moved can be larger.</span></span> <br/> <span data-ttu-id="ad46b-138">Das Zusammenführen von Funktionen ist vollständig optional. die Toleranz ist nur ein Hinweis.</span><span class="sxs-lookup"><span data-stu-id="ad46b-138">Feature merging is completely optional; the tolerance is only a hint.</span></span> <span data-ttu-id="ad46b-139">Die Implementierung kann in einigen Fällen zusammengeführt werden, nicht in anderen, oder es werden niemals Features überhaupt zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="ad46b-139">The implementation is free to merge in some cases and not in others, or to never merge features at all.</span></span> <span data-ttu-id="ad46b-140">Die Standardtoleranz ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ad46b-140">The default tolerance is zero.</span></span><br/> <span data-ttu-id="ad46b-141">Die aktuelle Implementierung führt Eckpunkte nur dann zusammen, wenn Sie unabhängig von der aktuellen Toleranz genau Coincident sind.</span><span class="sxs-lookup"><span data-stu-id="ad46b-141">The current implementation merges vertexes only if they are exactly coincident, regardless of the current tolerance.</span></span> <span data-ttu-id="ad46b-142">Ein Scheitelpunkt wird nur dann in einen Edge gesplitet, wenn die Implementierung nicht unterscheiden kann, auf welcher Seite der Kante der Scheitelpunkt liegt.</span><span class="sxs-lookup"><span data-stu-id="ad46b-142">A vertex is spliced into an edge only if the implementation is unable to distinguish which side of the edge the vertex lies on.</span></span> <span data-ttu-id="ad46b-143">Zwei Ränder werden nur zusammengeführt, wenn beide Endpunkte identisch sind.</span><span class="sxs-lookup"><span data-stu-id="ad46b-143">Two edges are merged only when both endpoints are identical.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="ad46b-144">*value*</span><span class="sxs-lookup"><span data-stu-id="ad46b-144">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="ad46b-145">Der Wert der angegeben Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ad46b-145">The value of the indicated property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad46b-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad46b-146">Return value</span></span>

<span data-ttu-id="ad46b-147">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ad46b-147">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad46b-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad46b-148">Remarks</span></span>

<span data-ttu-id="ad46b-149">Die Funktion " **glutessproperty** " steuert Eigenschaften, die in einem Mosaik Objekt gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="ad46b-149">The **gluTessProperty** function controls properties stored in a tessellation object.</span></span> <span data-ttu-id="ad46b-150">Diese Eigenschaften beeinflussen die Art und Weise, wie Polygone interpretiert und gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="ad46b-150">These properties affect the way the polygons are interpreted and rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad46b-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad46b-151">Requirements</span></span>



| <span data-ttu-id="ad46b-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad46b-152">Requirement</span></span> | <span data-ttu-id="ad46b-153">Wert</span><span class="sxs-lookup"><span data-stu-id="ad46b-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ad46b-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad46b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ad46b-155">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad46b-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ad46b-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad46b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ad46b-157">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad46b-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ad46b-158">Header</span><span class="sxs-lookup"><span data-stu-id="ad46b-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad46b-159"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad46b-159"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ad46b-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ad46b-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad46b-161"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad46b-161"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ad46b-162">DLL</span><span class="sxs-lookup"><span data-stu-id="ad46b-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad46b-163"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad46b-163"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad46b-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad46b-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad46b-165">**"glugettessproperty"**</span><span class="sxs-lookup"><span data-stu-id="ad46b-165">**gluGetTessProperty**</span></span>](glugettessproperty.md)
</dt> <dt>

[<span data-ttu-id="ad46b-166">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="ad46b-166">**gluNewTess**</span></span>](glunewtess.md)
</dt> </dl>

 

 





