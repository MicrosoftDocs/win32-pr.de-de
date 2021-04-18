---
title: glvertexpointer-Funktion (GL. h)
description: Die glvertexpointer-Funktion definiert ein Array von Vertex-Daten.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- glvertexpointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478228"
---
# <a name="glvertexpointer-function"></a><span data-ttu-id="c029f-104">glvertexpointer-Funktion</span><span class="sxs-lookup"><span data-stu-id="c029f-104">glVertexPointer function</span></span>

<span data-ttu-id="c029f-105">Die **glvertexpointer** -Funktion definiert ein Array von Vertex-Daten.</span><span class="sxs-lookup"><span data-stu-id="c029f-105">The **glVertexPointer** function defines an array of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c029f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c029f-106">Syntax</span></span>


```C++
void WINAPI glVertexPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="c029f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c029f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c029f-108">*size*</span><span class="sxs-lookup"><span data-stu-id="c029f-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="c029f-109">Die Anzahl der Koordinaten pro Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="c029f-109">The number of coordinates per vertex.</span></span> <span data-ttu-id="c029f-110">Der Wert von *size* muss 2, 3 oder 4 sein.</span><span class="sxs-lookup"><span data-stu-id="c029f-110">The value of *size* must be 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="c029f-111">*type*</span><span class="sxs-lookup"><span data-stu-id="c029f-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="c029f-112">Der Datentyp der einzelnen Koordinaten im Array mit den folgenden symbolischen Konstanten: GL \_ Short, GL \_ int, GL \_ float und GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="c029f-112">The data type of each coordinate in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="c029f-113">*Schritt*</span><span class="sxs-lookup"><span data-stu-id="c029f-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="c029f-114">Der Byte Offset zwischen aufeinander folgenden Vertices.</span><span class="sxs-lookup"><span data-stu-id="c029f-114">The byte offset between consecutive vertices.</span></span> <span data-ttu-id="c029f-115">Wenn *Stride* gleich 0 ist, werden die Scheitel Punkte im Array eng verpackt.</span><span class="sxs-lookup"><span data-stu-id="c029f-115">When *stride* is zero, the vertices are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="c029f-116">*Zeiger*</span><span class="sxs-lookup"><span data-stu-id="c029f-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="c029f-117">Ein Zeiger auf die erste Koordinate des ersten Vertex im Array.</span><span class="sxs-lookup"><span data-stu-id="c029f-117">A pointer to the first coordinate of the first vertex in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c029f-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c029f-118">Return value</span></span>

<span data-ttu-id="c029f-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c029f-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c029f-120">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c029f-120">Error codes</span></span>

<span data-ttu-id="c029f-121">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c029f-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c029f-122">Name</span><span class="sxs-lookup"><span data-stu-id="c029f-122">Name</span></span>                                                                                              | <span data-ttu-id="c029f-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c029f-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="c029f-124"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="c029f-124"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="c029f-125">die *Größe* lag nicht bei 2, 3 oder 4.</span><span class="sxs-lookup"><span data-stu-id="c029f-125">*size* was not 2, 3, or 4.</span></span> <br/>        |
| <dl> <span data-ttu-id="c029f-126"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c029f-126"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="c029f-127">der *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="c029f-127">*type* was not an accepted value.</span></span><br/>  |
| <dl> <span data-ttu-id="c029f-128"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="c029f-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="c029f-129">" *Stride* " oder " *count* " war negativ.</span><span class="sxs-lookup"><span data-stu-id="c029f-129">*stride* or *count* was negative.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="c029f-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c029f-130">Remarks</span></span>

<span data-ttu-id="c029f-131">Die **glvertexpointer** -Funktion gibt den Speicherort und die Daten eines Arrays von Vertex-Koordinaten an, die beim Rendern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c029f-131">The **glVertexPointer** function specifies the location and data of an array of vertex coordinates to use when rendering.</span></span> <span data-ttu-id="c029f-132">Der *size* -Parameter gibt die Anzahl der Koordinaten pro Scheitelpunkt an.</span><span class="sxs-lookup"><span data-stu-id="c029f-132">The *size* parameter specifies the number of coordinates per vertex.</span></span> <span data-ttu-id="c029f-133">Der *Typparameter* gibt den Datentyp der einzelnen Scheitelpunkt Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="c029f-133">The *type* parameter specifies the data type of each vertex coordinate.</span></span> <span data-ttu-id="c029f-134">Der *Stride* -Parameter bestimmt den Byte Offset von einem Scheitelpunkt zum nächsten und ermöglicht das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays.</span><span class="sxs-lookup"><span data-stu-id="c029f-134">The *stride* parameter determines the byte offset from one vertex to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="c029f-135">In einigen Implementierungen können das Speichern der Scheitel Punkte und Attribute in einem einzelnen Array effizienter sein als die Verwendung separater Arrays (siehe [**glinterleavedarrays**](glinterleavedarrays.md)).</span><span class="sxs-lookup"><span data-stu-id="c029f-135">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays (see [**glInterleavedArrays**](glinterleavedarrays.md)).</span></span>

<span data-ttu-id="c029f-136">Ein Scheitelpunkt Array wird aktiviert, wenn Sie die GL- \_ Vertex- \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="c029f-136">A vertex array is enabled when you specify the GL\_VERTEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="c029f-137">Wenn diese Option aktiviert ist, verwenden [**gldrawarrays**](gldrawarrays.md), [**gldrawelements**](gldrawelements.md)und [**glarrayelement**](glarrayelement.md) das Vertex-Array.</span><span class="sxs-lookup"><span data-stu-id="c029f-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the vertex array.</span></span> <span data-ttu-id="c029f-138">Standardmäßig ist das Scheitelpunkt Array deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c029f-138">By default, the vertex array is disabled.</span></span>

<span data-ttu-id="c029f-139">Sie können " **glvertexpointer** " nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="c029f-139">You cannot include **glVertexPointer** in display lists.</span></span>

<span data-ttu-id="c029f-140">Wenn Sie ein Scheitelpunkt Array mithilfe von **glvertexpointer** angeben, werden die Werte aller Scheitelpunkt Array-Parameter der Funktion in einem Client seitigen Zustand gespeichert, und statische Array Elemente können zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c029f-140">When you specify a vertex array using **glVertexPointer**, the values of all the function's vertex array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="c029f-141">Da es sich bei den Scheitelpunkt Array-Parametern um einen Client seitigen Zustand handelt, werden ihre Werte von [**glpushatpub**](glpushattrib.md) und **glpopatfferb** nicht gespeichert oder wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="c029f-141">Because the vertex array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="c029f-142">Obwohl kein Fehler generiert wird, wenn Sie **glvertexpointer** innerhalb von [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paaren aufrufen, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c029f-142">Although no error is generated if you call **glVertexPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="c029f-143">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glvertexpointer** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="c029f-143">The following functions retrieve information related to **glVertexPointer**:</span></span>

<span data-ttu-id="c029f-144">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der Größe des Argument-GL- \_ Vertex- \_ Arrays \_</span><span class="sxs-lookup"><span data-stu-id="c029f-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VERTEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="c029f-145">**glget** mit Argument GL \_ Vertex \_ array \_ Stride</span><span class="sxs-lookup"><span data-stu-id="c029f-145">**glGet** with argument GL\_VERTEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="c029f-146">**glget** mit Argument-GL-Anzahl der \_ Vertex- \_ Arrays \_</span><span class="sxs-lookup"><span data-stu-id="c029f-146">**glGet** with argument GL\_VERTEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="c029f-147">**glget** mit dem Argument "GL \_ Vertex- \_ \_ Arraytyp"</span><span class="sxs-lookup"><span data-stu-id="c029f-147">**glGet** with argument GL\_VERTEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="c029f-148">[**glgetpointerv**](glgetpointerv.md) mit Argument, GL \_ Vertex- \_ array \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="c029f-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_VERTEX\_ARRAY\_POINTER</span></span>

<span data-ttu-id="c029f-149">[**glisenabled**](glisenabled.md) mit Argument "GL \_ Vertex \_ Array"</span><span class="sxs-lookup"><span data-stu-id="c029f-149">[**glIsEnabled**](glisenabled.md) with argument GL\_VERTEX\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="c029f-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c029f-150">Requirements</span></span>



| <span data-ttu-id="c029f-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c029f-151">Requirement</span></span> | <span data-ttu-id="c029f-152">Wert</span><span class="sxs-lookup"><span data-stu-id="c029f-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c029f-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c029f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c029f-154">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c029f-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c029f-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c029f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c029f-156">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c029f-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c029f-157">Header</span><span class="sxs-lookup"><span data-stu-id="c029f-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="c029f-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c029f-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c029f-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c029f-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="c029f-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c029f-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c029f-161">DLL</span><span class="sxs-lookup"><span data-stu-id="c029f-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c029f-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c029f-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c029f-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c029f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c029f-164">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="c029f-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="c029f-165">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="c029f-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="c029f-166">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="c029f-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="c029f-167">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="c029f-167">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="c029f-168">**glenableclientstate**</span><span class="sxs-lookup"><span data-stu-id="c029f-168">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="c029f-169">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="c029f-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="c029f-170">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="c029f-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="c029f-171">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="c029f-171">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="c029f-172">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="c029f-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="c029f-173">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="c029f-173">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="c029f-174">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="c029f-174">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> </dl>

 

 





