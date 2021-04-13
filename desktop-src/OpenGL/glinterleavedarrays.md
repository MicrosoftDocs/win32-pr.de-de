---
title: glinterleavedarrays-Funktion (GL. h)
description: Die Funktion "glinterleavedarrays" gibt gleichzeitig mehrere verschachtelte Arrays in einem größeren Aggregat Array an und aktiviert Sie.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- glinterleavedarrays-Funktion OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391642"
---
# <a name="glinterleavedarrays-function"></a><span data-ttu-id="7510e-104">glinterleavedarrays-Funktion</span><span class="sxs-lookup"><span data-stu-id="7510e-104">glInterleavedArrays function</span></span>

<span data-ttu-id="7510e-105">Die Funktion " **glinterleavedarrays** " gibt gleichzeitig mehrere verschachtelte Arrays in einem größeren Aggregat Array an und aktiviert Sie.</span><span class="sxs-lookup"><span data-stu-id="7510e-105">The **glInterleavedArrays** function simultaneously specifies and enables several interleaved arrays in a larger aggregate array.</span></span>

## <a name="syntax"></a><span data-ttu-id="7510e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7510e-106">Syntax</span></span>


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="7510e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7510e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7510e-108">*format*</span><span class="sxs-lookup"><span data-stu-id="7510e-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="7510e-109">Der Typ des zu aktivierenden Arrays.</span><span class="sxs-lookup"><span data-stu-id="7510e-109">The type of array to enable.</span></span> <span data-ttu-id="7510e-110">Der Parameter kann einen der folgenden symbolischen Werte annehmen: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL \_ C4F \_ N3F \_ V3F, GL \_ T2F \_ V3F, GL T4F V4F \_ \_ , GL \_ T2F \_ C4UB \_ V3F, GL \_ T2F \_ C3F \_ V3F, GL \_ T2F \_ N3F \_ V3F, GL \_ T2F \_ C4F \_ N3F \_ V3F oder GL \_ T4F C4F N3F \_ \_ \_ V4F.</span><span class="sxs-lookup"><span data-stu-id="7510e-110">The parameter can assume one of the following symbolic values: GL\_V2F, GL\_V3F, GL\_C4UB\_V2F, GL\_C4UB\_V3F, GL\_C3F\_V3F, GL\_N3F\_V3F, GL\_C4F\_N3F\_V3F, GL\_T2F\_V3F, GL\_T4F\_V4F, GL\_T2F\_C4UB\_V3F, GL\_T2F\_C3F\_V3F, GL\_T2F\_N3F\_V3F, GL\_T2F\_C4F\_N3F\_V3F, or GL\_T4F\_C4F\_N3F\_V4F.</span></span>

</dd> <dt>

<span data-ttu-id="7510e-111">*Schritt*</span><span class="sxs-lookup"><span data-stu-id="7510e-111">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="7510e-112">Der Offset in Bytes zwischen jedem Aggregat Array Element.</span><span class="sxs-lookup"><span data-stu-id="7510e-112">The offset in bytes between each aggregate array element.</span></span>

</dd> <dt>

<span data-ttu-id="7510e-113">*Zeiger*</span><span class="sxs-lookup"><span data-stu-id="7510e-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="7510e-114">Ein Zeiger auf das erste Element eines Aggregat Arrays.</span><span class="sxs-lookup"><span data-stu-id="7510e-114">A pointer to the first element of an aggregate array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7510e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7510e-115">Return value</span></span>

<span data-ttu-id="7510e-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7510e-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7510e-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7510e-117">Error codes</span></span>

<span data-ttu-id="7510e-118">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7510e-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7510e-119">Name</span><span class="sxs-lookup"><span data-stu-id="7510e-119">Name</span></span>                                                                                                  | <span data-ttu-id="7510e-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7510e-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7510e-121"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7510e-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7510e-122">Das *Format* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="7510e-122">*format* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="7510e-123"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="7510e-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7510e-124">*Stride* war ein negativer Wert.</span><span class="sxs-lookup"><span data-stu-id="7510e-124">*stride* was a negative value.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="7510e-125"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="7510e-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7510e-126">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7510e-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7510e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7510e-127">Remarks</span></span>

<span data-ttu-id="7510e-128">Mit der **glinterleavedarrays** -Funktion können Sie mehrere verschachtelte Farb-, normal-, Textur-und Vertex-Arrays gleichzeitig angeben und aktivieren, deren Elemente Teil eines größeren Aggregat Array Elements sind.</span><span class="sxs-lookup"><span data-stu-id="7510e-128">With the **glInterleavedArrays** function, you can simultaneously specify and enable several interleaved color, normal, texture, and vertex arrays whose elements are part of a larger aggregate array element.</span></span> <span data-ttu-id="7510e-129">Bei einigen Speicher Architekturen ist dies effizienter als das separate angeben der Arrays.</span><span class="sxs-lookup"><span data-stu-id="7510e-129">For some memory architectures, this is more efficient than specifying the arrays separately.</span></span>

<span data-ttu-id="7510e-130">Wenn der *Stride* -Parameter 0 (null) ist, werden die Aggregat Array Elemente nacheinander gespeichert. Andernfalls erfolgt die Anzahl von *Stride* -Bytes zwischen Aggregat Array Elementen.</span><span class="sxs-lookup"><span data-stu-id="7510e-130">If the *stride* parameter is zero then the aggregate array elements are stored consecutively; otherwise *stride* bytes occur between aggregate array elements.</span></span>

<span data-ttu-id="7510e-131">Der *Format* -Parameter dient als Schlüssel, der beschreibt, wie einzelne Arrays aus dem Aggregat Array extrahiert werden:</span><span class="sxs-lookup"><span data-stu-id="7510e-131">The *format* parameter serves as a key that describes how to extract individual arrays from the aggregate array:</span></span>

-   <span data-ttu-id="7510e-132">Wenn das *Format* T enthält, werden Texturkoordinaten aus dem verschachtelten Array extrahiert.</span><span class="sxs-lookup"><span data-stu-id="7510e-132">If *format* contains a T, then texture coordinates are extracted from the interleaved array.</span></span>
-   <span data-ttu-id="7510e-133">Wenn C vorhanden ist, werden Farbwerte extrahiert.</span><span class="sxs-lookup"><span data-stu-id="7510e-133">If C is present, color values are extracted.</span></span>
-   <span data-ttu-id="7510e-134">Wenn N vorhanden ist, werden normale Koordinaten extrahiert.</span><span class="sxs-lookup"><span data-stu-id="7510e-134">If N is present, normal coordinates are extracted.</span></span>
-   <span data-ttu-id="7510e-135">Scheitelpunkt Koordinaten werden immer extrahiert.</span><span class="sxs-lookup"><span data-stu-id="7510e-135">Vertex coordinates are always extracted.</span></span>
-   <span data-ttu-id="7510e-136">Die Ziffern 2, 3 und 4 kennzeichnen, wie viele Werte extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="7510e-136">The digits 2, 3, and 4 denote how many values are extracted.</span></span>
-   <span data-ttu-id="7510e-137">F gibt an, dass Werte als Gleit Komma Werte extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="7510e-137">F indicates that values are extracted as floating point values.</span></span>
-   <span data-ttu-id="7510e-138">Wenn 4UB auf das C folgt, können Farben auch als 4 nicht signierte Bytes extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="7510e-138">If 4UB follows the C, colors may also be extracted as 4 unsigned bytes.</span></span> <span data-ttu-id="7510e-139">Wenn eine Farbe als 4 nicht signierte Bytes extrahiert wird, befindet sich das nachfolgende Vertex-Array Element an der ersten möglichen ausgerichteten Gleit Komma Adresse.</span><span class="sxs-lookup"><span data-stu-id="7510e-139">If a color is extracted as 4 unsigned bytes, the vertex array element that follows is located at the first possible floating-point aligned address.</span></span>

<span data-ttu-id="7510e-140">Wenn Sie bei der Kompilierung einer Anzeigeliste " **glinterleavedarrays** " aufrufen, wird diese nicht in die Liste kompiliert, sondern sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7510e-140">If you call **glInterleavedArrays** while compiling a display list, it is not compiled into the list but is executed immediately.</span></span>

<span data-ttu-id="7510e-141">Sie können keine Aufrufe von **glinterleavedarrays** in **gldisableclientstate** zwischen Aufrufen von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von **glEnd** einschließen.</span><span class="sxs-lookup"><span data-stu-id="7510e-141">You cannot include calls to **glInterleavedArrays** in **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to **glEnd**.</span></span>

> [!Note]  
> <span data-ttu-id="7510e-142">Die Funktion " **glinterleavedarrays** " ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7510e-142">The **glInterleavedArrays** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="7510e-143">Die Funktion " **glinterleavedarrays** " wird auf Clientseite ohne Protokoll implementiert.</span><span class="sxs-lookup"><span data-stu-id="7510e-143">The **glInterleavedArrays** function is implemented on the client side with no protocol.</span></span> <span data-ttu-id="7510e-144">Da es sich bei den Scheitelpunkt Array-Parametern um einen Client seitigen Zustand handelt, werden Sie von [**glpushatfferb**](glpushattrib.md) und **glpopatfferb** nicht gespeichert oder wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="7510e-144">Because the vertex array parameters are client-side state, they are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span> <span data-ttu-id="7510e-145">Verwenden Sie stattdessen [**glpushclientatpub**](glpushclientattrib.md) und **glpopclientatpub** .</span><span class="sxs-lookup"><span data-stu-id="7510e-145">Use [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="7510e-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7510e-146">Requirements</span></span>



| <span data-ttu-id="7510e-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7510e-147">Requirement</span></span> | <span data-ttu-id="7510e-148">Wert</span><span class="sxs-lookup"><span data-stu-id="7510e-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7510e-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7510e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7510e-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7510e-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7510e-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7510e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7510e-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7510e-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7510e-153">Header</span><span class="sxs-lookup"><span data-stu-id="7510e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7510e-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7510e-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7510e-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7510e-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="7510e-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7510e-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7510e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="7510e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7510e-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7510e-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7510e-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7510e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7510e-160">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="7510e-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="7510e-161">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="7510e-161">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="7510e-162">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="7510e-162">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="7510e-163">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="7510e-163">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="7510e-164">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="7510e-164">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="7510e-165">**glenableclientstate**</span><span class="sxs-lookup"><span data-stu-id="7510e-165">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="7510e-166">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="7510e-166">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="7510e-167">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="7510e-167">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="7510e-168">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="7510e-168">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="7510e-169">**glpushatpub**</span><span class="sxs-lookup"><span data-stu-id="7510e-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="7510e-170">**glpushclientatpub**</span><span class="sxs-lookup"><span data-stu-id="7510e-170">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="7510e-171">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="7510e-171">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="7510e-172">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="7510e-172">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





