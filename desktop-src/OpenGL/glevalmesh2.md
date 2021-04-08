---
title: glEvalMesh2-Funktion (GL. h)
description: Berechnet ein zweidimensionales Raster von Punkten oder Linien.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- glEvalMesh2-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740672"
---
# <a name="glevalmesh2-function"></a><span data-ttu-id="cb126-104">glEvalMesh2-Funktion</span><span class="sxs-lookup"><span data-stu-id="cb126-104">glEvalMesh2 function</span></span>

<span data-ttu-id="cb126-105">Berechnet ein zweidimensionales Raster von Punkten oder Linien.</span><span class="sxs-lookup"><span data-stu-id="cb126-105">Computes a two-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb126-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb126-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a><span data-ttu-id="cb126-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb126-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb126-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="cb126-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="cb126-109">Ein-Wert, der angibt, ob ein zweidimensionales Gitter von Punkten, Linien oder Polygonen berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb126-109">A value that specifies whether to compute a two-dimensional mesh of points, lines, or polygons.</span></span> <span data-ttu-id="cb126-110">Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ Point, GL \_ Line und GL \_ Fill.</span><span class="sxs-lookup"><span data-stu-id="cb126-110">The following symbolic constants are accepted: GL\_POINT, GL\_LINE, and GL\_FILL.</span></span>

</dd> <dt>

<span data-ttu-id="cb126-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="cb126-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="cb126-112">Der erste ganzzahlige Wert für die Raster Domänen Variable i.</span><span class="sxs-lookup"><span data-stu-id="cb126-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="cb126-113">*I2*</span><span class="sxs-lookup"><span data-stu-id="cb126-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="cb126-114">Der letzte ganzzahlige Wert für die Raster Domänen Variable i.</span><span class="sxs-lookup"><span data-stu-id="cb126-114">The last integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="cb126-115">*j1*</span><span class="sxs-lookup"><span data-stu-id="cb126-115">*j1*</span></span> 
</dt> <dd>

<span data-ttu-id="cb126-116">Der erste ganzzahlige Wert für die Raster Domänen Variable j.</span><span class="sxs-lookup"><span data-stu-id="cb126-116">The first integer value for grid domain variable j.</span></span>

</dd> <dt>

<span data-ttu-id="cb126-117">*j2*</span><span class="sxs-lookup"><span data-stu-id="cb126-117">*j2*</span></span> 
</dt> <dd>

<span data-ttu-id="cb126-118">Der letzte ganzzahlige Wert für die Raster Domänen Variable j.</span><span class="sxs-lookup"><span data-stu-id="cb126-118">The last integer value for grid domain variable j.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb126-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb126-119">Return value</span></span>

<span data-ttu-id="cb126-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb126-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb126-121">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cb126-121">Error codes</span></span>

<span data-ttu-id="cb126-122">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cb126-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cb126-123">Name</span><span class="sxs-lookup"><span data-stu-id="cb126-123">Name</span></span>                                                                                                  | <span data-ttu-id="cb126-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb126-124">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb126-125"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cb126-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cb126-126">Gibt an, dass der *Modus* kein akzeptierter Wert ist.</span><span class="sxs-lookup"><span data-stu-id="cb126-126">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="cb126-127"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="cb126-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cb126-128">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cb126-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="cb126-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb126-129">Remarks</span></span>

<span data-ttu-id="cb126-130">Verwenden Sie " [**glmapgrid**](glmapgrid-functions.md) " und " [**glevalmesh**](glevalmesh-functions.md) " gemeinsam, um eine Reihe von gleichmäßig getrennten Zuordnungs Domänen Werten effizient zu generieren und auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="cb126-130">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="cb126-131">Die **glevalmesh** -Funktion durchläuft die ganzzahlige Domäne eines ein-oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungs Zuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cb126-131">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="cb126-132">Der Mode-Parameter bestimmt, ob die resultierenden Scheitel Punkte als Punkte, Linien oder gefüllte Polygone miteinander verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="cb126-132">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="cb126-133">Im zweidimensionalen Fall, **glEvalMesh2**, Let</span><span class="sxs-lookup"><span data-stu-id="cb126-133">In the two-dimensional case, **glEvalMesh2**, let</span></span>

<span data-ttu-id="cb126-134">?</span><span class="sxs-lookup"><span data-stu-id="cb126-134">?</span></span> <span data-ttu-id="cb126-135">u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="cb126-135">u = (u2 u1)/n</span></span>

<span data-ttu-id="cb126-136">?</span><span class="sxs-lookup"><span data-stu-id="cb126-136">?</span></span> <span data-ttu-id="cb126-137">v = (V2 V1)/m,</span><span class="sxs-lookup"><span data-stu-id="cb126-137">v = (v2 v1)/m,</span></span>

<span data-ttu-id="cb126-138">Dabei sind n, U1, U2, m, v1 und v2 die Argumente der neuesten [**glMapGrid2**](glmapgrid-functions.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="cb126-138">where n, u1, u2, m, v1, and v2 are the arguments to the most recent [**glMapGrid2**](glmapgrid-functions.md) function.</span></span> <span data-ttu-id="cb126-139">Wenn der *Modus* dann "GL \_ Fill" ist, entspricht **glEvalMesh2** dem folgenden:</span><span class="sxs-lookup"><span data-stu-id="cb126-139">Then, if *mode* is GL\_FILL, **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="cb126-140">for (j = J1; j < J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="cb126-140">for (j = j1; j < j2; j += 1)</span></span>

<span data-ttu-id="cb126-141">{</span><span class="sxs-lookup"><span data-stu-id="cb126-141">{</span></span>

<span data-ttu-id="cb126-142">[**glBegin**](glbegin.md)(GL \_ Quad \_ Strip);</span><span class="sxs-lookup"><span data-stu-id="cb126-142">[**glBegin**](glbegin.md)(GL\_QUAD\_STRIP);</span></span>

<span data-ttu-id="cb126-143">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="cb126-143">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="cb126-144">{</span><span class="sxs-lookup"><span data-stu-id="cb126-144">{</span></span>

<span data-ttu-id="cb126-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), j?</span><span class="sxs-lookup"><span data-stu-id="cb126-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ?</span></span> <span data-ttu-id="cb126-146">v + v1);</span><span class="sxs-lookup"><span data-stu-id="cb126-146">v + v1);</span></span>

<span data-ttu-id="cb126-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), (j + 1)?</span><span class="sxs-lookup"><span data-stu-id="cb126-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ?</span></span> <span data-ttu-id="cb126-148">v + v1);</span><span class="sxs-lookup"><span data-stu-id="cb126-148">v + v1);</span></span>

<span data-ttu-id="cb126-149">}</span><span class="sxs-lookup"><span data-stu-id="cb126-149">}</span></span>

<span data-ttu-id="cb126-150">[**glEnd**](glend.md)(); }</span><span class="sxs-lookup"><span data-stu-id="cb126-150">[**glEnd**](glend.md)( ); }</span></span>

<span data-ttu-id="cb126-151">Wenn der *Modus* "GL" ist \_ , entspricht ein **glEvalMesh2** -Rückruf dem folgenden:</span><span class="sxs-lookup"><span data-stu-id="cb126-151">If *mode* is GL\_LINE, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="cb126-152">for (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="cb126-152">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="cb126-153">{</span><span class="sxs-lookup"><span data-stu-id="cb126-153">{</span></span>

<span data-ttu-id="cb126-154">[**glBegin**](glbegin.md)(GL- \_ Zeilen \_ Streifen);</span><span class="sxs-lookup"><span data-stu-id="cb126-154">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="cb126-155">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="cb126-155">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="cb126-156">{</span><span class="sxs-lookup"><span data-stu-id="cb126-156">{</span></span>

<span data-ttu-id="cb126-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="cb126-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="cb126-158">}</span><span class="sxs-lookup"><span data-stu-id="cb126-158">}</span></span>

<span data-ttu-id="cb126-159">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="cb126-159">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="cb126-160">}</span><span class="sxs-lookup"><span data-stu-id="cb126-160">}</span></span>

<span data-ttu-id="cb126-161">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="cb126-161">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="cb126-162">{</span><span class="sxs-lookup"><span data-stu-id="cb126-162">{</span></span>

<span data-ttu-id="cb126-163">[**glBegin**](glbegin.md)(GL- \_ Zeilen \_ Streifen);</span><span class="sxs-lookup"><span data-stu-id="cb126-163">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="cb126-164">for (j = J1; j <= J1; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="cb126-164">for (j = j1; j <= j1; j += 1)</span></span>

<span data-ttu-id="cb126-165">{</span><span class="sxs-lookup"><span data-stu-id="cb126-165">{</span></span>

<span data-ttu-id="cb126-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="cb126-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="cb126-167">}</span><span class="sxs-lookup"><span data-stu-id="cb126-167">}</span></span>

<span data-ttu-id="cb126-168">glEnd ();</span><span class="sxs-lookup"><span data-stu-id="cb126-168">glEnd( );</span></span>

<span data-ttu-id="cb126-169">}</span><span class="sxs-lookup"><span data-stu-id="cb126-169">}</span></span>

<span data-ttu-id="cb126-170">Wenn der *Modus* "GL Point" lautet \_ , entspricht ein **glEvalMesh2** -Rückruf dem folgenden:</span><span class="sxs-lookup"><span data-stu-id="cb126-170">And finally, if *mode* is GL\_POINT, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="cb126-171">[**glBegin**](glbegin.md)(GL- \_ Punkte);</span><span class="sxs-lookup"><span data-stu-id="cb126-171">[**glBegin**](glbegin.md)(GL\_POINTS);</span></span>

<span data-ttu-id="cb126-172">for (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="cb126-172">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="cb126-173">{</span><span class="sxs-lookup"><span data-stu-id="cb126-173">{</span></span>

<span data-ttu-id="cb126-174">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="cb126-174">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="cb126-175">{</span><span class="sxs-lookup"><span data-stu-id="cb126-175">{</span></span>

<span data-ttu-id="cb126-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="cb126-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="cb126-177">}</span><span class="sxs-lookup"><span data-stu-id="cb126-177">}</span></span>

<span data-ttu-id="cb126-178">}</span><span class="sxs-lookup"><span data-stu-id="cb126-178">}</span></span>

<span data-ttu-id="cb126-179">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="cb126-179">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="cb126-180">In allen drei Fällen sind die einzigen absoluten numerischen Anforderungen, dass der Wert, der von i u + U1 ist genau U2, und wenn j = m ist, dann wird der von j berechnete Wert angezeigt. v + v1 ist genau v2.</span><span class="sxs-lookup"><span data-stu-id="cb126-180">In all three cases, the only absolute numeric requirements are that if i = n, then the value computed from i? u + u1 is exactly u2, and if j = m, then the value computed from j? v + v1 is exactly v2.</span></span> <span data-ttu-id="cb126-181">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glevalmesh** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="cb126-181">The following functions retrieve information relating to **glEvalMesh**:</span></span>

<span data-ttu-id="cb126-182">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="cb126-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="cb126-183">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Domäne</span><span class="sxs-lookup"><span data-stu-id="cb126-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="cb126-184">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ zuordnung1 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="cb126-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="cb126-185">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ map2 \_ Raster \_ Segmente</span><span class="sxs-lookup"><span data-stu-id="cb126-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="cb126-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb126-186">Requirements</span></span>



| <span data-ttu-id="cb126-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb126-187">Requirement</span></span> | <span data-ttu-id="cb126-188">Wert</span><span class="sxs-lookup"><span data-stu-id="cb126-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb126-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb126-189">Minimum supported client</span></span><br/> | <span data-ttu-id="cb126-190">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb126-190">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cb126-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb126-191">Minimum supported server</span></span><br/> | <span data-ttu-id="cb126-192">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb126-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb126-193">Header</span><span class="sxs-lookup"><span data-stu-id="cb126-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb126-194"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb126-194"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cb126-195">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cb126-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb126-196"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb126-196"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cb126-197">DLL</span><span class="sxs-lookup"><span data-stu-id="cb126-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb126-198"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb126-198"><dt>Opengl32.dll</dt></span></span> </dl> |



 

 





