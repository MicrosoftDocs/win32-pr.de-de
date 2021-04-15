---
title: glcolorpointer-Funktion (GL. h)
description: Die glcolorpointer-Funktion definiert ein Array von Farben.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- glcolorpointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475846"
---
# <a name="glcolorpointer-function"></a><span data-ttu-id="94c0f-104">glcolorpointer-Funktion</span><span class="sxs-lookup"><span data-stu-id="94c0f-104">glColorPointer function</span></span>

<span data-ttu-id="94c0f-105">Die **glcolorpointer** -Funktion definiert ein Array von Farben.</span><span class="sxs-lookup"><span data-stu-id="94c0f-105">The **glColorPointer** function defines an array of colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="94c0f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="94c0f-106">Syntax</span></span>


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="94c0f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="94c0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94c0f-108">*size*</span><span class="sxs-lookup"><span data-stu-id="94c0f-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="94c0f-109">Die Anzahl der Komponenten pro Farbe.</span><span class="sxs-lookup"><span data-stu-id="94c0f-109">The number of components per color.</span></span> <span data-ttu-id="94c0f-110">Der Wert muss 3 oder 4 sein.</span><span class="sxs-lookup"><span data-stu-id="94c0f-110">The value must be either 3 or 4.</span></span>

</dd> <dt>

<span data-ttu-id="94c0f-111">*type*</span><span class="sxs-lookup"><span data-stu-id="94c0f-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="94c0f-112">Der Datentyp jeder Farbkomponente in einem Farbarray.</span><span class="sxs-lookup"><span data-stu-id="94c0f-112">The data type of each color component in a color array.</span></span> <span data-ttu-id="94c0f-113">Zulässige Datentypen werden mit den folgenden Konstanten angegeben: GL \_ Byte, GL \_ unsigned \_ Byte, GL \_ Short, GL \_ unsigned \_ Short, GL \_ int, GL \_ unsigned \_ int, GL \_ float oder GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="94c0f-113">Acceptable data types are specified with the following constants: GL\_BYTE, GL\_UNSIGNED\_BYTE, GL\_SHORT, GL\_UNSIGNED\_SHORT, GL\_INT, GL\_UNSIGNED\_INT, GL\_FLOAT, or GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="94c0f-114">*Schritt*</span><span class="sxs-lookup"><span data-stu-id="94c0f-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="94c0f-115">Der Byte Offset zwischen aufeinander folgenden Farben.</span><span class="sxs-lookup"><span data-stu-id="94c0f-115">The byte offset between consecutive colors.</span></span> <span data-ttu-id="94c0f-116">Wenn *Stride* 0 (null) ist, werden die Farben im Array eng verpackt.</span><span class="sxs-lookup"><span data-stu-id="94c0f-116">When *stride* is zero, the colors are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="94c0f-117">*Zeiger*</span><span class="sxs-lookup"><span data-stu-id="94c0f-117">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="94c0f-118">Ein Zeiger auf die erste Komponente des ersten Farb Elements in einem Farbarray.</span><span class="sxs-lookup"><span data-stu-id="94c0f-118">A pointer to the first component of the first color element in a color array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94c0f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94c0f-119">Return value</span></span>

<span data-ttu-id="94c0f-120">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="94c0f-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="94c0f-121">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="94c0f-121">Error codes</span></span>

<span data-ttu-id="94c0f-122">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="94c0f-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="94c0f-123">Name</span><span class="sxs-lookup"><span data-stu-id="94c0f-123">Name</span></span>                                                                                              | <span data-ttu-id="94c0f-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="94c0f-124">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="94c0f-125"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="94c0f-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="94c0f-126">*Größe* war nicht 3 oder 4.</span><span class="sxs-lookup"><span data-stu-id="94c0f-126">*size* was not 3 or 4.</span></span><br/>            |
| <dl> <span data-ttu-id="94c0f-127"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="94c0f-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="94c0f-128">der *Typ* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="94c0f-128">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="94c0f-129"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="94c0f-129"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="94c0f-130">" *Stride* " oder " *count* " war negativ.</span><span class="sxs-lookup"><span data-stu-id="94c0f-130">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="94c0f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94c0f-131">Remarks</span></span>

<span data-ttu-id="94c0f-132">Die **glcolorpointer** -Funktion gibt den Speicherort und das Datenformat eines Arrays von Farbkomponenten an, die beim Rendern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94c0f-132">The **glColorPointer** function specifies the location and data format of an array of color components to use when rendering.</span></span> <span data-ttu-id="94c0f-133">Der *Stride* -Parameter bestimmt den Byte Offset von einer Farbe zum nächsten und ermöglicht das Packen von Scheitelpunkt Attributen in einem einzelnen Array oder Speicher in separaten Arrays.</span><span class="sxs-lookup"><span data-stu-id="94c0f-133">The *stride* parameter determines the byte offset from one color to the next, enabling the packing of vertex attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="94c0f-134">In einigen Implementierungen kann das Speichern von Vertex-Attributen in einem einzelnen Array effizienter als die Verwendung separater Arrays sein.</span><span class="sxs-lookup"><span data-stu-id="94c0f-134">In some implementations, storing vertex attributes in a single array can be more efficient than the use of separate arrays.</span></span>

<span data-ttu-id="94c0f-135">Aktivieren Sie das Farbarray, indem Sie die GL- \_ Farb \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="94c0f-135">Enabled the color array by specifying the GL\_COLOR\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="94c0f-136">Beim Aufrufen von " [**glarrayelement**](glarrayelement.md)", " [**gldrawelements**](gldrawelements.md)" oder " [**gldrawarrays**](gldrawarrays.md) " wird das Farb Array verwendet, das daher aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="94c0f-136">Calling [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md) uses the color array that is thus enabled.</span></span> <span data-ttu-id="94c0f-137">Standardmäßig ist das Farbarray deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="94c0f-137">By default, the color array is disabled.</span></span> <span data-ttu-id="94c0f-138">Die **glcolorpointer** -Aufrufe können nicht in Anzeigelisten eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="94c0f-138">The **glColorPointer** calls cannot by entered in display lists.</span></span>

<span data-ttu-id="94c0f-139">Wenn Sie ein Farb Array mithilfe von **glcolorpointer** angeben, werden die Werte aller Farb Array Parameter der Funktion in einem Client seitigen Zustand gespeichert, und Sie können statische Array Elemente Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="94c0f-139">When you specify a color array using **glColorPointer**, the values of all the function's color array parameters are saved in a client-side state, and you can cache static array elements.</span></span> <span data-ttu-id="94c0f-140">Da sich die Farb Array Parameter in einem Client seitigen Zustand befinden, speichern oder wiederherstellen die Werte der Parameter von [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) nicht.</span><span class="sxs-lookup"><span data-stu-id="94c0f-140">Because the color array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore the parameters' values.</span></span>

<span data-ttu-id="94c0f-141">Obwohl die Angabe des farbarrays innerhalb von [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paaren keinen Fehler generiert, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="94c0f-141">Although specifying the color array within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="94c0f-142">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der Funktion " **glcolorpointer** " ab:</span><span class="sxs-lookup"><span data-stu-id="94c0f-142">The following functions retrieve information related to the **glColorPointer** function:</span></span>

<span data-ttu-id="94c0f-143">[**glisenabled**](glisenabled.md) mit Argument GL \_ - \_ Farbarray</span><span class="sxs-lookup"><span data-stu-id="94c0f-143">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_ARRAY</span></span>

<span data-ttu-id="94c0f-144">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit der \_ \_ array \_ Größe des Argument GL</span><span class="sxs-lookup"><span data-stu-id="94c0f-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_ARRAY\_SIZE</span></span>

<span data-ttu-id="94c0f-145">**glget** mit Argument GL \_ Color \_ array \_ Type</span><span class="sxs-lookup"><span data-stu-id="94c0f-145">**glGet** with argument GL\_COLOR\_ARRAY\_TYPE</span></span>

<span data-ttu-id="94c0f-146">**glget** mit Argument GL \_ Color \_ array \_ Stride</span><span class="sxs-lookup"><span data-stu-id="94c0f-146">**glGet** with argument GL\_COLOR\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="94c0f-147">**glget** mit Argument GL \_ Color \_ array \_ count</span><span class="sxs-lookup"><span data-stu-id="94c0f-147">**glGet** with argument GL\_COLOR\_ARRAY\_COUNT</span></span>

<span data-ttu-id="94c0f-148">[**glgetpointerv**](glgetpointerv.md) mit Argument GL \_ Color \_ array- \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="94c0f-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_COLOR\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="94c0f-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94c0f-149">Requirements</span></span>



| <span data-ttu-id="94c0f-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94c0f-150">Requirement</span></span> | <span data-ttu-id="94c0f-151">Wert</span><span class="sxs-lookup"><span data-stu-id="94c0f-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94c0f-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94c0f-152">Minimum supported client</span></span><br/> | <span data-ttu-id="94c0f-153">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94c0f-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94c0f-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94c0f-154">Minimum supported server</span></span><br/> | <span data-ttu-id="94c0f-155">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94c0f-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94c0f-156">Header</span><span class="sxs-lookup"><span data-stu-id="94c0f-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="94c0f-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="94c0f-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="94c0f-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94c0f-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="94c0f-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94c0f-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="94c0f-160">DLL</span><span class="sxs-lookup"><span data-stu-id="94c0f-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94c0f-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94c0f-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94c0f-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94c0f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c0f-163">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="94c0f-163">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="94c0f-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="94c0f-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="94c0f-165">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="94c0f-165">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="94c0f-166">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="94c0f-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="94c0f-167">**glenableclientstate**</span><span class="sxs-lookup"><span data-stu-id="94c0f-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="94c0f-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="94c0f-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="94c0f-169">**glget**</span><span class="sxs-lookup"><span data-stu-id="94c0f-169">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="94c0f-170">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="94c0f-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="94c0f-171">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="94c0f-171">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="94c0f-172">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="94c0f-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="94c0f-173">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="94c0f-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="94c0f-174">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="94c0f-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="94c0f-175">**glpopattenb**</span><span class="sxs-lookup"><span data-stu-id="94c0f-175">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="94c0f-176">**glpushatpub**</span><span class="sxs-lookup"><span data-stu-id="94c0f-176">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="94c0f-177">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="94c0f-177">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="94c0f-178">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="94c0f-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





