---
title: glindexpointer-Funktion (GL. h)
description: Die Funktion "glindexpointer" definiert ein Array von Farbindizes.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- glindexpointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475261"
---
# <a name="glindexpointer-function"></a><span data-ttu-id="018e2-104">glindexpointer-Funktion</span><span class="sxs-lookup"><span data-stu-id="018e2-104">glIndexPointer function</span></span>

<span data-ttu-id="018e2-105">Die Funktion " **glindexpointer** " definiert ein Array von Farbindizes.</span><span class="sxs-lookup"><span data-stu-id="018e2-105">The **glIndexPointer** function defines an array of color indexes.</span></span>

## <a name="syntax"></a><span data-ttu-id="018e2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="018e2-106">Syntax</span></span>


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="018e2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="018e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="018e2-108">*type*</span><span class="sxs-lookup"><span data-stu-id="018e2-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="018e2-109">Der Datentyp der einzelnen Farbindizes im Array mit den folgenden symbolischen Konstanten: GL \_ Short, GL \_ int, GL \_ float, GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="018e2-109">The data type of each color index in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="018e2-110">*Schritt*</span><span class="sxs-lookup"><span data-stu-id="018e2-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="018e2-111">Der Byte Offset zwischen aufeinander folgenden Farbindizes.</span><span class="sxs-lookup"><span data-stu-id="018e2-111">The byte offset between consecutive color indexes.</span></span> <span data-ttu-id="018e2-112">Wenn *Stride* gleich NULL ist, werden die Farbindizes im Array eng verpackt.</span><span class="sxs-lookup"><span data-stu-id="018e2-112">When *stride* is zero, the color indexes are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="018e2-113">*Zeiger*</span><span class="sxs-lookup"><span data-stu-id="018e2-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="018e2-114">Ein Zeiger auf den ersten Farb Index im Array.</span><span class="sxs-lookup"><span data-stu-id="018e2-114">A pointer to the first color index in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="018e2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="018e2-115">Return value</span></span>

<span data-ttu-id="018e2-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="018e2-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="018e2-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="018e2-117">Error codes</span></span>

<span data-ttu-id="018e2-118">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="018e2-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="018e2-119">Name</span><span class="sxs-lookup"><span data-stu-id="018e2-119">Name</span></span>                                                                                              | <span data-ttu-id="018e2-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="018e2-120">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="018e2-121"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="018e2-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="018e2-122">der *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="018e2-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="018e2-123"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="018e2-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="018e2-124">" *Stride* " oder " *count* " war negativ.</span><span class="sxs-lookup"><span data-stu-id="018e2-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="018e2-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="018e2-125">Remarks</span></span>

<span data-ttu-id="018e2-126">Die Funktion " **glindexpointer** " gibt den Speicherort und die Daten eines Arrays von Farbindizes an, die beim Rendern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="018e2-126">The **glIndexPointer** function specifies the location and data of an array of color indexes to use when rendering.</span></span> <span data-ttu-id="018e2-127">Der *Typparameter* gibt den Datentyp jedes Farbindexes an, und *Stride* bestimmt den Byte Offset von einem Farb Index zum nächsten und ermöglicht das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays.</span><span class="sxs-lookup"><span data-stu-id="018e2-127">The *type* parameter specifies the data type of each color index and *stride* determines the byte offset from one color index to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="018e2-128">In einigen Implementierungen können das Speichern der Scheitel Punkte und Attribute in einem einzelnen Array effizienter als die Verwendung von separaten Arrays sein.</span><span class="sxs-lookup"><span data-stu-id="018e2-128">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="018e2-129">Weitere Informationen finden Sie unter [**glinterleavedarrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="018e2-129">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span>

<span data-ttu-id="018e2-130">Ein Farb Index Array wird aktiviert, wenn Sie die GL- \_ Index \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="018e2-130">A color-index array is enabled when you specify the GL\_INDEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="018e2-131">Wenn diese Option aktiviert ist, verwenden " [**gldrawarrays**](gldrawarrays.md) " und " [**glarrayelement**](glarrayelement.md) " das Farb Index Array.</span><span class="sxs-lookup"><span data-stu-id="018e2-131">When enabled, [**glDrawArrays**](gldrawarrays.md) and [**glArrayElement**](glarrayelement.md) use the color-index array.</span></span> <span data-ttu-id="018e2-132">Standardmäßig ist das Farb Index Array deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="018e2-132">By default the color-index array is disabled.</span></span>

<span data-ttu-id="018e2-133">Sie können " **glindexpointer** " nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="018e2-133">You cannot include **glIndexPointer** in display lists.</span></span>

<span data-ttu-id="018e2-134">Wenn Sie ein Farb Index Array mithilfe von **glindexpointer** angeben, werden die Werte aller Farb Index Array-Parameter der Funktion in einem Client seitigen Zustand gespeichert, und statische Array Elemente können zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="018e2-134">When you specify a color-index array using **glIndexPointer**, the values of all the function's color-index array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="018e2-135">Da es sich bei den Farb Index Array-Parametern um einen Client seitigen Zustand handelt, werden ihre Werte von [**glpushatpub**](glpushattrib.md) und **glpopatpub** nicht gespeichert oder wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="018e2-135">Because the color-index array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="018e2-136">Obwohl kein Fehler generiert wird, wenn Sie **glindexpointer** innerhalb von [**glBegin**](glbegin.md) -und **glEnd** -Paaren aufzurufen, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="018e2-136">Although no error is generated when you call **glIndexPointer** within [**glBegin**](glbegin.md) and **glEnd** pairs, the results are undefined.</span></span>

<span data-ttu-id="018e2-137">Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glindexpointer** abgerufen:</span><span class="sxs-lookup"><span data-stu-id="018e2-137">The following functions retrieve information related to **glIndexPointer**:</span></span>

<span data-ttu-id="018e2-138">[**glisenabled**](glisenabled.md) mit Argument-GL- \_ Index \_ Array</span><span class="sxs-lookup"><span data-stu-id="018e2-138">[**glIsEnabled**](glisenabled.md) with argument GL\_INDEX\_ARRAY</span></span>

<span data-ttu-id="018e2-139">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit Argument GL \_ Index \_ array \_ Stride</span><span class="sxs-lookup"><span data-stu-id="018e2-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="018e2-140">**glget** mit Argument GL \_ Index \_ array \_ count</span><span class="sxs-lookup"><span data-stu-id="018e2-140">**glGet** with argument GL\_INDEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="018e2-141">**glget** mit Argument-Typ für GL- \_ Index \_ array \_</span><span class="sxs-lookup"><span data-stu-id="018e2-141">**glGet** with argument GL\_INDEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="018e2-142">**glget** mit Argument-GL- \_ Index \_ array \_ Größe</span><span class="sxs-lookup"><span data-stu-id="018e2-142">**glGet** with argument GL\_INDEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="018e2-143">[**glgetpointerv**](glgetpointerv.md) mit Argument GL \_ Index \_ array- \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="018e2-143">[**glGetPointerv**](glgetpointerv.md) with argument GL\_INDEX\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="018e2-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="018e2-144">Requirements</span></span>



| <span data-ttu-id="018e2-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="018e2-145">Requirement</span></span> | <span data-ttu-id="018e2-146">Wert</span><span class="sxs-lookup"><span data-stu-id="018e2-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="018e2-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="018e2-147">Minimum supported client</span></span><br/> | <span data-ttu-id="018e2-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="018e2-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="018e2-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="018e2-149">Minimum supported server</span></span><br/> | <span data-ttu-id="018e2-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="018e2-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="018e2-151">Header</span><span class="sxs-lookup"><span data-stu-id="018e2-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="018e2-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="018e2-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="018e2-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="018e2-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="018e2-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="018e2-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="018e2-155">DLL</span><span class="sxs-lookup"><span data-stu-id="018e2-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="018e2-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="018e2-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="018e2-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="018e2-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018e2-158">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="018e2-158">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="018e2-159">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="018e2-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="018e2-160">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="018e2-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="018e2-161">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="018e2-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="018e2-162">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="018e2-162">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="018e2-163">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="018e2-163">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="018e2-164">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="018e2-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="018e2-165">**glpushatpub**</span><span class="sxs-lookup"><span data-stu-id="018e2-165">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="018e2-166">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="018e2-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="018e2-167">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="018e2-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





