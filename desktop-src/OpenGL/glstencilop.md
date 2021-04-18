---
title: glstencilop-Funktion (GL. h)
description: Die Funktion "glstencilop" legt die Test Aktionen der Schablone fest.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- glstencilop-Funktion OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340355"
---
# <a name="glstencilop-function"></a><span data-ttu-id="c5029-104">glstencilop-Funktion</span><span class="sxs-lookup"><span data-stu-id="c5029-104">glStencilOp function</span></span>

<span data-ttu-id="c5029-105">Die Funktion " **glstencilop** " legt die Test Aktionen der Schablone fest.</span><span class="sxs-lookup"><span data-stu-id="c5029-105">The **glStencilOp** function sets the stencil test actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5029-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5029-106">Syntax</span></span>


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a><span data-ttu-id="c5029-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5029-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5029-108">*UN*</span><span class="sxs-lookup"><span data-stu-id="c5029-108">*fail*</span></span> 
</dt> <dd>

<span data-ttu-id="c5029-109">Die Aktion, die ausgeführt werden soll, wenn der Schablonen Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="c5029-109">The action to take when the stencil test fails.</span></span> <span data-ttu-id="c5029-110">Die folgenden sechs symbolischen Konstanten werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c5029-110">The following six symbolic constants are accepted.</span></span>



| <span data-ttu-id="c5029-111">Wert</span><span class="sxs-lookup"><span data-stu-id="c5029-111">Value</span></span>                                                                                                                                                | <span data-ttu-id="c5029-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c5029-112">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <span data-ttu-id="c5029-113"><dt>**GL \_ beibehalten**</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-113"><dt>**GL\_KEEP**</dt></span></span> </dl>          | <span data-ttu-id="c5029-114">Behält den aktuellen Wert bei.</span><span class="sxs-lookup"><span data-stu-id="c5029-114">Keeps the current value.</span></span><br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <span data-ttu-id="c5029-115"><dt>**GL \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-115"><dt>**GL\_ZERO**</dt></span></span> </dl>          | <span data-ttu-id="c5029-116">Legt den Schablonen Puffer Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="c5029-116">Sets the stencil buffer value to zero.</span></span><br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <span data-ttu-id="c5029-117"><dt>**GL \_ ersetzen**</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-117"><dt>**GL\_REPLACE**</dt></span></span> </dl> | <span data-ttu-id="c5029-118">Legt den Schablonen Puffer Wert entsprechend der Angabe durch **glstencilfunc** auf *ref* fest.</span><span class="sxs-lookup"><span data-stu-id="c5029-118">Sets the stencil buffer value to *ref*, as specified by **glStencilFunc**.</span></span><br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <span data-ttu-id="c5029-119"><dt>**GL- \_ INCR**</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-119"><dt>**GL\_INCR**</dt></span></span> </dl>          | <span data-ttu-id="c5029-120">Inkremente den aktuellen Schablonen Puffer Wert.</span><span class="sxs-lookup"><span data-stu-id="c5029-120">Increments the current stencil buffer value.</span></span> <span data-ttu-id="c5029-121">Bindet an den maximalen darstellbaren Wert ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c5029-121">Clamps to the maximum representable unsigned value.</span></span><br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <span data-ttu-id="c5029-122"><dt>**GL- \_ decr**</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-122"><dt>**GL\_DECR**</dt></span></span> </dl>          | <span data-ttu-id="c5029-123">Dekremente den aktuellen Schablonen Puffer Wert.</span><span class="sxs-lookup"><span data-stu-id="c5029-123">Decrements the current stencil buffer value.</span></span> <span data-ttu-id="c5029-124">Bindet auf NULL.</span><span class="sxs-lookup"><span data-stu-id="c5029-124">Clamps to zero.</span></span><br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="c5029-125"><dt>**GL \_ Invert**</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-125"><dt>**GL\_INVERT**</dt></span></span> </dl>    | <span data-ttu-id="c5029-126">Bitweise kehrt den aktuellen Schablonen Puffer Wert um.</span><span class="sxs-lookup"><span data-stu-id="c5029-126">Bitwise inverts the current stencil buffer value.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="c5029-127">*zfail*</span><span class="sxs-lookup"><span data-stu-id="c5029-127">*zfail*</span></span> 
</dt> <dd>

<span data-ttu-id="c5029-128">Schablone-Aktion, wenn der Schablone-Test erfolgreich verläuft, aber der tiefen Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="c5029-128">Stencil action when the stencil test passes, but the depth test fails.</span></span> <span data-ttu-id="c5029-129">Akzeptiert dieselben symbolischen Konstanten als *fehlgeschlagen.*</span><span class="sxs-lookup"><span data-stu-id="c5029-129">Accepts the same symbolic constants as *fail.*</span></span>

</dd> <dt>

<span data-ttu-id="c5029-130">*ZPass*</span><span class="sxs-lookup"><span data-stu-id="c5029-130">*zpass*</span></span> 
</dt> <dd>

<span data-ttu-id="c5029-131">Schablone-Aktion, wenn der Schablonen Test und der tiefen Test bestanden werden, oder wenn der Schablonen Test erfolgreich verläuft und entweder kein tiefen Puffer vorhanden ist oder keine tiefen Tests aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c5029-131">Stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled.</span></span> <span data-ttu-id="c5029-132">Akzeptiert dieselben symbolischen Konstanten als *fehl* geschlagen.</span><span class="sxs-lookup"><span data-stu-id="c5029-132">Accepts the same symbolic constants as *fail*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5029-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5029-133">Return value</span></span>

<span data-ttu-id="c5029-134">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c5029-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c5029-135">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c5029-135">Error codes</span></span>

<span data-ttu-id="c5029-136">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c5029-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c5029-137">Name</span><span class="sxs-lookup"><span data-stu-id="c5029-137">Name</span></span>                                                                                                  | <span data-ttu-id="c5029-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c5029-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5029-139"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c5029-140">" *Fail*", " *zfail*" oder " *ZPass* " war ein anderer Wert als die sechs definierten Konstanten Werte.</span><span class="sxs-lookup"><span data-stu-id="c5029-140">*fail*, *zfail*, or *zpass* was any value other than the six defined constant values.</span></span><br/>                                      |
| <dl> <span data-ttu-id="c5029-141"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c5029-142">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c5029-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c5029-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5029-143">Remarks</span></span>

<span data-ttu-id="c5029-144">Durch die Schablone, z. b. *z*-Pufferung, wird das Zeichnen pro Pixel aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c5029-144">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="c5029-145">Sie zeichnen mithilfe von OpenGL-Zeichen primitiven in die Schablone-Ebenen und erzeugen dann Geometrie und Bilder mithilfe der Schablonen Flächen, um Teile des Bildschirms zu maskieren.</span><span class="sxs-lookup"><span data-stu-id="c5029-145">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="c5029-146">Die Schablone wird in der Regel in Multipass-renderingalgorithmen verwendet, um besondere Effekte zu erzielen, wie z. b. Decals, Gliederung und konstruktives solides Geometrie Rendering.</span><span class="sxs-lookup"><span data-stu-id="c5029-146">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="c5029-147">Der Schablone-Test entfernt bedingt ein Pixel basierend auf dem Ergebnis eines Vergleichs zwischen dem Wert im Schablonen Puffer und einem Verweis Wert.</span><span class="sxs-lookup"><span data-stu-id="c5029-147">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="c5029-148">Der Test ist mit " [**glEnable**](glenable.md) "-und " [**gldeaktiviert**](gldisable.md) "-aufrufen mit dem Argument "GL \_ Stencil Test" aktiviert \_ und mit " [**glstencilfunc**](glstencilfunc.md)" gesteuert</span><span class="sxs-lookup"><span data-stu-id="c5029-148">The test is enabled with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) calls with argument GL\_STENCIL\_TEST, and controlled with [**glStencilFunc**](glstencilfunc.md).</span></span>

<span data-ttu-id="c5029-149">Die **glstencilop** -Funktion nimmt drei Argumente an, die angeben, was mit dem gespeicherten Schablonen Wert geschieht, während die Schablone aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c5029-149">The **glStencilOp** function takes three arguments that indicate what happens to the stored stencil value while stenciling is enabled.</span></span> <span data-ttu-id="c5029-150">Wenn der Schablone-Test fehlschlägt, wird keine Änderung an den Farb-oder tiefen Puffern des Pixels vorgenommen, und der Fehler gibt an, was mit dem Inhalt der *Schablone-Puffer* passiert.</span><span class="sxs-lookup"><span data-stu-id="c5029-150">If the stencil test fails, no change is made to the pixel's color or depth buffers, and *fail* specifies what happens to the stencil buffer contents.</span></span>

<span data-ttu-id="c5029-151">Schablonen Puffer Werte werden als ganze Zahlen ohne Vorzeichen behandelt.</span><span class="sxs-lookup"><span data-stu-id="c5029-151">Stencil buffer values are treated as unsigned integers.</span></span> <span data-ttu-id="c5029-152">Wenn inkrementiert und dekrementiert, werden die Werte an 0 und 2 *n* 1 gebunden, wobei *n* der Wert ist, der durch Abfragen von GL-Schablonen Bits zurückgegeben wird \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c5029-152">When incremented and decremented, values are clamped to 0 and 2 *n* 1, where *n* is the value returned by querying GL\_STENCIL\_BITS.</span></span>

<span data-ttu-id="c5029-153">Die anderen beiden Argumente für **glstencilop** geben Schablonen Puffer Aktionen an, wenn nachfolgende tiefen Puffer Tests erfolgreich verlaufen (*ZPass*) oder Fail (*zfail*).</span><span class="sxs-lookup"><span data-stu-id="c5029-153">The other two arguments to **glStencilOp** specify stencil buffer actions should subsequent depth buffer tests succeed (*zpass*) or fail (*zfail*).</span></span> <span data-ttu-id="c5029-154">(Siehe [**gldepthfunc**](gldepthfunc.md).) Sie werden mit denselben sechs symbolischen Konstanten wie " *Fail*" angegeben.</span><span class="sxs-lookup"><span data-stu-id="c5029-154">(See [**glDepthFunc**](gldepthfunc.md).) They are specified using the same six symbolic constants as *fail*.</span></span> <span data-ttu-id="c5029-155">Beachten Sie, dass *zfail* ignoriert wird, wenn kein tiefen Puffer vorhanden ist oder wenn der tiefen Puffer nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c5029-155">Note that *zfail* is ignored when there is no depth buffer, or when the depth buffer is not enabled.</span></span> <span data-ttu-id="c5029-156">In diesen Fällen geben *Fail* und *ZPass* eine Schablone-Aktion an, wenn der Schablonen Test fehlschlägt bzw. übergibt.</span><span class="sxs-lookup"><span data-stu-id="c5029-156">In these cases, *fail* and *zpass* specify stencil action when the stencil test fails and passes, respectively.</span></span>

<span data-ttu-id="c5029-157">Anfänglich ist der Schablonen Test deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c5029-157">Initially the stencil test is disabled.</span></span> <span data-ttu-id="c5029-158">Wenn kein Schablonen Puffer vorhanden ist, kann keine Schablone geändert werden, und es ist so, als ob die Schablonen Tests immer bestanden werden, unabhängig von jedem beliebigen Aufrufe von **glstencilop**.</span><span class="sxs-lookup"><span data-stu-id="c5029-158">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil tests always pass, regardless of any call to **glStencilOp**.</span></span>

<span data-ttu-id="c5029-159">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glstencilop** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="c5029-159">The following functions retrieve information related to **glStencilOp**:</span></span>

<span data-ttu-id="c5029-160">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Stencil \_ Fail</span><span class="sxs-lookup"><span data-stu-id="c5029-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FAIL</span></span>

<span data-ttu-id="c5029-161">**glget** mit dem Argument GL \_ Stencil \_ Pass \_ Tiefe \_ Pass</span><span class="sxs-lookup"><span data-stu-id="c5029-161">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_PASS</span></span>

<span data-ttu-id="c5029-162">**glget** mit dem Argument GL \_ Stencil \_ Pass \_ Tiefe \_ Fail</span><span class="sxs-lookup"><span data-stu-id="c5029-162">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_FAIL</span></span>

<span data-ttu-id="c5029-163">**glget** mit Argument GL- \_ Schablonen \_ Bits</span><span class="sxs-lookup"><span data-stu-id="c5029-163">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="c5029-164">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Stencil \_ Test</span><span class="sxs-lookup"><span data-stu-id="c5029-164">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="c5029-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5029-165">Requirements</span></span>



| <span data-ttu-id="c5029-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5029-166">Requirement</span></span> | <span data-ttu-id="c5029-167">Wert</span><span class="sxs-lookup"><span data-stu-id="c5029-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5029-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5029-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c5029-169">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5029-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c5029-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5029-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c5029-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5029-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c5029-172">Header</span><span class="sxs-lookup"><span data-stu-id="c5029-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5029-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c5029-174">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5029-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="c5029-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c5029-176">DLL</span><span class="sxs-lookup"><span data-stu-id="c5029-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5029-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5029-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5029-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5029-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5029-179">**glalphafunc**</span><span class="sxs-lookup"><span data-stu-id="c5029-179">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="c5029-180">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c5029-180">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c5029-181">**glblendfunc**</span><span class="sxs-lookup"><span data-stu-id="c5029-181">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="c5029-182">**gldepthfunc**</span><span class="sxs-lookup"><span data-stu-id="c5029-182">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="c5029-183">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="c5029-183">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="c5029-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c5029-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c5029-185">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="c5029-185">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="c5029-186">**gllogicop**</span><span class="sxs-lookup"><span data-stu-id="c5029-186">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="c5029-187">**glstencilfunc**</span><span class="sxs-lookup"><span data-stu-id="c5029-187">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





