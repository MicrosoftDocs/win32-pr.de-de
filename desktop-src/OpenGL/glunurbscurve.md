---
title: glunurbscurve-Funktion (glu. h)
description: Die Funktion "glunurbscurve" definiert die Form einer nicht einheitlichen rationellen B-Spline-Kurve (NURBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- glunurbscurve-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339140"
---
# <a name="glunurbscurve-function"></a><span data-ttu-id="6ba69-104">glunurbscurve-Funktion</span><span class="sxs-lookup"><span data-stu-id="6ba69-104">gluNurbsCurve function</span></span>

<span data-ttu-id="6ba69-105">Die Funktion " **glunurbscurve** " definiert die Form einer nicht einheitlichen rationellen B-Spline-Kurve ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="6ba69-105">The **gluNurbsCurve** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba69-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ba69-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="6ba69-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ba69-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba69-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="6ba69-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="6ba69-109">Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="6ba69-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6ba69-110">*nknoten*</span><span class="sxs-lookup"><span data-stu-id="6ba69-110">*nknots*</span></span> 
</dt> <dd>

<span data-ttu-id="6ba69-111">Die Anzahl der Knoten im- *Knoten*.</span><span class="sxs-lookup"><span data-stu-id="6ba69-111">The number of knots in *knot*.</span></span> <span data-ttu-id="6ba69-112">Der *nknoparameter* ist mit der Anzahl der Kontrollpunkte zuzüglich der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="6ba69-112">The *nknots* parameter equals the number of control points plus the order.</span></span>

</dd> <dt>

<span data-ttu-id="6ba69-113">*knir*</span><span class="sxs-lookup"><span data-stu-id="6ba69-113">*knot*</span></span> 
</dt> <dd>

<span data-ttu-id="6ba69-114">Ein Array von *nknoten-* Zeichen Werten, die sich nicht verkleinern.</span><span class="sxs-lookup"><span data-stu-id="6ba69-114">An array of *nknots* nondecreasing knot values.</span></span>

</dd> <dt>

<span data-ttu-id="6ba69-115">*Schritt*</span><span class="sxs-lookup"><span data-stu-id="6ba69-115">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="6ba69-116">Der Offset (als Anzahl von Gleit Komma Werten mit einfacher Genauigkeit) zwischen aufeinander folgenden Kurven Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="6ba69-116">The offset (as a number of single-precision floating-point values) between successive curve control points.</span></span>

</dd> <dt>

<span data-ttu-id="6ba69-117">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="6ba69-117">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="6ba69-118">Ein Zeiger auf ein Array von Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="6ba69-118">A pointer to an array of control points.</span></span> <span data-ttu-id="6ba69-119">Die Koordinaten müssen mit dem *Typ* übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6ba69-119">The coordinates must agree with *type*.</span></span>

</dd> <dt>

<span data-ttu-id="6ba69-120">*order*</span><span class="sxs-lookup"><span data-stu-id="6ba69-120">*order*</span></span> 
</dt> <dd>

<span data-ttu-id="6ba69-121">Die Reihenfolge der nursb-Kurve.</span><span class="sxs-lookup"><span data-stu-id="6ba69-121">The order of the NURBS curve.</span></span> <span data-ttu-id="6ba69-122">Der *Order* -Parameter ist mit dem Grad + 1; Daher hat eine kubische Kurve eine Reihenfolge von 4.</span><span class="sxs-lookup"><span data-stu-id="6ba69-122">The *order* parameter equals degree + 1; hence a cubic curve has an order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="6ba69-123">*type*</span><span class="sxs-lookup"><span data-stu-id="6ba69-123">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="6ba69-124">Der Typ der Kurve.</span><span class="sxs-lookup"><span data-stu-id="6ba69-124">The type of the curve.</span></span> <span data-ttu-id="6ba69-125">Wenn diese Kurve innerhalb eines " [**glubegincurve**](glubegincurve.md)"-Paares " / [**gluendcurve**](gluendcurve.md) " definiert ist, kann der Typ jeder der gültigen eindimensionalen auswerterypen (z. b. gl \_ zuordnung1 \_ Vertex \_ 3 oder GL \_ zuordnung1 \_ Color \_ 4) sein.</span><span class="sxs-lookup"><span data-stu-id="6ba69-125">If this curve is defined within a [**gluBeginCurve**](glubegincurve.md)/[**gluEndCurve**](gluendcurve.md) pair, then the type can be any of the valid one-dimensional evaluator types (such as GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_COLOR\_4).</span></span> <span data-ttu-id="6ba69-126">Zwischen einem " [**glubegintrim**](glubegintrim.md) / [**gluendtrim**](gluendtrim.md) "-paar sind nur die gültigen Typen "glu \_ zuordnung1 \_ Trim \_ 2" und "glu \_ zuordnung1 \_ Trim \_ 3" zulässig.</span><span class="sxs-lookup"><span data-stu-id="6ba69-126">Between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, the only valid types are GLU\_MAP1\_TRIM\_2 and GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba69-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ba69-127">Return value</span></span>

<span data-ttu-id="6ba69-128">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6ba69-128">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ba69-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ba69-129">Remarks</span></span>

<span data-ttu-id="6ba69-130">Wenn **glunurbscurve** zwischen einem " **glubegincurve**"-paar " / **gluendcurve** " angezeigt wird, wird eine Kurve beschrieben, die gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="6ba69-130">When **gluNurbsCurve** appears between a **gluBeginCurve**/**gluEndCurve** pair, it describes a curve to be rendered.</span></span> <span data-ttu-id="6ba69-131">Sie ordnen positionelle, Textur-und Farbkoordinaten zu, indem Sie diese als separate " **glunurbscurve** " zwischen einem " **glubegincurve**"-paar " / **gluendcurve** " darstellen.</span><span class="sxs-lookup"><span data-stu-id="6ba69-131">You associate positional, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** between a **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="6ba69-132">Nehmen Sie nicht mehr als einen Aufrufen von **glunurbscurve** für Farb-, Positions-und Textur Daten innerhalb eines einzelnen **glubegincurve**- / **gluendcurve** -Paars vor.</span><span class="sxs-lookup"><span data-stu-id="6ba69-132">Do not make more than one call to **gluNurbsCurve** for color, position, and texture data within a single **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="6ba69-133">Machen Sie genau einen Aufrufs, um die Position der Kurve zu beschreiben (ein *Typ* von GL \_ zuordnung1 \_ Vertex \_ 3 oder GL \_ zuordnung1 \_ Scheitelpunkt \_ 4).</span><span class="sxs-lookup"><span data-stu-id="6ba69-133">Make exactly one call to describe the position of the curve (a *type* of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4).</span></span>

<span data-ttu-id="6ba69-134">Wenn **glunurbscurve** zwischen einem " [**glubegintrim**](glubegintrim.md) / [**gluendtrim**](gluendtrim.md) "-paar angezeigt wird, wird eine Kürzungs Kurve auf einer nurb-Oberfläche beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ba69-134">When **gluNurbsCurve** appears between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, it describes a trimming curve on a NURBS surface.</span></span> <span data-ttu-id="6ba69-135">Wenn der *Typ* "glu \_ zuordnung1 Trim 2" ist, wird \_ \_ eine Kurve im zweidimensionalen (*u* -und *v*-) Parameter Bereich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ba69-135">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="6ba69-136">Wenn dies der Fall \_ ist \_ \_ , wird eine Kurve im zweidimensionalen, homogenen (*u*, *v*-und *w*)-Parameter Bereich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ba69-136">If it is GLU\_MAP1\_TRIM\_3, it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="6ba69-137">Weitere Informationen zu Kürzungs Kurven finden Sie unter " **glubegintrim**".</span><span class="sxs-lookup"><span data-stu-id="6ba69-137">For more discussion about trimming curves, see **gluBeginTrim**.</span></span>

## <a name="examples"></a><span data-ttu-id="6ba69-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ba69-138">Examples</span></span>

<span data-ttu-id="6ba69-139">Die folgenden Funktionen erzeugen eine strukturierte nursb-Kurve mit normalen:</span><span class="sxs-lookup"><span data-stu-id="6ba69-139">The following functions render a textured NURBS curve with normals:</span></span>

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
```

## <a name="requirements"></a><span data-ttu-id="6ba69-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ba69-140">Requirements</span></span>



| <span data-ttu-id="6ba69-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ba69-141">Requirement</span></span> | <span data-ttu-id="6ba69-142">Wert</span><span class="sxs-lookup"><span data-stu-id="6ba69-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba69-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ba69-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba69-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ba69-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6ba69-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ba69-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba69-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ba69-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6ba69-147">Header</span><span class="sxs-lookup"><span data-stu-id="6ba69-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ba69-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ba69-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="6ba69-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6ba69-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ba69-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ba69-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ba69-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6ba69-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ba69-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ba69-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba69-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ba69-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba69-154">**glubegincurve**</span><span class="sxs-lookup"><span data-stu-id="6ba69-154">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="6ba69-155">**glubegintrim**</span><span class="sxs-lookup"><span data-stu-id="6ba69-155">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="6ba69-156">**gluendcurve**</span><span class="sxs-lookup"><span data-stu-id="6ba69-156">**gluEndCurve**</span></span>](gluendcurve.md)
</dt> <dt>

[<span data-ttu-id="6ba69-157">**gluendtrim**</span><span class="sxs-lookup"><span data-stu-id="6ba69-157">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="6ba69-158">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="6ba69-158">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="6ba69-159">**glupwlcurve**</span><span class="sxs-lookup"><span data-stu-id="6ba69-159">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





