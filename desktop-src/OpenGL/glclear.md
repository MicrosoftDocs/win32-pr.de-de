---
title: glClear-Funktion (GL. h)
description: Die Funktion "glClear" löscht Puffer in voreingestellten Werte.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- glClear-Funktion OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338740"
---
# <a name="glclear-function"></a><span data-ttu-id="7c2ed-104">glClear-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c2ed-104">glClear function</span></span>

<span data-ttu-id="7c2ed-105">Die Funktion " **glClear** " löscht Puffer in voreingestellten Werte.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-105">The **glClear** function clears buffers to preset values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c2ed-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c2ed-106">Syntax</span></span>


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="7c2ed-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c2ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c2ed-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="7c2ed-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="7c2ed-109">Bitweise OR-Operatoren von Masken, die die zu löschenden Puffer angeben.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-109">Bitwise OR operators of masks that indicate the buffers to be cleared.</span></span> <span data-ttu-id="7c2ed-110">Die vier Masken sind wie folgt.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-110">The four masks are as follows.</span></span>



| <span data-ttu-id="7c2ed-111">Wert</span><span class="sxs-lookup"><span data-stu-id="7c2ed-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="7c2ed-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7c2ed-112">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <span data-ttu-id="7c2ed-113"><dt>**GL- \_ Farb \_ Puffer \_ Bit**</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-113"><dt>**GL\_COLOR\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="7c2ed-114">Die aktuell für das Schreiben von Farben aktivierten Puffer.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-114">The buffers currently enabled for color writing.</span></span><br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <span data-ttu-id="7c2ed-115"><dt>**GL- \_ Tiefe- \_ Puffer \_ Bit**</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-115"><dt>**GL\_DEPTH\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="7c2ed-116">Der tiefen Puffer.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-116">The depth buffer.</span></span><br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <span data-ttu-id="7c2ed-117"><dt>**GL- \_ Accum- \_ Puffer \_ Bit**</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-117"><dt>**GL\_ACCUM\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="7c2ed-118">Der Akkumulations Puffer.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-118">The accumulation buffer.</span></span><br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <span data-ttu-id="7c2ed-119"><dt>**GL- \_ Schablone- \_ Puffer \_ Bit**</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-119"><dt>**GL\_STENCIL\_BUFFER\_BIT**</dt></span></span> </dl> | <span data-ttu-id="7c2ed-120">Der Schablonen Puffer.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-120">The stencil buffer.</span></span><br/>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c2ed-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c2ed-121">Return value</span></span>

<span data-ttu-id="7c2ed-122">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-122">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7c2ed-123">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7c2ed-123">Error codes</span></span>

<span data-ttu-id="7c2ed-124">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7c2ed-125">Name</span><span class="sxs-lookup"><span data-stu-id="7c2ed-125">Name</span></span>                                                                                                  | <span data-ttu-id="7c2ed-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7c2ed-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c2ed-127"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-127"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7c2ed-128">Alle anderen Bits als die vier definierten Bits wurden in *Mask* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-128">Any bit other than the four defined bits was set in *mask*.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="7c2ed-129"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7c2ed-130">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7c2ed-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c2ed-131">Remarks</span></span>

<span data-ttu-id="7c2ed-132">Mit der Funktion " **glClear** " wird der bitplane-Bereich des Fensters auf Werte festgelegt, die zuvor von [**glclearcolor**](glclearcolor.md), [**glclearindex**](glclearindex.md), [**glcleartiefe**](glcleardepth.md), [**glclearstencil**](glclearstencil.md)und [**glclearaccum**](glclearaccum.md)ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-132">The **glClear** function sets the bitplane area of the window to values previously selected by [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), and [**glClearAccum**](glclearaccum.md).</span></span> <span data-ttu-id="7c2ed-133">Sie können mehrere Farb Puffer gleichzeitig löschen, indem Sie mit [**gldrawbuffer**](gldrawbuffer.md)mehr als einen Puffer gleichzeitig auswählen.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-133">You can clear multiple color buffers simultaneously by selecting more than one buffer at a time using [**glDrawBuffer**](gldrawbuffer.md).</span></span>

<span data-ttu-id="7c2ed-134">Der Pixel Besitz Test, die Scheren-Tests, die Dithering-und die Buffer-Schreibvorgänge wirken sich auf den Vorgang von **glClear** aus.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-134">The pixel-ownership test, the scissor test, dithering, and the buffer writemasks affect the operation of **glClear**.</span></span> <span data-ttu-id="7c2ed-135">Das Feld "Scheren" grenzt den gelöschten Bereich an.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-135">The scissor box bounds the cleared region.</span></span> <span data-ttu-id="7c2ed-136">Die Funktion " **glClear** " ignoriert die Funktionen "Alpha", "Blend", "logischer Vorgang", "Schablone", "Textur Zuordnung" und " *z*-Pufferung".</span><span class="sxs-lookup"><span data-stu-id="7c2ed-136">The **glClear** function ignores the alpha function, blend function, logical operation, stenciling, texture mapping, and *z*-buffering.</span></span>

<span data-ttu-id="7c2ed-137">Die Funktion " **glClear** " hat ein einzelnes Argument (*Mask*), bei dem es sich um das bitweise OR von mehreren Werten handelt, die angeben, welcher Puffer gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-137">The **glClear** function takes a single argument (*mask*) that is the bitwise OR of several values indicating which buffer is to be cleared.</span></span>

<span data-ttu-id="7c2ed-138">Der Wert, auf den der Puffer gelöscht wird, hängt von der Einstellung des Clear-Werts für diesen Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-138">The value to which each buffer is cleared depends on the setting of the clear value for that buffer.</span></span>

<span data-ttu-id="7c2ed-139">Wenn kein Puffer vorhanden ist, hat ein **glClear** -Befehl, der an diesen Puffer gerichtet ist, keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-139">If a buffer is not present, a **glClear** call directed at that buffer has no effect.</span></span>

<span data-ttu-id="7c2ed-140">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glClear** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="7c2ed-140">The following functions retrieve information related to **glClear**:</span></span>

<span data-ttu-id="7c2ed-141">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Accum \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="7c2ed-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="7c2ed-142">**glget** mit Argument GL- \_ Tiefe \_ Clear- \_ Wert</span><span class="sxs-lookup"><span data-stu-id="7c2ed-142">**glGet** with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

<span data-ttu-id="7c2ed-143">**glget** mit Argument GL- \_ Index \_ Clear- \_ Wert</span><span class="sxs-lookup"><span data-stu-id="7c2ed-143">**glGet** with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="7c2ed-144">**glget** mit dem Argument GL \_ Color \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="7c2ed-144">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

<span data-ttu-id="7c2ed-145">**glget** mit dem Argument GL \_ Stencil \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="7c2ed-145">**glGet** with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="7c2ed-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c2ed-146">Requirements</span></span>



| <span data-ttu-id="7c2ed-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c2ed-147">Requirement</span></span> | <span data-ttu-id="7c2ed-148">Wert</span><span class="sxs-lookup"><span data-stu-id="7c2ed-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2ed-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c2ed-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7c2ed-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c2ed-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7c2ed-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c2ed-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7c2ed-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c2ed-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c2ed-153">Header</span><span class="sxs-lookup"><span data-stu-id="7c2ed-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c2ed-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7c2ed-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c2ed-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c2ed-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c2ed-157">DLL</span><span class="sxs-lookup"><span data-stu-id="7c2ed-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c2ed-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c2ed-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c2ed-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c2ed-160">**glclearaccum**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-160">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="7c2ed-161">**glclearcolor**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-161">**glClearColor**</span></span>](glclearcolor.md)
</dt> <dt>

[<span data-ttu-id="7c2ed-162">**glcleartiefe**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-162">**glClearDepth**</span></span>](glcleardepth.md)
</dt> <dt>

[<span data-ttu-id="7c2ed-163">**glclearindex**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-163">**glClearIndex**</span></span>](glclearindex.md)
</dt> <dt>

[<span data-ttu-id="7c2ed-164">**glclearstencil**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-164">**glClearStencil**</span></span>](glclearstencil.md)
</dt> <dt>

[<span data-ttu-id="7c2ed-165">**gldrawbuffer**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-165">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="7c2ed-166">**glget**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-166">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7c2ed-167">**glscissor**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-167">**glScissor**</span></span>](glscissor.md)
</dt> </dl>

 

 





