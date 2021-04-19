---
title: gldrawbuffer-Funktion (GL. h)
description: Die gldrawbuffer-Funktion gibt an, in welche Farb Puffer gezeichnet werden soll.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- gldrawbuffer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341591"
---
# <a name="gldrawbuffer-function"></a><span data-ttu-id="b6b2b-104">gldrawbuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="b6b2b-104">glDrawBuffer function</span></span>

<span data-ttu-id="b6b2b-105">Die **gldrawbuffer** -Funktion gibt an, in welche Farb Puffer gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-105">The **glDrawBuffer** function specifies which color buffers are to be drawn into.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b2b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6b2b-106">Syntax</span></span>


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="b6b2b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6b2b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b2b-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="b6b2b-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b2b-109">Gibt bis zu vier Farb Puffer an, die in mit den folgenden akzeptablen symbolischen Konstanten gezeichnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-109">Specifies up to four color buffers to be drawn into with the following acceptable symbolic constants.</span></span>



| <span data-ttu-id="b6b2b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="b6b2b-110">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="b6b2b-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6b2b-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <span data-ttu-id="b6b2b-112"><dt>**GL \_ keine**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-112"><dt>**GL\_NONE**</dt></span></span> </dl>                                 | <span data-ttu-id="b6b2b-113">Es wurden keine Farb Puffer geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-113">No color buffers are written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <span data-ttu-id="b6b2b-114"><dt>**GL- \_ Front- \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-114"><dt>**GL\_FRONT\_LEFT**</dt></span></span> </dl>              | <span data-ttu-id="b6b2b-115">Nur der Front-Left-Farb Puffer wird geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-115">Only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <span data-ttu-id="b6b2b-116"><dt>**GL- \_ Front- \_ right**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-116"><dt>**GL\_FRONT\_RIGHT**</dt></span></span> </dl>           | <span data-ttu-id="b6b2b-117">Nur der Front-Right-Farb Puffer wird geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-117">Only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <span data-ttu-id="b6b2b-118"><dt>**GL \_ zurück \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-118"><dt>**GL\_BACK\_LEFT**</dt></span></span> </dl>                 | <span data-ttu-id="b6b2b-119">Nur der linke Farb Puffer wird geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-119">Only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <span data-ttu-id="b6b2b-120"><dt>**GL \_ zurück \_ Rechts**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-120"><dt>**GL\_BACK\_RIGHT**</dt></span></span> </dl>              | <span data-ttu-id="b6b2b-121">Nur der Hintergrund Farb Puffer wird geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-121">Only the back-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <span data-ttu-id="b6b2b-122"><dt>**GL. \_ Front**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-122"><dt>**GL\_FRONT**</dt></span></span> </dl>                              | <span data-ttu-id="b6b2b-123">Nur die Front-Left-und Front-Right-Farb Puffer werden geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-123">Only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="b6b2b-124">Wenn kein Vordergrund rechter Farb Puffer vorhanden ist, wird nur der vordere linke Farb Puffer geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-124">If there is no front-right color buffer, only the front left-color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <span data-ttu-id="b6b2b-125"><dt>**GL \_ zurück**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-125"><dt>**GL\_BACK**</dt></span></span> </dl>                                 | <span data-ttu-id="b6b2b-126">Es werden nur die Hintergrund-und Hintergrund Farb Puffer geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-126">Only the back-left and back-right color buffers are written.</span></span> <span data-ttu-id="b6b2b-127">Wenn kein Hintergrund Farb Puffer vorhanden ist, wird nur der Hintergrund Farb Puffer geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-127">If there is no back-right color buffer, only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <span data-ttu-id="b6b2b-128"><dt>**GL \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-128"><dt>**GL\_LEFT**</dt></span></span> </dl>                                 | <span data-ttu-id="b6b2b-129">Es werden nur die Vorder-und Hintergrundfarben geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-129">Only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="b6b2b-130">Wenn kein Hintergrund Farb Puffer vorhanden ist, wird nur der linke Farb Puffer in der Vorderseite geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-130">If there is no back-left color buffer, only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <span data-ttu-id="b6b2b-131"><dt>**GL \_ right**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-131"><dt>**GL\_RIGHT**</dt></span></span> </dl>                              | <span data-ttu-id="b6b2b-132">Es werden nur die Vorder-und Hintergrundfarben geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-132">Only the front-right and back-right color buffers are written.</span></span> <span data-ttu-id="b6b2b-133">Wenn kein Hintergrund Farb Puffer vorhanden ist, wird nur der Front-Right-Farb Puffer geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-133">If there is no back-right color buffer, only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <span data-ttu-id="b6b2b-134"><dt>**GL \_ vor \_ und \_ zurück**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-134"><dt>**GL\_FRONT\_AND\_BACK**</dt></span></span> </dl> | <span data-ttu-id="b6b2b-135">Alle Vorder-und Hintergrund Farbpuffer (Front-Left, Front-Right, Back-Left, Back-right) werden geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-135">All the front and back color buffers (front-left, front-right, back-left, back-right) are written.</span></span> <span data-ttu-id="b6b2b-136">Wenn keine Hintergrundfarben vorhanden sind, werden nur die Front-Left-und Front-Right-Farb Puffer geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-136">If there are no back color buffers, only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="b6b2b-137">Wenn keine rechten Farb Puffer vorhanden sind, werden nur die Front-Left-und Back-Left-Farb Puffer geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-137">If there are no right color buffers, only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="b6b2b-138">Wenn keine Rechte oder Hintergrundfarben Puffer vorhanden sind, wird nur der linke Farb Puffer in der Vorderseite geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-138">If there are no right or back color buffers, only the front-left color buffer is written.</span></span><br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <span data-ttu-id="b6b2b-139"><dt>**GL \_ Auxi**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-139"><dt>**GL\_AUXi**</dt></span></span> </dl>       | <span data-ttu-id="b6b2b-140">Nur der Zusatz Farb Puffer, den *ich geschrieben habe* . der *Wert liegt zwischen* 0 und GL, \_ aux \_ -Puffer-1.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-140">Only the auxiliary color buffer *i* is written; *i* is between 0 and GL\_AUX\_BUFFERS - 1.</span></span> <span data-ttu-id="b6b2b-141">(GL \_ AUX- \_ Puffer ist nicht die Obergrenze. verwenden Sie " [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", um die Anzahl der verfügbaren zusätzlichen Puffer abzufragen.)</span><span class="sxs-lookup"><span data-stu-id="b6b2b-141">(GL\_AUX\_BUFFERS is not the upper limit; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to query the number of available auxiliary buffers.)</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="b6b2b-142">Der Standardwert ist "GL \_ Front" für Einzel gepufferte Kontexte und "GL \_ Back" für doppelt gepufferte Kontexte.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-142">The default value is GL\_FRONT for single-buffered contexts, and GL\_BACK for double-buffered contexts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b2b-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6b2b-143">Return value</span></span>

<span data-ttu-id="b6b2b-144">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b6b2b-145">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b6b2b-145">Error codes</span></span>

<span data-ttu-id="b6b2b-146">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b6b2b-147">Name</span><span class="sxs-lookup"><span data-stu-id="b6b2b-147">Name</span></span>                                                                                                  | <span data-ttu-id="b6b2b-148">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6b2b-148">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6b2b-149"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-149"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b6b2b-150">der *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-150">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="b6b2b-151"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b6b2b-152">Keiner der durch den *Modus* gekennzeichneten Puffer war vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-152">None of the buffers indicated by *mode* existed.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="b6b2b-153"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b6b2b-154">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |


## <a name="remarks"></a><span data-ttu-id="b6b2b-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6b2b-155">Remarks</span></span>

<span data-ttu-id="b6b2b-156">Wenn Farben in den Framebuffer geschrieben werden, werden Sie in die von **gldrawbuffer** angegebenen Farb Puffer geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-156">When colors are written to the framebuffer, they are written into the color buffers specified by **glDrawBuffer**.</span></span>

<span data-ttu-id="b6b2b-157">Wenn mehr als ein Farb Puffer zum Zeichnen ausgewählt ist, werden Mischungs-oder logische Operationen berechnet und für jeden Farb Puffer unabhängig voneinander angewendet und können in jedem Puffer zu unterschiedlichen Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-157">If more than one color buffer is selected for drawing, then blending or logical operations are computed and applied independently for each color buffer and can produce different results in each buffer.</span></span>

<span data-ttu-id="b6b2b-158">Zu den monetischen Kontexten zählen nur linke Puffer, und stereoskopischen Kontexte enthalten sowohl den linken als auch den rechten Puffer.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-158">Monoscopic contexts include only left buffers, and stereoscopic contexts include both left and right buffers.</span></span> <span data-ttu-id="b6b2b-159">Ebenso umfassen Einzel gepufferte Kontexte nur Front-Puffer, und doppelt gepufferte Kontexte enthalten sowohl den vorderen als auch den Hintergrund Puffer.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-159">Likewise, single-buffered contexts include only front buffers, and double-buffered contexts include both front and back buffers.</span></span> <span data-ttu-id="b6b2b-160">Der Kontext wird bei der OpenGL-Initialisierung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-160">The context is selected at OpenGL initialization.</span></span>

<span data-ttu-id="b6b2b-161">Es ist immer der Fall, dass GL \_ aux *i* = GL \_ AUX0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="b6b2b-161">It is always the case that GL\_AUX *i* = GL\_AUX0 + *i*.</span></span>

<span data-ttu-id="b6b2b-162">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **gldrawbuffer** " ab:</span><span class="sxs-lookup"><span data-stu-id="b6b2b-162">The following functions retrieve information related to the **glDrawBuffer** function:</span></span>

<span data-ttu-id="b6b2b-163">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Zeichnungs \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="b6b2b-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DRAW\_BUFFER</span></span>

<span data-ttu-id="b6b2b-164">**glget** mit dem Argument GL \_ aux- \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="b6b2b-164">**glGet** with argument GL\_AUX\_BUFFERS</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b2b-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6b2b-165">Requirements</span></span>



| <span data-ttu-id="b6b2b-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6b2b-166">Requirement</span></span> | <span data-ttu-id="b6b2b-167">Wert</span><span class="sxs-lookup"><span data-stu-id="b6b2b-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b2b-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6b2b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b2b-169">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6b2b-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b6b2b-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6b2b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b2b-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6b2b-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6b2b-172">Header</span><span class="sxs-lookup"><span data-stu-id="b6b2b-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b2b-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b6b2b-174">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b6b2b-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6b2b-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6b2b-176">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b2b-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b2b-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6b2b-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6b2b-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6b2b-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b2b-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b6b2b-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b6b2b-180">**glblendfunc**</span><span class="sxs-lookup"><span data-stu-id="b6b2b-180">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="b6b2b-181">**glcolormask**</span><span class="sxs-lookup"><span data-stu-id="b6b2b-181">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="b6b2b-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b6b2b-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b6b2b-183">**glget**</span><span class="sxs-lookup"><span data-stu-id="b6b2b-183">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b6b2b-184">**glindexmask**</span><span class="sxs-lookup"><span data-stu-id="b6b2b-184">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="b6b2b-185">**gllogicop**</span><span class="sxs-lookup"><span data-stu-id="b6b2b-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="b6b2b-186">**glread Buffer**</span><span class="sxs-lookup"><span data-stu-id="b6b2b-186">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> </dl>

 

 





