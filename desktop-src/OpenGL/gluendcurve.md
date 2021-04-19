---
title: gluendcurve-Funktion (glu. h)
description: Die Funktionen "glubegincurve" und "gluendcurve" begrenzen eine nicht einheitliche (NURBS) Kurven Definition von Rational B. | gluendcurve-Funktion (glu. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- gluendcurve-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6c0c08bf31135ca82e87d2093ef3b57197955
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361821"
---
# <a name="gluendcurve-function"></a><span data-ttu-id="49cdf-105">gluendcurve-Funktion</span><span class="sxs-lookup"><span data-stu-id="49cdf-105">gluEndCurve function</span></span>

<span data-ttu-id="49cdf-106">Die Funktionen " [**glubegincurve**](glubegincurve.md) " und " **gluendcurve** " begrenzen eine nicht einheitliche ([NURBS](using-nurbs-curves-and-surfaces.md)) Kurven Definition von Rational B.</span><span class="sxs-lookup"><span data-stu-id="49cdf-106">The [**gluBeginCurve**](glubegincurve.md) and **gluEndCurve** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="49cdf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="49cdf-107">Syntax</span></span>


```C++
void WINAPI gluEndCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="49cdf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="49cdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49cdf-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="49cdf-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="49cdf-110">Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="49cdf-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49cdf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49cdf-111">Return value</span></span>

<span data-ttu-id="49cdf-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="49cdf-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49cdf-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49cdf-113">Remarks</span></span>

<span data-ttu-id="49cdf-114">Verwenden Sie " [**glubegincurve**](glubegincurve.md) ", um den Anfang einer nursb-Kurven Definition zu markieren.</span><span class="sxs-lookup"><span data-stu-id="49cdf-114">Use [**gluBeginCurve**](glubegincurve.md) to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="49cdf-115">Nachdem Sie " **glubegincurve**" aufgerufen haben, erstellen Sie einen oder mehrere Aufrufe von " [**glunurbscurve**](glunurbscurve.md) ", um die Attribute der Kurve zu definieren.</span><span class="sxs-lookup"><span data-stu-id="49cdf-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="49cdf-116">Genau einer der Aufrufe von **glunurbscurve** muss den Kurven-Typ GL \_ zuordnung1 \_ Vertex \_ 3 oder GL \_ zuordnung1 \_ Scheitelpunkt \_ 4 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="49cdf-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="49cdf-117">Um das Ende der nursb-Kurven Definition zu markieren, nennen Sie " **gluendcurve**".</span><span class="sxs-lookup"><span data-stu-id="49cdf-117">To mark the end of the NURBS curve definition, call **gluEndCurve**.</span></span>

<span data-ttu-id="49cdf-118">OpenGL-Evaluatoren werden verwendet, um die nursb-Kurve als Reihe von Liniensegmenten zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="49cdf-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="49cdf-119">Der auswersichtsstatus wird während des Renderings mit [**glpushatpub**](glpushattrib.md) (GL \_ eval \_ Bit) und [**glpopatpub**](glpopattrib.md)beibehalten.</span><span class="sxs-lookup"><span data-stu-id="49cdf-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT ) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="49cdf-120">Informationen dazu, in welchem Zustand diese Aufrufe beibehalten werden, finden Sie unter **glpushatpub**.</span><span class="sxs-lookup"><span data-stu-id="49cdf-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="49cdf-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49cdf-121">Examples</span></span>

<span data-ttu-id="49cdf-122">Die folgenden Funktionen erzeugen eine strukturierte nursb-Kurve mit Normals. Texturkoordinaten und normale werden auch als nursb-Kurven angegeben:</span><span class="sxs-lookup"><span data-stu-id="49cdf-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="49cdf-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49cdf-123">Requirements</span></span>



| <span data-ttu-id="49cdf-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49cdf-124">Requirement</span></span> | <span data-ttu-id="49cdf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="49cdf-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="49cdf-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49cdf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="49cdf-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49cdf-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="49cdf-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49cdf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="49cdf-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49cdf-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="49cdf-130">Header</span><span class="sxs-lookup"><span data-stu-id="49cdf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="49cdf-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="49cdf-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="49cdf-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49cdf-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="49cdf-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49cdf-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="49cdf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="49cdf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49cdf-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49cdf-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49cdf-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49cdf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cdf-137">**glpushatpub**</span><span class="sxs-lookup"><span data-stu-id="49cdf-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="49cdf-138">**glubeginsurface**</span><span class="sxs-lookup"><span data-stu-id="49cdf-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="49cdf-139">**glubegintrim**</span><span class="sxs-lookup"><span data-stu-id="49cdf-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="49cdf-140">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="49cdf-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="49cdf-141">**glunurbscurve**</span><span class="sxs-lookup"><span data-stu-id="49cdf-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





