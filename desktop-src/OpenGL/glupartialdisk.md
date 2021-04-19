---
title: glupartialdisk-Funktion (glu. h)
description: Die Funktion "glupartialdisk" zeichnet einen Bogen eines Datenträgers.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- glupartialdisk-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337283"
---
# <a name="glupartialdisk-function"></a><span data-ttu-id="94442-104">glupartialdisk-Funktion</span><span class="sxs-lookup"><span data-stu-id="94442-104">gluPartialDisk function</span></span>

<span data-ttu-id="94442-105">Die Funktion " **glupartialdisk** " zeichnet einen Bogen eines Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="94442-105">The **gluPartialDisk** function draws an arc of a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="94442-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="94442-106">Syntax</span></span>


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a><span data-ttu-id="94442-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="94442-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94442-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="94442-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="94442-109">Ein quadktobjekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="94442-109">A quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="94442-110">*innerradius*</span><span class="sxs-lookup"><span data-stu-id="94442-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="94442-111">Der innere Radius des partiellen Datenträgers (kann NULL sein).</span><span class="sxs-lookup"><span data-stu-id="94442-111">The inner radius of the partial disk (can be zero).</span></span>

</dd> <dt>

<span data-ttu-id="94442-112">*outerradius*</span><span class="sxs-lookup"><span data-stu-id="94442-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="94442-113">Der äußere Radius des partiellen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="94442-113">The outer radius of the partial disk.</span></span>

</dd> <dt>

<span data-ttu-id="94442-114">*aufs*</span><span class="sxs-lookup"><span data-stu-id="94442-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="94442-115">Die Anzahl der Unterteilungen um die z-Achse.</span><span class="sxs-lookup"><span data-stu-id="94442-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="94442-116">*Loops*</span><span class="sxs-lookup"><span data-stu-id="94442-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="94442-117">Die Anzahl der konzentrischen Ringe für den Ursprung, in den der Teil Datenträger unterteilt wird.</span><span class="sxs-lookup"><span data-stu-id="94442-117">The number of concentric rings about the origin into which the partial disk is subdivided.</span></span>

</dd> <dt>

<span data-ttu-id="94442-118">*Start Angle*</span><span class="sxs-lookup"><span data-stu-id="94442-118">*startAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="94442-119">Der Anfangs Winkel (in Grad) des Datenträger Teils.</span><span class="sxs-lookup"><span data-stu-id="94442-119">The starting angle, in degrees, of the disk portion.</span></span>

</dd> <dt>

<span data-ttu-id="94442-120">*sweepAngle*</span><span class="sxs-lookup"><span data-stu-id="94442-120">*sweepAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="94442-121">Der Mittelpunktswinkel des Datenträger Teils in Grad.</span><span class="sxs-lookup"><span data-stu-id="94442-121">The sweep angle, in degrees, of the disk portion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94442-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94442-122">Return value</span></span>

<span data-ttu-id="94442-123">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="94442-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94442-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94442-124">Remarks</span></span>

<span data-ttu-id="94442-125">Die Funktion " **glupartialdisk** " rendert einen partiellen Datenträger auf der *z* = 0-Ebene.</span><span class="sxs-lookup"><span data-stu-id="94442-125">The **gluPartialDisk** function renders a partial disk on the *z* = 0 plane.</span></span> <span data-ttu-id="94442-126">Ein Teil Datenträger ähnelt einem vollständigen Datenträger, mit dem Unterschied, dass nur die Teilmenge des Datenträgers von *startAngle* über *startAngle*  +  *sweepAngle* enthalten ist (wobei 0 Grad entlang der positiven y-Achse liegt, 90 Grad entlang der positiven x-Achse, 180 Grad entlang der negativen y-Achse und 270 Grad entlang der negativen x-Achse).</span><span class="sxs-lookup"><span data-stu-id="94442-126">A partial disk is similar to a full disk, except that only the subset of the disk from *startAngle* through *startAngle* + *sweepAngle* is included (where 0 degrees is along the positive y-axis, 90 degrees is along the positive x-axis, 180 degrees is along the negative y-axis, and 270 degrees is along the negative x-axis).</span></span>

<span data-ttu-id="94442-127">Der Teil Datenträger weist einen Radius von *outerradius* auf und enthält eine konzentrische zirkuläre Lücke mit einem Radius von *innerradius*.</span><span class="sxs-lookup"><span data-stu-id="94442-127">The partial disk has a radius of *outerRadius* and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="94442-128">Wenn *innerradius* gleich 0 (null) ist, wird kein Loch generiert.</span><span class="sxs-lookup"><span data-stu-id="94442-128">If *innerRadius* is zero, then no hole is generated.</span></span> <span data-ttu-id="94442-129">Der Teil Datenträger wird um die z-Achse in Slices (z. b. Pizza Slices) und auch über die z-Achse in Ringe (wie von *Slices* bzw. *Schleifen* angegeben) unterteilt.</span><span class="sxs-lookup"><span data-stu-id="94442-129">The partial disk is subdivided around the z-axis into slices (like pizza slices), and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="94442-130">Im Hinblick auf die Ausrichtung wird die positive z-Seite des partiellen Datenträgers als außerhalb betrachtet (siehe [**gluquadricorientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="94442-130">With respect to orientation, the positive z-side of the partial disk is considered to be outside (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="94442-131">Dies bedeutet Folgendes: Wenn die Ausrichtung auf "glu extern" festgelegt ist \_ , werden alle normalisieren generiert, die auf die positive z-Achse zeigen.</span><span class="sxs-lookup"><span data-stu-id="94442-131">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="94442-132">Wenn Sie die Texturierung (mit " [**gluquadrictexture**](gluquadrictexture.md)") aktiviert haben, generiert " **glupartialdisk** " die Texturkoordinaten linear, sodass *r*  =  *outerradius*, der Wert bei (*r*, 0, 0) ist (1, 0,5); bei (0, *r*, 0) ist es (0,5, 1); bei (*r*, 0, 0) ist es (0, 0,5); und bei (0, *r*, 0) ist es (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="94442-132">If you have turned on texturing (with [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** generates texture coordinates linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (*r*, 0, 0) it is (0, 0.5); and at (0, *r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="94442-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94442-133">Requirements</span></span>



| <span data-ttu-id="94442-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94442-134">Requirement</span></span> | <span data-ttu-id="94442-135">Wert</span><span class="sxs-lookup"><span data-stu-id="94442-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="94442-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94442-136">Minimum supported client</span></span><br/> | <span data-ttu-id="94442-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94442-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="94442-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94442-138">Minimum supported server</span></span><br/> | <span data-ttu-id="94442-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94442-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="94442-140">Header</span><span class="sxs-lookup"><span data-stu-id="94442-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="94442-141"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="94442-141"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="94442-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94442-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="94442-143"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94442-143"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="94442-144">DLL</span><span class="sxs-lookup"><span data-stu-id="94442-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94442-145"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94442-145"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94442-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94442-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94442-147">**gluzylinder**</span><span class="sxs-lookup"><span data-stu-id="94442-147">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="94442-148">**gludisk**</span><span class="sxs-lookup"><span data-stu-id="94442-148">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="94442-149">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="94442-149">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="94442-150">**gluquadricorientation**</span><span class="sxs-lookup"><span data-stu-id="94442-150">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="94442-151">**gluquadrictexture**</span><span class="sxs-lookup"><span data-stu-id="94442-151">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="94442-152">**glusphere**</span><span class="sxs-lookup"><span data-stu-id="94442-152">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





