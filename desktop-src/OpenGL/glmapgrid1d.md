---
title: glMapGrid1d-Funktion (GL. h)
description: Definiert ein eindimensionales Mesh. | glMapGrid1d-Funktion (GL. h)
ms.assetid: a0bc822e-dd98-4586-a322-2779e11f38ca
keywords:
- glMapGrid1d-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b1900f5597e8c516100504ca7288137ed99ded
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869712"
---
# <a name="glmapgrid1d-function"></a><span data-ttu-id="f33d7-105">glMapGrid1d-Funktion</span><span class="sxs-lookup"><span data-stu-id="f33d7-105">glMapGrid1d function</span></span>

<span data-ttu-id="f33d7-106">Definiert ein eindimensionales Mesh.</span><span class="sxs-lookup"><span data-stu-id="f33d7-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f33d7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f33d7-107">Syntax</span></span>


```C++
void WINAPI glMapGrid1d(
   GLint    un,
   GLdouble u1,
   GLdouble u2
);
```



## <a name="parameters"></a><span data-ttu-id="f33d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f33d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f33d7-109">*un*</span><span class="sxs-lookup"><span data-stu-id="f33d7-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="f33d7-110">Die Anzahl der Partitionen im Raster Bereichs Intervall \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="f33d7-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="f33d7-111">Dieser Wert muss positiv sein.</span><span class="sxs-lookup"><span data-stu-id="f33d7-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="f33d7-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="f33d7-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="f33d7-113">Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert i = 0 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f33d7-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="f33d7-114">*hinweg*</span><span class="sxs-lookup"><span data-stu-id="f33d7-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="f33d7-115">Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert i = UN verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f33d7-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f33d7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f33d7-116">Return value</span></span>

<span data-ttu-id="f33d7-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f33d7-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f33d7-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f33d7-118">Error codes</span></span>

<span data-ttu-id="f33d7-119">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f33d7-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f33d7-120">Name</span><span class="sxs-lookup"><span data-stu-id="f33d7-120">Name</span></span>                                                                                                  | <span data-ttu-id="f33d7-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f33d7-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f33d7-122"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="f33d7-122"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="f33d7-123">Entweder ' *UN* ' oder ' *VN* ' war nicht positiv.</span><span class="sxs-lookup"><span data-stu-id="f33d7-123">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="f33d7-124"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f33d7-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f33d7-125">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f33d7-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f33d7-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f33d7-126">Remarks</span></span>

<span data-ttu-id="f33d7-127">Verwenden Sie die Funktionen " **glmapgrid** " und " [glevalmesh](glevalmesh-functions.md) ", um eine Reihe von gleichmäßig getrennten Zuordnungs Domänen Werten effizient zu generieren und auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="f33d7-127">Use the **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions togetherto efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="f33d7-128">Die glevalmesh-Funktion durchläuft die ganzzahlige Domäne eines ein-oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungs Zuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f33d7-128">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="f33d7-129">Die **glMapGrid1** -Funktion und die [**glMapGrid2**](glmapgrid2d.md) -Funktion geben die linearen Raster Zuordnungen zwischen den ganzzahligen Raster Koordinaten i (bzw. i und j) und den Kartenkoordinaten für die Gleit Komma Auswertung von u (oder v) an.</span><span class="sxs-lookup"><span data-stu-id="f33d7-129">The **glMapGrid1** and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="f33d7-130">Ausführliche Informationen zur Auswertung von und v-Koordinaten finden Sie unter [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="f33d7-130">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="f33d7-131">Die **glMapGrid1** *-* Funktion gibt eine einzelne lineare Zuordnung so an, dass die ganzzahlige Raster Koordinate 0 genau zu U1 zugeordnet ist, und die ganzzahlige Raster Koordinate werden genau auf *U2*</span><span class="sxs-lookup"><span data-stu-id="f33d7-131">The **glMapGrid1** function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="f33d7-132">Alle anderen ganzzahligen Raster Koordinaten, die *mir* zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="f33d7-132">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="f33d7-133">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="f33d7-133">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="f33d7-134">Die [**glMapGrid2**](glmapgrid2d.md) -Funktion gibt zwei lineare Zuordnungen an.</span><span class="sxs-lookup"><span data-stu-id="f33d7-134">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="f33d7-135">Eine ordnet eine ganzzahlige Raster Koordinate *i = 0* genau auf *U1* an, und die ganzzahlige Raster Koordinate *i =* ist genau auf *U2*.</span><span class="sxs-lookup"><span data-stu-id="f33d7-135">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="f33d7-136">Der andere ordnet die ganzzahlige Raster Koordinate *j = 0* exakt auf *v1* und die ganzzahlige Raster Koordinate *j = VN* exakt auf *v2* zu.</span><span class="sxs-lookup"><span data-stu-id="f33d7-136">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="f33d7-137">Andere ganzzahlige Raster Koordinaten i und j werden zugeordnet, damit</span><span class="sxs-lookup"><span data-stu-id="f33d7-137">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="f33d7-138">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="f33d7-138">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="f33d7-139">*v = j (V2 V1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="f33d7-139">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="f33d7-140">Die von **glmapgrid** angegebenen Zuordnungen werden von [glevalmesh](glevalmesh-functions.md) und [**glevalpoint**](glevalpoint.md)identisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="f33d7-140">The mappings specified by **glMapGrid** are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="f33d7-141">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glmapgrid** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="f33d7-141">The following functions retrieve information related to **glMapGrid**:</span></span>

<dl>

<span data-ttu-id="f33d7-142">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="f33d7-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="f33d7-143">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="f33d7-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="f33d7-144">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="f33d7-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="f33d7-145">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="f33d7-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="f33d7-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f33d7-146">Requirements</span></span>



| <span data-ttu-id="f33d7-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f33d7-147">Requirement</span></span> | <span data-ttu-id="f33d7-148">Wert</span><span class="sxs-lookup"><span data-stu-id="f33d7-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f33d7-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f33d7-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f33d7-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f33d7-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f33d7-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f33d7-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f33d7-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f33d7-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f33d7-153">Header</span><span class="sxs-lookup"><span data-stu-id="f33d7-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f33d7-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f33d7-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f33d7-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f33d7-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="f33d7-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f33d7-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f33d7-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f33d7-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f33d7-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f33d7-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f33d7-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f33d7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33d7-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f33d7-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f33d7-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f33d7-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f33d7-162">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="f33d7-162">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f33d7-163">glevalmesh</span><span class="sxs-lookup"><span data-stu-id="f33d7-163">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="f33d7-164">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="f33d7-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="f33d7-165">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="f33d7-165">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="f33d7-166">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="f33d7-166">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





