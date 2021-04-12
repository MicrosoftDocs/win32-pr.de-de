---
title: glEvalMesh1-Funktion (GL. h)
description: Berechnet ein eindimensionales Raster von Punkten oder Zeilen.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- glEvalMesh1-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518095"
---
# <a name="glevalmesh1-function"></a><span data-ttu-id="d183f-104">glEvalMesh1-Funktion</span><span class="sxs-lookup"><span data-stu-id="d183f-104">glEvalMesh1 function</span></span>

<span data-ttu-id="d183f-105">Berechnet ein eindimensionales Raster von Punkten oder Zeilen.</span><span class="sxs-lookup"><span data-stu-id="d183f-105">Computes a one-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="d183f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d183f-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a><span data-ttu-id="d183f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d183f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d183f-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="d183f-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="d183f-109">Ein-Wert, der angibt, ob ein eindimensionales Mesh von Punkten oder Linien berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d183f-109">A value that specifies whether to compute a one-dimensional mesh of points or lines.</span></span> <span data-ttu-id="d183f-110">Die folgenden symbolischen Konstanten werden akzeptiert: GL \_ Point und GL \_ Line.</span><span class="sxs-lookup"><span data-stu-id="d183f-110">The following symbolic constants are accepted: GL\_POINT and GL\_LINE.</span></span>

</dd> <dt>

<span data-ttu-id="d183f-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="d183f-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="d183f-112">Der erste ganzzahlige Wert für die Raster Domänen Variable i.</span><span class="sxs-lookup"><span data-stu-id="d183f-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="d183f-113">*I2*</span><span class="sxs-lookup"><span data-stu-id="d183f-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="d183f-114">Der letzte ganzzahlige Wert für die Raster Domänen Variable i.</span><span class="sxs-lookup"><span data-stu-id="d183f-114">The last integer value for grid domain variable i.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d183f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d183f-115">Return value</span></span>

<span data-ttu-id="d183f-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d183f-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d183f-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d183f-117">Error codes</span></span>

<span data-ttu-id="d183f-118">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d183f-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d183f-119">Name</span><span class="sxs-lookup"><span data-stu-id="d183f-119">Name</span></span>                                                                                                  | <span data-ttu-id="d183f-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d183f-120">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d183f-121"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d183f-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d183f-122">Gibt an, dass der *Modus* kein akzeptierter Wert ist.</span><span class="sxs-lookup"><span data-stu-id="d183f-122">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="d183f-123"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="d183f-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d183f-124">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d183f-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="d183f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d183f-125">Remarks</span></span>

<span data-ttu-id="d183f-126">Verwenden Sie " [**glmapgrid**](glmapgrid-functions.md) " und " [**glevalmesh**](glevalmesh-functions.md) ", um eine Reihe von gleichmäßig getrennten Zuordnungs Domänen Werten effizient zu generieren und auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="d183f-126">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) together to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="d183f-127">Die **glevalmesh** -Funktion durchläuft die ganzzahlige Domäne eines ein-oder zweidimensionalen Rasters, dessen Bereich die Domäne der Auswertungs Zuordnungen ist, die von [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d183f-127">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="d183f-128">Der Mode-Parameter bestimmt, ob die resultierenden Scheitel Punkte als Punkte, Linien oder gefüllte Polygone miteinander verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="d183f-128">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="d183f-129">Im eindimensionalen Fall **glEvalMesh1** wird das Mesh generiert, als ob das folgende Code Fragment ausgeführt würde:</span><span class="sxs-lookup"><span data-stu-id="d183f-129">In the one-dimensional case, **glEvalMesh1**, the mesh is generated as if the following code fragment were executed:</span></span>

<span data-ttu-id="d183f-130">[**glBegin**](glbegin.md)(*Typ*);</span><span class="sxs-lookup"><span data-stu-id="d183f-130">[**glBegin**](glbegin.md)(*type*);</span></span>

<span data-ttu-id="d183f-131">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="d183f-131">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="d183f-132">{</span><span class="sxs-lookup"><span data-stu-id="d183f-132">{</span></span>

<span data-ttu-id="d183f-133">[**glEvalCoord1**](glevalcoord1d.md)(i? u + U1)</span><span class="sxs-lookup"><span data-stu-id="d183f-133">[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)</span></span>

<span data-ttu-id="d183f-134">}</span><span class="sxs-lookup"><span data-stu-id="d183f-134">}</span></span>

<span data-ttu-id="d183f-135">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="d183f-135">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="d183f-136">where</span><span class="sxs-lookup"><span data-stu-id="d183f-136">where</span></span>

<span data-ttu-id="d183f-137">? u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="d183f-137">?u = (u2 u1) / n</span></span>

<span data-ttu-id="d183f-138">und n, U1 und U2 sind die Argumente der neuesten [**glMapGrid1**](glmapgrid1d.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d183f-138">and n, u1, and u2 are the arguments to the most recent [**glMapGrid1**](glmapgrid1d.md) function.</span></span> <span data-ttu-id="d183f-139">Der *Typparameter* ist GL- \_ Punkte, wenn der Modus "GL Point" ist \_ , oder GL \_ Lines, wenn der Modus "GL \_ Line" ist</span><span class="sxs-lookup"><span data-stu-id="d183f-139">The *type* parameter is GL\_POINTS if mode is GL\_POINT, or GL\_LINES if mode is GL\_LINE.</span></span> <span data-ttu-id="d183f-140">Eine absolute numerische Anforderung besteht darin, dass der Wert, der von "i", "i" und "U1" berechnet wird, genau U2 ist.</span><span class="sxs-lookup"><span data-stu-id="d183f-140">The one absolute numeric requirement is that if i = n, then the value computed from i?u + u1 is exactly u2.</span></span>

## <a name="requirements"></a><span data-ttu-id="d183f-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d183f-141">Requirements</span></span>



| <span data-ttu-id="d183f-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d183f-142">Requirement</span></span> | <span data-ttu-id="d183f-143">Wert</span><span class="sxs-lookup"><span data-stu-id="d183f-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d183f-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d183f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d183f-145">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d183f-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d183f-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d183f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d183f-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d183f-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d183f-148">Header</span><span class="sxs-lookup"><span data-stu-id="d183f-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="d183f-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d183f-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d183f-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d183f-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="d183f-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d183f-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d183f-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d183f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d183f-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d183f-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d183f-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d183f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d183f-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d183f-155">**glBegin**</span></span>](glbegin.md)
</dt> </dl>

 

 





