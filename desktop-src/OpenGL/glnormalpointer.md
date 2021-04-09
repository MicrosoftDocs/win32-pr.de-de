---
title: glnormalpointer-Funktion (GL. h)
description: Die glnormalpointer-Funktion definiert ein Array von normalen.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- glnormalpointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957207"
---
# <a name="glnormalpointer-function"></a><span data-ttu-id="8be3a-104">glnormalpointer-Funktion</span><span class="sxs-lookup"><span data-stu-id="8be3a-104">glNormalPointer function</span></span>

<span data-ttu-id="8be3a-105">Die **glnormalpointer** -Funktion definiert ein Array von normalen.</span><span class="sxs-lookup"><span data-stu-id="8be3a-105">The **glNormalPointer** function defines an array of normals.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be3a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8be3a-106">Syntax</span></span>


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="8be3a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8be3a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be3a-108">*type*</span><span class="sxs-lookup"><span data-stu-id="8be3a-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="8be3a-109">Der Datentyp der einzelnen Koordinaten im Array mit den folgenden symbolischen Konstanten: GL \_ Byte, GL \_ Short, GL \_ int, GL \_ float und GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="8be3a-109">The data type of each coordinate in the array using the following symbolic constants: GL\_BYTE, GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="8be3a-110">*Schritt*</span><span class="sxs-lookup"><span data-stu-id="8be3a-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="8be3a-111">Der Byte Offset zwischen aufeinander folgenden normalen.</span><span class="sxs-lookup"><span data-stu-id="8be3a-111">The byte offset between consecutive normals.</span></span> <span data-ttu-id="8be3a-112">Wenn *Stride* 0 (null) ist, werden die normale eng im Array verpackt.</span><span class="sxs-lookup"><span data-stu-id="8be3a-112">When *stride* is zero, the normals are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="8be3a-113">*Zeiger*</span><span class="sxs-lookup"><span data-stu-id="8be3a-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="8be3a-114">Ein Zeiger auf den ersten normal im Array.</span><span class="sxs-lookup"><span data-stu-id="8be3a-114">A pointer to the first normal in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be3a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8be3a-115">Return value</span></span>

<span data-ttu-id="8be3a-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8be3a-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8be3a-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="8be3a-117">Error codes</span></span>

<span data-ttu-id="8be3a-118">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8be3a-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8be3a-119">Name</span><span class="sxs-lookup"><span data-stu-id="8be3a-119">Name</span></span>                                                                                                  | <span data-ttu-id="8be3a-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8be3a-120">Meaning</span></span>                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8be3a-121"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8be3a-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8be3a-122">der *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="8be3a-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="8be3a-123"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="8be3a-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8be3a-124">" *Stride* " oder " *count* " war negativ.</span><span class="sxs-lookup"><span data-stu-id="8be3a-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8be3a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8be3a-125">Remarks</span></span>

<span data-ttu-id="8be3a-126">Die **glnormalpointer** -Funktion gibt den Speicherort und die Daten eines Arrays von normalen an, die beim Rendern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8be3a-126">The **glNormalPointer** function specifies the location and data of an array of normals to use when rendering.</span></span> <span data-ttu-id="8be3a-127">Der *Typparameter* gibt den Datentyp der einzelnen normalen Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="8be3a-127">The *type* parameter specifies the data type of each normal coordinate.</span></span> <span data-ttu-id="8be3a-128">Der *Stride* -Parameter bestimmt den Byte Offset von einem normalen zum nächsten und ermöglicht das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays.</span><span class="sxs-lookup"><span data-stu-id="8be3a-128">The *stride* parameter determines the byte offset from one normal to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="8be3a-129">In einigen Implementierungen, die die Scheitel Punkte und Attribute in einem einzelnen Array speichern, kann es effizienter sein, als separate Arrays zu verwenden. Weitere Informationen finden Sie unter [**glinterleavedarrays**](glinterleavedarrays.md) .</span><span class="sxs-lookup"><span data-stu-id="8be3a-129">In some implementations storing the vertices and attributes in a single array can be more efficient than using separate arrays; see [**glInterleavedArrays**](glinterleavedarrays.md) for details.</span></span>

<span data-ttu-id="8be3a-130">Ein normales Array wird aktiviert, wenn Sie die reguläre GL- \_ \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="8be3a-130">A normal array is enabled when you specify the GL\_NORMAL\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="8be3a-131">Wenn diese Option aktiviert ist, verwenden [**gldrawarrays**](gldrawarrays.md), [**gldrawelements**](gldrawelements.md) und [**glarrayelement**](glarrayelement.md) das normale Array.</span><span class="sxs-lookup"><span data-stu-id="8be3a-131">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) and [**glArrayElement**](glarrayelement.md) use the normal array.</span></span> <span data-ttu-id="8be3a-132">Standardmäßig ist das normale Array deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8be3a-132">By default the normal array is disabled.</span></span>

<span data-ttu-id="8be3a-133">Sie können **glnormalpointer** nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="8be3a-133">You cannot include **glNormalPointer** in display lists.</span></span>

<span data-ttu-id="8be3a-134">Wenn Sie ein normales Array mit **glnormalpointer** angeben, werden die Werte aller normalen Array Parameter der Funktion in einem Client seitigen Zustand gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8be3a-134">When you specify a normal array using **glNormalPointer**, the values of all the function's normal array parameters are saved in a client-side state.</span></span> <span data-ttu-id="8be3a-135">Da die normalen Array Parameter in einem Client seitigen Zustand gespeichert werden, werden ihre Werte von [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md)nicht gespeichert oder wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="8be3a-135">Because the normal array parameters are saved in a client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="8be3a-136">Obwohl beim Abrufen von **glnormalpointer** innerhalb von [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paaren kein Fehler generiert wird, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8be3a-136">Although no error is generated when you call **glNormalPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="8be3a-137">Die folgenden Funktionen sind mit **glnormalpointer** verknüpft:</span><span class="sxs-lookup"><span data-stu-id="8be3a-137">The following functions are associated with **glNormalPointer**:</span></span>

<span data-ttu-id="8be3a-138">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ normales \_ array \_ Stride</span><span class="sxs-lookup"><span data-stu-id="8be3a-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NORMAL\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="8be3a-139">**glget** mit Argument GL \_ normale \_ array \_ Anzahl</span><span class="sxs-lookup"><span data-stu-id="8be3a-139">**glGet** with argument GL\_NORMAL\_ARRAY\_COUNT</span></span>

<span data-ttu-id="8be3a-140">**glget** mit Argument GL \_ normaler \_ \_ Arraytyp</span><span class="sxs-lookup"><span data-stu-id="8be3a-140">**glGet** with argument GL\_NORMAL\_ARRAY\_TYPE</span></span>

<span data-ttu-id="8be3a-141">**glgetpointerv** mit Argument GL \_ normaler \_ array \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="8be3a-141">**glGetPointerv** with argument GL\_NORMAL\_ARRAY\_POINTER</span></span>

<span data-ttu-id="8be3a-142">[**glisenabled**](glisenabled.md) mit Argument GL \_ Normal \_ Array</span><span class="sxs-lookup"><span data-stu-id="8be3a-142">[**glIsEnabled**](glisenabled.md) with argument GL\_NORMAL\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="8be3a-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8be3a-143">Requirements</span></span>



| <span data-ttu-id="8be3a-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8be3a-144">Requirement</span></span> | <span data-ttu-id="8be3a-145">Wert</span><span class="sxs-lookup"><span data-stu-id="8be3a-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8be3a-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8be3a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8be3a-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8be3a-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8be3a-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8be3a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8be3a-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8be3a-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8be3a-150">Header</span><span class="sxs-lookup"><span data-stu-id="8be3a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8be3a-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8be3a-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8be3a-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8be3a-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="8be3a-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8be3a-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8be3a-154">DLL</span><span class="sxs-lookup"><span data-stu-id="8be3a-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8be3a-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8be3a-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be3a-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8be3a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be3a-157">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="8be3a-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="8be3a-158">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="8be3a-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="8be3a-159">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="8be3a-159">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="8be3a-160">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="8be3a-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="8be3a-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="8be3a-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="8be3a-162">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="8be3a-162">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="8be3a-163">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="8be3a-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="8be3a-164">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="8be3a-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="8be3a-165">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="8be3a-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="8be3a-166">**glinterleavedarrays**</span><span class="sxs-lookup"><span data-stu-id="8be3a-166">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="8be3a-167">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="8be3a-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="8be3a-168">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="8be3a-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> <dt>

[<span data-ttu-id="8be3a-169">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="8be3a-169">**glGetString**</span></span>](glgetstring.md)
</dt> </dl>

 

 





