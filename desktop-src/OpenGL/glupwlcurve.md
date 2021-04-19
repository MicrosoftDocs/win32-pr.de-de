---
title: glupwlcurve-Funktion (glu. h)
description: Die Funktion "glupwlcurve" beschreibt eine schrittweise lineare, lineare, nicht einheitliche rationelle B-Spline-Kürzungs Kurve (NURBS).
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- glupwlcurve-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345913"
---
# <a name="glupwlcurve-function"></a><span data-ttu-id="ee017-104">glupwlcurve-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee017-104">gluPwlCurve function</span></span>

<span data-ttu-id="ee017-105">Die Funktion " **glupwlcurve** " beschreibt eine schrittweise lineare, lineare, nicht einheitliche rationelle B-Spline-Kürzungs Kurve ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="ee017-105">The **gluPwlCurve** function describes a piecewise linear Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee017-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee017-106">Syntax</span></span>


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="ee017-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee017-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee017-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="ee017-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="ee017-109">Das NURBS-Objekt (mit [**glunewnurbsrenderer**](glunewnurbsrenderer.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="ee017-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ee017-110">*count*</span><span class="sxs-lookup"><span data-stu-id="ee017-110">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="ee017-111">Die Anzahl der Punkte in der Kurve.</span><span class="sxs-lookup"><span data-stu-id="ee017-111">The number of points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="ee017-112">*array*</span><span class="sxs-lookup"><span data-stu-id="ee017-112">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="ee017-113">Ein Array, das die Kurven Punkte enthält.</span><span class="sxs-lookup"><span data-stu-id="ee017-113">An array containing the curve points.</span></span>

</dd> <dt>

<span data-ttu-id="ee017-114">*Schritt*</span><span class="sxs-lookup"><span data-stu-id="ee017-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="ee017-115">Der Offset (eine Anzahl von Gleit Komma Werten mit einfacher Genauigkeit) zwischen den Punkten der Kurve.</span><span class="sxs-lookup"><span data-stu-id="ee017-115">The offset (a number of single-precision floating-point values) between points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="ee017-116">*type*</span><span class="sxs-lookup"><span data-stu-id="ee017-116">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="ee017-117">Der Typ der Kurve.</span><span class="sxs-lookup"><span data-stu-id="ee017-117">The type of curve.</span></span> <span data-ttu-id="ee017-118">Muss entweder "glu \_ zuordnung1 \_ Trim \_ 2" oder "glu \_ zuordnung1 \_ Trim \_ 3" lauten.</span><span class="sxs-lookup"><span data-stu-id="ee017-118">Must be either GLU\_MAP1\_TRIM\_2 or GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee017-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee017-119">Return value</span></span>

<span data-ttu-id="ee017-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ee017-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee017-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee017-121">Remarks</span></span>

<span data-ttu-id="ee017-122">Die Funktion " **glupwlcurve** " beschreibt eine schrittweise lineare Kürzungs Kurve für eine nursb-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="ee017-122">The **gluPwlCurve** function describes a piecewise linear trimming curve for a NURBS surface.</span></span> <span data-ttu-id="ee017-123">Eine schrittweise lineare Kurve besteht aus einer Liste von Koordinaten der Punkte im Parameter Bereich für die zu gekürzte nursb-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="ee017-123">A piecewise linear curve consists of a list of coordinates of points in the parameter space for the NURBS surface to be trimmed.</span></span> <span data-ttu-id="ee017-124">Diese Punkte sind mit Liniensegmenten verbunden, um eine Kurve zu bilden.</span><span class="sxs-lookup"><span data-stu-id="ee017-124">These points are connected with line segments to form a curve.</span></span> <span data-ttu-id="ee017-125">Wenn die Kurve eine Annäherung an eine echte Kurve ist, sollten die Punkte nahe genug sein, damit der resultierende Pfad bei der in der Anwendung verwendeten Auflösung gekrümmte angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ee017-125">If the curve is an approximation to a real curve, the points should be close enough that the resulting path appears curved at the resolution used in the application.</span></span>

<span data-ttu-id="ee017-126">Wenn der *Typ* "glu \_ zuordnung1 Trim 2" ist, wird \_ \_ eine Kurve im zweidimensionalen (*u* -und *v*-) Parameter Bereich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee017-126">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="ee017-127">Wenn dies der Fall \_ ist \_ \_ , wird eine Kurve im zweidimensionalen, homogenen (*u*, *v*-und *w*)-Parameter Bereich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee017-127">If it is GLU\_MAP1\_TRIM\_3, then it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="ee017-128">Weitere Informationen zu Kürzungs Kurven finden Sie unter " [**glubegintrim**](glubegintrim.md)".</span><span class="sxs-lookup"><span data-stu-id="ee017-128">For more information about trimming curves, see [**gluBeginTrim**](glubegintrim.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee017-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee017-129">Requirements</span></span>



| <span data-ttu-id="ee017-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee017-130">Requirement</span></span> | <span data-ttu-id="ee017-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ee017-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ee017-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee017-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ee017-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee017-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ee017-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee017-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ee017-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee017-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ee017-136">Header</span><span class="sxs-lookup"><span data-stu-id="ee017-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee017-137"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee017-137"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ee017-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ee017-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee017-139"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee017-139"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ee017-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ee017-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee017-141"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee017-141"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee017-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee017-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee017-143">**glubegincurve**</span><span class="sxs-lookup"><span data-stu-id="ee017-143">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="ee017-144">**glubegintrim**</span><span class="sxs-lookup"><span data-stu-id="ee017-144">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="ee017-145">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="ee017-145">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="ee017-146">**glunurbscurve**</span><span class="sxs-lookup"><span data-stu-id="ee017-146">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





