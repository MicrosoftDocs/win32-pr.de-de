---
title: glubegintrim-Funktion (glu. h)
description: Die Funktionen "glubegintrim" und "gluendtrim" begrenzen eine nicht einheitliche, nicht einheitliche rationelle B-Spline (NURBS)-Kürzungs Schleifen Definition. | glubegintrim-Funktion (glu. h)
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- glubegintrim-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluBeginTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84cbe5c1cd0cc68ee892d42fc60db05b6ae2bea6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366582"
---
# <a name="glubegintrim-function"></a><span data-ttu-id="a2389-105">glubegintrim-Funktion</span><span class="sxs-lookup"><span data-stu-id="a2389-105">gluBeginTrim function</span></span>

<span data-ttu-id="a2389-106">Die Funktionen " **glubegintrim** " und " [**gluendtrim**](gluendtrim.md) " begrenzen eine nicht einheitliche, nicht einheitliche rationelle B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md))-Kürzungs Schleifen Definition.</span><span class="sxs-lookup"><span data-stu-id="a2389-106">The **gluBeginTrim** and [**gluEndTrim**](gluendtrim.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming loop definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2389-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2389-107">Syntax</span></span>


```C++
void WINAPI gluBeginTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="a2389-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2389-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2389-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="a2389-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="a2389-110">Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="a2389-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2389-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2389-111">Return value</span></span>

<span data-ttu-id="a2389-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a2389-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2389-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2389-113">Remarks</span></span>

<span data-ttu-id="a2389-114">Verwenden Sie " **glubegintrim** ", um den Anfang einer Kürzungs Schleife zu markieren, und " **gluendtrim** ", um das Ende einer Kürzungs Schleife zu markieren.</span><span class="sxs-lookup"><span data-stu-id="a2389-114">Use **gluBeginTrim** to mark the beginning of a trimming loop, and **gluEndTrim** to mark the end of a trimming loop.</span></span> <span data-ttu-id="a2389-115">Eine Kürzungs Schleife ist ein Satz orientierter Kurven Segmente (die eine geschlossene Kurve bilden), die Grenzen einer nursb-Oberfläche definieren.</span><span class="sxs-lookup"><span data-stu-id="a2389-115">A trimming loop is a set of oriented curve segments (forming a closed curve) that define boundaries of a NURBS surface.</span></span> <span data-ttu-id="a2389-116">Sie fügen diese Kürzungs Schleifen in die Definition einer nursb-Oberfläche ein, zwischen den Aufrufen von " [**glubeginsurface**](glubeginsurface.md) " und " [**gluendsurface**](gluendsurface.md)".</span><span class="sxs-lookup"><span data-stu-id="a2389-116">You include these trimming loops in the definition of a NURBS surface, between calls to [**gluBeginSurface**](glubeginsurface.md) and [**gluEndSurface**](gluendsurface.md).</span></span>

<span data-ttu-id="a2389-117">Die Definition für eine nursb-Oberfläche kann viele Kürzungs Schleifen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a2389-117">The definition for a NURBS surface can contain many trimming loops.</span></span> <span data-ttu-id="a2389-118">Wenn Sie z. b. eine Definition für eine nurb-Oberfläche schreiben, die einem Rechteck mit einem ausgepunkteten Loch ähnelt, würde die Definition zwei Kürzungs Schleifen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a2389-118">For example, if you write a definition for a NURBS surface that resembles a rectangle with a hole punched out, the definition would contain two trimming loops.</span></span> <span data-ttu-id="a2389-119">Eine Schleife würde den äußeren Rand des Rechtecks definieren. die andere würde die ausgepunktete Lücke definieren.</span><span class="sxs-lookup"><span data-stu-id="a2389-119">One loop would define the outer edge of the rectangle; the other would define the punched-out hole.</span></span> <span data-ttu-id="a2389-120">Die Definitionen der einzelnen Kürzungs Schleifen werden von einem " **glubegintrim**  /  **gluendtrim** "-paar in Klammern gesetzt.</span><span class="sxs-lookup"><span data-stu-id="a2389-120">The definitions of each of these trimming loops would be bracketed by a **gluBeginTrim** / **gluEndTrim** pair.</span></span>

<span data-ttu-id="a2389-121">Die Definition einer einzelnen geschlossenen Kürzungs Schleife kann aus mehreren Kurven Segmenten bestehen, die jeweils als eine Reihe von Liniensegmenten beschrieben werden, die eine lineare Kurve bilden (siehe [**glupwlcurve**](glupwlcurve.md)), als eine einzelne nurb-Kurve (siehe [**glunurbscurve**](glunurbscurve.md)) oder als eine Kombination aus beidem in beliebiger Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="a2389-121">The definition of a single closed trimming loop can consist of multiple curve segments, each described as a series of line segments that form a linear curve (see [**gluPwlCurve**](glupwlcurve.md)), as a single NURBS curve (see [**gluNurbsCurve**](glunurbscurve.md)), or as a combination of both in any order.</span></span> <span data-ttu-id="a2389-122">Die einzigen Bibliotheks Aufrufe, die in einer Kürzungs Schleifen Definition (zwischen den Aufrufen von " **glubegintrim** " und " **gluendtrim**") vorkommen können, sind " **glupwlcurve** " und " **glunurbscurve**".</span><span class="sxs-lookup"><span data-stu-id="a2389-122">The only library calls that can appear in a trimming-loop definition (between the calls to **gluBeginTrim** and **gluEndTrim**) are **gluPwlCurve** and **gluNurbsCurve**.</span></span>

<span data-ttu-id="a2389-123">Der angezeigte Bereich der nursb-Oberfläche ist die Region in der Domäne links neben der Kürzungs Kurve, wenn der Kurven Parameter zunimmt.</span><span class="sxs-lookup"><span data-stu-id="a2389-123">The displayed area of the NURBS surface is the region in the domain to the left of the trimming curve as the curve parameter increases.</span></span> <span data-ttu-id="a2389-124">Daher befindet sich der beibehaltene Bereich der nursb-Oberfläche in einer gegen Uhrzeigersinn enden Kürzungs Schleife und außerhalb einer umschneiderschleife im Uhrzeigersinn</span><span class="sxs-lookup"><span data-stu-id="a2389-124">Thus, the retained region of the NURBS surface is inside a counterclockwise trimming loop and outside a clockwise trimming loop.</span></span> <span data-ttu-id="a2389-125">Für das zuvor erwähnte Rechteck wird die Kürzungs Schleife für den äußeren Rand des Rechtecks gegen den Uhrzeigersinn ausgeführt, während die Kürzungs Schleife für das ausgepunktete Loch im Uhrzeigersinn ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2389-125">For the rectangle mentioned earlier, the trimming loop for the outer edge of the rectangle runs counterclockwise, while the trimming loop for the punched-out hole runs clockwise.</span></span>

<span data-ttu-id="a2389-126">Wenn Sie mehr als eine Kurve verwenden, um eine einzelne Kürzungs Schleife zu definieren, müssen die Kurven Segmente eine geschlossene Schleife bilden (d. h., der Endpunkt jeder Kurve muss der Ausgangspunkt der nächsten Kurve sein, und der Endpunkt der abschließenden Kurve muss der Ausgangspunkt der ersten Kurve sein).</span><span class="sxs-lookup"><span data-stu-id="a2389-126">If you use more than one curve to define a single trimming loop, the curve segments must form a closed loop (that is, the endpoint of each curve must be the starting point of the next curve, and the endpoint of the final curve must be the starting point of the first curve).</span></span> <span data-ttu-id="a2389-127">Wenn die Endpunkte der Kurve ausreichend nah beieinander sind, aber nicht genau Coincident, werden Sie gezwungen, eine Übereinstimmung zu finden.</span><span class="sxs-lookup"><span data-stu-id="a2389-127">If the endpoints of the curve are sufficiently close together but not exactly coincident, they will be forced to match.</span></span> <span data-ttu-id="a2389-128">Wenn die Endpunkte nicht ausreichend geschlossen sind, tritt ein Fehler auf (siehe [*glunurbscallback*](glunurbs.md)).</span><span class="sxs-lookup"><span data-stu-id="a2389-128">If the endpoints are not sufficiently close, an error results (see [*gluNurbsCallback*](glunurbs.md)).</span></span>

<span data-ttu-id="a2389-129">Wenn eine Kürzungs Schleifen Definition mehrere Kurven enthält, muss die Richtung der Kurven konsistent sein (d. h., der innere muss sich Links von allen Kurven befinden).</span><span class="sxs-lookup"><span data-stu-id="a2389-129">If a trimming-loop definition contains multiple curves, the direction of the curves must be consistent (that is, the inside must be to the left of all of the curves).</span></span> <span data-ttu-id="a2389-130">Sie können schsted-Kürzungs Schleifen verwenden, wenn sich die Kurve der Kurve ordnungsgemäß ausweist.</span><span class="sxs-lookup"><span data-stu-id="a2389-130">You can use nested trimming loops as long as the curve orientations alternate correctly.</span></span> <span data-ttu-id="a2389-131">Das verkürzen von Kurven kann sich nicht selbst überschneiden, und Sie können sich auch nicht untereinander (oder ein Fehler Ergebnis) überschneiden.</span><span class="sxs-lookup"><span data-stu-id="a2389-131">Trimming curves cannot be self-intersecting, nor can they intersect one another (or an error results).</span></span>

<span data-ttu-id="a2389-132">Wenn keine Kürzungs Informationen für eine nursb-Oberfläche angegeben werden, wird die gesamte Oberfläche gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a2389-132">If no trimming information is given for a NURBS surface, the entire surface is drawn.</span></span>

## <a name="examples"></a><span data-ttu-id="a2389-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2389-133">Examples</span></span>

<span data-ttu-id="a2389-134">Dieses Code Fragment definiert eine Kürzungs Schleife, die aus einer schrittweisen linearen Kurve und zwei nursb-Kurven besteht:</span><span class="sxs-lookup"><span data-stu-id="a2389-134">This code fragment defines a trimming loop that consists of one piecewise linear curve and two NURBS curves:</span></span>

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a><span data-ttu-id="a2389-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2389-135">Requirements</span></span>



| <span data-ttu-id="a2389-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2389-136">Requirement</span></span> | <span data-ttu-id="a2389-137">Wert</span><span class="sxs-lookup"><span data-stu-id="a2389-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2389-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2389-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a2389-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2389-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a2389-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2389-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a2389-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2389-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a2389-142">Header</span><span class="sxs-lookup"><span data-stu-id="a2389-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2389-143"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2389-143"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="a2389-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2389-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2389-145"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2389-145"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a2389-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a2389-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2389-147"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2389-147"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2389-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2389-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2389-149">**glubeginsurface**</span><span class="sxs-lookup"><span data-stu-id="a2389-149">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="a2389-150">**gluendsurface**</span><span class="sxs-lookup"><span data-stu-id="a2389-150">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="a2389-151">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="a2389-151">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="a2389-152">*glunurbscallback*</span><span class="sxs-lookup"><span data-stu-id="a2389-152">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="a2389-153">**glunurbscurve**</span><span class="sxs-lookup"><span data-stu-id="a2389-153">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="a2389-154">**glupwlcurve**</span><span class="sxs-lookup"><span data-stu-id="a2389-154">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





