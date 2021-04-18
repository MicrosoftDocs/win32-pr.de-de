---
title: glshademodel-Funktion (GL. h)
description: Die glshademodel-Funktion wählt Flat-oder Smooth-Schattierung aus.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- glshademodel-Funktion OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339958"
---
# <a name="glshademodel-function"></a><span data-ttu-id="f0981-104">glshademodel-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0981-104">glShadeModel function</span></span>

<span data-ttu-id="f0981-105">Die **glshademodel** -Funktion wählt Flat-oder Smooth-Schattierung aus.</span><span class="sxs-lookup"><span data-stu-id="f0981-105">The **glShadeModel** function selects flat or smooth shading.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0981-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0981-106">Syntax</span></span>


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="f0981-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0981-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0981-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="f0981-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="f0981-109">Ein symbolischer Wert, der eine Schattierungs Technik darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0981-109">A symbolic value representing a shading technique.</span></span> <span data-ttu-id="f0981-110">Akzeptierte Werte sind GL \_ Flat und GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="f0981-110">Accepted values are GL\_FLAT and GL\_SMOOTH.</span></span> <span data-ttu-id="f0981-111">Der Standardwert ist "GL \_ Smooth".</span><span class="sxs-lookup"><span data-stu-id="f0981-111">The default is GL\_SMOOTH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0981-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0981-112">Return value</span></span>

<span data-ttu-id="f0981-113">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f0981-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0981-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f0981-114">Error codes</span></span>

<span data-ttu-id="f0981-115">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f0981-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f0981-116">Name</span><span class="sxs-lookup"><span data-stu-id="f0981-116">Name</span></span>                                                                                                  | <span data-ttu-id="f0981-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f0981-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0981-118"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f0981-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f0981-119">der *Modus* war ein anderer Wert als GL \_ glat oder GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="f0981-119">*mode* was a value other than GL\_GLAT or GL\_SMOOTH.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="f0981-120"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f0981-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f0981-121">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f0981-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f0981-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0981-122">Remarks</span></span>

<span data-ttu-id="f0981-123">OpenGL-primitive können entweder flach oder Smooth Schattierung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f0981-123">OpenGL primitives can have either flat or smooth shading.</span></span> <span data-ttu-id="f0981-124">Die standardmäßige Schattierung bewirkt, dass die berechneten Farben der Scheitel Punkte interpoliert werden, wenn der primitive gerendert wird. in der Regel werden jedem resultierenden Pixel Fragment verschiedene Farben zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f0981-124">Smooth shading, the default, causes the computed colors of vertices to be interpolated as the primitive is rasterized, typically assigning different colors to each resulting pixel fragment.</span></span> <span data-ttu-id="f0981-125">Die flache Schattierung wählt die berechnete Farbe nur eines Scheitel Punkts aus und weist diese allen Pixel Fragmenten zu, die durch das rasterieren eines einzelnen primitiven generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f0981-125">Flat shading selects the computed color of just one vertex and assigns it to all the pixel fragments generated by rasterizing a single primitive.</span></span> <span data-ttu-id="f0981-126">In beiden Fällen ist die berechnete Farbe eines Scheitel Punkts das Ergebnis der Beleuchtung, wenn Beleuchtung aktiviert ist, oder es handelt sich um die aktuelle Farbe zum Zeitpunkt der Angabe des Scheitel Punkts, wenn die Beleuchtung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f0981-126">In either case, the computed color of a vertex is the result of lighting, if lighting is enabled, or it is the current color at the time the vertex was specified, if lighting is disabled.</span></span>

<span data-ttu-id="f0981-127">Flache und glatte Schattierung können nicht für Punkte unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="f0981-127">Flat and smooth shading are indistinguishable for points.</span></span> <span data-ttu-id="f0981-128">Beim zählen von Scheitel Punkten und primitiven von einem, beginnend bei der Ausgabe von [**glBegin**](glbegin.md) , erhält jedes flach schattierte *Liniensegment die* berechnete Farbe des Scheitel Punkts *i* + 1, dessen zweiter Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="f0981-128">Counting vertices and primitives from one, starting when [**glBegin**](glbegin.md) is issued, each flat-shaded line segment *i* is given the computed color of vertex *i* + 1, its second vertex.</span></span> <span data-ttu-id="f0981-129">Wenn Sie auf ähnliche Weise gezählt werden, erhält jedes flatschattierte Polygon die berechnete Farbe des Vertex, der in der folgenden Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="f0981-129">Counting similarly from one, each flat-shaded polygon is given the computed color of the vertex listed in the following table.</span></span> <span data-ttu-id="f0981-130">Dies ist der letzte Scheitelpunkt zum Angeben des Polygons in allen Fällen außer einzelnen Polygonen, wobei der erste Scheitelpunkt die flache schattierte Farbe angibt.</span><span class="sxs-lookup"><span data-stu-id="f0981-130">This is the last vertex to specify the polygon in all cases except single polygons, where the first vertex specifies the flat-shaded color.</span></span>



| <span data-ttu-id="f0981-131">Primitiver Typ von Polygon i</span><span class="sxs-lookup"><span data-stu-id="f0981-131">Primitive type of polygon i</span></span> | <span data-ttu-id="f0981-132">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="f0981-132">Vertex</span></span>   |
|-----------------------------|----------|
| <span data-ttu-id="f0981-133">Einzelnes Polygon (*I*= 1)</span><span class="sxs-lookup"><span data-stu-id="f0981-133">Single polygon (*I*=1)</span></span>      | <span data-ttu-id="f0981-134">1</span><span class="sxs-lookup"><span data-stu-id="f0981-134">1</span></span>        |
| <span data-ttu-id="f0981-135">Dreiecks Streifen</span><span class="sxs-lookup"><span data-stu-id="f0981-135">Triangle strip</span></span>              | <span data-ttu-id="f0981-136">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="f0981-136">*i* + 2</span></span>  |
| <span data-ttu-id="f0981-137">Dreiecks Lüfter</span><span class="sxs-lookup"><span data-stu-id="f0981-137">Triangle fan</span></span>                | <span data-ttu-id="f0981-138">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="f0981-138">*i* + 2</span></span>  |
| <span data-ttu-id="f0981-139">Unabhängiges Dreieck</span><span class="sxs-lookup"><span data-stu-id="f0981-139">Independent triangle</span></span>        | <span data-ttu-id="f0981-140">3 *I*</span><span class="sxs-lookup"><span data-stu-id="f0981-140">3 *I*</span></span>     |
| <span data-ttu-id="f0981-141">Quad-Strip</span><span class="sxs-lookup"><span data-stu-id="f0981-141">Quad strip</span></span>                  | <span data-ttu-id="f0981-142">2 *i* + 2</span><span class="sxs-lookup"><span data-stu-id="f0981-142">2 *i* + 2</span></span> |
| <span data-ttu-id="f0981-143">Unabhängiges Quad</span><span class="sxs-lookup"><span data-stu-id="f0981-143">Independent quad</span></span>            | <span data-ttu-id="f0981-144">4 *I*</span><span class="sxs-lookup"><span data-stu-id="f0981-144">4 *I*</span></span>     |



 

<span data-ttu-id="f0981-145">Die flache und die glatte Schattierung werden von **glshademodel** angegeben, wobei der *Modus* auf GL \_ Flat \_ bzw. gl Smooth festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f0981-145">Flat and smooth shading are specified by **glShadeModel** with *mode* set to GL\_FLAT and GL\_SMOOTH, respectively.</span></span>

<span data-ttu-id="f0981-146">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glshademodel** ab:</span><span class="sxs-lookup"><span data-stu-id="f0981-146">The following function retrieves information related to **glShadeModel**:</span></span>

<span data-ttu-id="f0981-147">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Schattierung- \_ Modell</span><span class="sxs-lookup"><span data-stu-id="f0981-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SHADE\_MODEL</span></span>

## <a name="requirements"></a><span data-ttu-id="f0981-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0981-148">Requirements</span></span>



| <span data-ttu-id="f0981-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0981-149">Requirement</span></span> | <span data-ttu-id="f0981-150">Wert</span><span class="sxs-lookup"><span data-stu-id="f0981-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0981-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0981-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f0981-152">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0981-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f0981-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0981-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f0981-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0981-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0981-155">Header</span><span class="sxs-lookup"><span data-stu-id="f0981-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0981-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0981-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f0981-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0981-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0981-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0981-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f0981-159">DLL</span><span class="sxs-lookup"><span data-stu-id="f0981-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0981-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0981-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0981-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0981-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0981-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f0981-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f0981-163">**glcolor**</span><span class="sxs-lookup"><span data-stu-id="f0981-163">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="f0981-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f0981-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f0981-165">**gllight**</span><span class="sxs-lookup"><span data-stu-id="f0981-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="f0981-166">**gllightmodel**</span><span class="sxs-lookup"><span data-stu-id="f0981-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





