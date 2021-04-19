---
title: glarrayelement-Funktion (GL. h)
description: Die Funktion "glarrayelement" gibt die Array Elemente an, die zum Rendering eines Scheitel Punkts verwendet werden.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- glarrayelement-Funktion OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346722"
---
# <a name="glarrayelement-function"></a><span data-ttu-id="a331d-104">glarrayelement-Funktion</span><span class="sxs-lookup"><span data-stu-id="a331d-104">glArrayElement function</span></span>

<span data-ttu-id="a331d-105">Die Funktion " **glarrayelement** " gibt die Array Elemente an, die zum Rendering eines Scheitel Punkts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a331d-105">The **glArrayElement** function specifies the array elements used to render a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="a331d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a331d-106">Syntax</span></span>


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a><span data-ttu-id="a331d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a331d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a331d-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="a331d-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="a331d-109">Ein Index in den aktivierten Arrays.</span><span class="sxs-lookup"><span data-stu-id="a331d-109">An index in the enabled arrays.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a331d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a331d-110">Return value</span></span>

<span data-ttu-id="a331d-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a331d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a331d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a331d-112">Remarks</span></span>

<span data-ttu-id="a331d-113">Verwenden Sie die Funktion " **glarrayelement** " innerhalb von [**glBegin**](glbegin.md) -und [**glEnd**](glend.md) -Paaren, um Vertex-und Attributdaten für Punkt-, Linien-und Polygon primitive anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a331d-113">Use the **glArrayElement** function within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs to specify vertex and attribute data for point, line, and polygon primitives.</span></span> <span data-ttu-id="a331d-114">Die Funktion " **glarrayelement** " gibt die Daten für einen einzelnen Scheitelpunkt mithilfe von Vertex-und Attributdaten an, die sich am *Index* der aktivierten Scheitelpunkt Arrays befinden.</span><span class="sxs-lookup"><span data-stu-id="a331d-114">The **glArrayElement** function specifies the data for a single vertex using vertex and attribute data located at the *index* of the enabled vertex arrays.</span></span>

<span data-ttu-id="a331d-115">Sie können " **glarrayelement** " verwenden, um primitive zu erstellen, indem Sie Scheitelpunkt Daten indizieren, anstatt durch das Streamen von Daten Arrays in der Reihenfolge der ersten bis letzten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="a331d-115">You can use **glArrayElement** to construct primitives by indexing vertex data, rather than by streaming through arrays of data in first-to-last order.</span></span> <span data-ttu-id="a331d-116">Da " **glarrayelement** " nur einen einzelnen Scheitelpunkt angibt, können Sie Attribute für einzelne primitive explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="a331d-116">Because **glArrayElement** specifies a single vertex only, you can explicitly specify attributes for individual primitives.</span></span> <span data-ttu-id="a331d-117">Beispielsweise können Sie für jedes einzelne Dreieck einen einzelnen Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="a331d-117">For example, you can set a single normal for each individual triangle.</span></span>

<span data-ttu-id="a331d-118">Wenn Sie in Anzeigelisten Aufrufe an " **glarrayelement** " einschließen, werden die erforderlichen Array Daten, die von den Array Zeigern und Aktivier Werten bestimmt werden, auch in der Anzeigeliste eingegeben.</span><span class="sxs-lookup"><span data-stu-id="a331d-118">When you include calls to **glArrayElement** in display lists, the necessary array data, determined by the array pointers and enable values, is entered in the display list also.</span></span> <span data-ttu-id="a331d-119">Array Zeiger und aktivierte Werte werden bestimmt, wenn Anzeigelisten erstellt werden, nicht, wenn Anzeigelisten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a331d-119">Array pointer and enable values are determined when display lists are created, not when display lists are executed.</span></span>

<span data-ttu-id="a331d-120">Sie können statische Array Daten jederzeit mit " **glarrayelement**" lesen und Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="a331d-120">You can read and cache static array data at any time with **glArrayElement**.</span></span> <span data-ttu-id="a331d-121">Wenn Sie die Elemente eines statischen Arrays ändern, ohne das Array erneut anzugeben, sind die Ergebnisse aller nachfolgenden Aufrufe von " **glarrayelement** " nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a331d-121">When you modify the elements of a static array without specifying the array again, the results of any subsequent calls to **glArrayElement** are undefined.</span></span>

<span data-ttu-id="a331d-122">Wenn Sie " **glarrayelement** " aufrufen, ohne zuerst " **glenableclientstate**" aufrufen \_ \_ zu müssen, erfolgt keine Zeichnung, aber die Attribute, die aktivierten Arrays entsprechen, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="a331d-122">When you call **glArrayElement** without first calling **glEnableClientState**(GL\_VERTEX\_ARRAY), no drawing occurs, but the attributes corresponding to enabled arrays are modified.</span></span> <span data-ttu-id="a331d-123">Obwohl kein Fehler generiert wird, wenn Sie ein Array innerhalb der **glBegin** -und **glEnd** -Paare angeben, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a331d-123">Although no error is generated when you specify an array within **glBegin** and **glEnd** pairs, the results are undefined.</span></span>

> [!Note]  
> <span data-ttu-id="a331d-124">Die Funktion " **glarrayelement** " ist nur in OpenGL, Version 1,1 oder höher, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a331d-124">The **glArrayElement** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a331d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a331d-125">Requirements</span></span>



| <span data-ttu-id="a331d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a331d-126">Requirement</span></span> | <span data-ttu-id="a331d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a331d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a331d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a331d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a331d-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a331d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a331d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a331d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a331d-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a331d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a331d-132">Header</span><span class="sxs-lookup"><span data-stu-id="a331d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a331d-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a331d-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a331d-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a331d-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a331d-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a331d-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a331d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a331d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a331d-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a331d-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a331d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a331d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a331d-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a331d-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a331d-140">**glcolorpointer**</span><span class="sxs-lookup"><span data-stu-id="a331d-140">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="a331d-141">**gldrawarrays**</span><span class="sxs-lookup"><span data-stu-id="a331d-141">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="a331d-142">**gledgeflagpointer**</span><span class="sxs-lookup"><span data-stu-id="a331d-142">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="a331d-143">**glenableclientstate**</span><span class="sxs-lookup"><span data-stu-id="a331d-143">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="a331d-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a331d-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a331d-145">**glgetpointerv**</span><span class="sxs-lookup"><span data-stu-id="a331d-145">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="a331d-146">**glgetstring**</span><span class="sxs-lookup"><span data-stu-id="a331d-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="a331d-147">**glindexpointer**</span><span class="sxs-lookup"><span data-stu-id="a331d-147">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="a331d-148">**glnormalpointer**</span><span class="sxs-lookup"><span data-stu-id="a331d-148">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="a331d-149">**gltexcoordpointer**</span><span class="sxs-lookup"><span data-stu-id="a331d-149">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="a331d-150">**glvertexpointer**</span><span class="sxs-lookup"><span data-stu-id="a331d-150">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





