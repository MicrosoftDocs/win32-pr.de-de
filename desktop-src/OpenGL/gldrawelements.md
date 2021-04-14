---
title: gldrawelements-Funktion (GL. h)
description: Die gldrawelements-Funktion rendert primitive aus Array Daten.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- gldrawelements-Funktion OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518101"
---
# <a name="gldrawelements-function"></a><span data-ttu-id="913e3-104">gldrawelements-Funktion</span><span class="sxs-lookup"><span data-stu-id="913e3-104">glDrawElements function</span></span>

<span data-ttu-id="913e3-105">Die **gldrawelements** -Funktion rendert primitive aus Array Daten.</span><span class="sxs-lookup"><span data-stu-id="913e3-105">The **glDrawElements** function renders primitives from array data.</span></span>

## <a name="syntax"></a><span data-ttu-id="913e3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="913e3-106">Syntax</span></span>


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a><span data-ttu-id="913e3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="913e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913e3-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="913e3-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="913e3-109">Die Art der zu Rendering enden primitiver.</span><span class="sxs-lookup"><span data-stu-id="913e3-109">The kind of primitives to render.</span></span> <span data-ttu-id="913e3-110">Es kann von einem der folgenden symbolischen Werte ausgegangen werden: GL- \_ Punkte, GL-Linien \_ \_ Streifen, GL \_ -Zeilen \_ Schleife, GL \_ -Linien, GL \_ \_ -Dreiecks Streifen, GL \_ \_ -Dreiecks Lüfter, GL \_ -Dreiecke, GL \_ Quad Strip, \_ GL \_ QUADS und GL- \_ Polygon.</span><span class="sxs-lookup"><span data-stu-id="913e3-110">It can assume one of the following symbolic values: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="913e3-111">*count*</span><span class="sxs-lookup"><span data-stu-id="913e3-111">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="913e3-112">Die Anzahl der Elemente, die gerendert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="913e3-112">The number of elements to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="913e3-113">*type*</span><span class="sxs-lookup"><span data-stu-id="913e3-113">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="913e3-114">Der Typ der Werte in Indizes.</span><span class="sxs-lookup"><span data-stu-id="913e3-114">The type of the values in indices.</span></span> <span data-ttu-id="913e3-115">Es muss sich um ein "GL \_ unsigned \_ Byte", "GL \_ unsigned \_ Short" oder "GL \_ unsigned \_ int" handeln.</span><span class="sxs-lookup"><span data-stu-id="913e3-115">Must be one of GL\_UNSIGNED\_BYTE, GL\_UNSIGNED\_SHORT, or GL\_UNSIGNED\_INT.</span></span>

</dd> <dt>

<span data-ttu-id="913e3-116">*Kei*</span><span class="sxs-lookup"><span data-stu-id="913e3-116">*indices*</span></span> 
</dt> <dd>

<span data-ttu-id="913e3-117">Ein Zeiger auf den Speicherort, an dem die Indizes gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="913e3-117">A pointer to the location where the indices are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913e3-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="913e3-118">Return value</span></span>

<span data-ttu-id="913e3-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="913e3-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="913e3-120">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="913e3-120">Error codes</span></span>

<span data-ttu-id="913e3-121">Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="913e3-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="913e3-122">Name</span><span class="sxs-lookup"><span data-stu-id="913e3-122">Name</span></span>                                                                                                  | <span data-ttu-id="913e3-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="913e3-123">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="913e3-124"><dt>**GL \_ ungültige Aufzählung. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="913e3-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="913e3-125">der *Modus* war kein akzeptierter Wert.</span><span class="sxs-lookup"><span data-stu-id="913e3-125">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="913e3-126"><dt>**\_Ungültiger GL- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="913e3-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="913e3-127">*count* war ein negativer Wert.</span><span class="sxs-lookup"><span data-stu-id="913e3-127">*count* was a negative value.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="913e3-128"><dt>**\_ungültiger \_ Vorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="913e3-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="913e3-129">Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="913e3-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="913e3-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="913e3-130">Remarks</span></span>

<span data-ttu-id="913e3-131">Mit der **gldrawelements** -Funktion können Sie mehrere geometrische Primitive mit sehr wenigen Funktionsaufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="913e3-131">The **glDrawElements** function enables you to specify multiple geometric primitives with very few function calls.</span></span> <span data-ttu-id="913e3-132">Anstatt eine OpenGL-Funktion aufzurufen, um die einzelnen Scheitel Punkte, normal oder Farben zu übergeben, können Sie im Vorfeld separate Arrays von Scheitel Punkten, normalen und Farben angeben und diese zum Definieren einer Sequenz von primitiven (alle desselben Typs) mit einem einzigen Aufruf von **gldrawelements** verwenden.</span><span class="sxs-lookup"><span data-stu-id="913e3-132">Instead of calling an OpenGL function to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors beforehand and use them to define a sequence of primitives (all of the same type) with a single call to **glDrawElements**.</span></span>

<span data-ttu-id="913e3-133">Wenn Sie die **gldrawelements** -Funktion aufzurufen, *werden sequenzielle* Elemente aus *Indizes* verwendet, um eine Sequenz geometrischer primitiver Elemente zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="913e3-133">When you call the **glDrawElements** function, it uses *count* sequential elements from *indices* to construct a sequence of geometric primitives.</span></span> <span data-ttu-id="913e3-134">Der *Mode* -Parameter gibt an, welche Art von primitiver Typen erstellt werden und wie die Array Elemente verwendet werden, um diese primitiven zu konstruieren.</span><span class="sxs-lookup"><span data-stu-id="913e3-134">The *mode* parameter specifies what kind of primitives are constructed, and how the array elements are used to construct these primitives.</span></span> <span data-ttu-id="913e3-135">Wenn das GL- \_ Scheitelpunkt \_ Array nicht aktiviert ist, werden keine geometrischen primitiven generiert.</span><span class="sxs-lookup"><span data-stu-id="913e3-135">If GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated.</span></span>

<span data-ttu-id="913e3-136">Vertex-Attribute, die von **gldrawelements** geändert werden, haben nach dem zurückkehren von **gldrawelements** einen nicht angegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="913e3-136">Vertex attributes that are modified by **glDrawElements** have an unspecified value after **glDrawElements** returns.</span></span> <span data-ttu-id="913e3-137">Wenn z. b. \_ das GL- \_ Farbarray aktiviert ist, ist der Wert der aktuellen Farbe nach der Ausführung von **gldrawelements** nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="913e3-137">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawElements** executes.</span></span> <span data-ttu-id="913e3-138">Attribute, die nicht geändert werden, bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="913e3-138">Attributes that aren't modified remain unchanged.</span></span>

<span data-ttu-id="913e3-139">Sie können die **gldrawelements** -Funktion in Anzeigelisten einschließen.</span><span class="sxs-lookup"><span data-stu-id="913e3-139">You can include the **glDrawElements** function in display lists.</span></span> <span data-ttu-id="913e3-140">Wenn **gldrawelements** in einer Anzeigeliste enthalten ist, werden die erforderlichen Array Daten (festgelegt durch die Array Zeiger und die Aktivierung) ebenfalls in die Anzeigeliste eingegeben.</span><span class="sxs-lookup"><span data-stu-id="913e3-140">When **glDrawElements** is included in a display list, the necessary array data (determined by the array pointers and enables) is also entered into the display list.</span></span> <span data-ttu-id="913e3-141">Da die Array Zeiger und-Aktivierung Client seitige Zustandsvariablen sind, beeinflussen Ihre Werte die Anzeigelisten, wenn die Listen erstellt werden, und nicht, wenn die Listen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="913e3-141">Because the array pointers and enables are client-side state variables, their values affect display lists when the lists are created, not when the lists are executed.</span></span>

> [!Note]  
> <span data-ttu-id="913e3-142">Die **gldrawelements** -Funktion ist nur in OpenGL-Version 1,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="913e3-142">The **glDrawElements** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="913e3-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="913e3-143">Requirements</span></span>



| <span data-ttu-id="913e3-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="913e3-144">Requirement</span></span> | <span data-ttu-id="913e3-145">Wert</span><span class="sxs-lookup"><span data-stu-id="913e3-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="913e3-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="913e3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="913e3-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="913e3-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="913e3-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="913e3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="913e3-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="913e3-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="913e3-150">Header</span><span class="sxs-lookup"><span data-stu-id="913e3-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="913e3-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="913e3-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="913e3-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="913e3-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="913e3-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="913e3-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="913e3-154">DLL</span><span class="sxs-lookup"><span data-stu-id="913e3-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="913e3-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="913e3-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913e3-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="913e3-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913e3-157">**glarrayelement**</span><span class="sxs-lookup"><span data-stu-id="913e3-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="913e3-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="913e3-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="913e3-159">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="913e3-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="913e3-160">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="913e3-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="913e3-161">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="913e3-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="913e3-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="913e3-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="913e3-163">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="913e3-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="913e3-164">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="913e3-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="913e3-165">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="913e3-165">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="913e3-166">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="913e3-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="913e3-167">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="913e3-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





