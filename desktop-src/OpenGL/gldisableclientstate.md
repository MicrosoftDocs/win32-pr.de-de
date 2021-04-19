---
title: gldisableclientstate-Funktion (GL. h)
description: Die Funktionen "glenableclientstate" und "gldisableclientstate" aktivieren bzw. deaktivieren Arrays. | gldisableclientstate-Funktion (GL. h)
ms.assetid: b3316519-00ed-45f8-9c4b-2e04c483751e
keywords:
- gldisableclientstate-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDisableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 163a7c3b679c979e5c800d2aa41ba2abb00e11f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350639"
---
# <a name="gldisableclientstate-function"></a><span data-ttu-id="f5731-105">gldisableclientstate-Funktion</span><span class="sxs-lookup"><span data-stu-id="f5731-105">glDisableClientState function</span></span>

<span data-ttu-id="f5731-106">Die Funktionen " [**glenableclientstate**](glenableclientstate.md) " und " **gldisableclientstate** " aktivieren bzw. deaktivieren Arrays.</span><span class="sxs-lookup"><span data-stu-id="f5731-106">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5731-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5731-107">Syntax</span></span>


```C++
void WINAPI glDisableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="f5731-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5731-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5731-109">*array*</span><span class="sxs-lookup"><span data-stu-id="f5731-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="f5731-110">Eine symbolische Konstante für das Array, das Sie aktivieren oder deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f5731-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="f5731-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="f5731-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="f5731-112">Wert</span><span class="sxs-lookup"><span data-stu-id="f5731-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="f5731-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f5731-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="f5731-114"><dt>**GL \_ - \_ Farbarray**</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="f5731-115">Wenn diese Option aktiviert ist, verwenden Sie Farb Arrays mit Aufrufen von [**glarrayelement**](glarrayelement.md), [**gldrawelements**](gldrawelements.md)oder [**gldrawarrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="f5731-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="f5731-116">Siehe auch [**glcolorpointer**](glcolorpointer.md).</span><span class="sxs-lookup"><span data-stu-id="f5731-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="f5731-117"><dt>**GL \_ - \_ edgeflag- \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="f5731-118">Wenn diese Option aktiviert ist, verwenden Sie Edge-Flag-Arrays mit Aufrufen von [**glarrayelement**](glarrayelement.md), [**gldrawelements**](gldrawelements.md)oder [**gldrawarrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="f5731-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="f5731-119">Siehe auch [**gledgeflagpointer**](gledgeflagpointer.md).</span><span class="sxs-lookup"><span data-stu-id="f5731-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="f5731-120"><dt>**GL- \_ Index \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="f5731-121">Wenn diese Option aktiviert ist, verwenden Sie Index Arrays mit Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md)".</span><span class="sxs-lookup"><span data-stu-id="f5731-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="f5731-122">Siehe auch [**glindexpointer**](glindexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="f5731-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="f5731-123"><dt>**GL- \_ normales \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="f5731-124">Wenn diese Option aktiviert ist, verwenden Sie normale Arrays mit Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md)".</span><span class="sxs-lookup"><span data-stu-id="f5731-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="f5731-125">Siehe auch [**glnormalpointer**](glnormalpointer.md).</span><span class="sxs-lookup"><span data-stu-id="f5731-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="f5731-126"><dt>**GL- \_ Textur \_ Koord- \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="f5731-127">Wenn diese Option aktiviert ist, verwenden Sie Texturkoordinaten Arrays mit Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md)".</span><span class="sxs-lookup"><span data-stu-id="f5731-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="f5731-128">Siehe auch [**gltexcoordpointer**](gltexcoordpointer.md).</span><span class="sxs-lookup"><span data-stu-id="f5731-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="f5731-129"><dt>**GL- \_ Scheitelpunkt \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="f5731-130">Wenn diese Option aktiviert ist, verwenden Sie Scheitelpunkt Arrays mit Aufrufen von [**glarrayelement**](glarrayelement.md), [**gldrawelements**](gldrawelements.md)oder [**gldrawarrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="f5731-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="f5731-131">Siehe auch [**glvertexpointer**](glvertexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="f5731-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5731-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5731-132">Return value</span></span>

<span data-ttu-id="f5731-133">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f5731-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f5731-134">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f5731-134">Error codes</span></span>

<span data-ttu-id="f5731-135">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f5731-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f5731-136">Name</span><span class="sxs-lookup"><span data-stu-id="f5731-136">Name</span></span>                                                                                             | <span data-ttu-id="f5731-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f5731-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="f5731-138"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="f5731-139">Das *Array* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="f5731-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f5731-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5731-140">Remarks</span></span>

<span data-ttu-id="f5731-141">Die Funktionen " [**glenableclientstate**](glenableclientstate.md) " und " **gldisableclientstate** " aktivieren und deaktivieren verschiedene individuelle Arrays.</span><span class="sxs-lookup"><span data-stu-id="f5731-141">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="f5731-142">Verwenden Sie " [**glisenabled**](glisenabled.md) " oder " [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", um die aktuelle Einstellung einer beliebigen Funktion zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f5731-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="f5731-143">Das Aufrufen von [**glenableclientstate**](glenableclientstate.md) und **gldisableclientstate** zwischen Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md) kann zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="f5731-143">Calling [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="f5731-144">Wenn kein Fehler generiert wird, ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f5731-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="f5731-145">Die Funktionen " [**glenableclientstate**](glenableclientstate.md) " und " **gldisableclientstate** " sind nur in der OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5731-145">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5731-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5731-146">Requirements</span></span>



| <span data-ttu-id="f5731-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5731-147">Requirement</span></span> | <span data-ttu-id="f5731-148">Wert</span><span class="sxs-lookup"><span data-stu-id="f5731-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5731-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5731-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f5731-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5731-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f5731-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5731-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f5731-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5731-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5731-153">Header</span><span class="sxs-lookup"><span data-stu-id="f5731-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5731-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f5731-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f5731-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5731-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5731-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f5731-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5731-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5731-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5731-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5731-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5731-160">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="f5731-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="f5731-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f5731-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f5731-162">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="f5731-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="f5731-163">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="f5731-163">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="f5731-164">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="f5731-164">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="f5731-165">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="f5731-165">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="f5731-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="f5731-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="f5731-167">**glenableclientstate**</span><span class="sxs-lookup"><span data-stu-id="f5731-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="f5731-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f5731-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f5731-169">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="f5731-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="f5731-170">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="f5731-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="f5731-171">**glinterleavedarrays**</span><span class="sxs-lookup"><span data-stu-id="f5731-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="f5731-172">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="f5731-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="f5731-173">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="f5731-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="f5731-174">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="f5731-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





