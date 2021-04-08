---
title: glutess normal-Funktion (glu. h)
description: Die Funktion "glutess normal" gibt eine normale für ein Polygon an.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- glutess normal-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957075"
---
# <a name="glutessnormal-function"></a><span data-ttu-id="73274-104">glutess normal-Funktion</span><span class="sxs-lookup"><span data-stu-id="73274-104">gluTessNormal function</span></span>

<span data-ttu-id="73274-105">Die Funktion " **glutess normal** " gibt eine normale für ein Polygon an.</span><span class="sxs-lookup"><span data-stu-id="73274-105">The **gluTessNormal** function specifies a normal for a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="73274-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="73274-106">Syntax</span></span>


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a><span data-ttu-id="73274-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="73274-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73274-108">*ATI*</span><span class="sxs-lookup"><span data-stu-id="73274-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="73274-109">Das Mosaik Objekt (mit [**glunewtess**](glunewtess.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="73274-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="73274-110">*x*</span><span class="sxs-lookup"><span data-stu-id="73274-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="73274-111">Die x-Koordinaten Komponente eines normalen.</span><span class="sxs-lookup"><span data-stu-id="73274-111">The x-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="73274-112">*y*</span><span class="sxs-lookup"><span data-stu-id="73274-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="73274-113">Die Komponente der y-Koordinate eines normalen.</span><span class="sxs-lookup"><span data-stu-id="73274-113">The y-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="73274-114">*z*</span><span class="sxs-lookup"><span data-stu-id="73274-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="73274-115">Die z-Koordinaten Komponente eines normalen.</span><span class="sxs-lookup"><span data-stu-id="73274-115">The z-coordinate component of a normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73274-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73274-116">Return value</span></span>

<span data-ttu-id="73274-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="73274-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73274-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73274-118">Remarks</span></span>

<span data-ttu-id="73274-119">Die Funktion " **glutess normal** " beschreibt einen normalen Wert für ein Polygon, das Sie definieren.</span><span class="sxs-lookup"><span data-stu-id="73274-119">The **gluTessNormal** function describes a normal for a polygon that you define.</span></span> <span data-ttu-id="73274-120">Alle Eingabedaten werden auf eine Ebene senkrecht zu einer der drei Koordinatenachsen vor dem Mosaik projiziert, und alle Ausgabe Dreiecke werden im Hinblick auf den normalen gegen den Uhrzeigersinn ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="73274-120">All input data is projected onto a plane perpendicular to one of the three coordinate axes before tessellation, and all output triangles are oriented counterclockwise with respect to the normal.</span></span> <span data-ttu-id="73274-121">(Um die Ausrichtung im Uhrzeigersinn zu erhalten, umkehren Sie das Vorzeichen der angegebenen normal).</span><span class="sxs-lookup"><span data-stu-id="73274-121">(To obtain clockwise orientation, reverse the sign of the supplied normal).</span></span> <span data-ttu-id="73274-122">Wenn Sie z. b. wissen, dass alle Polygone auf der x-y-Ebene liegen, nennen Sie " **glutess normal**(Tess, 0,0, 0,0, 1,0)", bevor Sie Polygone rendern.</span><span class="sxs-lookup"><span data-stu-id="73274-122">For example, if you know that all polygons lie in the x-y plane, call **gluTessNormal**(tess, 0.0, 0.0, 1.0) before rendering any polygons.</span></span>

<span data-ttu-id="73274-123">Wenn der angegebene normale Wert (0,0, 0,0, 0,0) (Standardwert) ist, wird der normale Wert wie folgt bestimmt:</span><span class="sxs-lookup"><span data-stu-id="73274-123">If the supplied normal is (0.0, 0.0, 0.0) (the default value), the normal is determined as follows:</span></span>

1.  <span data-ttu-id="73274-124">Die Richtung der normalen, bis zu ihrem Vorzeichen, wird gefunden, indem eine Ebene an die Eckpunkte angepasst wird, ohne dass die vertexen miteinander verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="73274-124">The direction of the normal, up to its sign, is found by fitting a plane to the vertexes, without regard to how the vertexes are connected.</span></span> <span data-ttu-id="73274-125">Es wird erwartet, dass die Eingabedaten ungefähr in der Ebene liegen. Andernfalls kann die Geometrie durch Projektion senkrecht zu einer der drei Koordinatenachsen erheblich geändert werden.</span><span class="sxs-lookup"><span data-stu-id="73274-125">It is expected that the input data lies approximately in the plane; otherwise projection perpendicular to one of the three coordinate axes can change the geometry substantially.</span></span>
2.  <span data-ttu-id="73274-126">Das Vorzeichen der normalen wird ausgewählt, sodass die Summe der signierten Bereiche aller Eingabe Konturen nicht negativ ist (wobei eine Kontur gegen den Uhrzeigersinn einen positiven Bereich aufweist).</span><span class="sxs-lookup"><span data-stu-id="73274-126">The sign of the normal is chosen so that the sum of the signed areas of all input contours is nonnegative (where a counterclockwise contour has positive area).</span></span>

<span data-ttu-id="73274-127">Die angegebene normale bleibt **bestehen, bis** Sie von einem anderen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="73274-127">The supplied normal persists until another call to **gluTessNormal** changes it.</span></span>

## <a name="requirements"></a><span data-ttu-id="73274-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73274-128">Requirements</span></span>



| <span data-ttu-id="73274-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73274-129">Requirement</span></span> | <span data-ttu-id="73274-130">Wert</span><span class="sxs-lookup"><span data-stu-id="73274-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="73274-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73274-131">Minimum supported client</span></span><br/> | <span data-ttu-id="73274-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73274-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="73274-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73274-133">Minimum supported server</span></span><br/> | <span data-ttu-id="73274-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73274-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="73274-135">Header</span><span class="sxs-lookup"><span data-stu-id="73274-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="73274-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="73274-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="73274-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73274-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="73274-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73274-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="73274-139">DLL</span><span class="sxs-lookup"><span data-stu-id="73274-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73274-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73274-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73274-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73274-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73274-142">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="73274-142">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="73274-143">**glutess beginpolygon**</span><span class="sxs-lookup"><span data-stu-id="73274-143">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="73274-144">**glutessendpolygon**</span><span class="sxs-lookup"><span data-stu-id="73274-144">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> </dl>

 

 





