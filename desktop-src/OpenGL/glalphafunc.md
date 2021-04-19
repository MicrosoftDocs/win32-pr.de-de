---
title: glalphafunc-Funktion (GL. h)
description: Die glalphafunc-Funktion ermöglicht der Anwendung das Festlegen der Alpha-Testfunktion.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- glalphafunc-Funktion OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342021"
---
# <a name="glalphafunc-function"></a><span data-ttu-id="4bcd5-104">glalphafunc-Funktion</span><span class="sxs-lookup"><span data-stu-id="4bcd5-104">glAlphaFunc function</span></span>

<span data-ttu-id="4bcd5-105">Die **glalphafunc** -Funktion ermöglicht der Anwendung das Festlegen der Alpha-Testfunktion.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-105">The **glAlphaFunc** function enables your application to set the alpha test function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bcd5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bcd5-106">Syntax</span></span>


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a><span data-ttu-id="4bcd5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bcd5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bcd5-108">*func*</span><span class="sxs-lookup"><span data-stu-id="4bcd5-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="4bcd5-109">Die Alpha Vergleichsfunktion.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-109">The alpha comparison function.</span></span> <span data-ttu-id="4bcd5-110">Im folgenden finden Sie die akzeptierten symbolischen Konstanten und ihre Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-110">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="4bcd5-111">Wert</span><span class="sxs-lookup"><span data-stu-id="4bcd5-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="4bcd5-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4bcd5-112">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="4bcd5-113"><dt>**GL \_ nie**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="4bcd5-114">Läuft nie ab.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-114">Never passes.</span></span><br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="4bcd5-115"><dt>**GL \_ weniger**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="4bcd5-116">Übergibt, wenn der eingehende Alpha-Wert kleiner als der Verweis Wert ist.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-116">Passes if the incoming alpha value is less than the reference value.</span></span><br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="4bcd5-117"><dt>**GL \_ gleich**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-117"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="4bcd5-118">Übergibt, wenn der eingehende Alpha Wert gleich dem Verweis Wert ist.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-118">Passes if the incoming alpha value is equal to the reference value.</span></span><br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="4bcd5-119"><dt>**GL \_ lequal**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-119"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="4bcd5-120">Übergibt, wenn der eingehende Alpha-Wert kleiner oder gleich dem Verweis Wert ist.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-120">Passes if the incoming alpha value is less than or equal to the reference value.</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="4bcd5-121"><dt>**GL \_ größer**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-121"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="4bcd5-122">Übergibt, wenn der eingehende Alpha-Wert größer als der Verweis Wert ist.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-122">Passes if the incoming alpha value is greater than the reference value.</span></span><br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="4bcd5-123"><dt>**GL- \_ NotEqual**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-123"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="4bcd5-124">Übergibt, wenn der eingehende Alpha Wert nicht gleich dem Verweis Wert ist.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-124">Passes if the incoming alpha value is not equal to the reference value.</span></span><br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="4bcd5-125"><dt>**GL \_ gequal**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-125"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="4bcd5-126">Übergibt, wenn der eingehende Alpha-Wert größer oder gleich dem Verweis Wert ist.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-126">Passes if the incoming alpha value is greater than or equal to the reference value.</span></span><br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="4bcd5-127"><dt>**immer GL. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-127"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="4bcd5-128">Übergibt immer.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-128">Always passes.</span></span> <span data-ttu-id="4bcd5-129">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-129">This is the default.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="4bcd5-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="4bcd5-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="4bcd5-131">Der Verweis Wert, mit dem eingehende Alpha Werte verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-131">The reference value to which incoming alpha values are compared.</span></span> <span data-ttu-id="4bcd5-132">Dieser Wert wird an den Bereich von 0 bis 1 gebunden, wobei 0 den niedrigsten möglichen Alpha-Wert und 1 den höchstmöglichen Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-132">This value is clamped to the range 0 through 1, where 0 represents the lowest possible alpha value and 1 the highest possible value.</span></span> <span data-ttu-id="4bcd5-133">Der Standard Verweis ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4bcd5-133">The default reference is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bcd5-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bcd5-134">Return value</span></span>

<span data-ttu-id="4bcd5-135">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4bcd5-136">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4bcd5-136">Error codes</span></span>

<span data-ttu-id="4bcd5-137">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4bcd5-138">Name</span><span class="sxs-lookup"><span data-stu-id="4bcd5-138">Name</span></span>                                                                                                  | <span data-ttu-id="4bcd5-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4bcd5-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4bcd5-140"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4bcd5-141">*Func* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-141">*func* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="4bcd5-142"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4bcd5-143">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4bcd5-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bcd5-144">Remarks</span></span>

<span data-ttu-id="4bcd5-145">Der Alpha Test verwirft Fragmente abhängig vom Ergebnis eines Vergleichs zwischen den Alpha Werten der eingehenden Fragmente und einem konstanten Verweis Wert.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-145">The alpha test discards fragments depending on the outcome of a comparison between the incoming fragments' alpha values and a constant reference value.</span></span> <span data-ttu-id="4bcd5-146">Die Funktion " **glalphafunc** " gibt den Verweis und die Vergleichsfunktion an.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-146">The **glAlphaFunc** function specifies the reference and comparison function.</span></span> <span data-ttu-id="4bcd5-147">Der Vergleich wird nur durchgeführt, wenn Alpha Tests aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-147">The comparison is performed only if alpha testing is enabled.</span></span> <span data-ttu-id="4bcd5-148">(Weitere Informationen zu GL \_ Alpha \_ Test, siehe [**glEnable**](glenable.md).)</span><span class="sxs-lookup"><span data-stu-id="4bcd5-148">(For more information on GL\_ALPHA\_TEST, see [**glEnable**](glenable.md).)</span></span>

<span data-ttu-id="4bcd5-149">Der *Func* -Parameter und der *ref* -Parameter geben die Bedingungen an, unter denen das Pixel gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-149">The *func* and *ref* parameters specify the conditions under which the pixel is drawn.</span></span> <span data-ttu-id="4bcd5-150">Der eingehende Alpha-Wert wird *mit der* -Funktion verglichen, die von *Func* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-150">The incoming alpha value is compared to *ref* using the function specified by *func*.</span></span> <span data-ttu-id="4bcd5-151">Wenn der Vergleich bestanden wird, wird das eingehende Fragment gezeichnet, bedingt bei nachfolgenden Schablonen-und tiefen Puffer Tests.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-151">If the comparison passes, the incoming fragment is drawn, conditional on subsequent stencil and depth-buffer tests.</span></span> <span data-ttu-id="4bcd5-152">Wenn der Vergleich fehlschlägt, erfolgt keine Änderung am Frame Puffer an dieser Pixelposition.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-152">If the comparison fails, no change is made to the framebuffer at that pixel location.</span></span>

<span data-ttu-id="4bcd5-153">Die **glalphafunc** -Funktion arbeitet mit allen Pixel Schreibvorgängen, einschließlich derjenigen, die sich aus der Scan Konvertierung von Punkten, Zeilen, Polygonen und Bitmaps ergeben, sowie aus Pixel Zeichnungs-und Kopier Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-153">The **glAlphaFunc** function operates on all pixel writes, including those resulting from the scan conversion of points, lines, polygons, and bitmaps, and from pixel draw and copy operations.</span></span> <span data-ttu-id="4bcd5-154">Die **glalphafunc** -Funktion wirkt sich nicht auf Bildschirm Löschvorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-154">The **glAlphaFunc** function does not affect screen clear operations.</span></span>

<span data-ttu-id="4bcd5-155">Alpha Tests werden nur im RGBA-Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bcd5-155">Alpha testing is done only in RGBA mode.</span></span>

<span data-ttu-id="4bcd5-156">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glalphafunc** " ab:</span><span class="sxs-lookup"><span data-stu-id="4bcd5-156">The following functions retrieve information related to the **glAlphaFunc** function:</span></span>

<span data-ttu-id="4bcd5-157">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ alpha \_ Test \_ Func</span><span class="sxs-lookup"><span data-stu-id="4bcd5-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ALPHA\_TEST\_FUNC</span></span>

<span data-ttu-id="4bcd5-158">**glget** mit Argument GL \_ alpha \_ Test \_ Ref</span><span class="sxs-lookup"><span data-stu-id="4bcd5-158">**glGet** with argument GL\_ALPHA\_TEST\_REF</span></span>

<span data-ttu-id="4bcd5-159">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ alpha \_ Test</span><span class="sxs-lookup"><span data-stu-id="4bcd5-159">[**glIsEnabled**](glisenabled.md) with argument GL\_ALPHA\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="4bcd5-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bcd5-160">Requirements</span></span>



| <span data-ttu-id="4bcd5-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bcd5-161">Requirement</span></span> | <span data-ttu-id="4bcd5-162">Wert</span><span class="sxs-lookup"><span data-stu-id="4bcd5-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcd5-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bcd5-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4bcd5-164">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bcd5-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4bcd5-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bcd5-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4bcd5-166">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bcd5-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4bcd5-167">Header</span><span class="sxs-lookup"><span data-stu-id="4bcd5-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bcd5-168"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-168"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4bcd5-169">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4bcd5-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="4bcd5-170"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-170"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4bcd5-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4bcd5-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bcd5-172"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd5-172"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bcd5-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bcd5-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bcd5-174">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4bcd5-174">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4bcd5-175">**glblendfunc**</span><span class="sxs-lookup"><span data-stu-id="4bcd5-175">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="4bcd5-176">**glClear**</span><span class="sxs-lookup"><span data-stu-id="4bcd5-176">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="4bcd5-177">**gldepthfunc**</span><span class="sxs-lookup"><span data-stu-id="4bcd5-177">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="4bcd5-178">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="4bcd5-178">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="4bcd5-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4bcd5-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4bcd5-180">**glget**</span><span class="sxs-lookup"><span data-stu-id="4bcd5-180">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4bcd5-181">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="4bcd5-181">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="4bcd5-182">**glstencilfunc**</span><span class="sxs-lookup"><span data-stu-id="4bcd5-182">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





