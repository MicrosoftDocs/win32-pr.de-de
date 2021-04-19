---
title: glEvalPoint2-Funktion (GL. h)
description: Die glEvalPoint1-Funktion und die glEvalPoint2-Funktion generieren und evaluieren einen einzelnen Punkt in einem Mesh. | glEvalPoint2-Funktion (GL. h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- glEvalPoint2-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fafe728249f988462b0929873bbb195fed1e7c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355769"
---
# <a name="glevalpoint2-function"></a><span data-ttu-id="f2b90-105">glEvalPoint2-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2b90-105">glEvalPoint2 function</span></span>

<span data-ttu-id="f2b90-106">Die [**glEvalPoint1**](glevalpoint.md) -Funktion und die **glEvalPoint2** -Funktion generieren und evaluieren einen einzelnen Punkt in einem Mesh.</span><span class="sxs-lookup"><span data-stu-id="f2b90-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b90-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2b90-107">Syntax</span></span>


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a><span data-ttu-id="f2b90-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2b90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b90-109">*i*</span><span class="sxs-lookup"><span data-stu-id="f2b90-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="f2b90-110">Der ganzzahlige Wert für die Raster Domänen Variable *i*.</span><span class="sxs-lookup"><span data-stu-id="f2b90-110">The integer value for grid domain variable *i*.</span></span>

</dd> <dt>

<span data-ttu-id="f2b90-111">*IStGH*</span><span class="sxs-lookup"><span data-stu-id="f2b90-111">*j*</span></span> 
</dt> <dd>

<span data-ttu-id="f2b90-112">Der ganzzahlige Wert für die Raster Domänen Variable *j* .</span><span class="sxs-lookup"><span data-stu-id="f2b90-112">The integer value for grid domain variable *j* .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b90-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2b90-113">Return value</span></span>

<span data-ttu-id="f2b90-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f2b90-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2b90-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2b90-115">Remarks</span></span>

<span data-ttu-id="f2b90-116">Die Funktionen [**glmapgrid**](glmapgrid-functions.md) und [**glevalmesh**](glevalmesh-functions.md) werden zusammen verwendet, um eine Reihe von Zuordnungs Domänen Werten, die gleichmäßig verteilt sind, effizient zu generieren und auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="f2b90-116">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="f2b90-117">Mithilfe von **glevalpoint** können Sie einen einzelnen Raster Punkt im gleichen Raster Bereich auswerten, der von **glevalmesh** durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="f2b90-117">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="f2b90-118">Das Aufrufen von [**glEvalPoint1**](glevalpoint.md) entspricht dem Aufrufen von.</span><span class="sxs-lookup"><span data-stu-id="f2b90-118">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="f2b90-119">**glEvalCoord1** (*i* *) u*  + 1);</span><span class="sxs-lookup"><span data-stu-id="f2b90-119">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="f2b90-120">where</span><span class="sxs-lookup"><span data-stu-id="f2b90-120">where</span></span>

<span data-ttu-id="f2b90-121">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="f2b90-121">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="f2b90-122">und *n*, *u* 1 und *u* 2 sind die Argumente der neuesten **glMapGrid1** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f2b90-122">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="f2b90-123">Eine absolute numerische Anforderung besteht darin, dass bei *i*  =  *n* der Wert, der von berechnet wird (*i* ?*u* + U1) ist genau *u* 2.</span><span class="sxs-lookup"><span data-stu-id="f2b90-123">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="f2b90-124">Im zweidimensionalen Fall, **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="f2b90-124">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="f2b90-125">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="f2b90-125">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="f2b90-126">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="f2b90-126">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="f2b90-127">dabei *sind n*, *u* 1, *u* 2, *m*, *v* 1 und *v* 2 die Argumente der neuesten **glMapGrid2** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f2b90-127">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="f2b90-128">Die **glEvalPoint2** -Funktion entspricht dem Aufrufen von.</span><span class="sxs-lookup"><span data-stu-id="f2b90-128">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="f2b90-129">**glEvalCoord2** (*i* *) u*  +  1, *j* ?*v*  +  *v* 1);</span><span class="sxs-lookup"><span data-stu-id="f2b90-129">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="f2b90-130">Die einzigen absoluten numerischen Anforderungen sind, dass bei *i* = *n* der Wert, der von berechnet wird (*i* ?*u*  +  1) ist genau U2, und wenn *j*  =  *m* ist, dann wird der von (j?) berechnete Wert (*j* ?*v*  +  *v* 1) ist genau *v* 2.</span><span class="sxs-lookup"><span data-stu-id="f2b90-130">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="f2b90-131">Die folgenden Funktionen rufen Informationen im Zusammenhang mit [**glEvalPoint1**](glevalpoint.md) und **glEvalPoint2** ab:</span><span class="sxs-lookup"><span data-stu-id="f2b90-131">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="f2b90-132">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="f2b90-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="f2b90-133">**glget** mit Argument GL \_ map2 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="f2b90-133">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="f2b90-134">**glget** mit Argument GL \_ zuordnung1 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="f2b90-134">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="f2b90-135">**glget** mit Argument GL \_ map2 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="f2b90-135">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b90-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2b90-136">Requirements</span></span>



| <span data-ttu-id="f2b90-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2b90-137">Requirement</span></span> | <span data-ttu-id="f2b90-138">Wert</span><span class="sxs-lookup"><span data-stu-id="f2b90-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b90-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2b90-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b90-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2b90-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f2b90-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2b90-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b90-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2b90-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2b90-143">Header</span><span class="sxs-lookup"><span data-stu-id="f2b90-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2b90-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b90-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f2b90-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2b90-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2b90-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2b90-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2b90-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f2b90-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2b90-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2b90-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b90-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2b90-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b90-150">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="f2b90-150">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f2b90-151">**glevalmesh**</span><span class="sxs-lookup"><span data-stu-id="f2b90-151">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="f2b90-152">**glget**</span><span class="sxs-lookup"><span data-stu-id="f2b90-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f2b90-153">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="f2b90-153">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="f2b90-154">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="f2b90-154">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="f2b90-155">**glmapgrid**</span><span class="sxs-lookup"><span data-stu-id="f2b90-155">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





