---
title: gledgeflagpointer-Funktion (GL. h)
description: Die Funktion gledgeflagpointer definiert ein Array von Edge-Flags.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- gledgeflagpointer-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742208"
---
# <a name="gledgeflagpointer-function"></a><span data-ttu-id="c8331-104">gledgeflagpointer-Funktion</span><span class="sxs-lookup"><span data-stu-id="c8331-104">glEdgeFlagPointer function</span></span>

<span data-ttu-id="c8331-105">Die Funktion **gledgeflagpointer** definiert ein Array von Edge-Flags.</span><span class="sxs-lookup"><span data-stu-id="c8331-105">The **glEdgeFlagPointer** function defines an array of edge flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8331-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8331-106">Syntax</span></span>


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="c8331-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8331-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8331-108">*Schritt*</span><span class="sxs-lookup"><span data-stu-id="c8331-108">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="c8331-109">Der Byte Offset zwischen aufeinander folgenden Edge-Flags.</span><span class="sxs-lookup"><span data-stu-id="c8331-109">The byte offset between consecutive edge flags.</span></span> <span data-ttu-id="c8331-110">Wenn *Stride* 0 (null) ist, werden die Edge-Flags im Array eng verpackt.</span><span class="sxs-lookup"><span data-stu-id="c8331-110">When *stride* is zero, the edge flags are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="c8331-111">*Zeiger*</span><span class="sxs-lookup"><span data-stu-id="c8331-111">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="c8331-112">Ein Zeiger auf das erste Edge-Flag im Array.</span><span class="sxs-lookup"><span data-stu-id="c8331-112">A pointer to the first edge flag in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8331-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8331-113">Return value</span></span>

<span data-ttu-id="c8331-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c8331-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8331-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c8331-115">Error codes</span></span>

<span data-ttu-id="c8331-116">Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8331-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c8331-117">Name</span><span class="sxs-lookup"><span data-stu-id="c8331-117">Name</span></span>                                                                                             | <span data-ttu-id="c8331-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c8331-118">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c8331-119"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c8331-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="c8331-120">" *Stride* " oder " *count* " war negativ.</span><span class="sxs-lookup"><span data-stu-id="c8331-120">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c8331-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8331-121">Remarks</span></span>

<span data-ttu-id="c8331-122">Die Funktion **gledgeflagpointer** gibt den Speicherort und die Daten eines Arrays von booleschen Edge-Flags an, die beim Rendern verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c8331-122">The **glEdgeFlagPointer** function specifies the location and data of an array of Boolean edge flags to use when rendering.</span></span> <span data-ttu-id="c8331-123">Der *Stride* -Parameter bestimmt den Byte Offset von einem edgeflag zum nächsten, das das Packen von Vertices und Attributen in einem einzelnen Array oder Speicher in separaten Arrays ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c8331-123">The *stride* parameter determines the byte offset from one edge flag to the next, which enables the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="c8331-124">In einigen Implementierungen können das Speichern der Scheitel Punkte und Attribute in einem einzelnen Array effizienter als die Verwendung von separaten Arrays sein.</span><span class="sxs-lookup"><span data-stu-id="c8331-124">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span>

<span data-ttu-id="c8331-125">Ein Edge-Flag-Array wird aktiviert, wenn Sie die GL- \_ Edge- \_ Flag- \_ Array Konstante mit [**glenableclientstate**](glenableclientstate.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="c8331-125">An edge-flag array is enabled when you specify the GL\_EDGE\_FLAG\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="c8331-126">Wenn diese Option aktiviert ist, verwendet [**gldrawarrays**](gldrawarrays.md) oder [**glarrayelement**](glarrayelement.md) das Edge-Flag-Array.</span><span class="sxs-lookup"><span data-stu-id="c8331-126">When enabled, [**glDrawArrays**](gldrawarrays.md) or [**glArrayElement**](glarrayelement.md) uses the edge-flag array.</span></span> <span data-ttu-id="c8331-127">Standardmäßig ist das Edge-Flag-Array deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8331-127">By default the edge-flag array is disabled.</span></span>

<span data-ttu-id="c8331-128">Verwenden Sie **gldrawarrays** , um eine Sequenz von primitiven (alle desselben Typs) aus den vorspezifizierten Vertex-und Vertex-Attribut Arrays zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c8331-128">Use **glDrawArrays** to construct a sequence of primitives (all of the same type) from prespecified vertex and vertex attribute arrays.</span></span> <span data-ttu-id="c8331-129">Verwenden Sie " **glarrayelement** ", um primitive durch Indizierung von Vertices und Scheitelpunkt Attributen anzugeben, und [**gldrawelements**](gldrawelements.md) zum Erstellen einer Sequenz von primitiven durch Indizierung von Vertices und Vertex-Attributen.</span><span class="sxs-lookup"><span data-stu-id="c8331-129">Use **glArrayElement** to specify primitives by indexing vertices and vertex attributes, and [**glDrawElements**](gldrawelements.md) to construct a sequence of primitives by indexing vertices and vertex attributes.</span></span>

<span data-ttu-id="c8331-130">Sie können **gledgeflagpointer** nicht in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="c8331-130">You cannot include **glEdgeFlagPointer** in display lists.</span></span>

<span data-ttu-id="c8331-131">Wenn Sie ein Edge-Flag-Array mit **gledgeflagpointer** angeben, werden die Werte aller Edge-Flag-Array Parameter der Funktion in einem Client seitigen Zustand gespeichert, und statische Array Elemente können zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c8331-131">When you specify an edge-flag array using **glEdgeFlagPointer**, the values of all the function's edge-flag array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="c8331-132">Da sich die Parameter des Edge-Flag-Arrays in einem Client seitigen Zustand [**befinden, speichern**](glpushattrib.md) oder Wiederherstellen [**Sie Ihre Werte nicht.**](glpopattrib.md)</span><span class="sxs-lookup"><span data-stu-id="c8331-132">Because the edge-flag array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore their values.</span></span>

<span data-ttu-id="c8331-133">Obwohl das Aufrufen von **gledgeflagpointer** innerhalb eines [**glBegin**](glbegin.md)- / [**glEnd**](glend.md) -Paars keinen Fehler generiert, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c8331-133">Although calling **glEdgeFlagPointer** within a [**glBegin**](glbegin.md)/[**glend**](glend.md) pair does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="c8331-134">Die folgenden Funktionen rufen Informationen im Zusammenhang mit der **gledgeflagpointer** -Funktion ab:</span><span class="sxs-lookup"><span data-stu-id="c8331-134">The following functions retrieve information related to the **glEdgeFlagPointer** function:</span></span>

<span data-ttu-id="c8331-135">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Edge- \_ Flag \_ array \_ Stride</span><span class="sxs-lookup"><span data-stu-id="c8331-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="c8331-136">**glget** mit dem Argument GL \_ Edge \_ Flag \_ array \_ count</span><span class="sxs-lookup"><span data-stu-id="c8331-136">**glGet** with argument GL\_EDGE\_FLAG\_ARRAY\_COUNT</span></span>

<span data-ttu-id="c8331-137">[**glgetpointerv**](glgetpointerv.md) mit Argument GL \_ Edge- \_ Flag \_ array \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="c8331-137">[**glGetPointerv**](glgetpointerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_POINTER</span></span>

<span data-ttu-id="c8331-138">[**glisenabled**](glisenabled.md) mit Argument GL \_ Edge- \_ Flag- \_ Array</span><span class="sxs-lookup"><span data-stu-id="c8331-138">[**glIsEnabled**](glisenabled.md) with argument GL\_EDGE\_FLAG\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="c8331-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8331-139">Requirements</span></span>



| <span data-ttu-id="c8331-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8331-140">Requirement</span></span> | <span data-ttu-id="c8331-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c8331-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8331-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8331-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c8331-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8331-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c8331-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8331-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c8331-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8331-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c8331-146">Header</span><span class="sxs-lookup"><span data-stu-id="c8331-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8331-147"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8331-147"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c8331-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c8331-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8331-149"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8331-149"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8331-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c8331-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8331-151"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8331-151"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8331-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8331-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8331-153">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="c8331-153">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="c8331-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c8331-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c8331-155">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="c8331-155">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="c8331-156">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="c8331-156">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="c8331-157">**glenableclientstate**</span><span class="sxs-lookup"><span data-stu-id="c8331-157">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="c8331-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c8331-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c8331-159">**glget**</span><span class="sxs-lookup"><span data-stu-id="c8331-159">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="c8331-160">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="c8331-160">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="c8331-161">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="c8331-161">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="c8331-162">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="c8331-162">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="c8331-163">**glisenabled**</span><span class="sxs-lookup"><span data-stu-id="c8331-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="c8331-164">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="c8331-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="c8331-165">**glpopattenb**</span><span class="sxs-lookup"><span data-stu-id="c8331-165">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="c8331-166">**glpushatpub**</span><span class="sxs-lookup"><span data-stu-id="c8331-166">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="c8331-167">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="c8331-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="c8331-168">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="c8331-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





