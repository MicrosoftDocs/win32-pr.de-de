---
title: gldrawarrays-Funktion (GL. h)
description: Die Funktion "gldrawarrays" gibt mehrere primitive zum Rendering an.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- gldrawarrays-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956600"
---
# <a name="gldrawarrays-function"></a><span data-ttu-id="b6744-104">gldrawarrays-Funktion</span><span class="sxs-lookup"><span data-stu-id="b6744-104">glDrawArrays function</span></span>

<span data-ttu-id="b6744-105">Die Funktion " **gldrawarrays** " gibt mehrere primitive zum Rendering an.</span><span class="sxs-lookup"><span data-stu-id="b6744-105">The **glDrawArrays** function specifies multiple primitives to render.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6744-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6744-106">Syntax</span></span>


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a><span data-ttu-id="b6744-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6744-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6744-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="b6744-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="b6744-109">Die Art der zu Rendering enden primitiver.</span><span class="sxs-lookup"><span data-stu-id="b6744-109">The kind of primitives to render.</span></span> <span data-ttu-id="b6744-110">Die folgenden Konstanten geben akzeptable Typen von primitiven an: GL- \_ Punkte, GL-Zeilen \_ \_ Streifen, GL- \_ Zeilen \_ Schleife, GL \_ -Linien, GL \_ \_ -Dreiecks Streifen, GL \_ \_ -Dreiecks Lüfter, GL \_ -Dreiecke, GL \_ Quad \_ Strip, GL \_ QUADS und GL- \_ Polygon.</span><span class="sxs-lookup"><span data-stu-id="b6744-110">The following constants specify acceptable types of primitives: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="b6744-111">*first*</span><span class="sxs-lookup"><span data-stu-id="b6744-111">*first*</span></span> 
</dt> <dd>

<span data-ttu-id="b6744-112">Der Start Index in den aktivierten Arrays.</span><span class="sxs-lookup"><span data-stu-id="b6744-112">The starting index in the enabled arrays.</span></span>

</dd> <dt>

<span data-ttu-id="b6744-113">*count*</span><span class="sxs-lookup"><span data-stu-id="b6744-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="b6744-114">Die Anzahl der zu Rendering enden Indizes.</span><span class="sxs-lookup"><span data-stu-id="b6744-114">The number of indexes to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6744-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6744-115">Return value</span></span>

<span data-ttu-id="b6744-116">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b6744-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b6744-117">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b6744-117">Error codes</span></span>

<span data-ttu-id="b6744-118">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b6744-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b6744-119">Name</span><span class="sxs-lookup"><span data-stu-id="b6744-119">Name</span></span>                                                                                                  | <span data-ttu-id="b6744-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b6744-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6744-121"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="b6744-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b6744-122">die *Anzahl* war negativ.</span><span class="sxs-lookup"><span data-stu-id="b6744-122">*count* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="b6744-123"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6744-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b6744-124">der *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="b6744-124">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="b6744-125"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="b6744-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b6744-126">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b6744-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b6744-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6744-127">Remarks</span></span>

<span data-ttu-id="b6744-128">Mit **gldrawarrays** können Sie mehrere geometrische Primitive zum Rendering angeben.</span><span class="sxs-lookup"><span data-stu-id="b6744-128">With **glDrawArrays**, you can specify multiple geometric primitives to render.</span></span> <span data-ttu-id="b6744-129">Anstatt separate OpenGL-Funktionen zum übergeben einzelner Scheitel Punkte, normaler Werte oder Farben aufzurufen, können Sie separate Arrays von Scheitel Punkten, normalen und Farben angeben, um eine Sequenz von primitiven (alle Arten) mit einem einzigen Aufruf von **gldrawarrays** zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b6744-129">Instead of calling separate OpenGL functions to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors to define a sequence of primitives (all the same kind) with a single call to **glDrawArrays**.</span></span>

<span data-ttu-id="b6744-130">Wenn Sie **gldrawarrays** aufzurufen, werden sequenzielle Elemente aus den einzelnen aktivierten Arrays *verwendet, um* eine Sequenz geometrischer primitiver Elemente zu erstellen, beginnend mit dem *ersten* Element.</span><span class="sxs-lookup"><span data-stu-id="b6744-130">When you call **glDrawArrays**, *count* sequential elements from each enabled array are used to construct a sequence of geometric primitives, beginning with the *first* element.</span></span> <span data-ttu-id="b6744-131">Der *Mode* -Parameter gibt an, welche Art von primitiver konstruiert werden soll und wie die Array Elemente zum Erstellen der primitiven verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6744-131">The *mode* parameter specifies what kind of primitive to construct and how to use the array elements to construct the primitives.</span></span>

<span data-ttu-id="b6744-132">Nachdem **gldrawarrays** zurückgegeben wurde, sind die Werte von Vertex-Attributen, die von **gldrawarrays** geändert werden, nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b6744-132">After **glDrawArrays** returns, the values of vertex attributes that are modified by **glDrawArrays** are undefined.</span></span> <span data-ttu-id="b6744-133">Wenn z. b. \_ das GL- \_ Farbarray aktiviert ist, ist der Wert der aktuellen Farbe nach dem Zurückgeben von **gldrawarrays** nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b6744-133">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawArrays** returns.</span></span> <span data-ttu-id="b6744-134">Von **gldrawarrays** nicht geänderte Attribute bleiben definiert.</span><span class="sxs-lookup"><span data-stu-id="b6744-134">Attributes not modified by **glDrawArrays** remain defined.</span></span> <span data-ttu-id="b6744-135">Wenn das GL- \_ Scheitelpunkt \_ Array nicht aktiviert ist, werden keine geometrischen primitiven generiert, aber die Attribute, die aktivierten Arrays entsprechen, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="b6744-135">When GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated but the attributes corresponding to enabled arrays are modified.</span></span>

<span data-ttu-id="b6744-136">Sie können **gldrawarrays** in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="b6744-136">You can include **glDrawArrays** in display lists.</span></span> <span data-ttu-id="b6744-137">Wenn Sie **gldrawarrays** in eine Anzeigeliste einschließen, werden die erforderlichen Array Daten, die durch die Array Zeiger und die aktiviert werden, in der Anzeigeliste generiert und eingegeben.</span><span class="sxs-lookup"><span data-stu-id="b6744-137">When you include **glDrawArrays** in a display list, the necessary array data, determined by the array pointers and the enables, are generated and entered in the display list.</span></span> <span data-ttu-id="b6744-138">Die Werte der Array Zeiger und-Aktivierung werden während der Erstellung von Anzeigelisten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b6744-138">The values of array pointers and enables are determined during the creation of display lists.</span></span>

<span data-ttu-id="b6744-139">Sie können statische Array Daten jederzeit lesen.</span><span class="sxs-lookup"><span data-stu-id="b6744-139">You can read static array data at any time.</span></span> <span data-ttu-id="b6744-140">Wenn statische Array Elemente geändert und das Array nicht erneut angegeben wird, sind die Ergebnisse aller nachfolgenden Aufrufe von **gldrawarrays** nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b6744-140">If any static array elements are modified and the array is not specified again, the results of any subsequent calls to **glDrawArrays** are undefined.</span></span>

<span data-ttu-id="b6744-141">Obwohl kein Fehler generiert wird, wenn Sie ein Array mehr als einmal innerhalb der [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paare angeben, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="b6744-141">Although no error is generated when you specify an array more than once within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs, the results are undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6744-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6744-142">Requirements</span></span>



| <span data-ttu-id="b6744-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6744-143">Requirement</span></span> | <span data-ttu-id="b6744-144">Wert</span><span class="sxs-lookup"><span data-stu-id="b6744-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6744-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6744-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b6744-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6744-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b6744-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6744-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b6744-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6744-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6744-149">Header</span><span class="sxs-lookup"><span data-stu-id="b6744-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6744-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6744-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b6744-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b6744-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6744-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6744-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6744-153">DLL</span><span class="sxs-lookup"><span data-stu-id="b6744-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6744-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6744-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6744-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6744-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6744-156">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="b6744-156">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="b6744-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b6744-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b6744-158">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="b6744-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="b6744-159">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="b6744-159">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="b6744-160">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b6744-160">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b6744-161">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="b6744-161">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="b6744-162">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="b6744-162">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="b6744-163">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="b6744-163">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="b6744-164">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="b6744-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="b6744-165">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="b6744-165">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="b6744-166">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="b6744-166">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





