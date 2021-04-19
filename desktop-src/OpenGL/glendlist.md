---
title: glendlist-Funktion (GL. h)
description: Die Funktionen "glnewlist" und "glendlist" erstellen oder ersetzen eine Anzeigeliste. | glendlist-Funktion (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- glendlist-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363094"
---
# <a name="glendlist-function"></a><span data-ttu-id="cd3c7-105">glendlist-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd3c7-105">glEndList function</span></span>

<span data-ttu-id="cd3c7-106">Die Funktionen " [**glnewlist**](glnewlist.md) " und " **glendlist** " erstellen oder ersetzen eine Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-106">The [**glNewList**](glnewlist.md) and **glEndList** functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd3c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd3c7-107">Syntax</span></span>


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a><span data-ttu-id="cd3c7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd3c7-108">Parameters</span></span>

<span data-ttu-id="cd3c7-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd3c7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd3c7-110">Return value</span></span>

<span data-ttu-id="cd3c7-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cd3c7-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cd3c7-112">Error codes</span></span>

<span data-ttu-id="cd3c7-113">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cd3c7-114">Name</span><span class="sxs-lookup"><span data-stu-id="cd3c7-114">Name</span></span>                                                                                                  | <span data-ttu-id="cd3c7-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cd3c7-115">Meaning</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd3c7-116"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="cd3c7-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cd3c7-117">" **glendlist** " wurde ohne vorherige " **glnewlist**" aufgerufen, oder, wenn " **glnewlist** " aufgerufen wurde, während eine Anzeigeliste definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-117">**glEndList** was called without a preceding **glNewList**, or if **glnewlist** was called while a display list was being defined.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cd3c7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd3c7-118">Remarks</span></span>

<span data-ttu-id="cd3c7-119">Anzeigelisten sind Gruppen von OpenGL-Befehlen, die für die nachfolgende Ausführung gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-119">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="cd3c7-120">Die Anzeigelisten werden mit " [**glnewlist**](glnewlist.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-120">The display lists are created with [**glNewList**](glnewlist.md).</span></span> <span data-ttu-id="cd3c7-121">Alle nachfolgenden Befehle werden in der Anzeigeliste in der ausgestellten Reihenfolge abgelegt, bis **glendlist** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-121">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="cd3c7-122">Die [**glnewlist**](glnewlist.md) -Funktion verfügt über zwei Parameter.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-122">The [**glNewList**](glnewlist.md) function has two parameters.</span></span> <span data-ttu-id="cd3c7-123">Der erste Parameter *List* ist eine positive ganze Zahl, die zum eindeutigen Namen für die Anzeigeliste wird.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-123">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="cd3c7-124">Namen können mit " [**glgenlists**](glgenlists.md) " erstellt und reserviert und auf Eindeutigkeit mit " [**glislist**](glislist.md)" getestet werden.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-124">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="cd3c7-125">Der zweite Parameter, der- *Modus*, ist eine symbolische Konstante, die einen der beiden vorangehenden Werte annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-125">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="cd3c7-126">Bestimmte Befehle werden nicht in die Anzeigeliste kompiliert, sondern sofort ausgeführt, unabhängig vom Anzeigelisten Modus.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-126">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="cd3c7-127">Diese Befehle sind " [**glcolorpointer**](glcolorpointer.md)", " [**gldelta etelists**](gldeletelists.md)", " [**gldisableclientstate**](gldisableclientstate.md)", " [**gledgeflagpointer**](gledgeflagpointer.md)", " [**glenableclientstate**](glenableclientstate.md)", " [**glfeedbackbuffer**](glfeedbackbuffer.md) [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", " [**glfinish**](glfinish.md)" [**, "**](glgenlists.md) [**glflush**](glflush.md)" " [**glindexpointer**](glindexpointer.md)", " [**glinterleavedarrays**](glinterleavedarrays.md)", " [**glisenabled**](glisenabled.md)", " [**glislist**](glislist.md)", " [**glnormalpointer**](glnormalpointer.md)", " [**glpopclientatlab**](glpopclientattrib.md)", " [**glpixelstore**](glpixelstore-functions.md)", " [**glpushclientatpub**](glpushclientattrib.md)", " [**gllesepixels**](glreadpixels.md)", " [**glrendermode**](glrendermode.md)", " [**glselectbuffer**](glselectbuffer.md) [**",**](glvertexpointer.md) [**"GL**](gltexcoordpointer.md)</span><span class="sxs-lookup"><span data-stu-id="cd3c7-127">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="cd3c7-128">Ebenso werden [**glTexImage2D**](glteximage2d.md) und [**glTexImage1D**](glteximage1d.md) sofort ausgeführt und nicht in die Anzeigeliste kompiliert, wenn Ihr erstes Argument die GL \_ \_ -Proxy Textur \_ 2D bzw. die GL \_ -Proxy \_ Textur \_ 1D ist.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-128">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="cd3c7-129">Wenn die Funktion " **glendlist** " gefunden wird, wird die Definition der Anzeigeliste abgeschlossen, indem die Liste mit der eindeutigen namens *Liste* verknüpft wird (angegeben im Befehl " [**glnewlist**](glnewlist.md) ").</span><span class="sxs-lookup"><span data-stu-id="cd3c7-129">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the [**glNewList**](glnewlist.md) command).</span></span> <span data-ttu-id="cd3c7-130">Wenn eine Anzeigeliste mit der namens *Liste* bereits vorhanden ist, wird Sie nur ersetzt, wenn " **glendlist** " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-130">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="cd3c7-131">Die Funktionen " [**glCallList**](glcalllist.md) " und " [**glcalllists**](glcalllists.md) " können in Anzeigelisten eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cd3c7-131">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="cd3c7-132">Die Befehle in der Anzeigeliste oder Listen, die von **glCallList** oder **glcalllists** ausgeführt werden, sind nicht in der erstellten Anzeigeliste enthalten, auch wenn der Listen Erstellungs Modus "GL Compile" und "Execute" lautet \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cd3c7-132">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="cd3c7-133">Die folgende Funktion Ruft Informationen im Zusammenhang mit [**glnewlist**](glnewlist.md)ab:</span><span class="sxs-lookup"><span data-stu-id="cd3c7-133">The following function retrieves information related to [**glNewList**](glnewlist.md):</span></span>

<span data-ttu-id="cd3c7-134">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem-Argument des GL- \_ Matrix \_ Modus</span><span class="sxs-lookup"><span data-stu-id="cd3c7-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="cd3c7-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd3c7-135">Requirements</span></span>



| <span data-ttu-id="cd3c7-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd3c7-136">Requirement</span></span> | <span data-ttu-id="cd3c7-137">Wert</span><span class="sxs-lookup"><span data-stu-id="cd3c7-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd3c7-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd3c7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cd3c7-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd3c7-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cd3c7-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd3c7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cd3c7-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd3c7-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd3c7-142">Header</span><span class="sxs-lookup"><span data-stu-id="cd3c7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd3c7-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd3c7-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cd3c7-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cd3c7-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd3c7-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd3c7-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd3c7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="cd3c7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd3c7-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd3c7-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd3c7-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd3c7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd3c7-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cd3c7-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cd3c7-150">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="cd3c7-150">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="cd3c7-151">**glcalllists**</span><span class="sxs-lookup"><span data-stu-id="cd3c7-151">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="cd3c7-152">**gldelta etelists**</span><span class="sxs-lookup"><span data-stu-id="cd3c7-152">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="cd3c7-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cd3c7-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cd3c7-154">**glgenlists**</span><span class="sxs-lookup"><span data-stu-id="cd3c7-154">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="cd3c7-155">**glislist**</span><span class="sxs-lookup"><span data-stu-id="cd3c7-155">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="cd3c7-156">**glnewlist**</span><span class="sxs-lookup"><span data-stu-id="cd3c7-156">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





