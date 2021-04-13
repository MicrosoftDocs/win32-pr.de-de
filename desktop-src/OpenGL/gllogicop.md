---
title: gllogicop-Funktion (GL. h)
description: Die Funktion "gllogicop" gibt einen logischen Pixel Vorgang für das Rendern von Farbindizes an.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- gllogicop-Funktion OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519151"
---
# <a name="gllogicop-function"></a><span data-ttu-id="71b2c-104">gllogicop-Funktion</span><span class="sxs-lookup"><span data-stu-id="71b2c-104">glLogicOp function</span></span>

<span data-ttu-id="71b2c-105">Die Funktion " **gllogicop** " gibt einen logischen Pixel Vorgang für das Rendern von Farbindizes an.</span><span class="sxs-lookup"><span data-stu-id="71b2c-105">The **glLogicOp** function specifies a logical pixel operation for color index rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b2c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="71b2c-106">Syntax</span></span>


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a><span data-ttu-id="71b2c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="71b2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71b2c-108">*OpCode*</span><span class="sxs-lookup"><span data-stu-id="71b2c-108">*opcode*</span></span> 
</dt> <dd>

<span data-ttu-id="71b2c-109">Eine symbolische Konstante, die eine logische Operation auswählt.</span><span class="sxs-lookup"><span data-stu-id="71b2c-109">A symbolic constant that selects a logical operation.</span></span> <span data-ttu-id="71b2c-110">Die folgenden Symbole werden akzeptiert, wenn s dem Wert des Quell Bits entspricht und d der Wert des Zielbits ist.</span><span class="sxs-lookup"><span data-stu-id="71b2c-110">The following symbols are accepted where s equals the value of the source bit and d is the value of the destination bit.</span></span>



| <span data-ttu-id="71b2c-111">Wert</span><span class="sxs-lookup"><span data-stu-id="71b2c-111">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="71b2c-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="71b2c-112">Meaning</span></span>              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <span data-ttu-id="71b2c-113"><dt>**GL \_ Clear**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-113"><dt>**GL\_CLEAR**</dt></span></span> </dl>                          | <span data-ttu-id="71b2c-114">0</span><span class="sxs-lookup"><span data-stu-id="71b2c-114">0</span></span><br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <span data-ttu-id="71b2c-115"><dt>**GL- \_ Satz**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-115"><dt>**GL\_SET**</dt></span></span> </dl>                                | <span data-ttu-id="71b2c-116">1</span><span class="sxs-lookup"><span data-stu-id="71b2c-116">1</span></span><br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <span data-ttu-id="71b2c-117"><dt>**GL- \_ Kopie**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-117"><dt>**GL\_COPY**</dt></span></span> </dl>                             | <span data-ttu-id="71b2c-118">s</span><span class="sxs-lookup"><span data-stu-id="71b2c-118">s</span></span><br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <span data-ttu-id="71b2c-119"><dt>**GL- \_ Kopie \_ invertiert**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-119"><dt>**GL\_COPY\_INVERTED**</dt></span></span> </dl> | <span data-ttu-id="71b2c-120">! s</span><span class="sxs-lookup"><span data-stu-id="71b2c-120">!s</span></span><br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <span data-ttu-id="71b2c-121"><dt>**GL. \_ NoOp**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-121"><dt>**GL\_NOOP**</dt></span></span> </dl>                             | <span data-ttu-id="71b2c-122">d</span><span class="sxs-lookup"><span data-stu-id="71b2c-122">d</span></span><br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="71b2c-123"><dt>**GL \_ Invert**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-123"><dt>**GL\_INVERT**</dt></span></span> </dl>                       | <span data-ttu-id="71b2c-124">! d</span><span class="sxs-lookup"><span data-stu-id="71b2c-124">!d</span></span><br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <span data-ttu-id="71b2c-125"><dt>**GL \_ und**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-125"><dt>**GL\_AND**</dt></span></span> </dl>                                | <span data-ttu-id="71b2c-126">s & d</span><span class="sxs-lookup"><span data-stu-id="71b2c-126">s & d</span></span><br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <span data-ttu-id="71b2c-127"><dt>**GL \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-127"><dt>**GL\_NAND**</dt></span></span> </dl>                             | <span data-ttu-id="71b2c-128">! (s & d)</span><span class="sxs-lookup"><span data-stu-id="71b2c-128">!(s & d)</span></span><br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <span data-ttu-id="71b2c-129"><dt>**GL \_ oder**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-129"><dt>**GL\_OR**</dt></span></span> </dl>                                   | <span data-ttu-id="71b2c-130">s \| d</span><span class="sxs-lookup"><span data-stu-id="71b2c-130">s \| d</span></span><br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <span data-ttu-id="71b2c-131"><dt>**GL \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-131"><dt>**GL\_NOR**</dt></span></span> </dl>                                | <span data-ttu-id="71b2c-132">! (s \| d)</span><span class="sxs-lookup"><span data-stu-id="71b2c-132">!(s \| d)</span></span><br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <span data-ttu-id="71b2c-133"><dt>**GL. \_ Xor**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-133"><dt>**GL\_XOR**</dt></span></span> </dl>                                | <span data-ttu-id="71b2c-134">s ^ d</span><span class="sxs-lookup"><span data-stu-id="71b2c-134">s ^ d</span></span><br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <span data-ttu-id="71b2c-135"><dt>**GL- \_ equiv**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-135"><dt>**GL\_EQUIV**</dt></span></span> </dl>                          | <span data-ttu-id="71b2c-136">! (s ^ d)</span><span class="sxs-lookup"><span data-stu-id="71b2c-136">!(s ^ d)</span></span><br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <span data-ttu-id="71b2c-137"><dt>**GL \_ und \_ umgekehrt**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-137"><dt>**GL\_AND\_REVERSE**</dt></span></span> </dl>       | <span data-ttu-id="71b2c-138">s &! d</span><span class="sxs-lookup"><span data-stu-id="71b2c-138">s & !d</span></span><br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <span data-ttu-id="71b2c-139"><dt>**GL \_ und \_ invertiert**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-139"><dt>**GL\_AND\_INVERTED**</dt></span></span> </dl>    | <span data-ttu-id="71b2c-140">! s & d</span><span class="sxs-lookup"><span data-stu-id="71b2c-140">!s & d</span></span><br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <span data-ttu-id="71b2c-141"><dt>**GL \_ oder \_ umgekehrt**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-141"><dt>**GL\_OR\_REVERSE**</dt></span></span> </dl>          | <span data-ttu-id="71b2c-142">s \| ! d</span><span class="sxs-lookup"><span data-stu-id="71b2c-142">s \| !d</span></span><br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <span data-ttu-id="71b2c-143"><dt>**GL \_ oder \_ invertiert**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-143"><dt>**GL\_OR\_INVERTED**</dt></span></span> </dl>       | <span data-ttu-id="71b2c-144">! s \| d</span><span class="sxs-lookup"><span data-stu-id="71b2c-144">!s \| d</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71b2c-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71b2c-145">Return value</span></span>

<span data-ttu-id="71b2c-146">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="71b2c-146">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71b2c-147">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="71b2c-147">Error codes</span></span>

<span data-ttu-id="71b2c-148">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="71b2c-148">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71b2c-149">Name</span><span class="sxs-lookup"><span data-stu-id="71b2c-149">Name</span></span>                                                                                                  | <span data-ttu-id="71b2c-150">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="71b2c-150">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71b2c-151"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-151"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="71b2c-152">*Opcode* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="71b2c-152">*opcode* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="71b2c-153"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71b2c-154">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="71b2c-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="71b2c-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71b2c-155">Remarks</span></span>

<span data-ttu-id="71b2c-156">Die Funktion " **gllogicop** " gibt eine logische Operation an, die bei Aktivierung zwischen dem eingehenden Farb Index und dem Farb Index an der entsprechenden Position im Framebuffer angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="71b2c-156">The **glLogicOp** function specifies a logical operation that, when enabled, is applied between the incoming color index and the color index at the corresponding location in the framebuffer.</span></span> <span data-ttu-id="71b2c-157">Die logische Operation wird mit " [**glEnable**](glenable.md) " und " **glEnable** " mithilfe der symbolischen Konstante "GL Logic op" aktiviert oder deaktiviert \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="71b2c-157">The logical operation is enabled or disabled with [**glEnable**](glenable.md) and **glDisable** using the symbolic constant GL\_LOGIC\_OP.</span></span>

<span data-ttu-id="71b2c-158">Der *Opcode* -Parameter ist eine symbolische Konstante, die aus der nachstehenden Liste ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="71b2c-158">The *opcode* parameter is a symbolic constant chosen from the list below.</span></span> <span data-ttu-id="71b2c-159">In der Erläuterung der logischen Vorgänge stellt *s* den eingehenden Farbindex und *d* den Index im Framebuffer dar.</span><span class="sxs-lookup"><span data-stu-id="71b2c-159">In the explanation of the logical operations, *s* represents the incoming color index and *d* represents the index in the framebuffer.</span></span> <span data-ttu-id="71b2c-160">Standard-C-sprach Operatoren werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="71b2c-160">Standard C-language operators are used.</span></span> <span data-ttu-id="71b2c-161">Wie diese bitweisen Operatoren vorschlagen, wird die logische Operation unabhängig von jedem bitpaar der Quell-und Ziel Indizes angewendet.</span><span class="sxs-lookup"><span data-stu-id="71b2c-161">As these bitwise operators suggest, the logical operation is applied independently to each bit pair of the source and destination indexes.</span></span>

<span data-ttu-id="71b2c-162">Logische Pixel Vorgänge werden nicht auf RGBA-Farb Puffer angewendet.</span><span class="sxs-lookup"><span data-stu-id="71b2c-162">Logical pixel operations are not applied to RGBA color buffers.</span></span>

<span data-ttu-id="71b2c-163">Wenn mehr als ein Farb Index Puffer für das Zeichnen aktiviert ist, werden logische Vorgänge für jeden aktivierten Puffer separat durchgeführt, wobei der Inhalt dieses Puffers für den Zielindex verwendet wird (siehe [**gldrawbuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="71b2c-163">When more than one color-index buffer is enabled for drawing, logical operations are done separately for each enabled buffer, using the contents of that buffer for the destination index (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span>

<span data-ttu-id="71b2c-164">Der *Opcode* -Parameter muss einer der 16 akzeptierten Werte sein.</span><span class="sxs-lookup"><span data-stu-id="71b2c-164">The *opcode* parameter must be one of the 16 accepted values.</span></span> <span data-ttu-id="71b2c-165">Andere Werte führen zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="71b2c-165">Other values result in an error.</span></span>

<span data-ttu-id="71b2c-166">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **gllogicop** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="71b2c-166">The following functions retrieve information related to **glLogicOp**:</span></span>

<span data-ttu-id="71b2c-167">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Logic \_ op \_ Mode</span><span class="sxs-lookup"><span data-stu-id="71b2c-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LOGIC\_OP\_MODE</span></span>

<span data-ttu-id="71b2c-168">[**glisenabled**](glisenabled.md) mit dem Argument GL \_ Logic \_ op</span><span class="sxs-lookup"><span data-stu-id="71b2c-168">[**glIsEnabled**](glisenabled.md) with argument GL\_LOGIC\_OP</span></span>

## <a name="requirements"></a><span data-ttu-id="71b2c-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71b2c-169">Requirements</span></span>



| <span data-ttu-id="71b2c-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71b2c-170">Requirement</span></span> | <span data-ttu-id="71b2c-171">Wert</span><span class="sxs-lookup"><span data-stu-id="71b2c-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71b2c-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71b2c-172">Minimum supported client</span></span><br/> | <span data-ttu-id="71b2c-173">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71b2c-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71b2c-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71b2c-174">Minimum supported server</span></span><br/> | <span data-ttu-id="71b2c-175">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71b2c-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71b2c-176">Header</span><span class="sxs-lookup"><span data-stu-id="71b2c-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b2c-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71b2c-178">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71b2c-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="71b2c-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71b2c-180">DLL</span><span class="sxs-lookup"><span data-stu-id="71b2c-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71b2c-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71b2c-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b2c-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71b2c-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b2c-183">**glalphafunc**</span><span class="sxs-lookup"><span data-stu-id="71b2c-183">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="71b2c-184">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="71b2c-184">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71b2c-185">**glblendfunc**</span><span class="sxs-lookup"><span data-stu-id="71b2c-185">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="71b2c-186">**gldrawbuffer**</span><span class="sxs-lookup"><span data-stu-id="71b2c-186">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="71b2c-187">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="71b2c-187">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="71b2c-188">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="71b2c-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71b2c-189">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="71b2c-189">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="71b2c-190">**glstencilop**</span><span class="sxs-lookup"><span data-stu-id="71b2c-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





