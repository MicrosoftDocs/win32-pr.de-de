---
title: glenableclientstate-Funktion (GL. h)
description: Die Funktionen "glenableclientstate" und "gldisableclientstate" aktivieren bzw. deaktivieren Arrays. | glenableclientstate-Funktion (GL. h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- glenableclientstate-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e333a51d4c1fe0a5ff11c717790e03aa6d054a09
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353319"
---
# <a name="glenableclientstate-function"></a><span data-ttu-id="37b02-105">glenableclientstate-Funktion</span><span class="sxs-lookup"><span data-stu-id="37b02-105">glEnableClientState function</span></span>

<span data-ttu-id="37b02-106">Die Funktionen " **glenableclientstate** " und " [**gldisableclientstate**](gldisableclientstate.md) " aktivieren bzw. deaktivieren Arrays.</span><span class="sxs-lookup"><span data-stu-id="37b02-106">The **glEnableClientState** and [**glDisableClientState**](gldisableclientstate.md) functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b02-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37b02-107">Syntax</span></span>


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="37b02-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="37b02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b02-109">*array*</span><span class="sxs-lookup"><span data-stu-id="37b02-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="37b02-110">Eine symbolische Konstante für das Array, das Sie aktivieren oder deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="37b02-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="37b02-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="37b02-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="37b02-112">Wert</span><span class="sxs-lookup"><span data-stu-id="37b02-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="37b02-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="37b02-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="37b02-114"><dt>**GL \_ - \_ Farbarray**</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="37b02-115">Wenn diese Option aktiviert ist, verwenden Sie Farb Arrays mit Aufrufen von [**glarrayelement**](glarrayelement.md), [**gldrawelements**](gldrawelements.md)oder [**gldrawarrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="37b02-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="37b02-116">Siehe auch [**glcolorpointer**](glcolorpointer.md).</span><span class="sxs-lookup"><span data-stu-id="37b02-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="37b02-117"><dt>**GL \_ - \_ edgeflag- \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="37b02-118">Wenn diese Option aktiviert ist, verwenden Sie Edge-Flag-Arrays mit Aufrufen von [**glarrayelement**](glarrayelement.md), [**gldrawelements**](gldrawelements.md)oder [**gldrawarrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="37b02-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="37b02-119">Siehe auch [**gledgeflagpointer**](gledgeflagpointer.md).</span><span class="sxs-lookup"><span data-stu-id="37b02-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="37b02-120"><dt>**GL- \_ Index \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="37b02-121">Wenn diese Option aktiviert ist, verwenden Sie Index Arrays mit Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md)".</span><span class="sxs-lookup"><span data-stu-id="37b02-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="37b02-122">Siehe auch [**glindexpointer**](glindexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="37b02-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="37b02-123"><dt>**GL- \_ normales \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="37b02-124">Wenn diese Option aktiviert ist, verwenden Sie normale Arrays mit Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md)".</span><span class="sxs-lookup"><span data-stu-id="37b02-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="37b02-125">Siehe auch [**glnormalpointer**](glnormalpointer.md).</span><span class="sxs-lookup"><span data-stu-id="37b02-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="37b02-126"><dt>**GL- \_ Textur \_ Koord- \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="37b02-127">Wenn diese Option aktiviert ist, verwenden Sie Texturkoordinaten Arrays mit Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md)".</span><span class="sxs-lookup"><span data-stu-id="37b02-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="37b02-128">Siehe auch [**gltexcoordpointer**](gltexcoordpointer.md).</span><span class="sxs-lookup"><span data-stu-id="37b02-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="37b02-129"><dt>**GL- \_ Scheitelpunkt \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="37b02-130">Wenn diese Option aktiviert ist, verwenden Sie Scheitelpunkt Arrays mit Aufrufen von [**glarrayelement**](glarrayelement.md), [**gldrawelements**](gldrawelements.md)oder [**gldrawarrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="37b02-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="37b02-131">Siehe auch [**glvertexpointer**](glvertexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="37b02-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b02-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37b02-132">Return value</span></span>

<span data-ttu-id="37b02-133">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="37b02-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="37b02-134">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="37b02-134">Error codes</span></span>

<span data-ttu-id="37b02-135">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="37b02-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="37b02-136">Name</span><span class="sxs-lookup"><span data-stu-id="37b02-136">Name</span></span>                                                                                             | <span data-ttu-id="37b02-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="37b02-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="37b02-138"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="37b02-139">Das *Array* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="37b02-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="37b02-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37b02-140">Remarks</span></span>

<span data-ttu-id="37b02-141">Die Funktionen " **glenableclientstate** " und " **gldisableclientstate** " aktivieren und deaktivieren verschiedene individuelle Arrays.</span><span class="sxs-lookup"><span data-stu-id="37b02-141">The **glEnableClientState** and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="37b02-142">Verwenden Sie " [**glisenabled**](glisenabled.md) " oder " [**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ", um die aktuelle Einstellung einer beliebigen Funktion zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="37b02-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="37b02-143">Das Aufrufen von **glenableclientstate** und **gldisableclientstate** zwischen Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md) kann zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="37b02-143">Calling **glEnableClientState** and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="37b02-144">Wenn kein Fehler generiert wird, ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="37b02-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="37b02-145">Die Funktionen " **glenableclientstate** " und " **gldisableclientstate** " sind nur in der OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="37b02-145">The **glEnableClientState** and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="37b02-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37b02-146">Requirements</span></span>



| <span data-ttu-id="37b02-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37b02-147">Requirement</span></span> | <span data-ttu-id="37b02-148">Wert</span><span class="sxs-lookup"><span data-stu-id="37b02-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37b02-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37b02-149">Minimum supported client</span></span><br/> | <span data-ttu-id="37b02-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37b02-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="37b02-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37b02-151">Minimum supported server</span></span><br/> | <span data-ttu-id="37b02-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37b02-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="37b02-153">Header</span><span class="sxs-lookup"><span data-stu-id="37b02-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="37b02-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="37b02-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="37b02-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="37b02-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="37b02-157">DLL</span><span class="sxs-lookup"><span data-stu-id="37b02-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37b02-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37b02-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b02-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37b02-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b02-160">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="37b02-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="37b02-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="37b02-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="37b02-162">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="37b02-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="37b02-163">**gldisableclientstate**</span><span class="sxs-lookup"><span data-stu-id="37b02-163">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="37b02-164">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="37b02-164">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="37b02-165">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="37b02-165">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="37b02-166">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="37b02-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="37b02-167">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="37b02-167">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="37b02-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="37b02-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="37b02-169">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="37b02-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="37b02-170">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="37b02-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="37b02-171">**glinterleavedarrays**</span><span class="sxs-lookup"><span data-stu-id="37b02-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="37b02-172">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="37b02-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="37b02-173">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="37b02-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="37b02-174">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="37b02-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





