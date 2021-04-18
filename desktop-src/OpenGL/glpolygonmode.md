---
title: glpolygonmode-Funktion (GL. h)
description: Die glpolygonmode-Funktion wählt einen Polygon-rasterisierungsmodus aus.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- glpolygonmode-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343892"
---
# <a name="glpolygonmode-function"></a><span data-ttu-id="f92f2-104">glpolygonmode-Funktion</span><span class="sxs-lookup"><span data-stu-id="f92f2-104">glPolygonMode function</span></span>

<span data-ttu-id="f92f2-105">Die **glpolygonmode** -Funktion wählt einen Polygon-rasterisierungsmodus aus.</span><span class="sxs-lookup"><span data-stu-id="f92f2-105">The **glPolygonMode** function selects a polygon rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="f92f2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f92f2-106">Syntax</span></span>


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="f92f2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f92f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f92f2-108">*mit*</span><span class="sxs-lookup"><span data-stu-id="f92f2-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="f92f2-109">Die Polygone, auf die der *Modus* angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f92f2-109">The polygons that *mode* applies to.</span></span> <span data-ttu-id="f92f2-110">Muss "GL \_ Front" für Front-on-Polygone, "GL \_ Back" für rückwärts gerichtete Polygone oder "GL \_ Front \_ und \_ Back" für Front-und Back-on-Polygone sein.</span><span class="sxs-lookup"><span data-stu-id="f92f2-110">Must be GL\_FRONT for front-facing polygons, GL\_BACK for back-facing polygons, or GL\_FRONT\_AND\_BACK for front- and back-facing polygons.</span></span>

</dd> <dt>

<span data-ttu-id="f92f2-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="f92f2-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="f92f2-112">Die Art und Weise, wie Polygone rasteriert werden.</span><span class="sxs-lookup"><span data-stu-id="f92f2-112">The way polygons will be rasterized.</span></span> <span data-ttu-id="f92f2-113">Die folgenden Modi sind definiert und können im- *Modus* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f92f2-113">The following modes are defined and can be specified in *mode*.</span></span> <span data-ttu-id="f92f2-114">Der Standardwert ist GL \_ Fill sowohl für Front-als auch für rückwärts gerichtete Polygone.</span><span class="sxs-lookup"><span data-stu-id="f92f2-114">The default is GL\_FILL for both front- and back-facing polygons.</span></span>



| <span data-ttu-id="f92f2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f92f2-115">Value</span></span>                                                                                                                                          | <span data-ttu-id="f92f2-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f92f2-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <span data-ttu-id="f92f2-117"><dt>**GL- \_ Punkt**</dt></span><span class="sxs-lookup"><span data-stu-id="f92f2-117"><dt>**GL\_POINT**</dt></span></span> </dl> | <span data-ttu-id="f92f2-118">Polygon Scheitel Punkte, die als Ausgangspunkt eines Begrenzungs Kanten gekennzeichnet sind, werden als Punkte gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f92f2-118">Polygon vertices that are marked as the start of a boundary edge are drawn as points.</span></span> <span data-ttu-id="f92f2-119">Die rasterisierung der Punkte wird von Punkt Attributen wie der GL \_ \_ -Punktgröße und dem GL- \_ Punkt \_ glatt gesteuert.</span><span class="sxs-lookup"><span data-stu-id="f92f2-119">Point attributes such as GL\_POINT\_SIZE and GL\_POINT\_SMOOTH control the rasterization of the points.</span></span> <span data-ttu-id="f92f2-120">Polygon-rasterisierungsattribute außer dem GL- \_ Polygon- \_ Modus haben keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="f92f2-120">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <span data-ttu-id="f92f2-121"><dt>**GL- \_ Zeile**</dt></span><span class="sxs-lookup"><span data-stu-id="f92f2-121"><dt>**GL\_LINE**</dt></span></span> </dl>    | <span data-ttu-id="f92f2-122">Begrenzungs Kanten des Polygons werden als Liniensegmente gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f92f2-122">Boundary edges of the polygon are drawn as line segments.</span></span> <span data-ttu-id="f92f2-123">Sie werden als verbundene Liniensegmente für den Zeilen stippling behandelt. der Zeilen stippingcounter und das Muster werden nicht zwischen Segmenten zurückgesetzt (siehe [**glLineStipple**](gllinestipple.md)).</span><span class="sxs-lookup"><span data-stu-id="f92f2-123">They are treated as connected line segments for line stippling; the line stipple counter and pattern are not reset between segments (see [**glLineStipple**](gllinestipple.md)).</span></span> <span data-ttu-id="f92f2-124">Linien Attribute wie GL \_ -Linienstärke \_ und GL- \_ Linien \_ Glättung steuern die rasterisierung der Zeilen.</span><span class="sxs-lookup"><span data-stu-id="f92f2-124">Line attributes such as GL\_LINE\_WIDTH and GL\_LINE\_SMOOTH control the rasterization of the lines.</span></span> <span data-ttu-id="f92f2-125">Polygon-rasterisierungsattribute außer dem GL- \_ Polygon- \_ Modus haben keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="f92f2-125">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <span data-ttu-id="f92f2-126"><dt>**Ausfüllen von GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f92f2-126"><dt>**GL\_FILL**</dt></span></span> </dl>    | <span data-ttu-id="f92f2-127">Das Innere des Polygons wird ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f92f2-127">The interior of the polygon is filled.</span></span> <span data-ttu-id="f92f2-128">Polygon-Attribute, wie z. b. gl \_ \_ -Polygon-Stippel und GL- \_ Polygon, \_ steuern die rasterisierung des Polygons.</span><span class="sxs-lookup"><span data-stu-id="f92f2-128">Polygon attributes such as GL\_POLYGON\_STIPPLE and GL\_POLYGON\_SMOOTH control the rasterization of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f92f2-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f92f2-129">Return value</span></span>

<span data-ttu-id="f92f2-130">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f92f2-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f92f2-131">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f92f2-131">Error codes</span></span>

<span data-ttu-id="f92f2-132">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f92f2-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f92f2-133">Name</span><span class="sxs-lookup"><span data-stu-id="f92f2-133">Name</span></span>                                                                                                  | <span data-ttu-id="f92f2-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f92f2-134">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f92f2-135"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f92f2-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f92f2-136">Entweder das *Gesicht* oder der *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="f92f2-136">Either *face* or *mode* was not an accepted value.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="f92f2-137"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f92f2-137"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f92f2-138">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f92f2-138">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f92f2-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f92f2-139">Remarks</span></span>

<span data-ttu-id="f92f2-140">Die Funktion " **glpolygonmode** " steuert die Interpretation von Polygonen für die rasterisierung.</span><span class="sxs-lookup"><span data-stu-id="f92f2-140">The **glPolygonMode** function controls the interpretation of polygons for rasterization.</span></span> <span data-ttu-id="f92f2-141">Der *Face* -Parameter beschreibt, für welchen polygonalmodus gilt: Front-on-Polygone (GL  \_ Front), Back-over-Polygone (GL \_ Back) oder beides (GL \_ Front \_ und \_ Back).</span><span class="sxs-lookup"><span data-stu-id="f92f2-141">The *face* parameter describes which polygons *mode* applies to: front-facing polygons (GL\_FRONT), back-facing polygons (GL\_BACK), or both (GL\_FRONT\_AND\_BACK).</span></span> <span data-ttu-id="f92f2-142">Der Polygon Modus wirkt sich nur auf die endgültige rasterisierung von Polygonen aus.</span><span class="sxs-lookup"><span data-stu-id="f92f2-142">The polygon mode affects only the final rasterization of polygons.</span></span> <span data-ttu-id="f92f2-143">Vor allem werden die Scheitel Punkte eines Polygons beleuchtet, und das Polygon wird abgeschnitten, und möglicherweise ist es möglich, bevor diese Modi angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f92f2-143">In particular, a polygon's vertices are lit and the polygon is clipped and possibly culled before these modes are applied.</span></span>

<span data-ttu-id="f92f2-144">Um eine Oberfläche mit gefüllten, rückwärts gerichteten Polygonen zu zeichnen und Front-End-Polygone zu sehen,</span><span class="sxs-lookup"><span data-stu-id="f92f2-144">To draw a surface with filled back-facing polygons and outlined front-facing polygons, call</span></span>

<span data-ttu-id="f92f2-145">**glpolygonmode**(GL \_ Front, GL \_ Line);</span><span class="sxs-lookup"><span data-stu-id="f92f2-145">**glPolygonMode**(GL\_FRONT, GL\_LINE);</span></span>

<span data-ttu-id="f92f2-146">Scheitel Punkte werden mit einem edgeflag als Begrenzung oder nonborder gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="f92f2-146">Vertices are marked as boundary or nonboundary with an edge flag.</span></span> <span data-ttu-id="f92f2-147">Edge-Flags werden intern von OpenGL generiert, wenn Polygone entfernt werden, und Sie können mithilfe von [**gledgeflag**](gledgeflag-functions.md)explizit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f92f2-147">Edge flags are generated internally by OpenGL when it decomposes polygons, and they can be set explicitly using [**glEdgeFlag**](gledgeflag-functions.md).</span></span>

<span data-ttu-id="f92f2-148">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glpolygonmode** ab:</span><span class="sxs-lookup"><span data-stu-id="f92f2-148">The following function retrieves information related to **glPolygonMode**:</span></span>

<span data-ttu-id="f92f2-149">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Polygon- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="f92f2-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="f92f2-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f92f2-150">Requirements</span></span>



| <span data-ttu-id="f92f2-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f92f2-151">Requirement</span></span> | <span data-ttu-id="f92f2-152">Wert</span><span class="sxs-lookup"><span data-stu-id="f92f2-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f92f2-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f92f2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f92f2-154">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f92f2-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f92f2-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f92f2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f92f2-156">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f92f2-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f92f2-157">Header</span><span class="sxs-lookup"><span data-stu-id="f92f2-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f92f2-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f92f2-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f92f2-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f92f2-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="f92f2-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f92f2-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f92f2-161">DLL</span><span class="sxs-lookup"><span data-stu-id="f92f2-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f92f2-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f92f2-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f92f2-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f92f2-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f92f2-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f92f2-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f92f2-165">**gledgeflag**</span><span class="sxs-lookup"><span data-stu-id="f92f2-165">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="f92f2-166">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f92f2-166">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f92f2-167">**gllinestippel**</span><span class="sxs-lookup"><span data-stu-id="f92f2-167">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="f92f2-168">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="f92f2-168">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="f92f2-169">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="f92f2-169">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="f92f2-170">**glpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="f92f2-170">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





