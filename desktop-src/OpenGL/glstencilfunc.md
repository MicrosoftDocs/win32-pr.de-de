---
title: glstencilfunc-Funktion (GL. h)
description: Die Funktion "glstencilfunc" legt die Funktion und den Verweis Wert für Schablonen Tests fest.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- glstencilfunc-Funktion OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346133"
---
# <a name="glstencilfunc-function"></a><span data-ttu-id="48b56-104">glstencilfunc-Funktion</span><span class="sxs-lookup"><span data-stu-id="48b56-104">glStencilFunc function</span></span>

<span data-ttu-id="48b56-105">Die Funktion " **glstencilfunc** " legt die Funktion und den Verweis Wert für Schablonen Tests fest.</span><span class="sxs-lookup"><span data-stu-id="48b56-105">The **glStencilFunc** function sets the function and reference value for stencil testing.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b56-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="48b56-106">Syntax</span></span>


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="48b56-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="48b56-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b56-108">*func*</span><span class="sxs-lookup"><span data-stu-id="48b56-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="48b56-109">Die Testfunktion.</span><span class="sxs-lookup"><span data-stu-id="48b56-109">The test function.</span></span> <span data-ttu-id="48b56-110">Die folgenden acht Token sind gültig.</span><span class="sxs-lookup"><span data-stu-id="48b56-110">The following eight tokens are valid.</span></span>



| <span data-ttu-id="48b56-111">Wert</span><span class="sxs-lookup"><span data-stu-id="48b56-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="48b56-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="48b56-112">Meaning</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="48b56-113"><dt>**GL \_ nie**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="48b56-114">Schlägt immer fehl.</span><span class="sxs-lookup"><span data-stu-id="48b56-114">Always fails.</span></span><br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="48b56-115"><dt>**GL \_ weniger**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="48b56-116">Übergibt if (*ref*  &  *Mask*) < (*Schablone*  &  *Mask*).</span><span class="sxs-lookup"><span data-stu-id="48b56-116">Passes if (*ref* & *mask*) < (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="48b56-117"><dt>**GL \_ lequal**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-117"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="48b56-118">Übergibt if (*ref*  &  *Mask*) = (*Schablone*  &  *Mask*).</span><span class="sxs-lookup"><span data-stu-id="48b56-118">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="48b56-119"><dt>**GL \_ größer**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-119"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="48b56-120">Übergibt if (*ref*  &  *Mask*) > (*Schablone*  &  *Mask*).</span><span class="sxs-lookup"><span data-stu-id="48b56-120">Passes if (*ref* & *mask*) > (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="48b56-121"><dt>**GL \_ gequal**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-121"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="48b56-122">Übergibt if (*ref*  &  *Mask*) = (*Schablone*  &  *Mask*).</span><span class="sxs-lookup"><span data-stu-id="48b56-122">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="48b56-123"><dt>**GL \_ gleich**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-123"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="48b56-124">Übergibt if (*ref*  &  *Mask*) = (*Schablone*  &  *Mask*).</span><span class="sxs-lookup"><span data-stu-id="48b56-124">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="48b56-125"><dt>**GL- \_ NotEqual**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-125"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="48b56-126">Übergibt if (*ref*  &  *Mask*)?</span><span class="sxs-lookup"><span data-stu-id="48b56-126">Passes if (*ref* & *mask*) ?</span></span> <span data-ttu-id="48b56-127">(*Schablone*  &  *Mask*).</span><span class="sxs-lookup"><span data-stu-id="48b56-127">(*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="48b56-128"><dt>**immer GL. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="48b56-129">Übergibt immer.</span><span class="sxs-lookup"><span data-stu-id="48b56-129">Always passes.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="48b56-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="48b56-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="48b56-131">Der Verweis Wert für den Schablonen Test.</span><span class="sxs-lookup"><span data-stu-id="48b56-131">The reference value for the stencil test.</span></span> <span data-ttu-id="48b56-132">Der *ref* -Parameter wird an den Bereich \[ von 0, 2 *n* 1 \] , gebunden, wobei *n* die Anzahl der bitebenen im Schablonen Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="48b56-132">The *ref* parameter is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

</dd> <dt>

<span data-ttu-id="48b56-133">*mask*</span><span class="sxs-lookup"><span data-stu-id="48b56-133">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="48b56-134">Eine Maske, die beim Abschluss des Tests sowohl mit dem Verweis Wert als auch mit dem gespeicherten Schablonen Wert **erstellt wird.**</span><span class="sxs-lookup"><span data-stu-id="48b56-134">A mask that is **AND** ed with both the reference value and the stored stencil value when the test is done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b56-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48b56-135">Return value</span></span>

<span data-ttu-id="48b56-136">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="48b56-136">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="48b56-137">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="48b56-137">Error codes</span></span>

<span data-ttu-id="48b56-138">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="48b56-138">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="48b56-139">Name</span><span class="sxs-lookup"><span data-stu-id="48b56-139">Name</span></span>                                                                                                  | <span data-ttu-id="48b56-140">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="48b56-140">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48b56-141"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-141"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="48b56-142">*Func* war keiner der acht akzeptierten Werte.</span><span class="sxs-lookup"><span data-stu-id="48b56-142">*func* was not one of the eight accepted values.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="48b56-143"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-143"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="48b56-144">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="48b56-144">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48b56-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48b56-145">Remarks</span></span>

<span data-ttu-id="48b56-146">Durch die Schablone, z. b. *z*-Pufferung, wird das Zeichnen pro Pixel aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="48b56-146">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="48b56-147">Sie zeichnen mithilfe von OpenGL-Zeichen primitiven in die Schablone-Ebenen und erzeugen dann Geometrie und Bilder mithilfe der Schablonen Flächen, um Teile des Bildschirms zu maskieren.</span><span class="sxs-lookup"><span data-stu-id="48b56-147">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="48b56-148">Die Schablone wird in der Regel in Multipass-renderingalgorithmen verwendet, um besondere Effekte zu erzielen, wie z. b. Decals, Gliederung und konstruktives solides Geometrie Rendering.</span><span class="sxs-lookup"><span data-stu-id="48b56-148">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="48b56-149">Der Schablone-Test entfernt bedingt ein Pixel basierend auf dem Ergebnis eines Vergleichs zwischen dem Verweis Wert und dem Wert im Schablonen Puffer.</span><span class="sxs-lookup"><span data-stu-id="48b56-149">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the reference value and the value in the stencil buffer.</span></span> <span data-ttu-id="48b56-150">Der Test wird durch [**glEnable**](glenable.md) und [**glEnable**](gldisable.md) mit dem Argument GL \_ Stencil \_ Test aktiviert.</span><span class="sxs-lookup"><span data-stu-id="48b56-150">The test is enabled by [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_STENCIL\_TEST.</span></span> <span data-ttu-id="48b56-151">Auf der Grundlage des Ergebnisses des Schablonen Tests ausgeführte Aktionen werden mit [**glstencilop**](glstencilop.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="48b56-151">Actions taken based on the outcome of the stencil test are specified with [**glStencilOp**](glstencilop.md).</span></span>

<span data-ttu-id="48b56-152">Der *Func* -Parameter ist eine symbolische Konstante, die die Schablone-Vergleichsfunktion bestimmt.</span><span class="sxs-lookup"><span data-stu-id="48b56-152">The *func* parameter is a symbolic constant that determines the stencil comparison function.</span></span> <span data-ttu-id="48b56-153">Er akzeptiert einen der oben gezeigten acht Werte.</span><span class="sxs-lookup"><span data-stu-id="48b56-153">It accepts one of the eight values shown above.</span></span> <span data-ttu-id="48b56-154">Der *ref* -Parameter ist ein ganzzahliger Verweis Wert, der im Schablone-Vergleich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="48b56-154">The *ref* parameter is an integer reference value that is used in the stencil comparison.</span></span> <span data-ttu-id="48b56-155">Der Wert wird an den Bereich \[ 0, 2 *n* 1 geklammert \] , wobei *n* die Anzahl der bitflächen im Schablonen Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="48b56-155">It is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span> <span data-ttu-id="48b56-156">Der *Mask* -Parameter ist bitweise **und** wird sowohl mit dem Verweis Wert als auch mit dem gespeicherten Schablonen Wert, wobei die Werte und die ED **-** Werte am Vergleich beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="48b56-156">The *mask* parameter is bitwise **AND** ed with both the reference value and the stored stencil value, with the **AND** ed values participating in the comparison.</span></span>

<span data-ttu-id="48b56-157">Wenn *Schablone* den Wert darstellt, der im entsprechenden Schablone-Puffer Speicherort gespeichert ist, zeigt die vorangehende Liste die Auswirkungen jeder Vergleichsfunktion an, die von *Func* angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="48b56-157">If *stencil* represents the value stored in the corresponding stencil buffer location, the preceding list shows the effect of each comparison function that can be specified by *func*.</span></span> <span data-ttu-id="48b56-158">Nur, wenn der Vergleich erfolgreich ist, wird das Pixel an die nächste Phase im rasterisierungsprozess übergeben (siehe [**glstencilop**](glstencilop.md)).</span><span class="sxs-lookup"><span data-stu-id="48b56-158">Only if the comparison succeeds is the pixel passed through to the next stage in the rasterization process (see [**glStencilOp**](glstencilop.md)).</span></span> <span data-ttu-id="48b56-159">Alle Tests behandeln *Schablonen* Werte als ganze Zahlen ohne Vorzeichen im Bereich \[ 0, 2 *n* 1 \] , wobei *n* die Anzahl der bitebenen im Schablonen Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="48b56-159">All tests treat *stencil* values as unsigned integers in the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

<span data-ttu-id="48b56-160">Anfänglich ist der Schablone-Test deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="48b56-160">Initially, the stencil test is disabled.</span></span> <span data-ttu-id="48b56-161">Wenn kein Schablonen Puffer vorhanden ist, kann keine Schablone geändert werden, und dies ist der Fall, wenn der Schablone-Test immer durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="48b56-161">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil test always passes.</span></span>

<span data-ttu-id="48b56-162">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glstencilfunc** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="48b56-162">The following functions retrieve information related to **glStencilFunc**:</span></span>

<span data-ttu-id="48b56-163">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Stencil \_ Func</span><span class="sxs-lookup"><span data-stu-id="48b56-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FUNC</span></span>

<span data-ttu-id="48b56-164">**glget** mit dem Argument GL \_ Stencil \_ Wert \_ Mask</span><span class="sxs-lookup"><span data-stu-id="48b56-164">**glGet** with argument GL\_STENCIL\_VALUE\_MASK</span></span>

<span data-ttu-id="48b56-165">**glget** mit Argument GL \_ Stencil \_ Ref</span><span class="sxs-lookup"><span data-stu-id="48b56-165">**glGet** with argument GL\_STENCIL\_REF</span></span>

<span data-ttu-id="48b56-166">**glget** mit Argument GL- \_ Schablonen \_ Bits</span><span class="sxs-lookup"><span data-stu-id="48b56-166">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="48b56-167">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Stencil \_ Test</span><span class="sxs-lookup"><span data-stu-id="48b56-167">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="48b56-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48b56-168">Requirements</span></span>



| <span data-ttu-id="48b56-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48b56-169">Requirement</span></span> | <span data-ttu-id="48b56-170">Wert</span><span class="sxs-lookup"><span data-stu-id="48b56-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48b56-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48b56-171">Minimum supported client</span></span><br/> | <span data-ttu-id="48b56-172">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b56-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="48b56-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48b56-173">Minimum supported server</span></span><br/> | <span data-ttu-id="48b56-174">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b56-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48b56-175">Header</span><span class="sxs-lookup"><span data-stu-id="48b56-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="48b56-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="48b56-177">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48b56-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="48b56-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="48b56-179">DLL</span><span class="sxs-lookup"><span data-stu-id="48b56-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48b56-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48b56-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48b56-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48b56-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b56-182">**glalphafunc**</span><span class="sxs-lookup"><span data-stu-id="48b56-182">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="48b56-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="48b56-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="48b56-184">**glblendfunc**</span><span class="sxs-lookup"><span data-stu-id="48b56-184">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="48b56-185">**gldepthfunc**</span><span class="sxs-lookup"><span data-stu-id="48b56-185">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="48b56-186">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="48b56-186">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="48b56-187">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="48b56-187">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="48b56-188">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="48b56-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="48b56-189">**gllogicop**</span><span class="sxs-lookup"><span data-stu-id="48b56-189">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="48b56-190">**glstencilop**</span><span class="sxs-lookup"><span data-stu-id="48b56-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





