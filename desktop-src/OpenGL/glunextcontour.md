---
title: glunextcontour-Funktion (glu. h)
description: Die Funktion "glunextcontour" markiert den Anfang einer anderen Kontur.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- glunextcontour-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391708"
---
# <a name="glunextcontour-function"></a><span data-ttu-id="6518b-104">glunextcontour-Funktion</span><span class="sxs-lookup"><span data-stu-id="6518b-104">gluNextContour function</span></span>

<span data-ttu-id="6518b-105">\[Die Funktion " **glunextcontour** " ist veraltet und wird nur aus Gründen der Abwärtskompatibilität bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6518b-105">\[The **gluNextContour** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="6518b-106">Die **glunextcontour** -Funktion wird " [**gluTessEndContour**](glutessendcontour.md) " gefolgt von " [**glutess begincontour**](glutessbegincontour.md)" zugeordnet.\]</span><span class="sxs-lookup"><span data-stu-id="6518b-106">The **gluNextContour** function is mapped to [**gluTessEndContour**](glutessendcontour.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="6518b-107">Die Funktion " **glunextcontour** " markiert den Anfang einer anderen Kontur.</span><span class="sxs-lookup"><span data-stu-id="6518b-107">The **gluNextContour** function marks the beginning of another contour.</span></span>

## <a name="syntax"></a><span data-ttu-id="6518b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6518b-108">Syntax</span></span>


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a><span data-ttu-id="6518b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6518b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6518b-110">*ATI*</span><span class="sxs-lookup"><span data-stu-id="6518b-110">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="6518b-111">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="6518b-111">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6518b-112">*type*</span><span class="sxs-lookup"><span data-stu-id="6518b-112">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="6518b-113">Der Typ der zu definierenden Kontur.</span><span class="sxs-lookup"><span data-stu-id="6518b-113">The type of the contour being defined.</span></span> <span data-ttu-id="6518b-114">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="6518b-114">The following values are valid.</span></span>



| <span data-ttu-id="6518b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6518b-115">Value</span></span>                                                                                                                                                                | <span data-ttu-id="6518b-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6518b-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <span data-ttu-id="6518b-117"><dt>**Glu, \_ außen**</dt></span><span class="sxs-lookup"><span data-stu-id="6518b-117"><dt>**GLU\_EXTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="6518b-118">Eine äußere Kontur definiert eine äußere Grenze des Polygons.</span><span class="sxs-lookup"><span data-stu-id="6518b-118">An exterior contour defines an exterior boundary of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <span data-ttu-id="6518b-119"><dt>**Glu- \_ innen**</dt></span><span class="sxs-lookup"><span data-stu-id="6518b-119"><dt>**GLU\_INTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="6518b-120">Eine innere Kontur definiert eine innere Grenze des Polygons (z. b. eine Lücke).</span><span class="sxs-lookup"><span data-stu-id="6518b-120">An interior contour defines an interior boundary of the polygon (such as a hole).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <span data-ttu-id="6518b-121"><dt>**Glu \_ unbekannt**</dt></span><span class="sxs-lookup"><span data-stu-id="6518b-121"><dt>**GLU\_UNKNOWN**</dt></span></span> </dl>              | <span data-ttu-id="6518b-122">Eine unbekannte Kontur wird von der Bibliothek analysiert, um zu bestimmen, ob Sie innen oder außen ist.</span><span class="sxs-lookup"><span data-stu-id="6518b-122">An unknown contour is analyzed by the library to determine whether it is interior or exterior.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <span data-ttu-id="6518b-123"><dt>**Glu \_ CCW, Glu \_ CW**</dt></span><span class="sxs-lookup"><span data-stu-id="6518b-123"><dt>**GLU\_CCW, GLU\_CW**</dt></span></span> </dl> | <span data-ttu-id="6518b-124">Der erste \_ definierte glu CCW-oder glu \_ CW-Contour wird als extern betrachtet.</span><span class="sxs-lookup"><span data-stu-id="6518b-124">The first GLU\_CCW or GLU\_CW contour defined is considered to be exterior.</span></span> <span data-ttu-id="6518b-125">Alle anderen Konturen werden als außen betrachtet, wenn Sie in der gleichen Richtung (im Uhrzeigersinn oder gegen den Uhrzeigersinn) als erste Kontur ausgerichtet sind, und inneren, wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="6518b-125">All other contours are considered to be exterior if they are oriented in the same direction (clockwise or counterclockwise) as the first contour, and interior if they are not.</span></span><br/> <span data-ttu-id="6518b-126">Wenn eine Kontur vom Typ "glu \_ CCW" oder "glu CW" ist \_ , müssen alle Konturen denselben Typ aufweisen (wenn Sie nicht sind, werden alle \_ die Kontur CCW-und glu CW-Kontur \_ in "glu unknown" geändert \_ ).</span><span class="sxs-lookup"><span data-stu-id="6518b-126">If one contour is of type GLU\_CCW or GLU\_CW, then all contours must be of the same type (if they are not, then all GLU\_CCW and GLU\_CW contours will be changed to GLU\_UNKNOWN).</span></span> <span data-ttu-id="6518b-127">Beachten Sie, dass es keinen wirklichen Unterschied zwischen den \_ Kontur Typen glu CCW und glu \_ CW gibt.</span><span class="sxs-lookup"><span data-stu-id="6518b-127">Note that there is no real difference between the GLU\_CCW and GLU\_CW contour types.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6518b-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6518b-128">Return value</span></span>

<span data-ttu-id="6518b-129">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6518b-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6518b-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6518b-130">Remarks</span></span>

<span data-ttu-id="6518b-131">Verwenden Sie die Funktion " **glunextcontour** ", um Polygone mit mehreren Kontur zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6518b-131">Use the **gluNextContour** function to describe polygons with multiple contours.</span></span> <span data-ttu-id="6518b-132">Nachdem Sie die erste Kontur durch eine Reihe von " [**glutess Vertex**](glutessvertex.md) "-aufrufen beschrieben haben, gibt ein **glunextcontour** -Aufruf an, dass die vorherige Kontur fertig ist und dass die nächste Kontur im Begriff ist, zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="6518b-132">After you describe the first contour through a series of [**gluTessVertex**](glutessvertex.md) calls, a **gluNextContour** call indicates that the previous contour is complete and that the next contour is about to begin.</span></span> <span data-ttu-id="6518b-133">Führen Sie eine weitere Reihe von **glutess Vertex** -aufrufen aus, um die neue Kontur zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6518b-133">Perform another series of **gluTessVertex** calls to describe the new contour.</span></span> <span data-ttu-id="6518b-134">Wiederholen Sie diesen Vorgang, bis alle Konturen beschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="6518b-134">Repeat this process until all contours have been described.</span></span>

<span data-ttu-id="6518b-135">Der *Typparameter* definiert, welcher Typ von Kontur folgt.</span><span class="sxs-lookup"><span data-stu-id="6518b-135">The *type* parameter defines what type of contour follows.</span></span>

<span data-ttu-id="6518b-136">Um den Typ der ersten Kontur zu definieren, können Sie " **glunextcontour** " vor der Beschreibung der ersten Kontur abrufen.</span><span class="sxs-lookup"><span data-stu-id="6518b-136">To define the type of the first contour, you can call **gluNextContour** before describing the first contour.</span></span> <span data-ttu-id="6518b-137">Wenn Sie " **glunextcontour** " nicht vor der ersten Kontur aufzurufen, wird die erste Kontur als "glu outside" gekennzeichnet \_ .</span><span class="sxs-lookup"><span data-stu-id="6518b-137">If you do not call **gluNextContour** before the first contour, the first contour is marked GLU\_EXTERIOR.</span></span>

## <a name="examples"></a><span data-ttu-id="6518b-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6518b-138">Examples</span></span>

<span data-ttu-id="6518b-139">Sie können ein Viereck mit einer dreieckigen Lücke wie folgt beschreiben:</span><span class="sxs-lookup"><span data-stu-id="6518b-139">You can describe a quadrilateral with a triangular hole in it as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="6518b-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6518b-140">Requirements</span></span>



| <span data-ttu-id="6518b-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6518b-141">Requirement</span></span> | <span data-ttu-id="6518b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="6518b-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6518b-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6518b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6518b-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6518b-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6518b-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6518b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6518b-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6518b-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6518b-147">Header</span><span class="sxs-lookup"><span data-stu-id="6518b-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6518b-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="6518b-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="6518b-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6518b-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="6518b-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6518b-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6518b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6518b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6518b-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6518b-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6518b-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6518b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6518b-154">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="6518b-154">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="6518b-155">**glutess begincontour**</span><span class="sxs-lookup"><span data-stu-id="6518b-155">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="6518b-156">**glutess beginpolygon**</span><span class="sxs-lookup"><span data-stu-id="6518b-156">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="6518b-157">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="6518b-157">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="6518b-158">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="6518b-158">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="6518b-159">**glutess Vertex**</span><span class="sxs-lookup"><span data-stu-id="6518b-159">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





