---
title: glEvalPoint1-Funktion (GL. h)
description: Die glEvalPoint1-Funktion und die glEvalPoint2-Funktion generieren und evaluieren einen einzelnen Punkt in einem Mesh. | glEvalPoint1-Funktion (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- glEvalPoint1-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870004"
---
# <a name="glevalpoint1-function"></a><span data-ttu-id="7ae7e-105">glEvalPoint1-Funktion</span><span class="sxs-lookup"><span data-stu-id="7ae7e-105">glEvalPoint1 function</span></span>

<span data-ttu-id="7ae7e-106">Die [**glEvalPoint1**](glevalpoint.md) -Funktion und die **glEvalPoint2** -Funktion generieren und evaluieren einen einzelnen Punkt in einem Mesh.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae7e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ae7e-107">Syntax</span></span>


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a><span data-ttu-id="7ae7e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ae7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae7e-109">*i*</span><span class="sxs-lookup"><span data-stu-id="7ae7e-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="7ae7e-110">Der ganzzahlige Wert für die Raster Domänen Variable *i*.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-110">The integer value for grid domain variable *i*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae7e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ae7e-111">Return value</span></span>

<span data-ttu-id="7ae7e-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae7e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ae7e-113">Remarks</span></span>

<span data-ttu-id="7ae7e-114">Die Funktionen [**glmapgrid**](glmapgrid-functions.md) und [**glevalmesh**](glevalmesh-functions.md) werden zusammen verwendet, um eine Reihe von Zuordnungs Domänen Werten, die gleichmäßig verteilt sind, effizient zu generieren und auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-114">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="7ae7e-115">Mithilfe von **glevalpoint** können Sie einen einzelnen Raster Punkt im gleichen Raster Bereich auswerten, der von **glevalmesh** durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-115">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="7ae7e-116">Das Aufrufen von [**glEvalPoint1**](glevalpoint.md) entspricht dem Aufrufen von.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-116">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="7ae7e-117">**glEvalCoord1** (*i* *) u*  + 1);</span><span class="sxs-lookup"><span data-stu-id="7ae7e-117">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="7ae7e-118">where</span><span class="sxs-lookup"><span data-stu-id="7ae7e-118">where</span></span>

<span data-ttu-id="7ae7e-119">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="7ae7e-119">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="7ae7e-120">und *n*, *u* 1 und *u* 2 sind die Argumente der neuesten **glMapGrid1** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-120">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="7ae7e-121">Eine absolute numerische Anforderung besteht darin, dass bei *i*  =  *n* der Wert, der von berechnet wird (*i* ?*u* + U1) ist genau *u* 2.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-121">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="7ae7e-122">Im zweidimensionalen Fall, **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="7ae7e-122">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="7ae7e-123">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="7ae7e-123">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="7ae7e-124">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="7ae7e-124">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="7ae7e-125">dabei *sind n*, *u* 1, *u* 2, *m*, *v* 1 und *v* 2 die Argumente der neuesten **glMapGrid2** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-125">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="7ae7e-126">Die **glEvalPoint2** -Funktion entspricht dem Aufrufen von.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-126">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="7ae7e-127">**glEvalCoord2** (*i* *) u*  +  1, *j* ?*v*  +  *v* 1);</span><span class="sxs-lookup"><span data-stu-id="7ae7e-127">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="7ae7e-128">Die einzigen absoluten numerischen Anforderungen sind, dass bei *i* = *n* der Wert, der von berechnet wird (*i* ?*u*  +  1) ist genau U2, und wenn *j*  =  *m* ist, dann wird der von (j?) berechnete Wert (*j* ?*v*  +  *v* 1) ist genau *v* 2.</span><span class="sxs-lookup"><span data-stu-id="7ae7e-128">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="7ae7e-129">Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glEvalPoint1**](glevalpoint.md) und **glEvalPoint2** ab:</span><span class="sxs-lookup"><span data-stu-id="7ae7e-129">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="7ae7e-130">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="7ae7e-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="7ae7e-131">**glget** mit Argument GL \_ map2 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="7ae7e-131">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="7ae7e-132">**glget** mit Argument GL \_ zuordnung1 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="7ae7e-132">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="7ae7e-133">**glget** mit Argument GL \_ map2 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="7ae7e-133">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae7e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ae7e-134">Requirements</span></span>



| <span data-ttu-id="7ae7e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ae7e-135">Requirement</span></span> | <span data-ttu-id="7ae7e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="7ae7e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae7e-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ae7e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7ae7e-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ae7e-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7ae7e-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ae7e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7ae7e-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ae7e-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ae7e-141">Header</span><span class="sxs-lookup"><span data-stu-id="7ae7e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ae7e-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ae7e-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7ae7e-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7ae7e-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ae7e-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ae7e-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ae7e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7ae7e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ae7e-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ae7e-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae7e-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ae7e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae7e-148">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="7ae7e-148">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="7ae7e-149">**glevalmesh**</span><span class="sxs-lookup"><span data-stu-id="7ae7e-149">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="7ae7e-150">**glget**</span><span class="sxs-lookup"><span data-stu-id="7ae7e-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7ae7e-151">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="7ae7e-151">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="7ae7e-152">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="7ae7e-152">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="7ae7e-153">**glmapgrid**</span><span class="sxs-lookup"><span data-stu-id="7ae7e-153">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





