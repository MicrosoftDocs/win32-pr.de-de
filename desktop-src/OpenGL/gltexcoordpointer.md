---
title: gltexcoordpointer-Funktion (GL. h)
description: Die gltexcoordpointer-Funktion definiert ein Array von Texturkoordinaten.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- gltexcoordpointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345939"
---
# <a name="gltexcoordpointer-function"></a><span data-ttu-id="30349-104">gltexcoordpointer-Funktion</span><span class="sxs-lookup"><span data-stu-id="30349-104">glTexCoordPointer function</span></span>

<span data-ttu-id="30349-105">Die **gltexcoordpointer** -Funktion definiert ein Array von Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="30349-105">The **glTexCoordPointer** function defines an array of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="30349-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="30349-106">Syntax</span></span>


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="30349-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="30349-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30349-108">*size*</span><span class="sxs-lookup"><span data-stu-id="30349-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="30349-109">Die Anzahl der Koordinaten pro Array Element.</span><span class="sxs-lookup"><span data-stu-id="30349-109">The number of coordinates per array element.</span></span> <span data-ttu-id="30349-110">Der Wert von *size* muss 1, 2, 3 oder 4 sein.</span><span class="sxs-lookup"><span data-stu-id="30349-110">The value of *size* must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="30349-111">*type*</span><span class="sxs-lookup"><span data-stu-id="30349-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="30349-112">Der Datentyp der einzelnen Texturkoordinaten im Array mit den folgenden symbolischen Konstanten: **GL \_ Short**, **GL \_ int**, **GL \_ float** und **GL \_ Double**.</span><span class="sxs-lookup"><span data-stu-id="30349-112">The data type of each texture coordinate in the array using the following symbolic constants: **GL\_SHORT**, **GL\_INT**, **GL\_FLOAT**, and **GL\_DOUBLE**.</span></span>

</dd> <dt>

<span data-ttu-id="30349-113">*Schritt*</span><span class="sxs-lookup"><span data-stu-id="30349-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="30349-114">Der Byte Offset zwischen aufeinander folgenden Array Elementen.</span><span class="sxs-lookup"><span data-stu-id="30349-114">The byte offset between consecutive array elements.</span></span> <span data-ttu-id="30349-115">Wenn *Stride* 0 (null) ist, werden die Array Elemente im Array eng verpackt.</span><span class="sxs-lookup"><span data-stu-id="30349-115">When *stride* is zero, the array elements are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="30349-116">*Zeiger*</span><span class="sxs-lookup"><span data-stu-id="30349-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="30349-117">Ein Zeiger auf die erste Koordinate des ersten Elements im Array.</span><span class="sxs-lookup"><span data-stu-id="30349-117">A pointer to the first coordinate of the first element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30349-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30349-118">Return value</span></span>

<span data-ttu-id="30349-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="30349-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30349-120">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="30349-120">Error codes</span></span>

<span data-ttu-id="30349-121">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="30349-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="30349-122">Name</span><span class="sxs-lookup"><span data-stu-id="30349-122">Name</span></span>                                                                                              | <span data-ttu-id="30349-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="30349-123">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="30349-124"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="30349-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="30349-125">der *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="30349-125">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="30349-126"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="30349-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="30349-127">die *Größe* lag nicht bei 1, 2, 3 oder 4.</span><span class="sxs-lookup"><span data-stu-id="30349-127">*size* was not 1, 2, 3, or 4.</span></span><br/>     |
| <dl> <span data-ttu-id="30349-128"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="30349-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="30349-129">*Stride* war negativ.</span><span class="sxs-lookup"><span data-stu-id="30349-129">*stride* was negative.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="30349-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30349-130">Remarks</span></span>

<span data-ttu-id="30349-131">Die **gltexcoordpointer** -Funktion gibt den Speicherort und die Daten eines Arrays von Texturkoordinaten an, die beim Rendern verwendet werden sollen. Der *size* -Parameter gibt die Anzahl der Koordinaten an, die für jedes Element des Arrays verwendet werden. Der *Typparameter* gibt den Datentyp der einzelnen Texturkoordinaten an.</span><span class="sxs-lookup"><span data-stu-id="30349-131">The **glTexCoordPointer** function specifies the location and data of an array of texture coordinates to use when rendering.The *size* parameter specifies the number of coordinates used for each element of the array.The *type* parameter specifies the data type of each texture coordinate.</span></span> <span data-ttu-id="30349-132">Der *Stride* -Parameter bestimmt den Byte Offset von einem Array Element zum nächsten und ermöglicht das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays.</span><span class="sxs-lookup"><span data-stu-id="30349-132">The *stride* parameter determines the byte offset from one array element to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="30349-133">In einigen Implementierungen können das Speichern der Scheitel Punkte und Attribute in einem einzelnen Array effizienter als die Verwendung von separaten Arrays sein.</span><span class="sxs-lookup"><span data-stu-id="30349-133">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="30349-134">Weitere Informationen finden Sie unter [**glinterleavedarrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="30349-134">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span> <span data-ttu-id="30349-135">Wenn ein Texturkoordinaten Array angegeben wird, werden Größe, Typ, Stride und Zeiger als Client seitiger Zustand gespeichert.</span><span class="sxs-lookup"><span data-stu-id="30349-135">When a texture coordinate array is specified, size, type, stride, and pointer are saved client-side state.</span></span>

<span data-ttu-id="30349-136">Ein Texturkoordinaten Array wird aktiviert, wenn Sie die **GL- \_ Textur \_ Koord- \_ Array** Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="30349-136">A texture coordinate array is enabled when you specify the **GL\_TEXTURE\_COORD\_ARRAY** constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="30349-137">Wenn diese Option aktiviert ist, verwenden [**gldrawarrays**](gldrawarrays.md), [**gldrawelements**](gldrawelements.md)und [**glarrayelement**](glarrayelement.md) das Array der Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="30349-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the texture coordinate array.</span></span> <span data-ttu-id="30349-138">Das Array der Textur Koordinate ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="30349-138">By default the texture coordinate array is disabled.</span></span>

<span data-ttu-id="30349-139">Sie können **gltexcoordpointer** nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="30349-139">You cannot include **glTexCoordPointer** in display lists.</span></span>

<span data-ttu-id="30349-140">Wenn Sie ein Texturkoordinaten Array mithilfe von **gltexcoordpointer** angeben, werden die Werte aller Texturkoordinaten Array-Parameter der Funktion in einem Client seitigen Zustand gespeichert, und statische Array Elemente können zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="30349-140">When you specify a texture coordinate array using **glTexCoordPointer**, the values of all the function's texture coordinate array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="30349-141">Da die Texturkoordinaten Array-Parameter den Client seitigen Zustand aufweisen, werden ihre Werte von [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md)nicht gespeichert oder wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="30349-141">Because the texture coordinate array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="30349-142">Obwohl beim Aufrufen von **gltexcoordpointer** innerhalb der [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paare kein Fehler generiert wird, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="30349-142">Although no error is generated when you call **glTexCoordPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="30349-143">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **gltexcoordpointer** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="30349-143">The following functions retrieve information related to **glTexCoordPointer**:</span></span>

<span data-ttu-id="30349-144">[**glisenabled**](glisenabled.md) mit Argument **GL \_ Textur \_ Koord- \_ Array**</span><span class="sxs-lookup"><span data-stu-id="30349-144">[**glIsEnabled**](glisenabled.md) with argument **GL\_TEXTURE\_COORD\_ARRAY**</span></span>

<span data-ttu-id="30349-145">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument **GL \_ Textur \_ Koord- \_ array \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="30349-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_SIZE**</span></span>

<span data-ttu-id="30349-146">**glget** mit dem Argument **GL \_ Texture \_ Koord \_ array \_ Stride**</span><span class="sxs-lookup"><span data-stu-id="30349-146">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_STRIDE**</span></span>

<span data-ttu-id="30349-147">**glget** mit Argument **GL \_ Textur \_ Koord- \_ array \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="30349-147">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_COUNT**</span></span>

<span data-ttu-id="30349-148">**glget** mit dem Argument **GL \_ Texture Koord- \_ Arraytyp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30349-148">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_TYPE**</span></span>

<span data-ttu-id="30349-149">[**glgetpointerv**](glgetpointerv.md) mit Argument **GL \_ Textur \_ Koord- \_ array \_ Zeiger**</span><span class="sxs-lookup"><span data-stu-id="30349-149">[**glGetPointerv**](glgetpointerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_POINTER**</span></span>

## <a name="requirements"></a><span data-ttu-id="30349-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30349-150">Requirements</span></span>



| <span data-ttu-id="30349-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30349-151">Requirement</span></span> | <span data-ttu-id="30349-152">Wert</span><span class="sxs-lookup"><span data-stu-id="30349-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30349-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30349-153">Minimum supported client</span></span><br/> | <span data-ttu-id="30349-154">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30349-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="30349-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30349-155">Minimum supported server</span></span><br/> | <span data-ttu-id="30349-156">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30349-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30349-157">Header</span><span class="sxs-lookup"><span data-stu-id="30349-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="30349-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="30349-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="30349-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30349-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="30349-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30349-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="30349-161">DLL</span><span class="sxs-lookup"><span data-stu-id="30349-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30349-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30349-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30349-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30349-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30349-164">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="30349-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="30349-165">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="30349-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="30349-166">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="30349-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="30349-167">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="30349-167">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="30349-168">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="30349-168">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="30349-169">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="30349-169">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="30349-170">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="30349-170">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="30349-171">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="30349-171">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="30349-172">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="30349-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="30349-173">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="30349-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="30349-174">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="30349-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="30349-175">**glpopclientattrb**</span><span class="sxs-lookup"><span data-stu-id="30349-175">**glPopClientAttrib**</span></span>](glpopclientattrib.md)
</dt> <dt>

[<span data-ttu-id="30349-176">**glpushclientatpub**</span><span class="sxs-lookup"><span data-stu-id="30349-176">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="30349-177">**gltexcoord**</span><span class="sxs-lookup"><span data-stu-id="30349-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="30349-178">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="30349-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





