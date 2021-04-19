---
title: glubeginpolygon-Funktion (glu. h)
description: Die Funktionen "glubeginpolygon" und "gluendpolygon" begrenzen eine Polygon Beschreibung. | glubeginpolygon-Funktion (glu. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- glubeginpolygon-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355755"
---
# <a name="glubeginpolygon-function"></a><span data-ttu-id="4754c-105">glubeginpolygon-Funktion</span><span class="sxs-lookup"><span data-stu-id="4754c-105">gluBeginPolygon function</span></span>

<span data-ttu-id="4754c-106">\[Die Funktion " **glubeginpolygon** " ist veraltet und wird nur aus Gründen der Abwärtskompatibilität bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4754c-106">\[The **gluBeginPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="4754c-107">Die Funktion " **glubeginpolygon** " ist " [**glutess beginpolygon**](glutessbeginpolygon.md) " gefolgt von " [**glutess begincontour**](glutessbegincontour.md)" zugeordnet.\]</span><span class="sxs-lookup"><span data-stu-id="4754c-107">The **gluBeginPolygon** function is mapped to [**gluTessBeginPolygon**](glutessbeginpolygon.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="4754c-108">Die Funktionen " **glubeginpolygon** " und " [**gluendpolygon**](gluendpolygon.md) " begrenzen eine Polygon Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="4754c-108">The **gluBeginPolygon** and [**gluEndPolygon**](gluendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4754c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4754c-109">Syntax</span></span>


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="4754c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4754c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4754c-111">*ATI*</span><span class="sxs-lookup"><span data-stu-id="4754c-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="4754c-112">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="4754c-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4754c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4754c-113">Return value</span></span>

<span data-ttu-id="4754c-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4754c-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4754c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4754c-115">Remarks</span></span>

<span data-ttu-id="4754c-116">Verwenden Sie " **glubeginpolygon** " und " **gluendpolygon** ", um die Definition eines nicht konvexen Polygons zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="4754c-116">Use **gluBeginPolygon** and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="4754c-117">Aufrufen von " **glubeginpolygon**".</span><span class="sxs-lookup"><span data-stu-id="4754c-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="4754c-118">Definieren Sie die Kontur des Polygons, indem Sie für jeden Scheitelpunkt und [**glunextcontour**](glunextcontour.md) den Wert " [**glutess Vertex**](glutessvertex.md) " aufrufen, um die einzelnen neuen Konturen zu starten</span><span class="sxs-lookup"><span data-stu-id="4754c-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="4754c-119">Nennen Sie " **gluendpolygon** ", um das Ende der Definition zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="4754c-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="4754c-120">Nachdem " **gluendpolygon** " aufgerufen wurde, wird das Polygon im Mosaik Prozess dargestellt, und die resultierenden Dreiecke werden durch Rückrufe beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4754c-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="4754c-121">Beschreibungen der Rückruf Funktionen finden Sie unter [*glutesscallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="4754c-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4754c-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4754c-122">Examples</span></span>

<span data-ttu-id="4754c-123">Im folgenden Beispiel wird ein Viereck mit einer dreieckigen Lücke beschrieben:</span><span class="sxs-lookup"><span data-stu-id="4754c-123">The following example describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="4754c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4754c-124">Requirements</span></span>



| <span data-ttu-id="4754c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4754c-125">Requirement</span></span> | <span data-ttu-id="4754c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4754c-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4754c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4754c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4754c-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4754c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4754c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4754c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4754c-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4754c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4754c-131">Header</span><span class="sxs-lookup"><span data-stu-id="4754c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4754c-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="4754c-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4754c-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4754c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="4754c-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4754c-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4754c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4754c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4754c-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4754c-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4754c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4754c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4754c-138">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="4754c-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="4754c-139">**glunextcontour**</span><span class="sxs-lookup"><span data-stu-id="4754c-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="4754c-140">**glutess begincontour**</span><span class="sxs-lookup"><span data-stu-id="4754c-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="4754c-141">**glutess beginpolygon**</span><span class="sxs-lookup"><span data-stu-id="4754c-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="4754c-142">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="4754c-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="4754c-143">**glutess Vertex**</span><span class="sxs-lookup"><span data-stu-id="4754c-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





