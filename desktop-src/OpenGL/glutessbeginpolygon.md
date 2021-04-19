---
title: glutess beginpolygon-Funktion (glu. h)
description: Die Funktionen "glutess beginpolygon" und "glutessendpolygon" begrenzen eine Polygon Beschreibung. | glutess beginpolygon-Funktion (glu. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- glutess beginpolygon-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353319"
---
# <a name="glutessbeginpolygon-function"></a><span data-ttu-id="cdfe4-105">glutess beginpolygon-Funktion</span><span class="sxs-lookup"><span data-stu-id="cdfe4-105">gluTessBeginPolygon function</span></span>

<span data-ttu-id="cdfe4-106">Die Funktionen " **glutess beginpolygon** " und " [**glutessendpolygon**](glutessendpolygon.md) " begrenzen eine Polygon Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-106">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdfe4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdfe4-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a><span data-ttu-id="cdfe4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdfe4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdfe4-109">*ATI*</span><span class="sxs-lookup"><span data-stu-id="cdfe4-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="cdfe4-110">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cdfe4-111">*Polygon \_ Daten*</span><span class="sxs-lookup"><span data-stu-id="cdfe4-111">*polygon\_data*</span></span> 
</dt> <dd>

<span data-ttu-id="cdfe4-112">Ein Zeiger auf eine vom Programmierer definierte Polygon-Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-112">A pointer to a programmer-defined polygon data structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdfe4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdfe4-113">Return value</span></span>

<span data-ttu-id="cdfe4-114">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdfe4-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdfe4-115">Remarks</span></span>

<span data-ttu-id="cdfe4-116">Die Funktionen " **glutess beginpolygon** " und " [**glutessendpolygon**](glutessendpolygon.md) " begrenzen die Definition eines nicht konvexen Polygons.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-116">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="cdfe4-117">Fügen Sie in jedem " **glutess beginpolygon**"-  /  Paar "glutessendpolygon" einen oder mehrere Aufrufe von " [**glutess begincontour**](glutessbegincontour.md)" ein.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-117">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="cdfe4-118">In jeder Kontur gibt es keine oder mehrere Aufrufe von " [**glutess Vertex**](glutessvertex.md)".</span><span class="sxs-lookup"><span data-stu-id="cdfe4-118">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="cdfe4-119">Die Eckpunkte geben eine geschlossene Kontur an (der letzte Scheitelpunkt jeder Kontur wird automatisch mit dem ersten-Element verknüpft).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-119">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="cdfe4-120">Der *Polygon- \_ Daten* Parameter ist ein Zeiger auf eine vom Programmierer definierte Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-120">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="cdfe4-121">Wenn die entsprechenden Rückrufe angegeben werden (siehe [*glutesscallback*](glutess.md)), wird dieser Zeiger an die Rückruffunktion oder Funktionen zurückgegeben, sodass er eine bequeme Möglichkeit zum Speichern von pro-Polygon-Informationen ist.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-121">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="cdfe4-122">Wenn Sie " [**glutessendpolygon**](glutessendpolygon.md)" aufrufen, wird das Polygon im Mosaik Prozess dargestellt, und die resultierenden Dreiecke werden durch Rückrufe beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-122">When you call [**gluTessEndPolygon**](glutessendpolygon.md), the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="cdfe4-123">Beschreibungen der Rückruf Funktionen finden Sie unter [*glutesscallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-123">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cdfe4-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdfe4-124">Examples</span></span>

<span data-ttu-id="cdfe4-125">Im folgenden wird ein Viereck mit einer dreieckigen Lücke beschrieben:</span><span class="sxs-lookup"><span data-stu-id="cdfe4-125">The following describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
```

## <a name="requirements"></a><span data-ttu-id="cdfe4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdfe4-126">Requirements</span></span>



| <span data-ttu-id="cdfe4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdfe4-127">Requirement</span></span> | <span data-ttu-id="cdfe4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cdfe4-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cdfe4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdfe4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cdfe4-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdfe4-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cdfe4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdfe4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cdfe4-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdfe4-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cdfe4-133">Header</span><span class="sxs-lookup"><span data-stu-id="cdfe4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdfe4-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe4-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="cdfe4-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cdfe4-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="cdfe4-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe4-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cdfe4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cdfe4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdfe4-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdfe4-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdfe4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdfe4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdfe4-140">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="cdfe4-140">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="cdfe4-141">**glutess begincontour**</span><span class="sxs-lookup"><span data-stu-id="cdfe4-141">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="cdfe4-142">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="cdfe4-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="cdfe4-143">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="cdfe4-143">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="cdfe4-144">**glutess normal**</span><span class="sxs-lookup"><span data-stu-id="cdfe4-144">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="cdfe4-145">**glutessproperty**</span><span class="sxs-lookup"><span data-stu-id="cdfe4-145">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="cdfe4-146">**glutess Vertex**</span><span class="sxs-lookup"><span data-stu-id="cdfe4-146">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





