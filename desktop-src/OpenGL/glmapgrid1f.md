---
title: glMapGrid1f-Funktion (GL. h)
description: Definiert ein eindimensionales Mesh. | glMapGrid1f-Funktion (GL. h)
ms.assetid: 242c0197-2fa6-4356-b536-627660ebd3a7
keywords:
- glMapGrid1f-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75479e8e25098fbfc5b906ba1785913cba9f2e30
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106364314"
---
# <a name="glmapgrid1f-function"></a><span data-ttu-id="f1c2d-105">glMapGrid1f-Funktion</span><span class="sxs-lookup"><span data-stu-id="f1c2d-105">glMapGrid1f function</span></span>

<span data-ttu-id="f1c2d-106">Definiert ein eindimensionales Mesh.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c2d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1c2d-107">Syntax</span></span>


```C++
void WINAPI glMapGrid1f(
   GLint   un,
   GLfloat u1,
   GLfloat u2
);
```



## <a name="parameters"></a><span data-ttu-id="f1c2d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1c2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1c2d-109">*un*</span><span class="sxs-lookup"><span data-stu-id="f1c2d-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="f1c2d-110">Die Anzahl der Partitionen im Raster Bereichs Intervall \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="f1c2d-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="f1c2d-111">Dieser Wert muss positiv sein.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="f1c2d-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="f1c2d-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="f1c2d-113">Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert i = 0 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="f1c2d-114">*hinweg*</span><span class="sxs-lookup"><span data-stu-id="f1c2d-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="f1c2d-115">Ein Wert, der als Zuordnung für den ganzzahligen Raster Domänen Wert i = UN verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1c2d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1c2d-116">Return value</span></span>

<span data-ttu-id="f1c2d-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f1c2d-118">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f1c2d-118">Error codes</span></span>

<span data-ttu-id="f1c2d-119">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f1c2d-120">Name</span><span class="sxs-lookup"><span data-stu-id="f1c2d-120">Name</span></span>                                                                                                  | <span data-ttu-id="f1c2d-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f1c2d-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1c2d-122"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c2d-122"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="f1c2d-123">Entweder ' *UN* ' oder ' *VN* ' war nicht positiv.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-123">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="f1c2d-124"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c2d-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f1c2d-125">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f1c2d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1c2d-126">Remarks</span></span>

<span data-ttu-id="f1c2d-127">Die Funktionen **glmapgrid** und [glevalmesh](glevalmesh-functions.md) werden zusammen verwendet, um eine Reihe von Zuordnungs Domänen Werten, die gleichmäßig verteilt sind, effizient zu generieren und auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-127">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="f1c2d-128">Die glevalmesh-Funktion durchläuft die ganzzahlige Domäne eines ein-oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungs Zuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-128">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="f1c2d-129">Die [**glMapGrid1**](glmapgrid1d.md) -Funktion und die [**glMapGrid2**](glmapgrid2d.md) -Funktion geben die linearen Raster Zuordnungen zwischen den ganzzahligen Raster Koordinaten i (bzw. i und j) und den Kartenkoordinaten für die Gleit Komma Auswertung von u (oder v) an.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-129">The [**glMapGrid1**](glmapgrid1d.md) and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="f1c2d-130">Ausführliche Informationen zur Auswertung von und v-Koordinaten finden Sie unter [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c2d-130">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="f1c2d-131">Die [**glMapGrid1**](glmapgrid1d.md) *-* Funktion gibt eine einzelne lineare Zuordnung so an, dass die ganzzahlige Raster Koordinate 0 genau zu U1 zugeordnet ist, und die ganzzahlige Raster Koordinate werden genau auf *U2*</span><span class="sxs-lookup"><span data-stu-id="f1c2d-131">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="f1c2d-132">Alle anderen ganzzahligen Raster Koordinaten, die *mir* zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="f1c2d-132">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="f1c2d-133">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="f1c2d-133">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="f1c2d-134">Die [**glMapGrid2**](glmapgrid2d.md) -Funktion gibt zwei lineare Zuordnungen an.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-134">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="f1c2d-135">Eine ordnet eine ganzzahlige Raster Koordinate *i = 0* genau auf *U1* an, und die ganzzahlige Raster Koordinate *i =* ist genau auf *U2*.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-135">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="f1c2d-136">Der andere ordnet die ganzzahlige Raster Koordinate *j = 0* exakt auf *v1* und die ganzzahlige Raster Koordinate *j = VN* exakt auf *v2* zu.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-136">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="f1c2d-137">Andere ganzzahlige Raster Koordinaten i und j werden zugeordnet, damit</span><span class="sxs-lookup"><span data-stu-id="f1c2d-137">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="f1c2d-138">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="f1c2d-138">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="f1c2d-139">*v = j (V2 V1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="f1c2d-139">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="f1c2d-140">Die von [**glmapgrid**](glmapgrid1d.md) angegebenen Zuordnungen werden von [glevalmesh](glevalmesh-functions.md) und [**glevalpoint**](glevalpoint.md)identisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1c2d-140">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="f1c2d-141">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit [**glmapgrid**](glmapgrid1d.md)abgerufen:</span><span class="sxs-lookup"><span data-stu-id="f1c2d-141">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="f1c2d-142">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="f1c2d-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="f1c2d-143">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="f1c2d-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="f1c2d-144">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="f1c2d-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="f1c2d-145">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="f1c2d-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="f1c2d-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1c2d-146">Requirements</span></span>



| <span data-ttu-id="f1c2d-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1c2d-147">Requirement</span></span> | <span data-ttu-id="f1c2d-148">Wert</span><span class="sxs-lookup"><span data-stu-id="f1c2d-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c2d-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1c2d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f1c2d-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1c2d-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f1c2d-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1c2d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f1c2d-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1c2d-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f1c2d-153">Header</span><span class="sxs-lookup"><span data-stu-id="f1c2d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1c2d-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1c2d-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f1c2d-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f1c2d-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1c2d-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1c2d-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f1c2d-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f1c2d-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1c2d-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1c2d-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1c2d-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1c2d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c2d-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f1c2d-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f1c2d-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f1c2d-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f1c2d-162">**glevalcoord**</span><span class="sxs-lookup"><span data-stu-id="f1c2d-162">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f1c2d-163">glevalmesh</span><span class="sxs-lookup"><span data-stu-id="f1c2d-163">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="f1c2d-164">**glevalpoint**</span><span class="sxs-lookup"><span data-stu-id="f1c2d-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="f1c2d-165">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="f1c2d-165">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="f1c2d-166">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="f1c2d-166">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





