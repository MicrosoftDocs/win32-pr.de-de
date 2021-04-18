---
title: glutessendpolygon-Funktion (glu. h)
description: Die Funktionen "glutess beginpolygon" und "glutessendpolygon" begrenzen eine Polygon Beschreibung. | glutessendpolygon-Funktion (glu. h)
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- glutessendpolygon-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f9176e5bdb64dc0e3cd21bd42735e57b541b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371851"
---
# <a name="glutessendpolygon-function"></a><span data-ttu-id="5259e-105">glutessendpolygon-Funktion</span><span class="sxs-lookup"><span data-stu-id="5259e-105">gluTessEndPolygon function</span></span>

<span data-ttu-id="5259e-106">Die Funktionen " [**glutess beginpolygon**](glutessbeginpolygon.md) " und " **glutessendpolygon** " begrenzen eine Polygon Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="5259e-106">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5259e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5259e-107">Syntax</span></span>


```C++
void WINAPI gluTessEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="5259e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5259e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5259e-109">*ATI*</span><span class="sxs-lookup"><span data-stu-id="5259e-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="5259e-110">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="5259e-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5259e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5259e-111">Return value</span></span>

<span data-ttu-id="5259e-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5259e-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5259e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5259e-113">Remarks</span></span>

<span data-ttu-id="5259e-114">Die Funktionen " [**glutess beginpolygon**](glutessbeginpolygon.md) " und " **glutessendpolygon** " begrenzen die Definition eines nicht konvexen Polygons.</span><span class="sxs-lookup"><span data-stu-id="5259e-114">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="5259e-115">Fügen Sie in jedem " **glutess beginpolygon**"-  /  Paar "glutessendpolygon" einen oder mehrere Aufrufe von " [**glutess begincontour**](glutessbegincontour.md)" ein.</span><span class="sxs-lookup"><span data-stu-id="5259e-115">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="5259e-116">In jeder Kontur gibt es keine oder mehrere Aufrufe von " [**glutess Vertex**](glutessvertex.md)".</span><span class="sxs-lookup"><span data-stu-id="5259e-116">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="5259e-117">Die Eckpunkte geben eine geschlossene Kontur an (der letzte Scheitelpunkt jeder Kontur wird automatisch mit dem ersten-Element verknüpft).</span><span class="sxs-lookup"><span data-stu-id="5259e-117">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="5259e-118">Der *Polygon- \_ Daten* Parameter ist ein Zeiger auf eine vom Programmierer definierte Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="5259e-118">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="5259e-119">Wenn die entsprechenden Rückrufe angegeben werden (siehe [*glutesscallback*](glutess.md)), wird dieser Zeiger an die Rückruffunktion oder Funktionen zurückgegeben, sodass er eine bequeme Möglichkeit zum Speichern von pro-Polygon-Informationen ist.</span><span class="sxs-lookup"><span data-stu-id="5259e-119">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="5259e-120">Wenn Sie " **glutessendpolygon**" aufrufen, wird das Polygon im Mosaik Prozess dargestellt, und die resultierenden Dreiecke werden durch Rückrufe beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5259e-120">When you call **gluTessEndPolygon**, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="5259e-121">Beschreibungen der Rückruf Funktionen finden Sie unter [*glutesscallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="5259e-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5259e-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5259e-122">Examples</span></span>

<span data-ttu-id="5259e-123">Im folgenden wird ein Viereck mit einer dreieckigen Lücke beschrieben:</span><span class="sxs-lookup"><span data-stu-id="5259e-123">The following describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="5259e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5259e-124">Requirements</span></span>



| <span data-ttu-id="5259e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5259e-125">Requirement</span></span> | <span data-ttu-id="5259e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5259e-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5259e-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5259e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5259e-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5259e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5259e-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5259e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5259e-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5259e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5259e-131">Header</span><span class="sxs-lookup"><span data-stu-id="5259e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5259e-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5259e-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="5259e-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5259e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="5259e-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5259e-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5259e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5259e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5259e-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5259e-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5259e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5259e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5259e-138">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="5259e-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="5259e-139">**glutess begincontour**</span><span class="sxs-lookup"><span data-stu-id="5259e-139">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="5259e-140">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="5259e-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="5259e-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="5259e-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="5259e-142">**glutess normal**</span><span class="sxs-lookup"><span data-stu-id="5259e-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="5259e-143">**glutessproperty**</span><span class="sxs-lookup"><span data-stu-id="5259e-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="5259e-144">**glutess Vertex**</span><span class="sxs-lookup"><span data-stu-id="5259e-144">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





