---
title: glrendermode-Funktion (GL. h)
description: Die glrendermode-Funktion legt den rasterisierungsmodus fest.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- glrendermode-Funktion OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106197"
---
# <a name="glrendermode-function"></a><span data-ttu-id="58277-104">glrendermode-Funktion</span><span class="sxs-lookup"><span data-stu-id="58277-104">glRenderMode function</span></span>

<span data-ttu-id="58277-105">Die **glrendermode** -Funktion legt den rasterisierungsmodus fest.</span><span class="sxs-lookup"><span data-stu-id="58277-105">The **glRenderMode** function sets the rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="58277-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="58277-106">Syntax</span></span>


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="58277-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="58277-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58277-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="58277-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="58277-109">Der rasterisierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="58277-109">The rasterization mode.</span></span> <span data-ttu-id="58277-110">Die folgenden drei Werte werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="58277-110">The following three values are accepted.</span></span> <span data-ttu-id="58277-111">Der Standardwert ist GL- \_ Rendering.</span><span class="sxs-lookup"><span data-stu-id="58277-111">The default value is GL\_RENDER.</span></span>



| <span data-ttu-id="58277-112">Wert</span><span class="sxs-lookup"><span data-stu-id="58277-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="58277-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="58277-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <span data-ttu-id="58277-114"><dt>**GL- \_ Rendering**</dt></span><span class="sxs-lookup"><span data-stu-id="58277-114"><dt>**GL\_RENDER**</dt></span></span> </dl>       | <span data-ttu-id="58277-115">Rendermodus.</span><span class="sxs-lookup"><span data-stu-id="58277-115">Render mode.</span></span> <span data-ttu-id="58277-116">Primitive sind rasterisiert und erzeugen Pixel Fragmente, die in den Framebuffer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="58277-116">Primitives are rasterized, producing pixel fragments, which are written into the framebuffer.</span></span> <span data-ttu-id="58277-117">Dies ist der normale Modus und auch der Standardmodus.</span><span class="sxs-lookup"><span data-stu-id="58277-117">This is the normal mode and also the default mode.</span></span><br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <span data-ttu-id="58277-118"><dt>**GL \_ auswählen**</dt></span><span class="sxs-lookup"><span data-stu-id="58277-118"><dt>**GL\_SELECT**</dt></span></span> </dl>       | <span data-ttu-id="58277-119">Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="58277-119">Selection mode.</span></span> <span data-ttu-id="58277-120">Es werden keine Pixel Fragmente erstellt, und es wird keine Änderung am Frame Puffer-Inhalt vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="58277-120">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="58277-121">Stattdessen wird ein Datensatz der Namen primitiver Elemente, die gezeichnet würden, wenn der Rendermodus "GL-Rendering" wäre \_ , in einem SELECT-Puffer zurückgegeben, der erstellt werden muss (siehe [**glselectbuffer**](glselectbuffer.md)), bevor der Auswahlmodus eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="58277-121">Instead, a record of the names of primitives that would have been drawn if the render mode was GL\_RENDER is returned in a select buffer, which must be created (see [**glSelectBuffer**](glselectbuffer.md)) before selection mode is entered.</span></span><br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <span data-ttu-id="58277-122"><dt>**GL- \_ Feedback**</dt></span><span class="sxs-lookup"><span data-stu-id="58277-122"><dt>**GL\_FEEDBACK**</dt></span></span> </dl> | <span data-ttu-id="58277-123">Feedback Modus.</span><span class="sxs-lookup"><span data-stu-id="58277-123">Feedback mode.</span></span> <span data-ttu-id="58277-124">Es werden keine Pixel Fragmente erstellt, und es wird keine Änderung am Frame Puffer-Inhalt vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="58277-124">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="58277-125">Stattdessen werden die Koordinaten und Attribute von Vertices, die gezeichnet würden, wenn der Rendermodus "GL-Rendering" wäre \_ , in einem Feedback Puffer zurückgegeben, der erstellt werden muss (siehe [**glfeedbackbuffer**](glfeedbackbuffer.md)), bevor der Feedback Modus eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="58277-125">Instead, the coordinates and attributes of vertices that would have been drawn had the render mode been GL\_RENDER are returned in a feedback buffer, which must be created (see [**glFeedbackBuffer**](glfeedbackbuffer.md)) before feedback mode is entered.</span></span><br/> |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="58277-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="58277-126">Error codes</span></span>

<span data-ttu-id="58277-127">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="58277-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="58277-128">Name</span><span class="sxs-lookup"><span data-stu-id="58277-128">Name</span></span>                                                                                                  | <span data-ttu-id="58277-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="58277-129">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58277-130"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58277-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="58277-131">der *Modus* war keiner von drei akzeptierten Werten.</span><span class="sxs-lookup"><span data-stu-id="58277-131">*mode* was not one of three accepted values.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="58277-132"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="58277-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="58277-133">Die Funktion wurde mit dem Argument GL \_ SELECT aufgerufen, bevor [**glselectbuffer**](glselectbuffer.md) mindestens einmal aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="58277-133">The function was called with argument GL\_SELECT before [**glSelectBuffer**](glselectbuffer.md) was called at least once.</span></span><br/>       |
| <dl> <span data-ttu-id="58277-134"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="58277-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="58277-135">Die Funktion wurde mit dem Argument GL \_ Feedback aufgerufen, bevor [**glbeedbackbuffer**](glfeedbackbuffer.md) mindestens einmal aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="58277-135">The function was called with argument GL\_FEEDBACK before [**glBeedbackBuffer**](glfeedbackbuffer.md) was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="58277-136"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="58277-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="58277-137">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="58277-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="58277-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58277-138">Remarks</span></span>

<span data-ttu-id="58277-139">Die Funktion " **glrendermode** " erfordert ein *Argument, das* einen von drei vordefinierten Werten annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="58277-139">The **glRenderMode** function takes one argument, *mode*, which can assume one of three predefined values above.</span></span>

<span data-ttu-id="58277-140">Der Rückgabewert der Funktion " **glrendermode** " wird durch den Rendermodus zum Zeitpunkt des Aufrufs von " **glrendermode** " und nicht durch den *Modus* bestimmt.</span><span class="sxs-lookup"><span data-stu-id="58277-140">The return value of the **glRenderMode** function is determined by the render mode at the time **glRenderMode** is called, rather than by *mode*.</span></span> <span data-ttu-id="58277-141">Die folgenden Werte werden für die drei Rendermodi zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="58277-141">The values returned for the three render modes are as follows.</span></span>



| <span data-ttu-id="58277-142">Wert</span><span class="sxs-lookup"><span data-stu-id="58277-142">Value</span></span>        | <span data-ttu-id="58277-143">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="58277-143">Meaning</span></span>                                                                 |
|--------------|-------------------------------------------------------------------------|
| <span data-ttu-id="58277-144">GL- \_ Rendering</span><span class="sxs-lookup"><span data-stu-id="58277-144">GL\_RENDER</span></span>   | <span data-ttu-id="58277-145">Keinen.</span><span class="sxs-lookup"><span data-stu-id="58277-145">Zero.</span></span>                                                                   |
| <span data-ttu-id="58277-146">GL \_ auswählen</span><span class="sxs-lookup"><span data-stu-id="58277-146">GL\_SELECT</span></span>   | <span data-ttu-id="58277-147">Die Anzahl der Treffer Datensätze, die an den ausgewählten Puffer übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="58277-147">The number of hit records transferred to the select buffer.</span></span>             |
| <span data-ttu-id="58277-148">GL- \_ Feedback</span><span class="sxs-lookup"><span data-stu-id="58277-148">GL\_FEEDBACK</span></span> | <span data-ttu-id="58277-149">Die Anzahl der Werte (keine Scheitel Punkte), die in den Feedback Puffer übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="58277-149">The number of values (not vertices) transferred to the feedback buffer.</span></span> |



 

<span data-ttu-id="58277-150">Weitere Informationen zum Vorgang zur Auswahl und zum Feedback finden Sie unter " [**glselectbuffer**](glselectbuffer.md) " und " [**glfeedbackbuffer**](glfeedbackbuffer.md) ".</span><span class="sxs-lookup"><span data-stu-id="58277-150">Refer to [**glSelectBuffer**](glselectbuffer.md) and [**glFeedbackBuffer**](glfeedbackbuffer.md) for more details concerning selection and feedback operation.</span></span>

<span data-ttu-id="58277-151">Wenn ein Fehler generiert wird, gibt **glrendermode unabhängig vom aktuellen Rendermodus** 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="58277-151">If an error is generated, **glRenderMode** returns zero regardless of the current render mode.</span></span>

<span data-ttu-id="58277-152">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glrendermode** ab:</span><span class="sxs-lookup"><span data-stu-id="58277-152">The following function retrieves information related to **glRenderMode**:</span></span>

<span data-ttu-id="58277-153">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ \_ Rendermodus</span><span class="sxs-lookup"><span data-stu-id="58277-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="58277-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58277-154">Requirements</span></span>



| <span data-ttu-id="58277-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58277-155">Requirement</span></span> | <span data-ttu-id="58277-156">Wert</span><span class="sxs-lookup"><span data-stu-id="58277-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58277-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58277-157">Minimum supported client</span></span><br/> | <span data-ttu-id="58277-158">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58277-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="58277-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58277-159">Minimum supported server</span></span><br/> | <span data-ttu-id="58277-160">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58277-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58277-161">Header</span><span class="sxs-lookup"><span data-stu-id="58277-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="58277-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="58277-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="58277-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="58277-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="58277-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58277-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="58277-165">DLL</span><span class="sxs-lookup"><span data-stu-id="58277-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58277-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58277-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58277-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58277-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58277-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="58277-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="58277-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="58277-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="58277-170">**glfeedbackbuffer**</span><span class="sxs-lookup"><span data-stu-id="58277-170">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="58277-171">**glinitnames**</span><span class="sxs-lookup"><span data-stu-id="58277-171">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="58277-172">**glloadname**</span><span class="sxs-lookup"><span data-stu-id="58277-172">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="58277-173">**glpassthrough**</span><span class="sxs-lookup"><span data-stu-id="58277-173">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="58277-174">**glpushname**</span><span class="sxs-lookup"><span data-stu-id="58277-174">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="58277-175">**glselectbuffer**</span><span class="sxs-lookup"><span data-stu-id="58277-175">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





