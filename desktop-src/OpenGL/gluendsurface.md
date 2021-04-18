---
title: gluendsurface-Funktion (glu. h)
description: Die Funktionen "glubeginsurface" und "gluendsurface" begrenzen eine nicht einheitliche Oberflächen Definition von "Rational B-Spline (NURBS)". | gluendsurface-Funktion (glu. h)
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
keywords:
- gluendsurface-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluEndSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54631d5c4ef752cffd989f8fa02f8cb512c67da3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530719"
---
# <a name="gluendsurface-function"></a><span data-ttu-id="dfde8-105">gluendsurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="dfde8-105">gluEndSurface function</span></span>

<span data-ttu-id="dfde8-106">Die Funktionen " [**glubeginsurface**](glubeginsurface.md) " und " **gluendsurface** " begrenzen eine nicht einheitliche Oberflächen Definition von "Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md))".</span><span class="sxs-lookup"><span data-stu-id="dfde8-106">The [**gluBeginSurface**](glubeginsurface.md) and **gluEndSurface** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfde8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfde8-107">Syntax</span></span>


```C++
void WINAPI gluEndSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="dfde8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfde8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfde8-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="dfde8-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="dfde8-110">Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="dfde8-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfde8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfde8-111">Return value</span></span>

<span data-ttu-id="dfde8-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dfde8-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfde8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfde8-113">Remarks</span></span>

<span data-ttu-id="dfde8-114">Die Funktionen " [**glubeginsurface**](glubeginsurface.md) " und " **gluendsurface** " markieren den Anfang und das Ende der nurb-Oberflächen Definitionen, die mit Aufrufen von " **glunurbssurface**" definiert werden.</span><span class="sxs-lookup"><span data-stu-id="dfde8-114">The [**gluBeginSurface**](glubeginsurface.md) and **gluEndSurface** functions mark the beginning and end of NURBS surface definitions, which are defined with calls to **gluNurbsSurface**.</span></span>

1.  <span data-ttu-id="dfde8-115">Aufrufen von " **glubeginsurface** ", um den Anfang einer nursb-Oberflächen Definition zu markieren.</span><span class="sxs-lookup"><span data-stu-id="dfde8-115">Call **gluBeginSurface** to mark the beginning of a NURBS surface definition.</span></span>
2.  <span data-ttu-id="dfde8-116">Erstellen Sie einen oder mehrere Aufrufe von **glunurbssurface** , um die Attribute der Oberfläche zu definieren.</span><span class="sxs-lookup"><span data-stu-id="dfde8-116">Make one or more calls to **gluNurbsSurface** to define the attributes of the surface.</span></span>

    <span data-ttu-id="dfde8-117">Genau einer dieser Aufrufe von **glunurbssurface** muss den Surface-Typ GL \_ map2 \_ Vertex \_ 3 oder GL \_ map2 \_ Scheitelpunkt \_ 4 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dfde8-117">Exactly one of these calls to **gluNurbsSurface** must have a surface type of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4.</span></span>

3.  <span data-ttu-id="dfde8-118">Um das Ende der nursb-Oberflächen Definition zu markieren, nennen Sie " **gluendsurface**".</span><span class="sxs-lookup"><span data-stu-id="dfde8-118">To mark the end of the NURBS surface definition, call **gluEndSurface**.</span></span>

<span data-ttu-id="dfde8-119">Die Funktionen [**glubegintrim**](glubegintrim.md), [**glupwlcurve**](glupwlcurve.md), [**glunurbscurve**](glunurbscurve.md)und **gluendtrim** unterstützen das Kürzen von nurb-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="dfde8-119">The [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md), and **gluEndTrim** functions support trimming of NURBS surfaces.</span></span>

<span data-ttu-id="dfde8-120">Verwenden Sie OpenGL-Auswertungen, um die nursb-Oberfläche als eine Reihe von Polygonen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="dfde8-120">Use OpenGL evaluators to render the NURBS surface as a set of polygons.</span></span> <span data-ttu-id="dfde8-121">Bewahren Sie den auswertsauswertszustand während des Renderings mit [**glpushatpub**](glpushattrib.md) (GL \_ eval \_ Bit) und [**glpopatpub**](glpopattrib.md)auf.</span><span class="sxs-lookup"><span data-stu-id="dfde8-121">Preserve the evaluator state during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dfde8-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfde8-122">Examples</span></span>

<span data-ttu-id="dfde8-123">Die folgenden Funktionen Renten eine strukturierte nursb-Oberfläche mit Normals. die Texturkoordinaten und normale werden auch als nursb-Oberflächen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="dfde8-123">The following functions render a textured NURBS surface with normals; the texture coordinates and normals are also described as NURBS surfaces:</span></span>

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a><span data-ttu-id="dfde8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfde8-124">Requirements</span></span>



| <span data-ttu-id="dfde8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfde8-125">Requirement</span></span> | <span data-ttu-id="dfde8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="dfde8-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dfde8-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfde8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dfde8-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfde8-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dfde8-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfde8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dfde8-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfde8-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dfde8-131">Header</span><span class="sxs-lookup"><span data-stu-id="dfde8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfde8-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfde8-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="dfde8-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dfde8-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="dfde8-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfde8-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dfde8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="dfde8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfde8-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfde8-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfde8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfde8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfde8-138">**glubegincurve**</span><span class="sxs-lookup"><span data-stu-id="dfde8-138">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="dfde8-139">**glubegintrim**</span><span class="sxs-lookup"><span data-stu-id="dfde8-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="dfde8-140">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="dfde8-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="dfde8-141">**glunurbscurve**</span><span class="sxs-lookup"><span data-stu-id="dfde8-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="dfde8-142">**glunurbssurface**</span><span class="sxs-lookup"><span data-stu-id="dfde8-142">**gluNurbsSurface**</span></span>](glunurbssurface.md)
</dt> <dt>

[<span data-ttu-id="dfde8-143">**glupwlcurve**</span><span class="sxs-lookup"><span data-stu-id="dfde8-143">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





