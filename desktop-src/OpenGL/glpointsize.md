---
title: glPointSize-Funktion (GL. h)
description: Die Funktion "glPointSize" gibt den Durchmesser der rasterisierten Punkte an.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- glPointSize-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339987"
---
# <a name="glpointsize-function"></a><span data-ttu-id="e54ef-104">glPointSize-Funktion</span><span class="sxs-lookup"><span data-stu-id="e54ef-104">glPointSize function</span></span>

<span data-ttu-id="e54ef-105">Die Funktion " **glPointSize** " gibt den Durchmesser der rasterisierten Punkte an.</span><span class="sxs-lookup"><span data-stu-id="e54ef-105">The **glPointSize** function specifies the diameter of rasterized points.</span></span>

## <a name="syntax"></a><span data-ttu-id="e54ef-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e54ef-106">Syntax</span></span>


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a><span data-ttu-id="e54ef-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e54ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e54ef-108">*size*</span><span class="sxs-lookup"><span data-stu-id="e54ef-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="e54ef-109">Der Durchmesser der rasterisierten Punkte.</span><span class="sxs-lookup"><span data-stu-id="e54ef-109">The diameter of rasterized points.</span></span> <span data-ttu-id="e54ef-110">Der Standardwert ist 1.0.</span><span class="sxs-lookup"><span data-stu-id="e54ef-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e54ef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e54ef-111">Return value</span></span>

<span data-ttu-id="e54ef-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e54ef-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e54ef-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e54ef-113">Error codes</span></span>

<span data-ttu-id="e54ef-114">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e54ef-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e54ef-115">Name</span><span class="sxs-lookup"><span data-stu-id="e54ef-115">Name</span></span>                                                                                                  | <span data-ttu-id="e54ef-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e54ef-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e54ef-117"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="e54ef-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="e54ef-118">die *Größe* war kleiner als oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e54ef-118">*size* was less than or equal to zero.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="e54ef-119"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="e54ef-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e54ef-120">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e54ef-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e54ef-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e54ef-121">Remarks</span></span>

<span data-ttu-id="e54ef-122">Die Funktion " **glPointSize** " gibt den rasterisierten Durchmesser von Aliasing-und Antialiasing-Punkten an.</span><span class="sxs-lookup"><span data-stu-id="e54ef-122">The **glPointSize** function specifies the rasterized diameter of both aliased and antialiased points.</span></span> <span data-ttu-id="e54ef-123">Die Verwendung einer anderen Punktgröße als 1,0 hat unterschiedliche Auswirkungen, abhängig davon, ob das Punkt-Antialiasing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e54ef-123">Using a point size other than 1.0 has different effects, depending on whether point antialiasing is enabled.</span></span> <span data-ttu-id="e54ef-124">Das Antialiasing von Punkten wird durch Aufrufen von [**glEnable und glEnable**](glenable.md) mit dem Argument GL  \_ Point Smooth gesteuert \_ .</span><span class="sxs-lookup"><span data-stu-id="e54ef-124">Point antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_POINT\_SMOOTH.</span></span>

<span data-ttu-id="e54ef-125">Wenn das Punkt-Antialiasing deaktiviert ist, wird die tatsächliche Größe festgelegt, indem die angegebene Größe auf die nächste ganze Zahl gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="e54ef-125">If point antialiasing is disabled, the actual size is determined by rounding the supplied size to the nearest integer.</span></span> <span data-ttu-id="e54ef-126">(Wenn die Rundung den Wert 0 (null) ergibt, ist Sie so, als ob die Punktgröße 1 ist.) Wenn die gerundete Größe ungerade ist, wird der Mittelpunkt (*x*,*y*) des Pixel Fragments, das den Punkt darstellt, als</span><span class="sxs-lookup"><span data-stu-id="e54ef-126">(If the rounding results in the value 0, it is as if the point size were 1.) If the rounded size is odd, then the center point (*x*,*y*) of the pixel fragment that represents the point is computed as</span></span>

<span data-ttu-id="e54ef-127">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="e54ef-127">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="e54ef-128">wobei *w* -Index Fenster Fenster Koordinaten angeben.</span><span class="sxs-lookup"><span data-stu-id="e54ef-128">where *w* subscripts indicate window coordinates.</span></span> <span data-ttu-id="e54ef-129">Alle Pixel, die innerhalb des quadratischen Rasters der gerundeten Größe liegen, die auf (*x*,*y*) zentriert ist, bilden das Fragment.</span><span class="sxs-lookup"><span data-stu-id="e54ef-129">All pixels that lie within the square grid of the rounded size centered at (*x*,*y*) make up the fragment.</span></span> <span data-ttu-id="e54ef-130">Wenn die Größe gerade ist, ist der Mittelpunkt</span><span class="sxs-lookup"><span data-stu-id="e54ef-130">If the size is even, the center point is</span></span>

<span data-ttu-id="e54ef-131">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="e54ef-131">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="e54ef-132">und die Kreis zentrierte Fragmente sind die halbzahligen Fenster Koordinaten innerhalb des Quadrats der gerundeten Größe, die auf (*x*,*y*) zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="e54ef-132">and the rasterized fragment's centers are the half-integer window coordinates within the square of the rounded size centered at (*x*,*y*).</span></span> <span data-ttu-id="e54ef-133">Allen Pixel Fragmenten, die bei der rasterisierung eines nicht-Antialiasing-Punkts erstellt werden, werden dieselben zugeordneten Daten zugewiesen. die des Scheitel Punkts, der dem Punkt entspricht.</span><span class="sxs-lookup"><span data-stu-id="e54ef-133">All pixel fragments produced in rasterizing a nonantialiased point are assigned the same associated data; that of the vertex corresponding to the point.</span></span>

<span data-ttu-id="e54ef-134">Wenn Antialiasing aktiviert ist, erzeugt die Punkt-rasterisierung ein Fragment für jedes Pixel Quadrat, das den Bereich überschneidet, der sich innerhalb des Kreises befindet und einen Durchmesser gleich der aktuellen Punktgröße aufweist und sich an den Punkten (*x*<sub>w</sub> ,*y*<sub>w</sub> ) befindet.</span><span class="sxs-lookup"><span data-stu-id="e54ef-134">If antialiasing is enabled, then point rasterization produces a fragment for each pixel square that intersects the region lying within the circle having diameter equal to the current point size and centered at the points (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span></span> <span data-ttu-id="e54ef-135">Der Abdeckungs Wert für jedes Fragment ist der Fenster Koordinaten Bereich der Schnittmenge des kreisförmigen Bereichs mit dem entsprechenden Pixel Quadrat.</span><span class="sxs-lookup"><span data-stu-id="e54ef-135">The coverage value for each fragment is the window coordinate area of the intersection of the circular region with the corresponding pixel square.</span></span> <span data-ttu-id="e54ef-136">Dieser Wert wird gespeichert und im abschließenden rasterisierungsschritt verwendet.</span><span class="sxs-lookup"><span data-stu-id="e54ef-136">This value is saved and used in the final rasterization step.</span></span> <span data-ttu-id="e54ef-137">Die den einzelnen Fragmenten zugeordneten Daten sind die Daten, die dem zu ragenden Punkt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e54ef-137">The data associated with each fragment is the data associated with the point being rasterized.</span></span>

<span data-ttu-id="e54ef-138">Nicht alle Größen werden unterstützt, wenn das Punkt-Antialiasing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e54ef-138">Not all sizes are supported when point antialiasing is enabled.</span></span> <span data-ttu-id="e54ef-139">Wenn eine nicht unterstützte Größe angefordert wird, wird die nächstgelegene unterstützte Größe verwendet.</span><span class="sxs-lookup"><span data-stu-id="e54ef-139">If an unsupported size is requested, the nearest supported size is used.</span></span> <span data-ttu-id="e54ef-140">Es wird garantiert, dass nur die Größe 1,0 unterstützt wird. andere sind von der Implementierung abhängig.</span><span class="sxs-lookup"><span data-stu-id="e54ef-140">Only size 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="e54ef-141">Der Bereich der unterstützten Größen und der Größenunterschied zwischen unterstützten Größen innerhalb des Bereichs kann durch Aufrufen von [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit den Argumenten GL \_ \_ -Punktgröße \_ und- \_ Granularität der GL- \_ Punktgröße \_ abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="e54ef-141">The range of supported sizes and the size difference between supported sizes within the range can be queried by calling [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with arguments GL\_POINT\_SIZE\_RANGE and GL\_POINT\_SIZE\_GRANULARITY.</span></span>

<span data-ttu-id="e54ef-142">Die durch **glPointSize** angegebene Punktgröße wird immer zurückgegeben, wenn die GL- \_ Punkt \_ Größe abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="e54ef-142">The point size specified by **glPointSize** is always returned when GL\_POINT\_SIZE is queried.</span></span> <span data-ttu-id="e54ef-143">Das Spannen und Runden von Aliasing-und Antialiasing-Punkten hat keine Auswirkung auf den angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e54ef-143">Clamping and rounding for aliased and antialiased points have no effect on the specified value.</span></span>

<span data-ttu-id="e54ef-144">Die Größe des nicht-Antialiasing-Werts kann an einen von der Implementierung abhängigen maximalen Wert gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="e54ef-144">Non-antialiased point size may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="e54ef-145">Obwohl dieser Höchstwert nicht abgefragt werden kann, darf er nicht kleiner sein als der Maximalwert für Antialiasing Punkte, gerundet auf den nächsten ganzzahligen Wert.</span><span class="sxs-lookup"><span data-stu-id="e54ef-145">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased points, rounded to the nearest integer value.</span></span>

<span data-ttu-id="e54ef-146">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glPointSize** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="e54ef-146">The following functions retrieve information related to **glPointSize**:</span></span>

<span data-ttu-id="e54ef-147">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument-GL- \_ Punkt \_ Größe</span><span class="sxs-lookup"><span data-stu-id="e54ef-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POINT\_SIZE</span></span>

<span data-ttu-id="e54ef-148">**glget** mit Argument-GL- \_ Punkt \_ Größen \_ Bereich</span><span class="sxs-lookup"><span data-stu-id="e54ef-148">**glGet** with argument GL\_POINT\_SIZE\_RANGE</span></span>

<span data-ttu-id="e54ef-149">**glget** mit der Granularität der GL- \_ Punktgröße des Arguments \_ \_</span><span class="sxs-lookup"><span data-stu-id="e54ef-149">**glGet** with argument GL\_POINT\_SIZE\_GRANULARITY</span></span>

<span data-ttu-id="e54ef-150">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Point \_ Smooth</span><span class="sxs-lookup"><span data-stu-id="e54ef-150">[**glIsEnabled**](glisenabled.md) with argument GL\_POINT\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="e54ef-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e54ef-151">Requirements</span></span>



| <span data-ttu-id="e54ef-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e54ef-152">Requirement</span></span> | <span data-ttu-id="e54ef-153">Wert</span><span class="sxs-lookup"><span data-stu-id="e54ef-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e54ef-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e54ef-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e54ef-155">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e54ef-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e54ef-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e54ef-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e54ef-157">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e54ef-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e54ef-158">Header</span><span class="sxs-lookup"><span data-stu-id="e54ef-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="e54ef-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e54ef-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e54ef-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e54ef-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="e54ef-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e54ef-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e54ef-162">DLL</span><span class="sxs-lookup"><span data-stu-id="e54ef-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e54ef-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e54ef-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e54ef-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e54ef-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54ef-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e54ef-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e54ef-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="e54ef-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="e54ef-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e54ef-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e54ef-168">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="e54ef-168">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





