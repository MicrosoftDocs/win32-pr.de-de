---
title: gludisk-Funktion (glu. h)
description: Die Funktion "gludisk" zeichnet einen Datenträger.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- gludisk-Funktion OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040576"
---
# <a name="gludisk-function"></a><span data-ttu-id="5e4b2-104">gludisk-Funktion</span><span class="sxs-lookup"><span data-stu-id="5e4b2-104">gluDisk function</span></span>

<span data-ttu-id="5e4b2-105">Die Funktion " **gludisk** " zeichnet einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-105">The **gluDisk** function draws a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e4b2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e4b2-106">Syntax</span></span>


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a><span data-ttu-id="5e4b2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e4b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e4b2-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="5e4b2-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4b2-109">Das Quadric-Objekt (mit [**glunewquadric**](glunewquadric.md)erstellt).</span><span class="sxs-lookup"><span data-stu-id="5e4b2-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5e4b2-110">*innerradius*</span><span class="sxs-lookup"><span data-stu-id="5e4b2-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4b2-111">Der innere Radius des Datenträgers (kann NULL sein).</span><span class="sxs-lookup"><span data-stu-id="5e4b2-111">The inner radius of the disk (may be zero).</span></span>

</dd> <dt>

<span data-ttu-id="5e4b2-112">*outerradius*</span><span class="sxs-lookup"><span data-stu-id="5e4b2-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4b2-113">Der äußere Radius des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-113">The outer radius of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="5e4b2-114">*aufs*</span><span class="sxs-lookup"><span data-stu-id="5e4b2-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4b2-115">Die Anzahl der Unterteilungen um die z-Achse.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="5e4b2-116">*Loops*</span><span class="sxs-lookup"><span data-stu-id="5e4b2-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4b2-117">Die Anzahl der konzentrischen Ringe für den Ursprung, in den der Datenträger unterteilt wird.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-117">The number of concentric rings about the origin into which the disk is subdivided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e4b2-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e4b2-118">Return value</span></span>

<span data-ttu-id="5e4b2-119">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e4b2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e4b2-120">Remarks</span></span>

<span data-ttu-id="5e4b2-121">Die Funktion " **gludisk** " rendert einen Datenträger auf der *z* = 0-Ebene.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-121">The **gluDisk** function renders a disk on the *z* = 0 plane.</span></span> <span data-ttu-id="5e4b2-122">Der Datenträger weist einen Radius von *outerradius* auf und enthält eine konzentrische zirkuläre Lücke mit einem Radius von *innerradius*.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-122">The disk has a radius of *outerRadius*, and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="5e4b2-123">Wenn *innerradius* 0 ist, wird kein Loch generiert.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-123">If *innerRadius* is 0, then no hole is generated.</span></span> <span data-ttu-id="5e4b2-124">Der Datenträger ist um die z-Achse in Slices (z. b. Pizza Slices) und auch über die z-Achse in Ringe (wie von *Slices* bzw. *Schleifen* angegeben) unterteilt.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-124">The disk is subdivided around the z-axis into slices (like pizza slices) and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="5e4b2-125">Im Hinblick auf die Ausrichtung wird die positive *z*-Seite des Datenträgers als *außerhalb* betrachtet (siehe [**gluquadricorientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="5e4b2-125">With respect to orientation, the positive *z*-side of the disk is considered to be *outside* (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="5e4b2-126">Dies bedeutet Folgendes: Wenn die Ausrichtung auf "glu extern" festgelegt ist \_ , werden alle normalisieren generiert, die auf die positive z-Achse zeigen.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-126">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="5e4b2-127">Wenn die Texturierung aktiviert ist (mit " [**gluquadrictexture**](gluquadrictexture.md)"), werden die Texturkoordinaten linear generiert, sodass *r*  =  *outerradius*, der Wert bei (*r*, 0, 0) ist (1, 0,5); bei (0, *r*, 0) ist er (0,5, 1); bei (-*r*, 0, 0) ist er (0, 0,5); und bei (0,-*r*, 0) ist er (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="5e4b2-127">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)), texture coordinates are generated linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (-*r*, 0, 0) it is (0, 0.5); and at (0, -*r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4b2-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e4b2-128">Requirements</span></span>



| <span data-ttu-id="5e4b2-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e4b2-129">Requirement</span></span> | <span data-ttu-id="5e4b2-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5e4b2-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5e4b2-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e4b2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5e4b2-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e4b2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5e4b2-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e4b2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5e4b2-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e4b2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5e4b2-135">Header</span><span class="sxs-lookup"><span data-stu-id="5e4b2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e4b2-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e4b2-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="5e4b2-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e4b2-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e4b2-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e4b2-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5e4b2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5e4b2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e4b2-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e4b2-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e4b2-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e4b2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4b2-142">**gluzylinder**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-142">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="5e4b2-143">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-143">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="5e4b2-144">**glupartialdisk**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-144">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="5e4b2-145">**gluquadricorientation**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-145">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="5e4b2-146">**gluquadrictexture**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-146">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="5e4b2-147">**glusphere**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-147">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





