---
title: glMapGrid2d-Funktion (GL. h)
description: Definiert ein eindimensionales Mesh. | glMapGrid2d-Funktion (GL. h)
ms.assetid: 5e5887d1-e137-434b-a1f3-b3f10d462823
keywords:
- glMapGrid2d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6992a904528cf961f27335e7241c50fbd14f058b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361787"
---
# <a name="glmapgrid2d-function"></a><span data-ttu-id="3a234-105">glMapGrid2d-Funktion</span><span class="sxs-lookup"><span data-stu-id="3a234-105">glMapGrid2d function</span></span>

<span data-ttu-id="3a234-106">Definiert ein eindimensionales Mesh.</span><span class="sxs-lookup"><span data-stu-id="3a234-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a234-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a234-107">Syntax</span></span>


```C++
void WINAPI glMapGrid2d(
   GLint    un,
   GLdouble u1,
   GLdouble u2,
   GLint    vn,
   GLdouble v1,
   GLdouble v2
);
```



## <a name="parameters"></a><span data-ttu-id="3a234-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a234-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a234-109">*un*</span><span class="sxs-lookup"><span data-stu-id="3a234-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="3a234-110">Die Anzahl der Partitionen im Raster Bereichs Intervall \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="3a234-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="3a234-111">Dieser Wert muss positiv sein.</span><span class="sxs-lookup"><span data-stu-id="3a234-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="3a234-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="3a234-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="3a234-113">Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert i = 0 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a234-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="3a234-114">*hinweg*</span><span class="sxs-lookup"><span data-stu-id="3a234-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="3a234-115">Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert i = UN verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a234-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> <dt>

<span data-ttu-id="3a234-116">*VN*</span><span class="sxs-lookup"><span data-stu-id="3a234-116">*vn*</span></span> 
</dt> <dd>

<span data-ttu-id="3a234-117">Die Anzahl der Partitionen im Raster Bereichs Intervall \[ v1 (v2) \] .</span><span class="sxs-lookup"><span data-stu-id="3a234-117">The number of partitions in the grid range interval \[v1, v2\].</span></span>

</dd> <dt>

<span data-ttu-id="3a234-118">*v1*</span><span class="sxs-lookup"><span data-stu-id="3a234-118">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="3a234-119">Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert j = 0 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a234-119">A value used as the mapping for integer grid domain value j = 0.</span></span>

</dd> <dt>

<span data-ttu-id="3a234-120">*v2*</span><span class="sxs-lookup"><span data-stu-id="3a234-120">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="3a234-121">Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert j = VN verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a234-121">A value used as the mapping for integer grid domain value j = vn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a234-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a234-122">Return value</span></span>

<span data-ttu-id="3a234-123">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3a234-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3a234-124">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3a234-124">Error codes</span></span>

<span data-ttu-id="3a234-125">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3a234-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3a234-126">Name</span><span class="sxs-lookup"><span data-stu-id="3a234-126">Name</span></span>                                                                                                  | <span data-ttu-id="3a234-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3a234-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3a234-128"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="3a234-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="3a234-129">Entweder ' *UN* ' oder ' *VN* ' war nicht positiv.</span><span class="sxs-lookup"><span data-stu-id="3a234-129">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="3a234-130"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="3a234-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3a234-131">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a234-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3a234-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a234-132">Remarks</span></span>

<span data-ttu-id="3a234-133">Die Funktionen **glmapgrid** und [glevalmesh](glevalmesh-functions.md) werden zusammen verwendet, um eine Reihe von Zuordnungs Domänen Werten, die gleichmäßig verteilt sind, effizient zu generieren und auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="3a234-133">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="3a234-134">Die glevalmesh-Funktion durchläuft die ganzzahlige Domäne eines ein-oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungs Zuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3a234-134">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="3a234-135">Die [**glMapGrid1**](glmapgrid1d.md) -Funktion und die **glMapGrid2** -Funktion geben die linearen Raster Zuordnungen zwischen den ganzzahligen Raster Koordinaten i (bzw. i und j) und den Kartenkoordinaten für die Gleit Komma Auswertung von u (oder v) an.</span><span class="sxs-lookup"><span data-stu-id="3a234-135">The [**glMapGrid1**](glmapgrid1d.md) and **glMapGrid2** functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="3a234-136">Ausführliche Informationen zur Auswertung von und v-Koordinaten finden Sie unter [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="3a234-136">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="3a234-137">Die [**glMapGrid1**](glmapgrid1d.md) *-* Funktion gibt eine einzelne lineare Zuordnung so an, dass die ganzzahlige Raster Koordinate 0 genau zu U1 zugeordnet ist, und die ganzzahlige Raster Koordinate werden genau auf *U2*</span><span class="sxs-lookup"><span data-stu-id="3a234-137">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="3a234-138">Alle anderen ganzzahligen Raster Koordinaten, die *mir* zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="3a234-138">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="3a234-139">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="3a234-139">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="3a234-140">Die **glMapGrid2** -Funktion gibt zwei lineare Zuordnungen an.</span><span class="sxs-lookup"><span data-stu-id="3a234-140">The **glMapGrid2** function specifies two such linear mappings.</span></span> <span data-ttu-id="3a234-141">Eine ordnet eine ganzzahlige Raster Koordinate *i = 0* genau auf *U1* an, und die ganzzahlige Raster Koordinate *i =* ist genau auf *U2*.</span><span class="sxs-lookup"><span data-stu-id="3a234-141">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="3a234-142">Der andere ordnet die ganzzahlige Raster Koordinate *j = 0* exakt auf *v1* und die ganzzahlige Raster Koordinate *j = VN* exakt auf *v2* zu.</span><span class="sxs-lookup"><span data-stu-id="3a234-142">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="3a234-143">Andere ganzzahlige Raster Koordinaten i und j werden zugeordnet, damit</span><span class="sxs-lookup"><span data-stu-id="3a234-143">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="3a234-144">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="3a234-144">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="3a234-145">*v = j (V2 V1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="3a234-145">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="3a234-146">Die von [**glmapgrid**](glmapgrid1d.md) angegebenen Zuordnungen werden von [glevalmesh](glevalmesh-functions.md) und [**glevalpoint**](glevalpoint.md)identisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a234-146">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="3a234-147">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit [**glmapgrid**](glmapgrid1d.md)abgerufen:</span><span class="sxs-lookup"><span data-stu-id="3a234-147">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="3a234-148">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="3a234-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="3a234-149">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="3a234-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="3a234-150">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="3a234-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="3a234-151">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="3a234-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="3a234-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a234-152">Requirements</span></span>



| <span data-ttu-id="3a234-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a234-153">Requirement</span></span> | <span data-ttu-id="3a234-154">Wert</span><span class="sxs-lookup"><span data-stu-id="3a234-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a234-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a234-155">Minimum supported client</span></span><br/> | <span data-ttu-id="3a234-156">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a234-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3a234-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a234-157">Minimum supported server</span></span><br/> | <span data-ttu-id="3a234-158">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a234-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3a234-159">Header</span><span class="sxs-lookup"><span data-stu-id="3a234-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a234-160"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a234-160"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3a234-161">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a234-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a234-162"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a234-162"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3a234-163">DLL</span><span class="sxs-lookup"><span data-stu-id="3a234-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a234-164"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a234-164"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a234-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a234-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a234-166">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3a234-166">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3a234-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3a234-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3a234-168">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="3a234-168">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3a234-169">glevalmesh</span><span class="sxs-lookup"><span data-stu-id="3a234-169">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="3a234-170">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="3a234-170">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="3a234-171">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="3a234-171">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="3a234-172">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="3a234-172">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





