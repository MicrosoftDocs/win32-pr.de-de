---
title: glnewlist-Funktion (GL. h)
description: Die Funktionen "glnewlist" und "glendlist" erstellen oder ersetzen eine Anzeigeliste. | glnewlist-Funktion (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- glnewlist-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366600"
---
# <a name="glnewlist-function"></a><span data-ttu-id="f7b98-105">glnewlist-Funktion</span><span class="sxs-lookup"><span data-stu-id="f7b98-105">glNewList function</span></span>

<span data-ttu-id="f7b98-106">Die Funktionen " **glnewlist** " und " [**glendlist**](glendlist.md) " erstellen oder ersetzen eine Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="f7b98-106">The **glNewList** and [**glEndList**](glendlist.md) functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b98-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7b98-107">Syntax</span></span>


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="f7b98-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7b98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b98-109">*list*</span><span class="sxs-lookup"><span data-stu-id="f7b98-109">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b98-110">Der Name der Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="f7b98-110">The display list name.</span></span>

</dd> <dt>

<span data-ttu-id="f7b98-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="f7b98-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b98-112">Der Kompilierungs Modus.</span><span class="sxs-lookup"><span data-stu-id="f7b98-112">The compilation mode.</span></span> <span data-ttu-id="f7b98-113">Die folgenden Werte werden akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f7b98-113">The following values are accepted.</span></span>



| <span data-ttu-id="f7b98-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f7b98-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="f7b98-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f7b98-115">Meaning</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <span data-ttu-id="f7b98-116"><dt>**GL- \_ Kompilierung**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b98-116"><dt>**GL\_COMPILE**</dt></span></span> </dl>                                       | <span data-ttu-id="f7b98-117">Befehle werden lediglich kompiliert.</span><span class="sxs-lookup"><span data-stu-id="f7b98-117">Commands are merely compiled.</span></span><br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <span data-ttu-id="f7b98-118"><dt>**GL \_ -Kompilierung \_ und- \_ Ausführung**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b98-118"><dt>**GL\_COMPILE\_AND\_EXECUTE**</dt></span></span> </dl> | <span data-ttu-id="f7b98-119">Befehle werden ausgeführt, wenn Sie in die Anzeigeliste kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="f7b98-119">Commands are executed as they are compiled into the display list.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b98-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7b98-120">Return value</span></span>

<span data-ttu-id="f7b98-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f7b98-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7b98-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f7b98-122">Error codes</span></span>

<span data-ttu-id="f7b98-123">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f7b98-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f7b98-124">Name</span><span class="sxs-lookup"><span data-stu-id="f7b98-124">Name</span></span>                                                                                                  | <span data-ttu-id="f7b98-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f7b98-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7b98-126"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b98-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="f7b98-127">die *Liste* war NULL.</span><span class="sxs-lookup"><span data-stu-id="f7b98-127">*list* was zero.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="f7b98-128"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b98-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f7b98-129">der *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="f7b98-129">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="f7b98-130"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b98-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f7b98-131">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f7b98-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f7b98-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7b98-132">Remarks</span></span>

<span data-ttu-id="f7b98-133">Anzeigelisten sind Gruppen von OpenGL-Befehlen, die für die nachfolgende Ausführung gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="f7b98-133">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="f7b98-134">Die Anzeigelisten werden mit " **glnewlist**" erstellt.</span><span class="sxs-lookup"><span data-stu-id="f7b98-134">The display lists are created with **glNewList**.</span></span> <span data-ttu-id="f7b98-135">Alle nachfolgenden Befehle werden in der Anzeigeliste in der ausgestellten Reihenfolge abgelegt, bis **glendlist** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f7b98-135">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="f7b98-136">Die **glnewlist** -Funktion verfügt über zwei Parameter.</span><span class="sxs-lookup"><span data-stu-id="f7b98-136">The **glNewList** function has two parameters.</span></span> <span data-ttu-id="f7b98-137">Der erste Parameter *List* ist eine positive ganze Zahl, die zum eindeutigen Namen für die Anzeigeliste wird.</span><span class="sxs-lookup"><span data-stu-id="f7b98-137">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="f7b98-138">Namen können mit " [**glgenlists**](glgenlists.md) " erstellt und reserviert und auf Eindeutigkeit mit " [**glislist**](glislist.md)" getestet werden.</span><span class="sxs-lookup"><span data-stu-id="f7b98-138">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="f7b98-139">Der zweite Parameter, der- *Modus*, ist eine symbolische Konstante, die einen der beiden vorangehenden Werte annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="f7b98-139">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="f7b98-140">Bestimmte Befehle werden nicht in die Anzeigeliste kompiliert, sondern sofort ausgeführt, unabhängig vom Anzeigelisten Modus.</span><span class="sxs-lookup"><span data-stu-id="f7b98-140">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="f7b98-141">Diese Befehle sind " [**glcolorpointer**](glcolorpointer.md)", " [**gldelta etelists**](gldeletelists.md)", " [**gldisableclientstate**](gldisableclientstate.md)", " [**gledgeflagpointer**](gledgeflagpointer.md)", " [**glenableclientstate**](glenableclientstate.md)", " [**glfeedbackbuffer**](glfeedbackbuffer.md) [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", " [**glfinish**](glfinish.md)" [**, "**](glgenlists.md) [**glflush**](glflush.md)" " [**glindexpointer**](glindexpointer.md)", " [**glinterleavedarrays**](glinterleavedarrays.md)", " [**glisenabled**](glisenabled.md)", " [**glislist**](glislist.md)", " [**glnormalpointer**](glnormalpointer.md)", " [**glpopclientatlab**](glpopclientattrib.md)", " [**glpixelstore**](glpixelstore-functions.md)", " [**glpushclientatpub**](glpushclientattrib.md)", " [**gllesepixels**](glreadpixels.md)", " [**glrendermode**](glrendermode.md)", " [**glselectbuffer**](glselectbuffer.md) [**",**](glvertexpointer.md) [**"GL**](gltexcoordpointer.md)</span><span class="sxs-lookup"><span data-stu-id="f7b98-141">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="f7b98-142">Ebenso werden [**glTexImage2D**](glteximage2d.md) und [**glTexImage1D**](glteximage1d.md) sofort ausgeführt und nicht in die Anzeigeliste kompiliert, wenn Ihr erstes Argument die GL \_ \_ -Proxy Textur \_ 2D bzw. die GL \_ -Proxy \_ Textur \_ 1D ist.</span><span class="sxs-lookup"><span data-stu-id="f7b98-142">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="f7b98-143">Wenn die Funktion " **glendlist** " gefunden wird, wird die Definition der Anzeigeliste abgeschlossen, indem die Liste mit der eindeutigen namens *Liste* verknüpft wird (angegeben im Befehl " **glnewlist** ").</span><span class="sxs-lookup"><span data-stu-id="f7b98-143">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the **glNewList** command).</span></span> <span data-ttu-id="f7b98-144">Wenn eine Anzeigeliste mit der namens *Liste* bereits vorhanden ist, wird Sie nur ersetzt, wenn " **glendlist** " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f7b98-144">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="f7b98-145">Die Funktionen " [**glCallList**](glcalllist.md) " und " [**glcalllists**](glcalllists.md) " können in Anzeigelisten eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7b98-145">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="f7b98-146">Die Befehle in der Anzeigeliste oder Listen, die von **glCallList** oder **glcalllists** ausgeführt werden, sind nicht in der erstellten Anzeigeliste enthalten, auch wenn der Listen Erstellungs Modus "GL Compile" und "Execute" lautet \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f7b98-146">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="f7b98-147">Die folgende Funktion Ruft Informationen im Zusammenhang mit **glnewlist** ab:</span><span class="sxs-lookup"><span data-stu-id="f7b98-147">The following function retrieves information related to **glNewList**:</span></span>

<span data-ttu-id="f7b98-148">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="f7b98-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b98-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7b98-149">Requirements</span></span>



| <span data-ttu-id="f7b98-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7b98-150">Requirement</span></span> | <span data-ttu-id="f7b98-151">Wert</span><span class="sxs-lookup"><span data-stu-id="f7b98-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b98-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7b98-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b98-153">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7b98-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f7b98-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7b98-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b98-155">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7b98-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7b98-156">Header</span><span class="sxs-lookup"><span data-stu-id="f7b98-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b98-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b98-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f7b98-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f7b98-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7b98-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7b98-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7b98-160">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b98-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b98-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b98-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b98-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7b98-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b98-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f7b98-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f7b98-164">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="f7b98-164">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="f7b98-165">**glcalllists**</span><span class="sxs-lookup"><span data-stu-id="f7b98-165">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="f7b98-166">**gldelta etelists**</span><span class="sxs-lookup"><span data-stu-id="f7b98-166">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="f7b98-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f7b98-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f7b98-168">**glendlist**</span><span class="sxs-lookup"><span data-stu-id="f7b98-168">**glEndList**</span></span>](glendlist.md)
</dt> <dt>

[<span data-ttu-id="f7b98-169">**glgenlists**</span><span class="sxs-lookup"><span data-stu-id="f7b98-169">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="f7b98-170">**glislist**</span><span class="sxs-lookup"><span data-stu-id="f7b98-170">**glIsList**</span></span>](glislist.md)
</dt> </dl>

 

 





